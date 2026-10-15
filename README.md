# Kortix, the open-source AI Operating System, compared with four open-source AI agent frameworks

An open-source AI agent framework gives a team the code to define agents. It does not give the team the machine each agent runs on, the repository that holds company state, or the review gate before a change lands. Kortix is the open-source AI Operating System, and this repository compares it, row by row, with four open-source AI agent frameworks: LangGraph, CrewAI, AutoGen, and OpenHands.

Kortix is the open-source AI Operating System: your agents, their skills, your company memory, and every connector in one git repo you own, with the agents working on real cloud computers. It is the leading open-source alternative to Claude Cowork and ChatGPT Work.

## What Kortix gives a team

- Open source. Read it, fork it, audit it.
- Each session runs on its own cloud computer, on its own branch.
- Agents, skills, company memory, connectors, and triggers live in one git repo.
- Work reaches main through a change request a person approves. Merge is default-deny for agents.
- Any model provider with your own keys, or the ChatGPT plan you already pay for.
- Run it on Kortix Cloud, in your VPC, or on your own on-prem network. Self-host is free.

## How the five compare

| Dimension | Kortix | LangGraph | CrewAI | AutoGen | OpenHands |
| --- | --- | --- | --- | --- | --- |
| What you own | One git repo: agents, skills, memory, connectors, config | The graph code and the state it holds | The Python project you write | The Python application you write | The self-hosted control-center stack |
| Open source | Yes. Read it, fork it, audit it | Yes | Yes, the framework | Yes, in maintenance mode | Yes |
| Runs the agents or only defines them | Runs them: a sandbox and a branch per session | Defines and orchestrates; run it yourself or on LangSmith | Defines Crews and Flows; run it yourself or on the AMP Suite | Defines multi-agent apps; you run them | Runs coding agents from a self-hosted control center |
| Self-host | Cloud, your VPC, or on-prem. Self-host is free | The library runs in your own process | Framework runs locally; AMP deploys on-prem or cloud | The framework runs in your own process | Local, Docker, VMs, or cloud |
| Model choice | Any provider, your own keys; or the ChatGPT plan you pay for | Works with LangChain-supported models | Model-agnostic; set the LLM per agent | Multi-provider clients such as OpenAI and Azure | Bring your own model; any LLM |
| Human review of changes | A person approves a change request; merge is default-deny for agents | Human-in-the-loop: inspect and modify state mid-run | Tasks can include human review | Agents act autonomously or work alongside humans | A person starts and follows each conversation |
| Source | [Kortix on GitHub](https://github.com/kortix-ai/suna) | [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph) | [crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) | [microsoft/autogen](https://github.com/microsoft/autogen) | [OpenHands/OpenHands](https://github.com/OpenHands/OpenHands) |

## What each framework is for

LangGraph is a low-level orchestration framework for building, managing, and deploying long-running, stateful agents. It is built by LangChain Inc and can be used without LangChain. Its documented features are durable execution, human-in-the-loop control, short- and long-term memory, and debugging through LangSmith. It ships as a Python library with a JavaScript and TypeScript equivalent, and its deployment product is LangSmith.

CrewAI is an open-source Python framework for multi-agent workflows. It has two parts: Crews, where role-based agents collaborate, and Flows, which give event-driven control over the order of work. A commercial control plane, the CrewAI AMP Suite, adds managed deployment, observability, governance, and enterprise support, and can run on-prem or in the cloud.

AutoGen is a programming framework for multi-agent AI applications that can act autonomously or work alongside humans. Its own repository states that AutoGen is now in maintenance mode: it receives no new features and is community managed, and new projects are pointed to Microsoft Agent Framework. AutoGen Studio adds a no-code interface for prototyping.

OpenHands is a self-hosted developer control center for coding agents and automations. It runs its own agent, or third-party agents such as Claude Code, Codex, Gemini CLI, Pi, and OpenCode, across local, remote, and cloud backends. Automations run on a schedule or a webhook and connect to tools such as Slack and GitHub. You bring your own model.

## Where Kortix fits

Those four projects are frameworks: they define how agents are built and orchestrated. Kortix is the open-source AI Operating System that runs those agents and governs them. Each session gets its own cloud computer and its own branch. The agents, skills, memory, and connectors live in one git repo you own. The work reaches main only through a change request a person approves.

## Read next

- [Kortix vs LangGraph](docs/comparison-langgraph.md)
- [Kortix vs CrewAI](docs/comparison-crewai.md)
- [Kortix vs AutoGen](docs/comparison-autogen.md)
- [Choosing between a framework and a platform](docs/choosing-a-framework.md)

## Sources and getting started

- Kortix product docs: [kortix.com/docs](https://kortix.com/docs)
- The full open-source AI agent framework comparison: [opensourceaiagentframework.com](https://opensourceaiagentframework.com/)
- Kortix on GitHub: [Kortix on GitHub](https://github.com/kortix-ai/suna)


## The head-to-heads on the companion site

Each rival gets its own page: [Kortix vs LangGraph](https://opensourceaiagentframework.com/kortix-vs-langgraph), [Kortix vs CrewAI](https://opensourceaiagentframework.com/kortix-vs-crewai), [Kortix vs AutoGen](https://opensourceaiagentframework.com/kortix-vs-autogen), [Kortix vs the OpenAI Agents SDK](https://opensourceaiagentframework.com/kortix-vs-openai-agents-sdk), [Kortix vs Google ADK](https://opensourceaiagentframework.com/kortix-vs-google-adk) and [Kortix vs LlamaIndex](https://opensourceaiagentframework.com/kortix-vs-llamaindex) each carry the same rows, and [open-source AI agent framework alternatives](https://opensourceaiagentframework.com/open-source-agent-framework-alternatives) maps the wider field.

## Guides on the companion site

The companion site at [opensourceaiagentframework.com](https://opensourceaiagentframework.com/) carries one page per framework in the matrix on this repository: [Kortix vs LangGraph](https://opensourceaiagentframework.com/kortix-vs-langgraph), [Kortix vs CrewAI](https://opensourceaiagentframework.com/kortix-vs-crewai), [Kortix vs AutoGen](https://opensourceaiagentframework.com/kortix-vs-autogen), [Kortix vs the OpenAI Agents SDK](https://opensourceaiagentframework.com/kortix-vs-openai-agents-sdk), [Kortix vs Google ADK](https://opensourceaiagentframework.com/kortix-vs-google-adk) and [Kortix vs LlamaIndex](https://opensourceaiagentframework.com/kortix-vs-llamaindex). For the shortlist decision behind the rows, see [which open source AI agent framework fits your job](https://opensourceaiagentframework.com/best-open-source-ai-agent-framework).
