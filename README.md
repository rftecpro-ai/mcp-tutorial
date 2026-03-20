# Model Context Protocol (MCP)

> **An open standard by Anthropic for enabling AI agents to communicate, collaborate, and integrate with the world around them.**

---

## What is MCP?

Model Context Protocol (MCP) was introduced in **2024 by Anthropic** as an open standard that helps multiple AI agents work together efficiently. It enables:

- **Structured communication** between agents and tools
- **Context sharing** across sessions and systems
- **Seamless integration** with external tools and data sources

---

## Before & After MCP

Before MCP connecting models to new data source requires custom implementation, which can get expensive.

After MCP agent collaborate in real-time using shared memory, enabling seamless interaction across tools like slack, notion, and Google Drive through unified protocol

| | Before MCP | After MCP |
|---|---|---|
| **Integration** | Each new data source required custom implementation | Unified protocol for all tools and sources |
| **Cost** | Expensive and time-consuming to scale | Reusable, standardized connections |
| **Collaboration** | Agents operated in silos | Agents collaborate in real-time using shared memory |
| **Tools** | Custom connectors per tool | Works out-of-the-box with Slack, Notion, Google Drive, and more |

---

## MCP Architecture

MCP is built around **three core components**: **Host**, **Client**, and **Server**.

<img width="1541" height="753" alt="Screenshot 2026-03-20 at 2 20 59 PM" src="https://github.com/user-attachments/assets/f408ad13-5ee7-415c-8bb0-835709fb44aa" />



### Host
The **Host** is an LLM application (e.g., Claude Desktop) that provides the environment where the AI system runs. It manages interactions between the Client and Server — think of it as the *home* where the AI lives and operates.

<img width="1537" height="765" alt="Screenshot 2026-03-20 at 2 22 03 PM" src="https://github.com/user-attachments/assets/1d78d106-52a5-4bc4-a255-a0161ee7881d" />


### Client
The **Client** is a lightweight process or module that lives inside the Host. Its responsibilities include:
- Interpreting instructions from the AI agent
- Sending those instructions to the appropriate MCP Server
- Receiving results and relaying them back to the agent

<img width="1514" height="987" alt="mcpserver" src="https://github.com/user-attachments/assets/2d41d93a-7478-4dc3-bc75-8b285d2eaf47" />



### Server
The **Server** is where all the actual tools and data sources live — it's the *action centre*. It can be:
- A **local app** running on your computer
- A **remote server** hosted in the cloud

It houses predefined tools and services such as APIs, file access systems, and code execution environments.

---

## Message Threading & Turn-Taking

MCP also handles **turn-taking and message threading**, ensuring that even when agents are spread across different systems — such as email, Slack, or custom tools — they remain in sync and can hand off context cleanly.

---

## Why MCP Matters

As AI becomes more collaborative and tool-dependent, MCP is setting the standard for how intelligent systems **communicate**, **integrate**, and **scale**. By providing a shared protocol, MCP reduces friction, lowers development costs, and unlocks the full potential of multi-agent AI workflows.

---

## Resources

- [Anthropic MCP Documentation](https://docs.anthropic.com)
- [MCP GitHub (modelcontextprotocol)](https://github.com/modelcontextprotocol)
- [Claude by Anthropic](https://claude.ai)

---

*Created as part of an AI learning series.*
