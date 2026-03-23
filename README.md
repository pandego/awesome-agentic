# Awesome Agentic Builders 🚀

Opinionated picks for builders who want to ship real agent systems.

> Focus: coding agents, agent frameworks, and specialized layers that earn a place in a serious builder stack.

## Contents
- [Core Picks](#core-picks)
- [Specialized Picks](#specialized-picks)
- [How to choose](#how-to-choose)
- [How entries are evaluated](#how-entries-are-evaluated)
- [Contributing](#contributing)

---

## Core Picks

### OpenClaw
- **Link:** https://github.com/openclaw/openclaw
- **Why it stands out:** open-source assistant that runs on your infra, with strong multi-channel and tool integrations for operator-style workflows.
- **Best for:** builders who want an extensible assistant product, not just a thin agent loop.

### Goose
- **Link:** https://github.com/block/goose
- **Why it stands out:** open-source, extensible agent that can install, execute, edit, and test across real dev workflows.
- **Best for:** builders who want a general-purpose coding agent with broad model flexibility.

### LangGraph
- **Link:** https://github.com/langchain-ai/langgraph
- **Why it stands out:** stateful graph-based orchestration with explicit control over branching, retries, and execution flow.
- **Best for:** teams building complex, durable agent systems.

### PydanticAI
- **Link:** https://github.com/pydantic/pydantic-ai
- **Why it stands out:** typed agent framework with strong validation, tool orchestration, and Python-first ergonomics.
- **Best for:** builders who care about correctness, schema discipline, and maintainability.

### OpenAI Agents Python SDK
- **Link:** https://github.com/openai/openai-agents-python
- **Why it stands out:** lightweight but practical primitives for tools, handoffs, and multi-agent workflows.
- **Best for:** Python teams that want a fast path to structured assistant behavior.

---

## Specialized Picks

### LiveKit Agents
- **Link:** https://github.com/livekit/agents
- **Why it stands out:** production-oriented framework for realtime voice, video, and multimodal agent systems.
- **Best for:** low-latency interactive agents where realtime UX is the product.

### Deep Agents
- **Link:** https://github.com/langchain-ai/deepagents
- **Why it stands out:** a sharper harness layer on top of LangGraph with planning, filesystem-backed context, subagents, and long-running task ergonomics built in.
- **Best for:** builders who like LangGraph's control but want a more opinionated starting point for complex agent execution.

### Mem0
- **Link:** https://github.com/mem0ai/mem0
- **Why it stands out:** dedicated long-term memory layer for AI agents with retrieval, personalization, and cross-session recall patterns.
- **Best for:** products where durable context and memory quality matter more than one-shot interactions.

### Google ADK (Python)
- **Link:** https://github.com/google/adk-python
- **Why it stands out:** fast-moving, code-first Python toolkit with broad model and provider integration surface.
- **Best for:** builders who want flexibility and momentum in Python ecosystems.

### CrewAI
- **Link:** https://github.com/crewAIInc/crewAI
- **Why it stands out:** strong team-style abstractions for role-based, multi-agent collaboration.
- **Best for:** business workflows where explicit agent roles are the main mental model.

### VoltAgent
- **Link:** https://github.com/VoltAgent/voltagent
- **Why it stands out:** modern TypeScript-first framework ergonomics for building agent applications quickly.
- **Best for:** teams that want a developer-friendly TypeScript stack.

### Hermes Agent
- **Link:** https://github.com/NousResearch/hermes-agent
- **Why it stands out:** practical coding-agent workflows with active iteration and an experimentation-friendly posture.
- **Best for:** fast-moving builders exploring agentic engineering patterns.

### Agno
- **Link:** https://github.com/agno-agi/agno
- **Why it stands out:** broad production-oriented surface for building and operating agentic software.
- **Best for:** teams that want an all-in-one platform-style framework.

### pi-mono
- **Link:** https://github.com/badlogic/pi-mono
- **Why it stands out:** lightweight coding-agent toolkit with strong terminal, markdown, and workflow utility.
- **Best for:** builders who want a focused, hackable toolkit rather than a heavyweight framework.

---

## How to choose

- **Want an operator-style assistant product:** start with **OpenClaw**.
- **Want a strong general-purpose coding agent:** start with **Goose**.
- **Want explicit orchestration and durable workflows:** start with **LangGraph**.
- **Want typed Python ergonomics and validation:** start with **PydanticAI**.
- **Want lightweight Python primitives for tools and handoffs:** start with **OpenAI Agents Python SDK**.
- **Need realtime voice or multimodal experiences:** look at **LiveKit Agents**.
- **Want a more opinionated harness on top of LangGraph:** look at **Deep Agents**.
- **Need durable memory as a layer in your stack:** look at **Mem0**.
- **Need role-based multi-agent teamwork:** look at **CrewAI**.

## How entries are evaluated

Each entry should score well on:
1. **Shipping velocity** - how quickly builders can deliver value
2. **Reliability** - error handling, stability, maintainability
3. **Ecosystem health** - active maintainers, PR throughput, docs quality
4. **Extensibility** - tooling, plugin/model/provider support
5. **Production relevance** - whether it helps teams build real systems, not just demos

---

## Contributing

PRs welcome. Please include:
- Why this project belongs in the list
- Category placement
- 1-2 sentence evidence-based summary with no hype
- Optional: benchmark or reference links

### Entry template
```md
### Project Name
- **Link:** https://github.com/org/repo
- **Why it stands out:** ...
- **Best for:** ...
```

---

## Notes
- This list is intentionally opinionated and builder-first.
- Priority goes to tools that help engineers ship real agent systems, not demo-only stacks.
- If a project is interesting but not clearly stronger than existing picks, it should stay off the page until the case is obvious.
