# Kortix, the open-source AI Operating System, compared with LangGraph

LangGraph is a low-level orchestration framework for building stateful agents. The machine each agent runs on, the repository that holds company state, and the gate before a change lands are the other half of the problem, and Kortix, the open-source AI Operating System, handles that half. This page compares them row by row.

## What LangGraph is

LangGraph is a low-level orchestration framework for building, managing, and deploying long-running, stateful agents. It is built by LangChain Inc, the maker of LangChain, and can be used without LangChain. Its documented features are durable execution, human-in-the-loop control, short- and long-term memory, and debugging through LangSmith. It ships as a Python library with a JavaScript and TypeScript equivalent, and its deployment product is LangSmith, which handles scale for long-running, stateful workflows. The framework itself runs inside your own process.

## What Kortix is

Your agents, their skills, your company memory, and every connector live in one git repo you own, with the agents working on real cloud computers. A project is a git repo with `kortix.yaml` at its root. A session runs one agent on its own cloud computer and its own branch. The agent commits, pushes, and opens a change request, and a person merges it.

## The two side by side

| Dimension | Kortix | LangGraph |
| --- | --- | --- |
| Category | Open-source AI Operating System | Orchestration framework |
| What you own | One git repo: agents, skills, memory, connectors, config | The graph code and the state it holds |
| Runs the agents or defines them | Runs them: a sandbox and a branch per session | Defines them; run the process yourself or deploy on LangSmith |
| Model choice | Any provider, your own keys; or the ChatGPT plan you already pay for | Works with LangChain-supported models |
| Human review | A change request a person approves; merge is default-deny for agents | Human-in-the-loop: inspect and modify state mid-run |
| Source | [Kortix on GitHub](https://github.com/kortix-ai/suna) | [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph) |

## Pick LangGraph when

You are building one agent's behavior in code and you want control over the graph, the state, and the execution loop. LangGraph fits a single engineering team that owns the runtime and the deployment, and it fits applications where the agent's state is the application's own concern, held and moved by that team's code.

## Pick Kortix when

You want the agents, their skills, company memory, and connectors in one repo, each session on its own cloud computer, and a review step before anything reaches main. Kortix fits teams that run several agents across several tools, in the background, without building the runtime, the isolation, and the review path around each one.

## Read next

- [Kortix vs CrewAI](comparison-crewai.md)
- [Kortix vs AutoGen](comparison-autogen.md)
- [Choosing between a framework and a platform](choosing-a-framework.md)
- The full open-source AI agent framework comparison: [opensourceaiagentframework.com](https://opensourceaiagentframework.com/)
