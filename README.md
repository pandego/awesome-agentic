# Awesome Agents 🚀

Curated list of agentic tools for builders who ship.

> Focus: coding agents, memory-strong assistants, and fast agent frameworks.

## Contents
- [Coding Agents (Terminal-First)](#coding-agents-terminal-first)
- [Coding Assistants (Memory / Workflow)](#coding-assistants-memory--workflow)
- [Agent Frameworks (Build Fast)](#agent-frameworks-build-fast)
- [How entries are evaluated](#how-entries-are-evaluated)
- [Contributing](#contributing)

---

## Coding Agents (Terminal-First)

### OpenClaw
- **Link:** https://github.com/openclaw/openclaw
- **Why it stands out:** open-source assistant that runs on your infra, strong multi-channel + tool integrations, great for autonomous workflows.
- **Best for:** operators who want control + extensibility.

### Hermes Agent
- **Link:** https://github.com/NousResearch/hermes-agent
- **Why it stands out:** practical coding-agent workflows with active iteration.
- **Best for:** fast-moving agentic engineering experimentation.

### Goose
- **Link:** https://github.com/block/goose
- **Why it stands out:** open-source, extensible agent that can install, execute, edit, and test across real dev workflows.
- **Best for:** builders who want a general-purpose coding agent with broad model flexibility.

### pi-mono
- **Link:** https://github.com/badlogic/pi-mono
- **Why it stands out:** lightweight terminal-style productivity + markdown-oriented workflow surfaces.
- **Best for:** builders who want simple, focused dev loops.

---

## Coding Assistants (Memory / Workflow)

### OpenClaw (memory-driven assistants)
- **Link:** https://github.com/openclaw/openclaw
- **Strength:** persistent memory, multi-session orchestration, channel-native ops.
- **Use when:** you need continuity across days/projects.

### OpenAI Agents Python SDK
- **Link:** https://github.com/openai/openai-agents-python
- **Strength:** practical building blocks for assistant workflows, tool calls, handoffs.
- **Use when:** you want structured Python-first assistant behavior.

### Google ADK (Python)
- **Link:** https://github.com/google/adk-python
- **Strength:** rapidly evolving agent workflows, model/provider integration surface.
- **Use when:** you need speed and broad integrations in Python ecosystems.

### Mem0
- **Link:** https://github.com/mem0ai/mem0
- **Strength:** dedicated long-term memory layer for AI agents with retrieval, personalization, and cross-session recall patterns.
- **Use when:** memory quality and durable user context matter more than one-shot interactions.

---

## Agent Frameworks (Build Fast)

### Agno
- **Link:** https://github.com/agno-agi/agno
- **Why it’s great:** speed to production + pragmatic APIs.
- **Use when:** you want to ship agent systems quickly.

### PydanticAI
- **Link:** https://github.com/pydantic/pydantic-ai
- **Why it’s great:** typed agent framework with strong validation, tool orchestration, and Python-first ergonomics.
- **Use when:** correctness, schema discipline, and structured agent behavior matter.

### LangGraph
- **Link:** https://github.com/langchain-ai/langgraph
- **Why it’s great:** stateful/graph-oriented agent orchestration.
- **Use when:** you need explicit control over branching and execution graphs.

### CrewAI
- **Link:** https://github.com/crewAIInc/crewAI
- **Why it’s great:** multi-agent collaboration patterns and team-style orchestration.
- **Use when:** role-based agent cooperation is core.

### LiveKit Agents
- **Link:** https://github.com/livekit/agents
- **Why it’s great:** production-oriented framework for realtime voice, video, and multimodal agent systems.
- **Use when:** low-latency, interactive agent experiences are the product.

### VoltAgent
- **Link:** https://github.com/VoltAgent/voltagent
- **Why it’s great:** modern framework ergonomics for agent app development.
- **Use when:** you want quick full-stack-ish agent implementations.

---

## How entries are evaluated

Each entry should score well on:
1. **Shipping velocity** (how quickly builders can deliver value)
2. **Reliability** (error handling, stability, maintainability)
3. **Ecosystem health** (active maintainers, PR throughput, docs quality)
4. **Extensibility** (tooling, plugin/model/provider support)
5. **Production readiness** (observability, config sanity, deployment posture)

---

## Contributing

PRs welcome. Please include:
- Why this project belongs in the list
- Category placement
- 1–2 sentence evidence-based summary (no hype)
- Optional: benchmark/reference links

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
