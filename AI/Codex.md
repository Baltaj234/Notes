# Codex

![alt text](image-2.png)

## 1. What Codex Is

Codex is OpenAI's software-engineering agent. It is the same agent surfaced in
several places, all tied to a ChatGPT account: the **CLI**, the **IDE
extension**, the **cloud/web app** (plus iOS and desktop), and integrations
like **GitHub** and **Slack**.

It is not a chat window that pastes snippets back at you. It reads a
repository, plans a change, edits files, runs your local tools (build, test,
lint), inspects the result, and iterates until the work matches the request.
That closed loop — plan, act, observe, correct — is the whole point.

Current default model in the CLI at the time of writing is **GPT-6.1 Sol**
(medium reasoning default), with **GPT-6 Luna** and **GPT-6.1 Terra** also
available depending on plan and version. Model availability moves fast; check
the plan's model list rather than assuming.

**Availability and cost (as of late 2026):**

| Plan | Codex access |
| --- | --- |
| Free / Go | Limited trial usage |
| Plus ($20/mo) | Focused coding sessions per week; cloud features, code review, Slack |
| Pro (from ~$100/mo) | Much higher limits; multi-project full workdays |
| Business / Enterprise | Per-seat, shared workspace, admin controls |
| API key | Usage-based, but **no cloud features** (GitHub review, Slack) |

Usage limits are shared across agentic features, so heavy Codex use can eat
the same budget as other agent work.

---

## 2. The Surfaces

### CLI

The core loop lives in the terminal, started inside a repo. Key entry points:

    /init        create an AGENTS.md with instructions for Codex
    /status      show current session configuration
    /permissions choose what Codex is allowed to do
    /model       pick model and reasoning effort
    /review      review changes and find issues

The refreshed CLI adds an **`/agents` view** for delegating work and tracking
multiple tasks, **voice** input and spoken responses, session resume, prompt
editing, and worktree support.

### IDE extension

VS Code and compatible editors (Cursor, Windsurf) use the Codex extension;
Xcode and JetBrains IDEs ship their own integrations. The advantage is context
already in view — open files, selection, diagnostics — so you ask about the
code in front of you. Use it for explaining unfamiliar code, focused edits,
and debugging; pair it with Git checkpoints so a bad run is one revert away.

### Codex Cloud

Run tasks against a repo in the cloud, with reusable per-repo environments,
network/secrets controls, and results reviewable from web, mobile, or desktop.
Start cloud work from the CLI (`codex cloud`) or hand it off and close your
laptop — the task keeps going.

### Other entry points

- **GitHub**: `@codex review`, `@codex security review`, automatic reviews on
  new PRs, and `@codex <request>` to delegate a change.
- **Slack**: delegate tasks or ask questions in a channel or thread.
- **Codex SDK**: embed the same agent in your own tools and workflows.
- **GitHub Action** (`openai/codex-action@v1`): run `codex exec` in CI.

---

## 3. Non-Interactive Automation

`codex exec` is the headless mode — the workhorse for anything scripted. It
runs without a TUI, so it slots into:

- CI/CD pipelines
- Git hooks
- Cron-style maintenance jobs
- Custom internal tooling via the SDK

The GitHub Action wraps this: it installs the CLI, optionally starts the
Responses API proxy when you supply an API key, and runs `codex exec` under
permissions you declare. Useful flags include `codex-args` for profiles, MCP
settings, and `--ephemeral` for throwaway sessions. Store the key as a repo
secret (`OPENAI_API_KEY`).

**Reach for CI automation when you want to:**

- Automate review feedback on PRs or releases without managing the CLI yourself
- Gate merges on Codex-driven quality checks
- Run repeatable tasks — migrations, release prep, review — from a workflow file

Model note from OpenAI's own cookbook: strong models are recommended for review
accuracy and consistency, and older recipes name `gpt-5.5` for that role. Model
naming has since moved on; pick the strongest reasoning model your plan exposes
for review-grade work.

---

## 4. AGENTS.md — Durable Guidance

`AGENTS.md` is the single highest-leverage file in a Codex setup. Think of it
as an **open-format README for agents**: it loads into context automatically
and encodes how you and your team want Codex to work in that repository.

**Discovery order:**

1. **Global** — `~/.codex/AGENTS.override.md` if present, otherwise
   `~/.codex/AGENTS.md`. Only the first non-empty file at this level is used.
2. **Project** — starting at the project root (typically the Git root), Codex
   walks down through directories, collecting guidance.
3. **Nested** — files closer to the code they govern take precedence in
   practice; put service-specific rules in a nested file.

**What a good AGENTS.md covers:**

- Repo goal and a high-level summary
- Build, test, and lint commands
- Coding conventions and directory layout
- Testing standards and what "done" means
- Relevant context files
- Commands to run before declaring success — lint, format, type check
- How to verify the final behavior matches the request
- What to inspect in the diff: bugs, regressions, risky patterns

**When to update it:**

- The agent repeats a mistake → add a rule
- You leave the same PR feedback twice → codify it
- A convention is implicit → write it down

You can even delegate the edit: tag `@codex add this to AGENTS.md` in a PR
comment and let a cloud task do it.

---

## 5. Code Review Automation

Codex review reads the PR diff, follows repository guidance, and posts a
standard GitHub review focused on serious issues.

**Setup:**

