# AI MCP Servers

An MCP server is a server that allows AI applications (such as Claude, ChatGPT or Cursor) to connect to external tools, services, databases and information through a standardized protocol. 

MCP stands for Model Context Protocol. IT was introduced by Anthropic in November of 2024.

It is a universal connector between an AI model and the tools it needs to perform tasks.

# How does an MCP Server work?

There are three primary components to an MCP server

1. The MCP host, which is the actual AI application such as claude desktop or cursor.
2. The MCP Client which manages communications between the host and MCP servers.
3. THe actual MCP server that exposes tools and resources to the AI application.

An MCP server can expose three important capabilities:

1. Tools, which are the actions AI can execute, such as creating a GitHub issue or querying a database.
2. Resources, which is the information AI can retrieve such as files, database records or, documentation.
3. Prompts, which are reusable templates that help structure interactions.

# Real world examples of MCP Servers

Here are some real-world examples of what MCP servers can connect to.

## GitHub MCP server
Allows AI assistants to interact with repositories, commits, pull requests, issues, and branches

## PostgreSQL MCP Server
Allows AI assistants to query databases, inspect schemas, and retrieve records.

## Filesystem MCP Server
Allows AI assistants to read, write, search, and manage files within permitted directories.

## Google Drive MCP Server
Allows AI assistants to search documents, retrieve information, and interact with Drive files.