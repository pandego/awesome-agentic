# Awesome Agentic 🚀🧠

Opinionated picks for people building real agentic systems.

This is not a random directory. It is a practical decision map for the agentic stack: frameworks, coding agents, agentic IDEs, RAG, memory, PersonalOS, browser agents, MCP, sandboxes, benchmarks, and observability.

If you are building agents seriously, you usually need several layers:

- **Builders** - frameworks, runtimes, orchestration, and agent platforms
- **Coding systems** - terminal agents, IDEs, autonomous engineers, and app builders
- **Context systems** - RAG, indexing, memory, and PersonalOS layers
- **Document systems** - OCR, parsing, layout understanding, and agent-ready extraction
- **Execution systems** - browser agents, sandboxes, MCP servers, tools, and runtime infra
- **Quality systems** - benchmarks, evals, traces, observability, and regression tests

## Contents

- [How to use this list](#how-to-use-this-list)
- [Best starting points](#best-starting-points)
- [Builders](#builders)
  - [Broad frameworks and platforms](#broad-frameworks-and-platforms)
  - [Specialized frameworks](#specialized-frameworks)
  - [Coding-agent builders](#coding-agent-builders)
  - [How to choose](#how-to-choose)
- [Coding agents and agentic IDEs](#coding-agents-and-agentic-ides)
  - [Terminal-native coding agents](#terminal-native-coding-agents)
  - [Agentic IDEs](#agentic-ides)
  - [Autonomous software engineers](#autonomous-software-engineers)
  - [App builders](#app-builders)
- [RAG, indexing, and context engineering](#rag-indexing-and-context-engineering)
  - [Graph RAG systems](#graph-rag-systems)
  - [End-to-end RAG systems](#end-to-end-rag-systems)
  - [RAG infrastructure and frameworks](#rag-infrastructure-and-frameworks)
  - [RAG evaluation and benchmarks](#rag-evaluation-and-benchmarks)
  - [Research directions worth watching](#research-directions-worth-watching)
- [OCR, document parsing, and multimodal extraction](#ocr-document-parsing-and-multimodal-extraction)
- [Memory and personal context](#memory-and-personal-context)
  - [Stateful agent platforms](#stateful-agent-platforms)
  - [Memory extraction and lifecycle layers](#memory-extraction-and-lifecycle-layers)
  - [Context engines and graph memory](#context-engines-and-graph-memory)
  - [Local-first and personal memory](#local-first-and-personal-memory)
  - [Memory evaluation and operations](#memory-evaluation-and-operations)
- [PersonalOS and AI operating systems](#personalos-and-ai-operating-systems)
- [Browser, computer-use, and web agents](#browser-computer-use-and-web-agents)
- [MCP, tools, and integrations](#mcp-tools-and-integrations)
- [Sandboxes and runtime infrastructure](#sandboxes-and-runtime-infrastructure)
- [Evaluation, benchmarks, and observability](#evaluation-benchmarks-and-observability)
  - [Agent and coding benchmarks](#agent-and-coding-benchmarks)
  - [LLM and agent eval frameworks](#llm-and-agent-eval-frameworks)
  - [Agent security and red-teaming](#agent-security-and-red-teaming)
  - [Observability and tracing](#observability-and-tracing)
- [How entries are evaluated](#how-entries-are-evaluated)
- [Contributing](#contributing)
- [Migration note](#migration-note)
- [Notes](#notes)

---

## How to use this list

Treat this as a practical stack map, not a link dump.

- If you are choosing a **general agent framework**, start with [Builders](#builders).
- If you are choosing a **coding workflow**, start with [Coding agents and agentic IDEs](#coding-agents-and-agentic-ides).
- If your agent needs knowledge, start with [RAG, indexing, and context engineering](#rag-indexing-and-context-engineering).
- If your agent needs continuity across sessions, start with [Memory and personal context](#memory-and-personal-context).
- If your agent needs to act in the world, look at [Browser, computer-use, and web agents](#browser-computer-use-and-web-agents), [MCP](#mcp-tools-and-integrations), and [Sandboxes](#sandboxes-and-runtime-infrastructure).
- If you want to know whether it actually works, start with [Evaluation, benchmarks, and observability](#evaluation-benchmarks-and-observability).

Many projects blur category boundaries. That is fine. The goal is useful orientation for builders, not taxonomy perfection.

---

## Best starting points

Fast recommendations if you do not want to read everything first.

- **Best default orchestration layer:** [LangGraph](https://github.com/langchain-ai/langgraph)
- **Best typed Python agent framework:** [PydanticAI](https://github.com/pydantic/pydantic-ai)
- **Best lightweight Python SDK:** [OpenAI Agents Python SDK](https://github.com/openai/openai-agents-python)
- **Best role-based multi-agent framework:** [CrewAI](https://github.com/crewAIInc/crewAI)
- **Best realtime voice/multimodal agent framework:** [LiveKit Agents](https://github.com/livekit/agents)
- **Best terminal coding agents to compare first:** [Claude Code](https://github.com/anthropics/claude-code), [Codex CLI](https://github.com/openai/codex), [Gemini CLI](https://github.com/google-gemini/gemini-cli), [Aider](https://github.com/Aider-AI/aider), [OpenCode](https://github.com/anomalyco/opencode), [OpenHands](https://github.com/OpenHands/OpenHands)
- **Best agentic IDEs to compare first:** [Cursor](https://cursor.com/), [Windsurf](https://windsurf.com/), [Zed](https://zed.dev/)
- **Best autonomous software engineer reference:** [Devin](https://devin.ai/) and [OpenHands](https://github.com/OpenHands/OpenHands)
- **Best RAG/context starting points:** [LlamaIndex](https://github.com/run-llama/llama_index), [Haystack](https://github.com/deepset-ai/haystack), [RAGFlow](https://github.com/infiniflow/ragflow), [R2R](https://github.com/SciPhi-AI/R2R), [Onyx](https://github.com/onyx-dot-app/onyx)
- **Best GraphRAG starting points:** [Microsoft GraphRAG](https://github.com/microsoft/graphrag), [LightRAG](https://github.com/HKUDS/LightRAG), [Neo4j GraphRAG for Python](https://github.com/neo4j/neo4j-graphrag-python)
- **Best document parsing/OCR starting points:** [Docling](https://github.com/docling-project/docling), [Marker](https://github.com/datalab-to/marker), [MinerU](https://github.com/opendatalab/MinerU), [LiteParse](https://github.com/run-llama/liteparse), [olmOCR](https://github.com/allenai/olmocr), [LlamaParse](https://www.llamaindex.ai/llamaparse)
- **Best memory starting points:** [Mem0](https://github.com/mem0ai/mem0), [Letta](https://github.com/letta-ai/letta), [Cognee](https://github.com/topoteretes/cognee), [Zep](https://github.com/getzep/zep), [Supermemory](https://github.com/supermemoryai/supermemory)
- **Best PersonalOS / AI OS starting points:** [Personal AI Infrastructure](https://github.com/danielmiessler/Personal_AI_Infrastructure), [OpenClaw](https://github.com/openclaw/openclaw), [QwenPaw](https://github.com/agentscope-ai/QwenPaw), [Thoth](https://github.com/siddsachar/Thoth), [Aman Khan's Personal OS](https://github.com/amanaiproduct/personal-os)
- **Best browser-agent stack to compare first:** [Browser Use](https://github.com/browser-use/browser-use), [Stagehand](https://github.com/browserbase/stagehand), [Browserbase](https://www.browserbase.com/), [TinyFish](https://www.tinyfish.ai/)
- **Best web extraction layer for agents:** [Firecrawl](https://github.com/firecrawl/firecrawl) for open crawling, [TinyFish](https://www.tinyfish.ai/) for live search/fetch plus browser-agent execution
- **Best tool integration layer to watch:** [Model Context Protocol](https://modelcontextprotocol.io/)
- **Best coding/terminal benchmarks to track:** [Terminal-Bench](https://www.tbench.ai/), [SWE-bench](https://www.swebench.com/), [SWE-agent](https://github.com/SWE-agent/SWE-agent)
- **Best broader agent benchmarks to track:** [OSWorld](https://os-world.github.io/) for real computer-use tasks, [BrowserGym](https://github.com/ServiceNow/BrowserGym) for web-agent benchmark harnesses, [τ-bench](https://taubench.com/) for tool-agent-user workflows
- **Best eval/observability stack to compare first:** [Langfuse](https://github.com/langfuse/langfuse), [Phoenix](https://github.com/Arize-ai/phoenix), [DeepEval](https://github.com/confident-ai/deepeval), [Ragas](https://github.com/vibrantlabsai/ragas)
- **Best agent security/red-team starting points:** [AgentDojo](https://github.com/ethz-spylab/agentdojo), [PyRIT](https://github.com/microsoft/PyRIT), [garak](https://github.com/NVIDIA/garak)

---

## Builders

### Broad frameworks and platforms

These are the strongest starting points when you need a general builder stack, not just one narrow capability.

### OpenClaw
- **Link:** https://github.com/openclaw/openclaw
- **Why it stands out:** open-source assistant that runs on your infra, with strong multi-channel and tool integrations for operator-style workflows.
- **Best for:** builders who want an extensible assistant product, not just a thin agent loop.

### LangGraph
- **Link:** https://github.com/langchain-ai/langgraph
- **Why it stands out:** stateful graph-based orchestration with explicit control over branching, retries, state, and durable execution flow.
- **Best for:** teams building complex, long-running, or production-oriented agent systems.

### PydanticAI
- **Link:** https://github.com/pydantic/pydantic-ai
- **Why it stands out:** typed agent framework with strong validation, tool orchestration, and Python-first ergonomics.
- **Best for:** builders who care about correctness, schema discipline, and maintainability.

### OpenAI Agents Python SDK
- **Link:** https://github.com/openai/openai-agents-python
- **Why it stands out:** lightweight but practical primitives for tools, handoffs, tracing, and multi-agent workflows.
- **Best for:** Python teams that want a fast path to structured assistant behavior.

### Google ADK (Python)
- **Link:** https://github.com/google/adk-python
- **Why it stands out:** code-first Python toolkit for building, evaluating, and deploying agents with broad model and provider integration surface.
- **Best for:** builders who want flexibility and momentum in Python ecosystems.

### Microsoft Agent Framework
- **Link:** https://github.com/microsoft/agent-framework
- **Why it stands out:** broad builder platform with clear first-party docs, orchestration primitives, and serious Python plus .NET support.
- **Best for:** teams that want a cross-language agent platform with strong vendor backing and a more platform-like posture than a lightweight SDK.

### AutoGen
- **Link:** https://github.com/microsoft/autogen
- **Why it stands out:** one of the most visible programming frameworks for multi-agent systems, with strong research and enterprise ecosystem gravity.
- **Best for:** teams exploring multi-agent patterns, conversation-based coordination, and Microsoft-backed agent research.

### Semantic Kernel
- **Link:** https://github.com/microsoft/semantic-kernel
- **Why it stands out:** mature app-integration framework for LLM workflows, planners, connectors, and enterprise-oriented AI application development.
- **Best for:** teams building agentic features inside larger enterprise software stacks.

### CrewAI
- **Link:** https://github.com/crewAIInc/crewAI
- **Why it stands out:** strong team-style abstractions for role-based, multi-agent collaboration.
- **Best for:** business workflows where explicit roles, tasks, and crews are the main mental model.

### Agno
- **Link:** https://github.com/agno-agi/agno
- **Why it stands out:** broad production-oriented surface for building, running, and managing agent platforms.
- **Best for:** teams that want an all-in-one platform-style framework.

### VoltAgent
- **Link:** https://github.com/VoltAgent/voltagent
- **Why it stands out:** modern TypeScript-first framework ergonomics for building agent applications quickly.
- **Best for:** teams that want a developer-friendly TypeScript stack.

### DSPy
- **Link:** https://github.com/stanfordnlp/dspy
- **Why it stands out:** programming model for optimizing LM pipelines instead of hand-prompting every component.
- **Best for:** builders who want systematic prompt/program optimization for RAG and agent pipelines.

### Specialized frameworks

### LiveKit Agents
- **Link:** https://github.com/livekit/agents
- **Why it stands out:** production-oriented framework for realtime voice, video, and multimodal agent systems.
- **Best for:** low-latency interactive agents where realtime UX is the product.

### Deep Agents
- **Link:** https://github.com/langchain-ai/deepagents
- **Why it stands out:** an opinionated harness on top of LangGraph with planning, filesystem-backed context, subagents, and long-running task ergonomics built in.
- **Best for:** builders who like LangGraph's control but want a sharper starting point for complex agent execution.

### Langflow
- **Link:** https://github.com/langflow-ai/langflow
- **Why it stands out:** visual system for building and deploying AI-powered agents and workflows.
- **Best for:** teams that want a low-code or visual workflow surface without losing connection to real agent stacks.

### Coding-agent builders

These are better read as execution harnesses and coding-agent products than as general-purpose agent foundations.

### Goose
- **Link:** https://github.com/aaif-goose/goose
- **Why it stands out:** open-source, extensible agent that can install, execute, edit, and test across real dev workflows.
- **Best for:** builders who want a general-purpose coding agent with broad model flexibility.

### OpenHands
- **Link:** https://github.com/OpenHands/OpenHands
- **Why it stands out:** one of the strongest open-source autonomous coding-agent projects, with CLI, SDK, local operation, and more autonomous execution patterns.
- **Best for:** builders who want an open-source coding agent that spans terminal use, local operation, and autonomous development workflows.

### SWE-agent
- **Link:** https://github.com/SWE-agent/SWE-agent
- **Why it stands out:** turns GitHub issues into attempted patches and is tightly connected to coding-agent benchmark culture.
- **Best for:** builders researching autonomous issue resolution and SWE-bench-style workflows.

### pi-mono
- **Link:** https://github.com/badlogic/pi-mono
- **Why it stands out:** lightweight coding-agent toolkit with strong terminal, markdown, and workflow utility.
- **Best for:** builders who want a focused, hackable toolkit rather than a heavyweight framework.

### How to choose

- **Want an operator-style assistant product:** start with **OpenClaw**.
- **Want explicit orchestration and durable workflows:** start with **LangGraph**.
- **Want typed Python ergonomics and validation:** start with **PydanticAI**.
- **Want lightweight Python primitives for tools and handoffs:** start with **OpenAI Agents Python SDK**.
- **Want cross-language enterprise posture:** look at **Microsoft Agent Framework** or **Semantic Kernel**.
- **Need realtime voice or multimodal experiences:** look at **LiveKit Agents**.
- **Want a more opinionated harness on top of LangGraph:** look at **Deep Agents**.
- **Need role-based multi-agent teamwork:** look at **CrewAI**.
- **Want TypeScript-first agent application ergonomics:** look at **VoltAgent**.
- **Want optimization rather than prompt fiddling:** look at **DSPy**.
- **Want visual agent/workflow building:** look at **Langflow**.
- **Want a broader open coding-agent product rather than a pure framework:** look at **OpenHands** or **Goose**.

---

## Coding agents and agentic IDEs

This is the fastest-moving part of the ecosystem. Separate terminal agents, IDEs, autonomous engineers, and app builders because they solve different problems.

### Terminal-native coding agents

These are the terminal-first harnesses and products serious builders use to execute coding work.

### Claude Code
- **Link:** https://github.com/anthropics/claude-code
- **Why it stands out:** one of the most recognizable terminal-native coding agents, with strong real-world adoption and a practical interactive workflow for repo exploration, edits, and git operations.
- **Best for:** builders who want a polished terminal coding UX with strong interactive steering.

### Codex CLI
- **Link:** https://github.com/openai/codex
- **Why it stands out:** lightweight coding agent that runs in your terminal, with strong patching, repo navigation, and task execution posture.
- **Best for:** builders who want a high-ceiling terminal harness and care about benchmark-visible execution quality.

### Gemini CLI
- **Link:** https://github.com/google-gemini/gemini-cli
- **Why it stands out:** open-source terminal agent from Google with strong ecosystem relevance.
- **Best for:** builders who want a first-party Google terminal agent in their comparison set.

### Aider
- **Link:** https://github.com/Aider-AI/aider
- **Why it stands out:** one of the clearest open-source references for repo-aware terminal coding workflows, especially pair-programming style iteration and git-centric changes.
- **Best for:** builders who want a proven open-source terminal coding assistant with a large real-user footprint.

### OpenCode
- **Link:** https://github.com/anomalyco/opencode
- **Why it stands out:** open-source coding agent with a clean terminal-first posture and strong community signal.
- **Best for:** builders who want an open-source terminal agent worth watching closely.

### Agentic IDEs

These are product surfaces where the editor becomes the agentic workspace.

### Cursor
- **Link:** https://cursor.com/
- **Why it stands out:** mainstream AI-first IDE with deep codebase awareness, agentic editing, and strong adoption among builders.
- **Best for:** teams that want the most obvious default AI IDE to compare against.

### Windsurf
- **Link:** https://windsurf.com/
- **Why it stands out:** agentic IDE focused on flow, codebase context, and AI-assisted development across larger tasks.
- **Best for:** builders comparing IDE-native agent UX against Cursor and terminal agents.

### Zed
- **Link:** https://zed.dev/
- **Why it stands out:** high-performance collaborative editor with increasing AI relevance and a strong native-editor foundation.
- **Best for:** builders who care about speed, collaboration, editor quality, and an AI-capable future path.

### Autonomous software engineers

These products and systems try to own larger chunks of software work, not just assist an edit.

### Devin
- **Link:** https://devin.ai/
- **Why it stands out:** category-defining commercial autonomous software engineer product.
- **Best for:** teams evaluating delegated engineering work beyond pair-programming.

### OpenHands
- **Link:** https://github.com/OpenHands/OpenHands
- **Why it stands out:** open-source autonomous development system with real repo execution workflows.
- **Best for:** builders who want to study or self-host autonomous coding-agent patterns.

### SWE-agent
- **Link:** https://github.com/SWE-agent/SWE-agent
- **Why it stands out:** benchmark-adjacent system for taking GitHub issues and attempting fixes.
- **Best for:** research and practical experiments around autonomous issue resolution.

### App builders

These tools turn prompts into web apps or product prototypes. They are adjacent to coding agents but deserve their own category.

### Lovable
- **Link:** https://lovable.dev/
- **Why it stands out:** popular prompt-to-app builder with strong founder/prototyping adoption.
- **Best for:** fast product prototypes and nontraditional app-building workflows.

### Bolt
- **Link:** https://bolt.new/
- **Why it stands out:** browser-based AI app builder with rapid full-stack prototyping workflows.
- **Best for:** quickly generating and iterating web apps in a hosted development environment.

### v0
- **Link:** https://v0.app/
- **Why it stands out:** strong UI-generation workflow connected to the Vercel ecosystem.
- **Best for:** frontend prototypes, UI scaffolding, and design-to-code workflows.

### Replit AI
- **Link:** https://replit.com/ai
- **Why it stands out:** AI-assisted development inside a hosted development environment.
- **Best for:** accessible app building, education, prototypes, and hosted iteration.

---

## RAG, indexing, and context engineering

Curated list of practical Retrieval-Augmented Generation systems, infrastructure, evaluation tooling, and notable research directions.

### Graph RAG systems

- **Microsoft GraphRAG** - https://github.com/microsoft/graphrag - modular graph-based RAG system for knowledge graph indexing and query-time synthesis.
- **LightRAG** - https://github.com/HKUDS/LightRAG - lightweight graph-enhanced RAG focused on simple indexing and fast retrieval.
- **Neo4j GraphRAG for Python** - https://github.com/neo4j/neo4j-graphrag-python - production-oriented GraphRAG toolkit for Python apps built on Neo4j.

### End-to-end RAG systems

- **RAGFlow** - https://github.com/infiniflow/ragflow - open-source RAG engine with document parsing, indexing, retrieval orchestration, and agent capabilities.
- **R2R** - https://github.com/SciPhi-AI/R2R - production-focused retrieval stack and API for agentic RAG workflows.
- **Onyx** - https://github.com/onyx-dot-app/onyx - open-source enterprise search and chat platform with connectors, indexing, and retrieval over private knowledge bases.
- **OpenRAG** - https://github.com/langflow-ai/openrag - packaged RAG distribution that combines Langflow, Docling, and OpenSearch into a developer-friendly agentic search stack.

### RAG infrastructure and frameworks

- **LlamaIndex** - https://github.com/run-llama/llama_index - document agent, indexing, OCR, retrieval, and data framework for context-heavy LLM applications.
- **Haystack** - https://github.com/deepset-ai/haystack - modular LLM orchestration framework with mature retrieval pipelines, routing, and evaluation building blocks.
- **Pathway** - https://github.com/pathwaycom/pathway - real-time data pipeline framework commonly used for continuously updating RAG ingestion and retrieval stacks.
- **LangChain** - https://github.com/langchain-ai/langchain - broad LLM application framework with retrieval, tools, integrations, and agent ecosystem gravity.

### RAG evaluation and benchmarks

- **Ragas** - https://github.com/vibrantlabsai/ragas - evaluation framework for LLM and RAG applications.
- **DeepEval** - https://github.com/confident-ai/deepeval - LLM evaluation framework with test-style workflows.
- **Open RAG Eval** - https://github.com/vectara/open-rag-eval - evaluates RAG quality without relying only on golden-answer datasets.
- **FlashRAG** - https://github.com/RUC-NLPIR/FlashRAG - research-oriented RAG experimentation toolkit with strong evaluation coverage across retrieval, generation, and pipeline variants.

### Research directions worth watching

- **LinearRAG** - https://github.com/DEEP-PolyU/LinearRAG - research-heavy long-context retrieval direction centered on linearized retrieval and generation flow rather than a production platform.

Projects here should earn their spot by introducing a distinct retrieval pattern, evaluation insight, or systems idea that practitioners may want to watch.

---

## OCR, document parsing, and multimodal extraction

Agents that operate businesses eventually hit messy PDFs, scans, tables, slides, charts, invoices, and reports. This section favors tools that turn documents into agent-ready Markdown, JSON, chunks, or structured data, not generic OCR demos.

### Docling
- **Link:** https://github.com/docling-project/docling
- **Why it stands out:** IBM-backed open-source parser with broad format coverage, local execution, layout/table/formula understanding, GenAI integrations, and an MCP server for agentic applications.
- **Best for:** teams that need a self-hostable document ingestion layer for RAG, agents, and sensitive enterprise documents.

### Marker
- **Link:** https://github.com/datalab-to/marker
- **Why it stands out:** high-adoption open-source converter for PDFs and office documents to Markdown, JSON, chunks, and HTML, with table/form/equation handling and optional LLM-assisted accuracy boosts.
- **Best for:** builders who want fast document-to-context conversion with hackable local control.

### MinerU
- **Link:** https://github.com/opendatalab/MinerU
- **Why it stands out:** high-adoption document parser for PDFs, images, DOCX, PPTX, and XLSX, with Markdown/JSON outputs, layout/table/formula extraction, 109-language OCR, CLI/API/WebUI deployment, and explicit pure-CPU mode via the `pipeline` backend.
- **Best for:** teams that need a stronger local multimodal document parser than lightweight PDF-only tools, while keeping an on-prem/self-hosted path for agentic ingestion.
- **License note:** MinerU uses the MinerU Open Source License, based on Apache-2.0 with additional commercial-threshold and online-service attribution conditions, so do not label it plain Apache-2.0. Last checked: 2026-05-17.

### olmOCR
- **Link:** https://github.com/allenai/olmocr
- **Why it stands out:** Allen AI toolkit and model family for linearizing PDFs into clean text, with an explicit benchmark culture around reading order, tables, multi-column pages, headers, and document structure.
- **Best for:** teams evaluating OCR quality for LLM training data, scientific PDFs, and structure-preserving document pipelines.

### LlamaParse
- **Link:** https://www.llamaindex.ai/llamaparse
- **Why it stands out:** production document parser from the LlamaIndex ecosystem with multimodal parsing, layout-aware extraction, enterprise-scale processing, and direct fit with RAG workflows.
- **Best for:** teams that want a managed parser tightly connected to LlamaIndex-style context engineering.

### LiteParse
- **Link:** https://github.com/run-llama/liteparse
- **Why it stands out:** Apache-2.0 local-first document parser from the LlamaIndex ecosystem, focused on fast PDF parsing, spatial text extraction, bounding boxes, screenshots, and Tesseract.js OCR without GPU or cloud dependency.
- **Best for:** builders who need a lightweight open-source parser for local agent/RAG ingestion before reaching for managed OCR or heavier multimodal document stacks.
- **Evidence:** active `run-llama/liteparse` repo, Apache-2.0 license, v1.5.3 release on 2026-04-29, and local/no-cloud README positioning. Last checked: 2026-05-17.

### ParseBench
- **Link:** https://arxiv.org/html/2604.08538v3
- **Why it stands out:** document parsing benchmark for AI agents that evaluates tables, charts, content faithfulness, semantic formatting, and visual grounding instead of only text similarity.
- **Best for:** builders comparing parsers on agent-critical document failures before trusting extraction in business workflows.

---

## Memory and personal context

Curated list of memory systems, layers, and operational patterns for AI agents.

The goal is not to collect every repo that says "memory". This section favors projects that help serious builders reason about how agents remember, retrieve, update, assemble, and govern context over time.

### Stateful agent platforms

Projects where memory is part of the agent architecture, not just an attached storage API.

- **Mem0** - https://github.com/mem0ai/mem0 - widely adopted universal memory layer for personalized and long-term agent memory.
- **Letta** - https://github.com/letta-ai/letta - stateful agent platform with explicit memory management and long-horizon behavior.
- **Cognee** - https://github.com/topoteretes/cognee - memory control plane and knowledge engine for agents.

### Memory extraction and lifecycle layers

Projects that expose memory APIs, tooling, or reusable building blocks rather than a full end-to-end platform.

- **LangMem** - https://github.com/langchain-ai/langmem - tools and background managers for extracting, updating, and searching agent memory.
- **Memobase** - https://github.com/memodb-io/memobase - long-term user profile memory for chatbot and assistant applications.
- **Hindsight** - https://github.com/vectorize-io/hindsight - practical memory patterns focused on improving recall from prior interactions.

### Context engines and graph memory

Systems that emphasize relationship-aware retrieval, temporal knowledge, or memory assembly across multiple sources.

- **Zep** - https://github.com/getzep/zep - context engineering platform with temporal graph retrieval for production agents.
- **Redis Agent Memory Server** - https://github.com/redis/agent-memory-server - retrieval-oriented memory service built around Redis.

### Local-first and personal memory

Projects oriented toward self-hosted, user-controlled, or assistant-facing memory experiences.

- **OpenMemory** - https://github.com/CaviraOSS/OpenMemory - local-first persistent memory for LLM apps and coding assistants.
- **Supermemory** - https://github.com/supermemoryai/supermemory - fast memory engine and API for search and recall across user context.

### Memory evaluation and operations

Operational concerns matter as much as raw retrieval quality.

Look for projects and papers that test:

- recall precision
- temporal correctness
- relevance under long-running sessions
- drift and stale-memory behavior
- multi-hop retrieval quality

Look for tools and patterns for:

- retention and TTL policies
- privacy and access controls
- auditability and traceability
- memory compaction and cleanup
- observability for what was stored and recalled

---

## PersonalOS and AI operating systems

PersonalOS is the agentic layer around a person or team: memory, tasks, notes, files, calendars, messages, automations, agents, and ambient context.

This is distinct from generic agent memory. A memory system remembers. A PersonalOS helps operate.

### Personal AI Infrastructure
- **Link:** https://github.com/danielmiessler/Personal_AI_Infrastructure
- **Why it stands out:** Claude Code-native Life Operating System with Pulse dashboard, digital-assistant identity, structured skills, workflows, hooks, and plain-text personal context.
- **Best for:** builders designing a full personal AI infrastructure layer around goals, memory, skills, and day-to-day execution.

### OpenClaw
- **Link:** https://github.com/openclaw/openclaw
- **Why it stands out:** open-source assistant product with multi-channel, tool, and operator-style workflow orientation.
- **Best for:** self-hosted or productized personal/team assistant systems.

### Personal OS
- **Link:** https://github.com/pandego/personal-os
- **Why it stands out:** blueprint for managing life and work with AI-powered workflows.
- **Best for:** people designing an opinionated personal AI operating layer.

### Aman Khan's Personal OS
- **Link:** https://github.com/amanaiproduct/personal-os
- **Why it stands out:** local AI-agent task-management framework with strong builder interest and active updates.
- **Best for:** builders studying practical local-first PersonalOS workflows around tasks and execution.

### Thoth
- **Link:** https://github.com/siddsachar/Thoth
- **Why it stands out:** local-first desktop AI assistant with personal knowledge graph, workflows, tool integrations, local model support, channels, and no hosted account requirement.
- **Best for:** builders comparing sovereign personal assistants that combine memory, automation, developer workflows, and everyday operating surfaces.

### OpenFang
- **Link:** https://github.com/RightNow-AI/openfang
- **Why it stands out:** open-source agent operating system with active releases and stronger public adoption than the older mirror.
- **Best for:** builders exploring OS-like abstractions for agents.

### QwenPaw
- **Link:** https://github.com/agentscope-ai/QwenPaw
- **Why it stands out:** self-hostable personal AI assistant with local/cloud deployment, memory, proactive scheduling, multi-channel chat, MCP, skills, and explicit tool/file security controls.
- **Best for:** builders comparing practical PersonalOS products that combine channels, personal memory, cron-like automations, and local control.

### Letta
- **Link:** https://github.com/letta-ai/letta
- **Why it stands out:** stateful agents with memory that can learn and self-improve over time.
- **Best for:** PersonalOS foundations where continuity and state are central.

### Supermemory
- **Link:** https://github.com/supermemoryai/supermemory
- **Why it stands out:** fast memory engine and app/API for recall across user context.
- **Best for:** personal memory and context layers.

### Mem0
- **Link:** https://github.com/mem0ai/mem0
- **Why it stands out:** portable memory layer that can sit underneath assistants and apps.
- **Best for:** adding personalized memory to agentic products.

---

## Browser, computer-use, and web agents

Agents need to browse, click, extract, fill forms, and operate websites. This category covers browser automation, hosted browser infra, and web extraction.

### Browser Use
- **Link:** https://github.com/browser-use/browser-use
- **Why it stands out:** popular open-source browser automation layer for AI agents.
- **Best for:** giving agents practical website interaction ability.

### Stagehand
- **Link:** https://github.com/browserbase/stagehand
- **Why it stands out:** SDK for browser agents with a developer-oriented abstraction layer.
- **Best for:** teams building browser agents on top of reliable browser infrastructure.

### Browserbase
- **Link:** https://www.browserbase.com/
- **Why it stands out:** hosted browser infrastructure for agents and web automation.
- **Best for:** production browser-agent workloads where reliability and scale matter.

### Firecrawl
- **Link:** https://github.com/firecrawl/firecrawl
- **Why it stands out:** API to search, scrape, and interact with the web for AI systems.
- **Best for:** web extraction, crawling, and agent-readable content ingestion.

### TinyFish
- **Link:** https://www.tinyfish.ai/
- **Why it stands out:** productized live-web infrastructure for agents, combining search, rendered fetch, web-agent execution, and hosted browser sessions behind one API. Its public positioning emphasizes production workflows such as dynamic pages, authenticated flows, structured outputs, and scale.
- **Best for:** teams that need agents to operate the live web, not just scrape static pages.
- **Evidence:** TinyFish reports free Search/Fetch APIs, MCP support, customer references, and an 89.9% Mind2Web web-agent accuracy claim on its product site; its GitHub org includes active agent/web extraction repos such as `tinyfish-cookbook` and `agentql`. Last checked: 2026-05-08.

---

## MCP, tools, and integrations

Tooling is where agents cross from text into action. MCP is becoming a standard integration layer for connecting models and agents to external systems.

### Model Context Protocol
- **Link:** https://modelcontextprotocol.io/
- **Why it stands out:** protocol for connecting AI systems to tools, data, and external context.
- **Best for:** builders who want a standard integration surface rather than custom tool glue everywhere.

### MCP Servers
- **Link:** https://github.com/modelcontextprotocol/servers
- **Why it stands out:** central collection of MCP servers and examples.
- **Best for:** discovering and wiring tools into MCP-capable agents.

### FastMCP
- **Link:** https://github.com/jlowin/fastmcp
- **Why it stands out:** Pythonic way to build MCP servers and clients.
- **Best for:** Python teams building custom tools for agents.

Good MCP/tool entries should be evaluated on:

- permission model
- auth/secrets handling
- reliability under repeated calls
- schema clarity
- observability
- tool discovery
- compatibility across clients

---

## Sandboxes and runtime infrastructure

Agents that execute code need isolation, process control, and safe runtime environments.

### E2B
- **Link:** https://www.e2b.dev/
- **Why it stands out:** sandbox infrastructure for AI agents and code execution.
- **Best for:** safely running generated code, tools, and experiments.

### Modal
- **Link:** https://modal.com/
- **Why it stands out:** serverless compute platform useful for AI workloads, tools, and scalable execution.
- **Best for:** teams that need elastic execution for model/tool workloads.

### Docker
- **Link:** https://www.docker.com/
- **Why it stands out:** still the default isolation primitive for many coding-agent and tool-execution stacks.
- **Best for:** local and production sandboxing where portability matters.

Look for runtime systems that provide:

- filesystem isolation
- network controls
- process lifecycle management
- reproducibility
- artifact capture
- cost controls
- audit logs

---

## Evaluation, benchmarks, and observability

Agentic systems need evals because demos lie. Benchmark scores are not the whole truth, but they are much better than vibes.

### Agent and coding benchmarks

### Terminal-Bench
- **Link:** https://www.tbench.ai/
- **Why it stands out:** benchmark for terminal-agent performance on realistic terminal tasks.
- **Best for:** comparing terminal-native coding and operator agents.

### SWE-bench
- **Link:** https://www.swebench.com/
- **Why it stands out:** benchmark for resolving real software engineering issues from GitHub repositories.
- **Best for:** evaluating autonomous coding agents and issue-resolution systems.

### SWE-agent
- **Link:** https://github.com/SWE-agent/SWE-agent
- **Why it stands out:** both a system and a research reference for issue-to-patch workflows.
- **Best for:** hands-on benchmark experimentation.

### OSWorld
- **Link:** https://os-world.github.io/
- **Why it stands out:** benchmark and executable environment for multimodal agents doing open-ended desktop and web tasks across real applications.
- **Best for:** evaluating computer-use agents beyond browser-only or coding-only tasks.

### BrowserGym
- **Link:** https://github.com/ServiceNow/BrowserGym
- **Why it stands out:** open benchmark harness for web agents that unifies MiniWoB, WebArena, WebArena Verified, VisualWebArena, WorkArena, AssistantBench, WebLINX, OpenApps, and TimeWarp-style tasks.
- **Best for:** teams evaluating browser agents across multiple web task suites without wiring every benchmark from scratch.

### τ-bench
- **Link:** https://taubench.com/
- **Why it stands out:** benchmark family for tool-agent-user interaction in realistic enterprise workflows, now extending into knowledge and full-duplex voice modes.
- **Best for:** evaluating conversational agents that must follow policy, use tools, and coordinate with users across multi-turn tasks.

Evaluation axes for coding agents:

- task completion rate
- patch correctness
- test pass rate
- repo navigation quality
- shell/tool reliability
- cost per successful task
- human steering burden
- reproducibility
- traceability

### LLM and agent eval frameworks

### DeepEval
- **Link:** https://github.com/confident-ai/deepeval
- **Why it stands out:** test-style LLM evaluation framework.
- **Best for:** teams that want CI-like evals for LLM apps and agents.

### Ragas
- **Link:** https://github.com/vibrantlabsai/ragas
- **Why it stands out:** practical eval framework for RAG and LLM applications.
- **Best for:** retrieval-heavy systems and RAG quality measurement.

### AgentEvals
- **Link:** https://github.com/langchain-ai/agentevals
- **Why it stands out:** readymade evaluators for agent trajectories.
- **Best for:** evaluating tool-use paths, trajectories, and agent behavior beyond final answers.

### Promptflow
- **Link:** https://github.com/microsoft/promptflow
- **Why it stands out:** framework for prototyping, testing, evaluating, and monitoring LLM applications.
- **Best for:** teams already aligned with Microsoft/Azure-style LLM operations.

### Agent security and red-teaming

Agentic security needs its own eval loop because prompt injection, tool misuse, data exfiltration, and unsafe action chains are runtime failures, not just model failures.

### AgentDojo
- **Link:** https://github.com/ethz-spylab/agentdojo
- **Why it stands out:** benchmark environment for prompt-injection attacks and defenses in tool-using LLM agents, with direct relevance to real assistant workflows.
- **Best for:** teams testing whether agents can keep task utility while resisting malicious instructions in workspace, travel, and tool-use scenarios.

### PyRIT
- **Link:** https://github.com/microsoft/PyRIT
- **Why it stands out:** Microsoft-backed open-source framework for proactive generative-AI risk identification and red-team automation.
- **Best for:** security teams building repeatable adversarial tests for LLM apps and agentic systems.

### garak
- **Link:** https://github.com/NVIDIA/garak
- **Why it stands out:** mature LLM vulnerability scanner with active releases and a broad probe/plugin posture.
- **Best for:** teams that want a fast baseline scan before deeper agent-specific red teaming.

### Observability and tracing

### Langfuse
- **Link:** https://github.com/langfuse/langfuse
- **Why it stands out:** open-source LLM engineering platform for observability, metrics, evals, prompt management, datasets, and traces.
- **Best for:** production LLM/agent teams that need traceability and evaluation loops.

### Phoenix
- **Link:** https://github.com/Arize-ai/phoenix
- **Why it stands out:** AI observability and evaluation platform with strong tracing and analysis posture.
- **Best for:** debugging and evaluating complex LLM and RAG systems.

### LangSmith
- **Link:** https://www.langchain.com/langsmith
- **Why it stands out:** tracing, evaluation, and observability platform integrated with the LangChain/LangGraph ecosystem.
- **Best for:** teams building on LangGraph or LangChain who want native observability.

### agenttrace
- **Link:** https://github.com/luoyuctl/agenttrace
- **Why it stands out:** local TUI and report generator for AI coding agent session logs across cost, tokens, latency, failures, anomalies, and health.
- **Best for:** builders auditing local Claude Code, Codex CLI, Gemini CLI, Aider, Cursor, OpenCode, OpenClaw, and similar coding-agent runs.

---

## How entries are evaluated

Each entry should score well on:

1. **Shipping velocity** - how quickly builders can deliver value
2. **Reliability** - error handling, stability, maintainability
3. **Ecosystem health** - active maintainers, PR throughput, docs quality
4. **Extensibility** - tooling, plugin/model/provider support
5. **Production relevance** - whether it helps teams build real systems, not just demos
6. **Distinctiveness** - whether it adds a meaningful layer, pattern, or capability instead of repeating what is already here
7. **Evidence** - benchmark, adoption, release activity, production reference, paper, or strong practitioner signal

Useful informal badges:

- **Best default** - safest first recommendation for most builders
- **Production-ready** - strong operational posture and real-world use
- **Best open-source** - strongest open-source pick in its category
- **Best for Python** - unusually good Python ergonomics
- **Best for TypeScript** - unusually good TypeScript ergonomics
- **Watchlist** - promising, but not yet a default recommendation
- **Research-only** - useful idea, not necessarily a production platform

---

## Contributing

PRs welcome. Please include:

- Why this project belongs in the list
- Category placement
- 1-2 sentence evidence-based summary with no hype
- Optional benchmark, production reference, paper, or comparison link

### Entry template

```md
### Project Name
- **Link:** https://github.com/org/repo
- **Why it stands out:** ...
- **Best for:** ...
```

Avoid adding projects only because they are new, viral, or claim to be agentic. This list should help builders choose, not drown them in options.

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
- Benchmark results should inform curation, but should not replace practical builder judgment.
- This README should stay readable. If the list grows too large, split only when the maintenance benefit is obvious.