1. Codex cloud configured for the repo.
2. An `AGENTS.md` with a `## Code Review Rules` section, placed closest to the
   code the rules govern.
3. Request with `@codex review`, or turn on **Automatic reviews** in Codex
   settings to review every new PR.

**Writing review rules well:**

- Keep them concise: state the behavior to flag and any safe path or exception
- Put repository-wide checks at the root, service-specific ones in nested files
- **Leave mechanical checks in CI** — formatting, lint, and deterministic
  checks do not belong in review rules
- Open a representative PR, request a review, then narrow or remove rules that
  produce noise
- Rules guide Codex; they do not replace tests, branch protections, or required
  approvals

For a one-off focus, add the instruction to the PR comment instead of the file.

**On-prem or non-GitHub SCM:** the cloud review path needs GitHub. You can
replicate it on your own runners (GitLab CI, Azure DevOps, Jenkins) by
prompting Codex in headless mode with the review prompt that ships with the
CLI, plus a structured output JSON schema.

---

## 6. Subagents and Parallel Work

Subagents spawn specialized agents in parallel and collect their results into
one response. This shines on **highly parallel, read-heavy** work.

**The pattern:**

- Keep the **main agent** on requirements, decisions, and final output
- Run **subagents** for exploration, tests, log analysis, triage, and
  summarization
- Return **summaries** from subagents, not raw intermediate output
- In local clients you can define custom agents with their own model configs
  and instructions

**Worked example — PR review split three ways:**

- `pr_explorer` maps the codebase and gathers evidence
- a test/verification agent checks behavior claims
- a review agent inspects the diff against rules

**Cautions:**

- Subagent workflows **cost more tokens** than a single-agent run
- Read-heavy parallel work is safe; **write-heavy parallel work creates
  conflicts** and coordination overhead
- Trigger with plain language ("spawn two agents", "delegate this in parallel",
  "one agent per point")

---

## 7. Automation Playbook by Development Type

**Greenfield / new features**
Start by populating `AGENTS.md`. Give Codex the feature plan, let it scaffold,
then have it write tests first and implement against them. Use the cloud so
long builds survive closing the laptop.

**Brownfield / unfamiliar codebases**
Ask it to explain the area before changing anything. Have it produce a written
plan, review the plan, then execute. This front-loads the cheap correction.

**Bug triage**
Feed it the issue plus logs and a repro. Ask for a root-cause hypothesis with
evidence in the diff, not just a patch. Delegate log analysis to subagents
running in parallel.

**Test coverage**
Ask for tests that fail against the current code before the fix, so the suite
proves the bug existed and is now closed. Have it run them.

**Refactors and migrations**
Best done as CI-scheduled, repeatable `codex exec` tasks with a tight scope per
run. Gate each on the test suite. Mechanical rewrites it can handle;
cross-cutting architectural rewrites need human review at each step.

**Deprecation and dependency bumps**
Excellent fit for headless runs: bump, build, run tests, report breakage. Pair
with a check that confirms public API behavior is unchanged.

**Release prep**
Draft release notes, verify changelog accuracy against the commit range, and
check CI failures. All are repetitive, well-bounded, and reviewable.

**Docs and drift**
Use automations to detect drift between docs and code, and to codify recurring
corrections back into `AGENTS.md`.

**Security review**
`@codex security review` on PRs, plus a security-focused pass in CI for repos
with a recurring class of issue.

---

## 8. Customization Beyond AGENTS.md

- **Skills** — reusable workflows and domain expertise, packaged so they work
  across projects. Codify a good prompting pattern once you find it instead of
  repeating it manually.
- **MCP** — connect external systems (local or remote servers) so the agent can
  reach tools and data it otherwise cannot. Authenticate as needed and inspect
  what is connected.
- **Profiles and permission modes** — decide up front what the agent may do.
  `/permissions` covers this interactively; profiles cover it in CI. Sandboxing
  and auto-review settings control the escape hatches.
- **Plugins** — browse marketplaces and install what fits the workflow.

---

## 9. Working Practices That Hold Up

1. **Commit before and after** a significant agent task, or use Git
   checkpoints. Reverting is your cheapest safety net.
2. **Scope tightly.** One task per run beats "fix the repo". Small diffs are
   reviewable; sprawling ones are not.
3. **Make it verify.** Instructions to run tests, lint, and actually confirm
   behavior turn a plausible diff into a checked one.
4. **Write down what worked.** Every repeated correction is a missing
   AGENTS.md rule.
5. **Keep human gates** on anything irreversible — deploys, schema migrations,
   auth changes, production secrets.
6. **Watch cost.** Parallel agents and long sessions consume tokens fast, and
   usage shares a budget with other agentic features.
7. **Keep mechanical checks in CI.** Do not spend agent reasoning on
   formatting.
8. **Review the diff, not the summary.** The agent's description of what it did
   is a claim, not evidence.

---

## 10. Limits to Keep in Mind

- Codex is an agent with file and terminal access; permission configuration is
  a real security boundary, not a formality.
- Cloud features (GitHub review, Slack) are **not** available on API-key-only
  usage.
- Model names, default reasoning levels, plan limits, and feature availability
  change on a short cycle — verify against current docs rather than a
  remembered feature list.
- Parallel write-heavy work is where multi-agent setups degrade.
- Code review rules supplement, never replace, tests, branch protection, and
  required human approval.

---
