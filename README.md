# Awesome Agentic 🚀🧠

Opinionated picks for people building real agentic systems.

This list consolidates three previously separate curation tracks into one canonical map of the stack:
- **Builders** - frameworks, runtimes, and agent tooling
- **RAG Systems** - retrieval systems, infra, and evaluation
- **Memory** - long-term context, memory layers, and recall systems

If you are building agents seriously, you usually need all three.

## Contents
- [How to use this list](#how-to-use-this-list)
- [Builders](#builders)
  - [Core picks](#core-picks)
  - [Specialized picks](#specialized-picks)
  - [Terminal-native coding agents](#terminal-native-coding-agents)
  - [How to choose](#how-to-choose)
- [RAG Systems](#rag-systems)
  - [Graph RAG systems](#graph-rag-systems)
  - [End-to-end RAG systems](#end-to-end-rag-systems)
  - [RAG evaluation and benchmarks](#rag-evaluation-and-benchmarks)
  - [RAG infrastructure and frameworks](#rag-infrastructure-and-frameworks)
  - [Research directions worth watching](#research-directions-worth-watching)
- [Memory](#memory)
  - [Stateful agent platforms](#stateful-agent-platforms)
  - [Memory extraction and lifecycle layers](#memory-extraction-and-lifecycle-layers)
  - [Context engines and graph memory](#context-engines-and-graph-memory)
  - [Local-first and personal memory](#local-first-and-personal-memory)
  - [Memory evaluation and operations](#memory-evaluation-and-operations)
- [How entries are evaluated](#how-entries-are-evaluated)
- [Contributing](#contributing)
- [Migration note](#migration-note)

---

## How to use this list

Treat this as a practical stack map, not a random link dump.

- **Builders** help you create and operate agents.
- **RAG systems** help agents find and synthesize external knowledge.
- **Memory systems** help agents retain, update, and retrieve context over time.

Many projects blur category boundaries. That is fine. The goal here is useful orientation for builders, not taxonomy perfection.

---

## Builders

### Core picks

### Broad frameworks and platforms

These are the strongest starting points when you need a general builder stack, not just one narrow capability.

### OpenClaw
- **Link:** https://github.com/openclaw/openclaw
- **Why it stands out:** open-source assistant that runs on your infra, with strong multi-channel and tool integrations for operator-style workflows.
- **Best for:** builders who want an extensible assistant product, not just a thin agent loop.

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

### Specialized picks

### LiveKit Agents
- **Link:** https://github.com/livekit/agents
- **Why it stands out:** production-oriented framework for realtime voice, video, and multimodal agent systems.
- **Best for:** low-latency interactive agents where realtime UX is the product.

### Deep Agents
- **Link:** https://github.com/langchain-ai/deepagents
- **Why it stands out:** a sharper harness layer on top of LangGraph with planning, filesystem-backed context, subagents, and long-running task ergonomics built in.
- **Best for:** builders who like LangGraph's control but want a more opinionated starting point for complex agent execution.

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

### Agno
- **Link:** https://github.com/agno-agi/agno
- **Why it stands out:** broad production-oriented surface for building and operating agentic software.
- **Best for:** teams that want an all-in-one platform-style framework.

### Coding-agent builders

These are better read as execution harnesses and coding-agent products than as general-purpose agent foundations.

### Goose
- **Link:** https://github.com/block/goose
- **Why it stands out:** open-source, extensible agent that can install, execute, edit, and test across real dev workflows.
- **Best for:** builders who want a general-purpose coding agent with broad model flexibility.

### Hermes Agent
- **Link:** https://github.com/NousResearch/hermes-agent
- **Why it stands out:** practical coding-agent workflows with active iteration and an experimentation-friendly posture.
- **Best for:** fast-moving builders exploring agentic engineering patterns.

### pi-mono
- **Link:** https://github.com/badlogic/pi-mono
- **Why it stands out:** lightweight coding-agent toolkit with strong terminal, markdown, and workflow utility.
- **Best for:** builders who want a focused, hackable toolkit rather than a heavyweight framework.

### Terminal-native coding agents

These are the terminal-first harnesses and products serious builders are actually using to execute coding work, not just design flows on a whiteboard.

### Codex CLI
- **Link:** https://github.com/openai/codex
- **Why it stands out:** benchmark-backed terminal coding agent with a strong mix of patching, repo navigation, and task execution. Current Terminal-Bench 2.0 leaderboard snapshots still place Codex-derived CLI entries among the strongest public terminal-agent results.
- **Best for:** builders who want a high-ceiling terminal harness and care about benchmark-visible execution quality.

### Claude Code
- **Link:** https://github.com/anthropics/claude-code
- **Why it stands out:** one of the most recognizable terminal-native coding agents, with strong real-world adoption and a very practical interactive workflow for repo exploration, edits, and iterative tasking.
- **Best for:** builders who want a polished terminal coding UX with strong interactive steering.

### Gemini CLI
- **Link:** https://github.com/google-gemini/gemini-cli
- **Why it stands out:** fast-moving terminal harness from Google with strong ecosystem relevance and improving benchmark visibility.
- **Best for:** builders who want a first-party Google terminal agent in their comparison set.

### Aider
- **Link:** https://github.com/Aider-AI/aider
- **Why it stands out:** still one of the clearest open-source references for repo-aware terminal coding workflows, especially for pair-programming style iteration and git-centric changes.
- **Best for:** builders who want a proven open-source terminal coding assistant with a big real-user footprint.

### OpenCode
- **Link:** https://github.com/sst/opencode
- **Why it stands out:** modern open-source coding agent with a clean terminal-first posture and growing relevance in the CLI agent stack.
- **Best for:** builders who want a newer open-source terminal agent worth watching closely.

### How to choose

- **Want an operator-style assistant product:** start with **OpenClaw**.
- **Want explicit orchestration and durable workflows:** start with **LangGraph**.
- **Want typed Python ergonomics and validation:** start with **PydanticAI**.
- **Want lightweight Python primitives for tools and handoffs:** start with **OpenAI Agents Python SDK**.
- **Need realtime voice or multimodal experiences:** look at **LiveKit Agents**.
- **Want a more opinionated harness on top of LangGraph:** look at **Deep Agents**.
- **Need role-based multi-agent teamwork:** look at **CrewAI**.
- **Want the strongest terminal-native coding harnesses:** compare **Codex CLI**, **Claude Code**, **Gemini CLI**, **Aider**, and **OpenCode** first.
- **Want a broader open coding-agent product rather than a pure terminal harness:** look at **Goose**.
- **Want a more experimental coding-agent harness:** compare **Hermes Agent** and **pi-mono**.

---

## RAG Systems

Curated list of practical Retrieval-Augmented Generation systems, infrastructure, evaluation tooling, and notable research directions.

### Graph RAG systems
- **Microsoft GraphRAG** - https://github.com/microsoft/graphrag - modular graph-based RAG system for knowledge graph indexing and query-time synthesis.
- **LightRAG** - https://github.com/HKUDS/LightRAG - lightweight graph-enhanced RAG focused on simple indexing and fast retrieval.
- **Neo4j GraphRAG for Python** - https://github.com/neo4j/neo4j-graphrag-python - production-oriented GraphRAG toolkit for Python apps built on Neo4j.

### End-to-end RAG systems
- **RAGFlow** - https://github.com/infiniflow/ragflow - open-source RAG engine with document parsing, indexing, and retrieval orchestration.
- **OpenRAG** - https://github.com/langflow-ai/openrag - packaged RAG distribution that combines Langflow, Docling, and OpenSearch into a developer-friendly agentic search stack.
- **R2R** - https://github.com/SciPhi-AI/R2R - production-focused retrieval stack and API for agentic RAG workflows.
- **Onyx** - https://github.com/onyx-dot-app/onyx - open-source enterprise search and chat platform with connectors, indexing, and retrieval over private knowledge bases.

### RAG evaluation and benchmarks
- **Open RAG Eval** - https://github.com/vectara/open-rag-eval - evaluates RAG quality without relying on golden-answer datasets.
- **FlashRAG** - https://github.com/RUC-NLPIR/FlashRAG - research-oriented RAG experimentation toolkit with strong evaluation coverage across retrieval, generation, and pipeline variants.

### RAG infrastructure and frameworks
- **Pathway** - https://github.com/pathwaycom/pathway - real-time data pipeline framework commonly used to build continuously updating RAG ingestion and retrieval stacks.
- **Haystack** - https://github.com/deepset-ai/haystack - modular LLM orchestration framework with mature retrieval pipelines, routing, and evaluation building blocks for production RAG systems.

### Research directions worth watching
- **LinearRAG** - https://github.com/DEEP-PolyU/LinearRAG - research-heavy long-context retrieval direction centered on linearized retrieval and generation flow rather than a production platform.

Projects here should earn their spot by introducing a distinct retrieval pattern, evaluation insight, or systems idea that practitioners may want to watch.

---

## Memory

Curated list of memory systems, layers, and operational patterns for AI agents.

The goal is not to collect every repo that says "memory". This section favors projects that help serious builders reason about how agents remember, retrieve, update, assemble, and govern context over time.

### Stateful agent platforms
Projects where memory is part of the agent architecture, not just an attached storage API.

- **Mem0** - https://github.com/mem0ai/mem0 - Widely adopted memory layer for personalized and long-term agent memory.
- **Letta** - https://github.com/letta-ai/letta - Stateful agent platform with explicit memory management and long-horizon behavior.
- **Cognee** - https://github.com/topoteretes/cognee - Knowledge engine that combines memory extraction and retrieval for agents.

### Memory extraction and lifecycle layers
Projects that expose memory APIs, tooling, or reusable building blocks rather than a full end-to-end platform.

- **LangMem** - https://github.com/langchain-ai/langmem - Tools and background managers for extracting, updating, and searching agent memory.
- **Memobase** - https://github.com/memodb-io/memobase - Long-term user profile memory for chatbot and assistant applications.
- **Hindsight** - https://github.com/vectorize-io/hindsight - Practical memory patterns focused on improving recall from prior interactions.

### Context engines and graph memory
Systems that emphasize relationship-aware retrieval, temporal knowledge, or memory assembly across multiple sources.

- **Zep** - https://github.com/getzep/zep - Context engineering platform with temporal graph retrieval for production agents.
- **Redis Agent Memory Server** - https://github.com/redis/agent-memory-server - Retrieval-oriented memory service built around Redis.

### Local-first and personal memory
Projects oriented toward self-hosted, user-controlled, or assistant-facing memory experiences.

- **OpenMemory** - https://github.com/CaviraOSS/OpenMemory - Local-first persistent memory for LLM apps and coding assistants.
- **Supermemory** - https://github.com/supermemoryai/supermemory - Fast memory engine and API for search and recall across user context.

### Memory evaluation and operations
Operational concerns matter as much as raw retrieval quality.

#### Evaluation
Look for projects and papers that test:
- recall precision
- temporal correctness
- relevance under long-running sessions
- drift and stale-memory behavior
- multi-hop retrieval quality

#### Ops
Look for tools and patterns for:
- retention and TTL policies
- privacy and access controls
- auditability and traceability
- memory compaction and cleanup
- observability for what was stored and recalled

---

## How entries are evaluated

Each entry should score well on:
1. **Shipping velocity** - how quickly builders can deliver value
2. **Reliability** - error handling, stability, maintainability
3. **Ecosystem health** - active maintainers, PR throughput, docs quality
4. **Extensibility** - tooling, plugin/model/provider support
5. **Production relevance** - whether it helps teams build real systems, not just demos
6. **Distinctiveness** - whether it adds a meaningful layer, pattern, or capability instead of repeating what is already here

---

## Contributing

PRs welcome. Please include:
- Why this project belongs in the list
- Category placement
- 1-2 sentence evidence-based summary with no hype
- Optional benchmark, production reference, or comparison link

### Entry template
```md
### Project Name
- **Link:** https://github.com/org/repo
- **Why it stands out:** ...
- **Best for:** ...
```

---

## Migration note

This repo is now the canonical umbrella list.

The previous focused repos:
- `awesome-rag-systems`
- `awesome-agentic-memory`

should remain available as lightweight pointer archives or redirect repos so existing links do not break, while all active curation happens here.

---

## Notes
- This list is intentionally opinionated and builder-first.
- Priority goes to tools that help engineers ship real agent systems, not demo-only stacks.
- If a project is interesting but not clearly stronger than existing picks, it should stay off the page until the case is obvious.
