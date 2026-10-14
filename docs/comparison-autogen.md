# Kortix, the open-source AI Operating System, compared with AutoGen

AutoGen is a programming framework for multi-agent AI applications, and its own repository now states that it is in maintenance mode. That status is the first thing to weigh before a new project starts on it. This page compares AutoGen with Kortix, the open-source AI Operating System, on what a team owns, where the agents run, self-hosting, model choice, and who reviews a change.

## What AutoGen is

AutoGen is a framework for creating multi-agent AI applications that can act autonomously or work alongside humans. It is layered: a Core API for message passing and event-driven agents, an AgentChat API for common multi-agent patterns, and an Extensions API for model clients and capabilities. AutoGen Studio adds a no-code graphical interface for prototyping. Its repository states that AutoGen is now in maintenance mode: it will not receive new features or enhancements, it is community managed, and contributions are limited to bug fixes, security patches, and documentation. Microsoft points new projects to Microsoft Agent Framework as the successor, with a migration guide for existing users. The repository asked for Python 3.10 or later.

## What Kortix is

Your agents, their skills, your company memory, and every connector live in one git repo you own, with the agents working on real cloud computers. Each session runs one agent on its own cloud computer and its own branch, and the agent opens a change request that a person merges. The whole team's configuration lives in the repo.

## The two side by side

| Dimension | Kortix | AutoGen |
| --- | --- | --- |
| Category | Open-source AI Operating System | Multi-agent programming framework |
| Status | Actively developed | Maintenance mode, community managed |
| What you own | One git repo: agents, skills, memory, connectors, config | The Python application you write |
| Runs the agents or defines them | Runs them: a sandbox and a branch per session | Defines multi-agent apps; you run them |
| Self-host | Cloud, your VPC, or on-prem. Self-host is free | The framework runs in your own process |
| Model choice | Any provider, your own keys; or the ChatGPT plan you already pay for | Multi-provider clients such as OpenAI and Azure |
| Human review | A change request a person approves; merge is default-deny for agents | Agents act autonomously or work alongside humans |
| Source | [Kortix on GitHub](https://github.com/kortix-ai/suna) | [microsoft/autogen](https://github.com/microsoft/autogen) |

## Pick AutoGen when

You have an existing AutoGen application and you are maintaining it on bug fixes, security patches, and documentation. For a new build, the framework's own repository directs teams to Microsoft Agent Framework, so the honest starting point there is the successor project, not AutoGen.

## Pick Kortix when

You want one repo to hold the agents, their skills, company memory, and connectors, each session isolated on its own cloud computer, and a person in front of every change. Kortix fits teams that want agents running in the background across several tools with the runtime, the isolation, and the review path handled for them.

## Read next

- [Kortix vs LangGraph](comparison-langgraph.md)
- [Kortix vs CrewAI](comparison-crewai.md)
- [Choosing between a framework and a platform](choosing-a-framework.md)
- The full open-source AI agent framework comparison: [opensourceaiagentframework.com](https://opensourceaiagentframework.com/)
