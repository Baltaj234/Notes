# Wireshark Notes

## What it is
Wireshark is a free, open-source packet analyzer. It captures network traffic passing through an interface and lets you inspect it protocol by protocol — the standard tool for troubleshooting, security analysis, and learning how networks actually behave.

## Where it fits
- **Capture** — grab raw frames off a live interface or read a saved `.pcap`/`.pcapng` file.
- **Display** — dissect each packet down to field level.
- **Analyze** — filter, follow streams, and reconstruct conversations.

`tshark` is the command-line version (same dissection engine, scriptable). `dumpcap` is capture-only and lighter — useful when you just need to record traffic.

## Install and permissions
- Linux: `sudo apt install wireshark` (add yourself to the `wireshark` group to capture without root).
- macOS/Windows: installers from wireshark.org; Windows needs **Npcap**.

Promiscuous mode sees all traffic on a segment (on switched networks you only see broadcast, multicast, and your own traffic unless you use a SPAN/mirror port or a capture device with port mirroring).

## The interface, briefly
- **Packet list** — one row per frame (time, source, destination, protocol, info).
- **Packet details** — the protocol tree, expandable field by field.
- **Packet bytes** — hex and ASCII of the raw data.

Color rules highlight by protocol; the status bar shows capture statistics.

## Capture filters vs display filters
This trips everyone up. They use **different syntax**.

| | Capture filter | Display filter |
|---|---|---|
| Applied | Before capture | After capture |
| Syntax | BPF (`tcp port 80`) | Wireshark's own (`tcp.port == 80`) |
| Effect | Packets dropped, gone forever | Only viewing hidden; data stays |
| Can be changed | Only by restarting capture | Any time |

**Display filter examples:**

Operators: `==` `!=` `>` `<` `>=` `<=`, `&&` `||` `!`, `contains`, `matches` (regex), `in {…}`.

## Traps worth memorizing
- **TCP handshake** — SYN → SYN/ACK → ACK. A SYN with no reply often means a firewall or an unreachable host.
- **Reset (RST)** — a connection killed abruptly; often a closed port or a middlebox.
- **Retransmissions** — `tcp.analysis.retransmission`; look for packet loss or congestion.
- **Zero window** — `tcp.analysis.zero_window`; the receiver's buffer is full, sender must wait.
- **DNS** — filter `dns`; check for slow or unanswered lookups, NXDOMAIN, and weirdly long names.
- **TLS** — you'll see handshake metadata but payload is encrypted unless you supply keys (Preferences → Protocols → TLS → *(Pre)-Master-Secret log filename*).

## Common workflow
1. Pick the right interface, set a capture filter if you know what you're after.
2. Reproduce the problem while capturing.
3. Stop, then narrow with display filters.
4. Right-click a packet → **Follow → TCP/HTTP/UDP Stream** to read the whole conversation.
5. **Statistics** menu for conversations, endpoints, protocol hierarchy, and IO graphs.
6. **File → Export Specified Packets** to save just what matters.

## Handy features
- **Coloring rules** — custom highlight sets.
- **Decode As** — force a dissector when a protocol runs on a non-standard port.
- **Expert Information** — Wireshark's own flags for errors, warnings, and notes.
- **Profiles** — save filter/column/layout setups per project.
- **Name resolution** — turn on MAC, network, and transport resolution for readable output (off by default for speed).

## Practical cautions
- Capture files can be large fast; use a capture filter or a ring buffer (`dumpcap -b`) for long runs.
- On busy links, buffer drops show up in the status bar — capture on a quieter point or filter harder.
- Captured traffic may contain credentials and personal data. Treat `.pcap` files as sensitive, and note that capturing others' traffic can have legal implications where you are.

## Useful entry points
- Display filter reference: the `Display Filter Reference` page on wireshark.org.
- Sample captures: the Wireshark wiki's SampleCaptures page — good for practice.
- `tshark -r file.pcap -Y "http" -T fields -e http.host` for quick scripted extraction.
