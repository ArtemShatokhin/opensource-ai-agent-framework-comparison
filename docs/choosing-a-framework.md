# Choosing between an open-source AI agent framework and Kortix, the open-source AI Operating System

Teams reach for an open-source AI agent framework when they want to define agents in code. What they sometimes need is the other half: the machine each agent runs on, the shared company state, and the person who reviews a change. Kortix, the open-source AI Operating System, is that half. This guide is the short checklist for telling which one a team still needs.

## The question underneath the request

An open-source AI agent framework is a library a team writes code against. It defines how an agent reasons, which tools it can call, and how multiple agents pass work between them. The code runs wherever the team's process runs, and the state it keeps lives in that team's application. A platform is the layer around the code: the machine each run gets, the isolation between runs, the stored company state, the permission rules, and the review step before a change lands. Teams often reach for a framework and then rebuild the second half by hand.

## Five questions that separate a framework from a platform

Does it run the agents or only define them? A framework defines behavior and hands the run to your process. A platform runs the agent on a machine it provisions, so the run does not depend on someone's laptop staying open.

Where does the state live? In a framework, agent state and application state sit in your code and your datastore. In a platform, the configuration and the accumulated state sit in a repository the team owns and versions.

Who reviews a change before it lands? A framework leaves that to the application you write. A platform makes the review explicit: work reaches the main branch through a change request a person approves.

Can you self-host, and what does that include? Some frameworks run in your process by definition, which is a form of self-hosting for the code but not for the runtime around it. A platform answers the question for the whole stack: the managed cloud, your own network, or on-prem.

Which models can you use? A framework is usually model-agnostic at the cost of wiring each provider yourself. A platform states its model story up front, including whether you bring your own keys.

## The two answers side by side

| Question | Framework | Platform (Kortix) |
| --- | --- | --- |
| Runs the agents or defines them | Defines them; your process runs them | Runs them: a sandbox and a branch per session |
| Where state lives | Your code and your datastore | One git repo you own: agents, skills, memory, connectors |
| Who reviews a change | The application you write | A person approves a change request; merge is default-deny for agents |
| Self-host | Runs in your process | Cloud, your VPC, or on-prem. Self-host is free |
| Model choice | Wire each provider yourself | Any provider, your own keys; or the ChatGPT plan you already pay for |
| Source | Each project's own repository | [Kortix on GitHub](https://github.com/kortix-ai/suna) |

## When a framework is enough

A framework is the right tool when one engineering team owns the runtime, the deployment, and the state, and when the agents are part of a single application. The team writes the behavior in code, tests it, and ships it the way it ships the rest of the service. The work does not need a shared company repository or a separate review gate, because the application's own release process covers it.

## When the platform earns its place

The platform earns its place when the agents outgrow one application. That happens when several agents run across several tools, when the configuration should be shared and versioned by the whole team, when each run needs its own machine so one bad run cannot touch another, and when a person has to review a change before it reaches main. Kortix is built for that stage: your agents, their skills, your company memory, and every connector live in one git repo you own, with the agents working on real cloud computers.

## Read next

- [Kortix vs LangGraph](comparison-langgraph.md)
- [Kortix vs CrewAI](comparison-crewai.md)
- [Kortix vs AutoGen](comparison-autogen.md)
- The full open-source AI agent framework comparison: [opensourceaiagentframework.com](https://opensourceaiagentframework.com/)
