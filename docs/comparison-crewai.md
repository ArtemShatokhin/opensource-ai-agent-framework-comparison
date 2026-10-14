# Kortix, the open-source AI Operating System, compared with CrewAI

CrewAI is an open-source Python framework for building multi-agent workflows. The runtime around those agents, the shared company state, and the review step are separate concerns, and Kortix, the open-source AI Operating System, covers them. This page compares the two on what a team owns, where the agents run, self-hosting, model choice, and who reviews a change.

## What CrewAI is

CrewAI is an open-source Python framework with high-level abstractions and low-level APIs for building multi-agent workflows. It offers two parts. Crews are teams of role-based agents that collaborate and delegate tasks among themselves. Flows are event-driven workflows that give precise control over execution paths, state between tasks, and conditional branching, with native support for Crews. An agent and a task live in project files such as `agents/*.jsonc` and `crew.jsonc`. For companies that want a control plane around the framework, the commercial CrewAI AMP Suite adds managed deployment, observability, governance, and enterprise support, and can run on-prem or in the cloud.

## What Kortix is

Your agents, their skills, your company memory, and every connector live in one git repo you own, with the agents working on real cloud computers. A session runs one agent on its own cloud computer and its own branch, and the agent opens a change request that a person merges. The configuration for the whole team lives in the repo, not in one machine.

## The two side by side

| Dimension | Kortix | CrewAI |
| --- | --- | --- |
| Category | Open-source AI Operating System | Multi-agent Python framework |
| What you own | One git repo: agents, skills, memory, connectors, config | The Python project you write |
| Runs the agents or defines them | Runs them: a sandbox and a branch per session | Defines Crews and Flows; run it yourself or on the AMP Suite |
| Self-host | Cloud, your VPC, or on-prem. Self-host is free | Framework runs locally; the AMP Suite deploys on-prem or cloud |
| Model choice | Any provider, your own keys; or the ChatGPT plan you already pay for | Model-agnostic; set the LLM per agent |
| Human review | A change request a person approves; merge is default-deny for agents | Tasks can include human review |
| Source | [Kortix on GitHub](https://github.com/kortix-ai/suna) | [crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) |

## Pick CrewAI when

You are writing a Python application and you want role-based agent collaboration or an event-driven workflow in that code. CrewAI fits teams that already run Python services and want the framework inside their process, with the option to move to a managed control plane later.

## Pick Kortix when

You want one repo to hold the agents, their skills, company memory, and connectors, each session isolated on its own cloud computer, and a human review step before a change lands. Kortix fits teams that want the agents to run in the background across several tools, rather than inside one application's process.

## Read next

- [Kortix vs LangGraph](comparison-langgraph.md)
- [Kortix vs AutoGen](comparison-autogen.md)
- [Choosing between a framework and a platform](choosing-a-framework.md)
- The full open-source AI agent framework comparison: [opensourceaiagentframework.com](https://opensourceaiagentframework.com/)
