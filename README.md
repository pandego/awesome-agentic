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
- **Best full-stack TypeScript agent framework:** [Mastra](https://github.com/mastra-ai/mastra)
- **Best lightweight Python SDK:** [OpenAI Agents Python SDK](https://github.com/openai/openai-agents-python)
- **Best role-based multi-agent framework:** [CrewAI](https://github.com/crewAIInc/crewAI)
- **Best realtime voice/multimodal agent frameworks:** [LiveKit Agents](https://github.com/livekit/agents), [Pipecat](https://github.com/pipecat-ai/pipecat), [TEN Framework](https://github.com/TEN-framework/ten-framework)
- **Best terminal coding agents to compare first:** [Claude Code](https://github.com/anthropics/claude-code), [Codex CLI](https://github.com/openai/codex), [Gemini CLI](https://github.com/google-gemini/gemini-cli), [Aider](https://github.com/Aider-AI/aider), [OpenCode](https://github.com/anomalyco/opencode), [Pi](https://github.com/earendil-works/pi), [OpenHands](https://github.com/OpenHands/OpenHands)
- **Best agentic IDEs to compare first:** [Cursor](https://cursor.com/), [Windsurf](https://windsurf.com/), [Cline](https://github.com/cline/cline), [Zed](https://zed.dev/)
- **Best autonomous software engineer reference:** [Devin](https://devin.ai/) and [OpenHands](https://github.com/OpenHands/OpenHands)
- **Best RAG/context starting points:** [LlamaIndex](https://github.com/run-llama/llama_index), [Haystack](https://github.com/deepset-ai/haystack), [RAGFlow](https://github.com/infiniflow/ragflow), [R2R](https://github.com/SciPhi-AI/R2R), [Onyx](https://github.com/onyx-dot-app/onyx), [OpenViking](https://github.com/volcengine/OpenViking)
- **Best GraphRAG starting points:** [Microsoft GraphRAG](https://github.com/microsoft/graphrag), [LightRAG](https://github.com/HKUDS/LightRAG), [Neo4j GraphRAG for Python](https://github.com/neo4j/neo4j-graphrag-python)
- **Best document parsing/OCR starting points:** [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR), [Docling](https://github.com/docling-project/docling), [Marker](https://github.com/datalab-to/marker), [MinerU](https://github.com/opendatalab/MinerU), [LiteParse](https://github.com/run-llama/liteparse), [olmOCR](https://github.com/allenai/olmocr), [LlamaParse](https://www.llamaindex.ai/llamaparse)
- **Best memory starting points:** [Mem0](https://github.com/mem0ai/mem0), [Letta](https://github.com/letta-ai/letta), [Cognee](https://github.com/topoteretes/cognee), [Zep](https://github.com/getzep/zep), [MemOS](https://github.com/MemTensor/MemOS), [EverOS](https://github.com/EverMind-AI/EverOS), [Signet](https://github.com/Signet-AI/signetai), [Supermemory](https://github.com/supermemoryai/supermemory), [Screenpipe](https://github.com/screenpipe/screenpipe)
- **Best agent-memory benchmark to track:** [AMA-Bench](https://github.com/AMA-Bench/AMA-Bench) for long-horizon memory over real agent trajectories, not dialogue-only recall
- **Best PersonalOS / AI OS starting points:** [LifeOS / Personal AI Infrastructure](https://github.com/danielmiessler/LifeOS), [OpenClaw](https://github.com/openclaw/openclaw), [Hermes Agent](https://github.com/NousResearch/hermes-agent), [Nanobot](https://github.com/HKUDS/nanobot), [OpenHuman](https://github.com/tinyhumansai/openhuman), [CORE](https://github.com/RedPlanetHQ/core), [OpenJarvis](https://github.com/open-jarvis/OpenJarvis), [OpenFang](https://github.com/RightNow-AI/openfang), [IronClaw](https://github.com/nearai/ironclaw), [Row-Bot](https://github.com/siddsachar/row-bot), [QwenPaw](https://github.com/agentscope-ai/QwenPaw), [Khoj](https://github.com/khoj-ai/khoj), [AIOS](https://github.com/agiresearch/AIOS), [OpenDAN](https://github.com/fiatrete/OpenDAN-Personal-AI-OS), [Aman Khan's Personal OS](https://github.com/amanaiproduct/personal-os), [Dex](https://github.com/davekilleen/Dex)
- **Best PersonalOS benchmark to track:** [π-Bench](https://github.com/Simplified-Reasoning/Pi-Bench) for proactive help across long-horizon, multi-session workflows
- **Best browser/computer-use stack to compare first:** [Agent S](https://github.com/simular-ai/Agent-S), [Agent Desktop](https://github.com/lahfir/agent-desktop), [Agent Browser](https://github.com/vercel-labs/agent-browser), [Browser Use](https://github.com/browser-use/browser-use), [Stagehand](https://github.com/browserbase/stagehand), [Browserbase](https://www.browserbase.com/), [TinyFish](https://www.tinyfish.ai/)
- **Best web extraction layer for agents:** [Firecrawl](https://github.com/firecrawl/firecrawl) for open crawling, [TinyFish](https://www.tinyfish.ai/) for live search/fetch plus browser-agent execution
- **Best MCP integration, gateway, and runtime layers:** [Model Context Protocol](https://modelcontextprotocol.io/), [MCP Registry](https://modelcontextprotocol.io/registry/about), [FastMCP](https://github.com/PrefectHQ/fastmcp), [mcp-agent](https://github.com/lastmile-ai/mcp-agent), [ContextForge](https://github.com/IBM/mcp-context-forge), [Agentgateway](https://github.com/agentgateway/agentgateway), [ToolHive](https://github.com/stacklok/toolhive)
- **Best MCP tool-use benchmark to track:** [MCPMark Verified](https://github.com/eval-sys/mcpmark) for reproducible work across real Notion, GitHub, filesystem, Postgres, and browser tools
- **Best agent-native project/task layer:** [Backlog.md](https://github.com/MrLesk/Backlog.md)
- **Best sandbox/runtime layers to compare first:** [E2B](https://www.e2b.dev/), [Daytona](https://github.com/daytonaio/daytona), [Fly.io Sprites](https://fly.io/sprites/), [OpenSandbox](https://github.com/opensandbox-group/OpenSandbox), [Kubernetes Agent Sandbox](https://github.com/kubernetes-sigs/agent-sandbox), [Modal](https://modal.com/)
- **Best coding/terminal benchmarks to track:** [Artificial Analysis Coding Agent Index](https://artificialanalysis.ai/agents/coding-agents) for harness, cost, and runtime comparisons, [Terminal-Bench](https://www.tbench.ai/), [Long-Horizon Terminal-Bench](https://github.com/zli12321/LHTB) for sustained hundred-step work, [SWE-bench](https://www.swebench.com/), [ProgramBench](https://github.com/facebookresearch/ProgramBench) for building whole programs from scratch, and [mini-SWE-agent](https://github.com/SWE-agent/mini-swe-agent) as a minimal reproducible baseline
- **Best broader agent benchmarks to track:** [HAL](https://hal.cs.princeton.edu/) for cost-aware comparisons across benchmark families, [WebArena-Verified](https://github.com/ServiceNow/webarena-verified) for reproducible browser workflows, [WebBench](https://github.com/Halluminate/WebBench) for live-web read/write tasks and infrastructure failures, [OSWorld](https://os-world.github.io/) and [Windows Agent Arena](https://github.com/microsoft/WindowsAgentArena) for real computer-use tasks, [BrowserGym](https://github.com/ServiceNow/BrowserGym) for web-agent benchmark harnesses, [τ-bench](https://taubench.com/) for tool-agent-user workflows, [TRAIL](https://github.com/patronus-ai/trail-benchmark) for debugging long agent traces
- **Best realtime voice-model leaderboard:** [Artificial Analysis Speech to Speech Index](https://artificialanalysis.ai/speech-to-speech) for reasoning, conversational dynamics, grounded tool-use completion, latency, and price in one comparison
- **Best eval/observability stack to compare first:** [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai), [MLflow](https://github.com/mlflow/mlflow), [Langfuse](https://github.com/langfuse/langfuse), [Phoenix](https://github.com/Arize-ai/phoenix), [Opik](https://github.com/comet-ml/opik), [Laminar](https://github.com/lmnr-ai/lmnr), [DeepEval](https://github.com/confident-ai/deepeval), [Promptfoo](https://github.com/promptfoo/promptfoo), [Ragas](https://github.com/vibrantlabsai/ragas)
- **Best portable agent telemetry layers:** [OpenInference](https://github.com/Arize-ai/openinference) for cross-language agent/RAG instrumentation, [OpenLLMetry](https://github.com/traceloop/openllmetry) for Python-first auto-instrumentation into existing OpenTelemetry backends
- **Best agent security, governance, and red-team starting points:** [Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit), [AgentDojo](https://github.com/ethz-spylab/agentdojo), [DecodingTrust-Agent](https://github.com/AI-secure/DecodingTrust-Agent), [MCP Security Bench](https://github.com/dongsenzhang/MSB), [AgentDoG](https://github.com/AI45Lab/AgentDoG), [Snyk Agent Scan](https://github.com/snyk/agent-scan), [DeepTeam](https://github.com/confident-ai/deepteam), [Promptfoo](https://github.com/promptfoo/promptfoo), [PyRIT](https://github.com/microsoft/PyRIT), [garak](https://github.com/NVIDIA/garak)

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

### Mastra
- **Link:** https://github.com/mastra-ai/mastra
- **Why it stands out:** TypeScript-first framework that combines agents, resumable graph workflows, memory, MCP, evals, observability, and Node-compatible deployment instead of requiring a separate package for every production layer.
- **Best for:** TypeScript teams that want an integrated path from agent prototype to deployed application.
- **Evidence:** 26k+ GitHub stars and active July 2026 releases; the core is Apache-2.0, while `ee/` features use the Mastra Enterprise License. Last checked: 2026-07-23.

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
- **Why it stands out:** production-grade Python and .NET framework that unifies graph workflows, durable checkpoints, multi-agent patterns, middleware, memory, OpenTelemetry, MCP, and A2A behind stable 1.0 APIs.
- **Best for:** cross-language enterprise teams that need provider flexibility and an official migration path from AutoGen or Semantic Kernel rather than a lightweight agent loop.
- **Evidence:** MIT-licensed, 12.8k+ GitHub stars, production-ready 1.0 releases for Python and .NET, and active Python v1.14 releases through August 2026. Last checked: 2026-08-17.

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
- **Why it stands out:** Apache-2.0 Python and TypeScript framework that pairs voice-agent orchestration with WebRTC clients, telephony, job scheduling, semantic turn detection, MCP, testing, and a self-hostable media stack.
- **Best for:** production voice and video agents that need realtime transport, client SDKs, and runtime operations in one ecosystem.
- **Evidence:** 11.5k+ GitHub stars and active v1.6 releases through July 2026. Last checked: 2026-07-27.

### Pipecat
- **Link:** https://github.com/pipecat-ai/pipecat
- **Why it stands out:** open-source Python framework for realtime voice and multimodal agents, with composable audio/video pipelines, broad service integrations, client SDKs, subagents, and deployment paths.
- **Best for:** teams building voice-first agents that need low-latency orchestration across speech, tools, transports, and conversation state.

### TEN Framework
- **Link:** https://github.com/TEN-framework/ten-framework
- **Why it stands out:** active polyglot realtime framework with graph-based multimodal composition, RTC and WebSocket transports, SIP, hardware examples, VAD, turn detection, and visual tooling in one ecosystem.
- **Best for:** teams that want a lower-level, cross-language voice-agent runtime rather than a Python-only orchestration layer.

### Deep Agents
- **Link:** https://github.com/langchain-ai/deepagents
- **Why it stands out:** an opinionated harness on top of LangGraph with planning, filesystem-backed context, subagents, and long-running task ergonomics built in.
- **Best for:** builders who like LangGraph's control but want a sharper starting point for complex agent execution.

### DeerFlow
- **Link:** https://github.com/bytedance/deer-flow
- **Why it stands out:** ByteDance's MIT-licensed long-horizon harness packages LangGraph orchestration with subagents, persistent memory, skills, sandboxed execution, files, messaging channels, and tracing instead of leaving those layers as integration work.
- **Best for:** builders who want a batteries-included research-and-creation agent to run as a product or dismantle into a custom harness.
- **Evidence:** 79k+ GitHub stars, active development, and a ground-up 2.0 release backed by 182 merged PRs. Last checked: 2026-08-11.

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

### Pi
- **Link:** https://github.com/earendil-works/pi
- **Why it stands out:** unusually extensible terminal coding agent whose small agent core, unified multi-provider API, TUI library, extensions, and session tooling can also serve as a kit for building custom agents.
- **Best for:** builders who want a focused, hackable coding harness and will supply sandboxing when stronger filesystem, process, network, or credential boundaries are required.
- **Evidence:** MIT-licensed, 81k+ GitHub stars, and active v0.83 releases through July 2026. Last checked: 2026-07-31.

### How to choose

- **Want an operator-style assistant product:** start with **OpenClaw**.
- **Want explicit orchestration and durable workflows:** start with **LangGraph**.
- **Want typed Python ergonomics and validation:** start with **PydanticAI**.
- **Want lightweight Python primitives for tools and handoffs:** start with **OpenAI Agents Python SDK**.
- **Want cross-language enterprise posture:** look at **Microsoft Agent Framework** or **Semantic Kernel**.
- **Need realtime voice or multimodal experiences:** look at **LiveKit Agents**.
- **Want a more opinionated harness on top of LangGraph:** look at **Deep Agents**.
- **Need role-based multi-agent teamwork:** look at **CrewAI**.
- **Want a full-stack TypeScript agent framework:** start with **Mastra**; compare **VoltAgent** for its broader agent-engineering platform posture.
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

### Cline
- **Link:** https://github.com/cline/cline
- **Why it stands out:** Apache-2.0 coding agent that now spans VS Code, JetBrains, terminal and headless CLI use, an SDK, multi-agent teams, and human-approved file and shell actions without locking builders to one model provider.
- **Best for:** teams that want one open agent core across editor, terminal, CI, and custom coding-agent products.
- **Evidence:** 65k+ GitHub stars, active v4 releases through July 2026, and first-party SDK, CLI, IDE, MCP, and scheduled-agent surfaces. Last checked: 2026-07-25.

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
- **OpenViking** - https://github.com/volcengine/OpenViking - agent-native context database that unifies resources, memories, and skills in a virtual filesystem, with tiered loading, recursive retrieval, observable traces, and automatic session-memory extraction; AGPL-3.0 and still pre-1.0.
- **LangChain** - https://github.com/langchain-ai/langchain - broad LLM application framework with retrieval, tools, integrations, and agent ecosystem gravity.

### RAG evaluation and benchmarks

- **Ragas** - https://github.com/vibrantlabsai/ragas - evaluation framework for LLM and RAG applications.
- **DeepEval** - https://github.com/confident-ai/deepeval - LLM evaluation framework with test-style workflows.
- **Open RAG Eval** - https://github.com/vectara/open-rag-eval - evaluates RAG quality without relying only on golden-answer datasets.
- **FlashRAG** - https://github.com/RUC-NLPIR/FlashRAG - research-oriented RAG experimentation toolkit with strong evaluation coverage across retrieval, generation, and pipeline variants.

### Research directions worth watching

- **Agentic Context Engine (ACE)** - https://github.com/kayba-ai/agentic-context-engine - practical implementation of the [ACE research pattern](https://github.com/ace-agent/ace) that turns execution traces and feedback into a persistent, curated skillbook, with runners for browser-use, LangChain, Claude Code, and MCP; promising as a self-improvement layer, but still pre-1.0. Last checked: 2026-08-20.
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

### PaddleOCR
- **Link:** https://github.com/PaddlePaddle/PaddleOCR
- **Why it stands out:** Apache-2.0 document AI stack with 100+ language OCR, layout/table/formula/chart parsing, LLM-ready Markdown/JSON, compact PaddleOCR-VL models, and deployment paths from browser and edge hardware to GPU services.
- **Best for:** teams that need a mature multilingual OCR foundation plus modern structure-aware document parsing for RAG and agent workflows.
- **Evidence:** 85k+ GitHub stars, integrations with RAGFlow, Dify, Pathway, and Haystack, and active 2026 releases through v3.7.0. Last checked: 2026-07-18.

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

### PureDocBench
- **Link:** https://github.com/zhihengli-casia/PureDocBench
- **Why it stands out:** source-traceable benchmark whose images and ground truth come from the same HTML/CSS sources, with clean, digitally degraded, and real-degraded tracks for text, formulas, tables, and reading order.
- **Best for:** teams comparing parser accuracy and degradation robustness without treating noisy or saturated legacy annotations as ground truth.
- **Evidence:** 1,475 pages, 4,425 images, 40 evaluated systems, public scoring tooling, and a correction workflow for versioned ground truth. Last checked: 2026-08-06.

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
- **MemOS** - https://github.com/MemTensor/MemOS - memory operating system for LLM agents with unified graph-style memory APIs, multimodal/tool-trace memory, memory-cube isolation, and published long-memory benchmark claims.
- **Redis Agent Memory Server** - https://github.com/redis/agent-memory-server - retrieval-oriented memory service built around Redis.

### Local-first and personal memory

Projects oriented toward self-hosted, user-controlled, or assistant-facing memory experiences.

- **OpenMemory** - https://github.com/CaviraOSS/OpenMemory - local-first persistent memory for LLM apps and coding assistants.
- **Signet** - https://github.com/Signet-AI/signetai - local-first context layer for agent identity, memory, transcripts, provenance, secrets, repair, and portability across agent shells.
- **EverOS** - https://github.com/EverMind-AI/EverOS - local-first, Markdown-native memory runtime that separates user and agent memory, keeps SQLite/LanceDB indexes rebuildable from files, and targets portability across Claude Code, Codex, OpenClaw, Hermes, and other agent surfaces.
- **Neurite** - https://github.com/satellitecomponent/Neurite - local visual graph workspace for notes, links, files, AI nodes, conversation history, Zettelkasten-style archives, and graph-based personal context.
- **Supermemory** - https://github.com/supermemoryai/supermemory - fast memory engine and API for search and recall across user context.
- **Screenpipe** - https://github.com/screenpipe/screenpipe - local desktop context capture for screen/audio memory, search, MCP access, and activity-triggered agents.
- **MIRIX** - https://github.com/Mirix-AI/MIRIX - Apache-2.0 personal memory system that turns screen activity and conversation into six typed local memory stores, with explicit consolidation and published multimodal/long-conversation evaluations.

### Memory evaluation and operations

Operational concerns matter as much as raw retrieval quality.

### AMA-Bench
- **Link:** https://github.com/AMA-Bench/AMA-Bench
- **Why it stands out:** evaluates recall, causal inference, state updating, and abstraction over long real-world agent trajectories rather than treating memory as dialogue lookup.
- **Best for:** comparing memory systems on evidence accumulated through software engineering, web, tool-use, embodied, game, and text-to-SQL workflows.
- **Evidence:** ICML 2026 benchmark with an MIT-licensed harness, public dataset and leaderboard, six task domains, and judge-consistency analysis. Last checked: 2026-08-10.

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

### LifeOS / Personal AI Infrastructure
- **Link:** https://github.com/danielmiessler/LifeOS
- **Why it stands out:** fast-moving Claude Code-native life operating system with Pulse dashboard, digital-assistant identity, current-to-ideal-state workflow primitives, structured skills, hooks, and plain-text personal context.
- **Best for:** builders designing a full personal AI infrastructure layer around goals, memory, skills, and day-to-day execution.

### OpenClaw
- **Link:** https://github.com/openclaw/openclaw
- **Why it stands out:** open-source assistant product with multi-channel, tool, and operator-style workflow orientation.
- **Best for:** self-hosted or productized personal/team assistant systems.

### PocketPaw
- **Link:** https://github.com/pocketpaw/pocketpaw
- **Why it stands out:** self-hosted personal AI with desktop installer, web dashboard, many chat channels, pluggable agent backends, memory, tools, and explicit security controls.
- **Best for:** builders comparing installable PersonalOS agents that need local control plus Telegram/Discord/Slack/WhatsApp-style operating surfaces.

### Hermes Agent
- **Link:** https://github.com/NousResearch/hermes-agent
- **Why it stands out:** self-improving agent platform with persistent memory, autonomous skill creation, cross-session search, messaging gateways, cron automations, and portable execution backends.
- **Best for:** builders comparing PersonalOS systems where learning loops, channels, scheduled work, and long-lived user context are core product primitives.

### Hermes Life OS
- **Link:** https://github.com/Lethe044/hermes-life-os
- **Why it stands out:** MIT-licensed quantified-self PersonalOS built on Hermes patterns, with local life tracking, scheduled briefings, correlation analysis, pluggable notifications, multi-provider models, and a tested Atropos training environment.
- **Best for:** builders studying proactive personal agents that turn longitudinal mood, sleep, habit, and focus data into recurring pattern-aware guidance.
- **Evidence:** v1.6.0 adds Ollama, OpenAI, Anthropic, and OpenRouter support; the project reports 129 tests across its modular runtime. Last checked: 2026-07-20.

### Nanobot
- **Link:** https://github.com/HKUDS/nanobot
- **Why it stands out:** unusually lightweight personal-agent stack with active releases, chat-channel gateways, WebUI, MCP/CLI-app extensions, project workspaces, local-model options, and a small core that is easier to audit than full assistant platforms.
- **Best for:** builders who want an owned personal AI agent for tools, chats, and workflows without starting from a large OpenClaw-style system.

### OpenHuman
- **Link:** https://github.com/tinyhumansai/openhuman
- **Why it stands out:** open-source desktop PersonalOS with local-first Memory Tree, Obsidian-style vault, scheduled connector sync, broad integrations, voice/video surfaces, and active beta releases.
- **Best for:** builders comparing full personal AI assistants that combine readable memory, everyday tool context, and proactive automation.

### CORE
- **Link:** https://github.com/RedPlanetHQ/core
- **Why it stands out:** self-hosted Personal AI OS that watches connected apps and agent sessions, uses a memory knowledge graph plus skills, and can act through email, Linear, GitHub, Slack, terminal, browser, Claude Code, and Codex.
- **Best for:** builders studying ambient PersonalOS designs where the agent notices events, applies memory and policies, then either acts or asks for judgment.

### CoWork OS
- **Link:** https://github.com/CoWork-OS/CoWork-OS
- **Why it stands out:** local-first desktop and CLI PersonalOS that puts coding, email, browser work, documents, spreadsheets, presentations, automations, memory, agents, approvals, and sandbox policy in one inspectable workspace.
- **Best for:** builders comparing broad personal work operating layers where agents produce and revise everyday artifacts, not just chat or execute code.
- **Evidence:** MIT-licensed, 400+ GitHub stars, 3,200+ automated tests reported by the project, and active v0.5 releases through July 2026. Last checked: 2026-08-08.

### Aivy OS
- **Link:** https://github.com/Bo1202/Aivy-OS
- **Why it stands out:** local AI companion OS with persistent memory, IDE workspace, browser automation, MCP, multichannel surfaces, proactive wakeups, and active Windows releases; note its commercial/activation-key posture.
- **Best for:** builders comparing companion-first PersonalOS products where personality, continuity, local tools, and desktop operation are the core product rather than an add-on.

### Osaurus
- **Link:** https://github.com/osaurus-ai/osaurus
- **Why it stands out:** native Swift PersonalOS harness for Apple Silicon that combines local/cloud models, layered memory, agents, MCP, scheduling, browser use, and per-agent Linux VM sandboxes without an Electron or hosted control plane.
- **Best for:** Mac users who want an owned, offline-capable personal agent runtime rather than a cross-platform web shell.
- **Evidence:** MIT-licensed, 7.7k+ GitHub stars, and active v0.23 releases through August 2026; the Linux VM sandbox requires macOS 26, with Seatbelt confinement on earlier supported releases. Last checked: 2026-08-21.

### OpenJarvis
- **Link:** https://github.com/open-jarvis/OpenJarvis
- **Why it stands out:** Stanford-backed local-first personal AI framework that treats on-device agents, energy/latency/cost-aware evals, and local trace learning as first-class primitives.
- **Best for:** builders who want personal AI to run on the user's device by default, with cloud calls as an exception rather than the architecture.

### Personal OS
- **Link:** https://github.com/pandego/personal-os
- **Why it stands out:** starter workspace for shaping a personal AI operating system around real life, work, priorities, memories, writing voice, and assistant workflows.
- **Best for:** builders designing a plain-file PersonalOS that behaves like an assistant home folder instead of another app silo.

### Aman Khan's Personal OS
- **Link:** https://github.com/amanaiproduct/personal-os
- **Why it stands out:** local AI-agent task-management framework built around plain-file backlog capture, goal-driven prioritization, knowledge base, session evals, and an optional MCP server.
- **Best for:** builders studying practical local-first PersonalOS workflows around tasks, priorities, and everyday execution.

### Claude Context OS
- **Link:** https://github.com/conorbronsdon/claude-context-os
- **Why it stands out:** file-based Claude context workspace with versioned identity/project/state files, `/start`→`/end` session loops, auto-memory, and curator passes for stale or contradictory context.
- **Best for:** builders who want a lightweight personal context operating layer across Claude Code and Claude projects without adopting a full assistant platform.

### Dex
- **Link:** https://github.com/davekilleen/Dex
- **Why it stands out:** role-configured Claude/Cursor PersonalOS starter kit with daily planning, meeting intelligence, relationship tracking, task sync, career evidence, and self-updating workflows.
- **Best for:** non-engineers and teams who want a practical AI chief-of-staff vault rather than a framework; note its noncommercial license.

### Row-Bot
- **Link:** https://github.com/siddsachar/row-bot
- **Why it stands out:** successor to Thoth with active releases, local-first desktop operation, personal knowledge graph, Goal Mode, child-agent delegation, Developer/Designer Studios, channels, workflows, MCP/plugins, and explicit safety controls.
- **Best for:** builders comparing sovereign personal assistants that combine memory, automation, developer workflows, everyday operating surfaces, and local-first data boundaries.

### Aiden
- **Link:** https://github.com/taracodlabs/aiden
- **Why it stands out:** local-first autonomous engine with browser, shell, file, workflow, channel, trigger, recovery, and persistent-memory primitives in one installable runtime.
- **Best for:** builders studying desktop-native PersonalOS agents that can operate files, tools, and scheduled/local events without becoming a hosted assistant product.

### LLMbasedOS
- **Link:** https://github.com/iluxu/llmbasedos
- **Why it stands out:** local-first runtime for tool-using agents with Docker boundaries, explicit mounted-folder scope, MCP-style narrow tools, local-model defaults, and no ambient monitoring.
- **Best for:** privacy-sensitive builders who want an observable personal-agent runtime before giving assistants broad host, email, shell, or screen access.

### OpenFang
- **Link:** https://github.com/RightNow-AI/openfang
- **Why it stands out:** single-binary Rust Agent OS with scheduled autonomous "Hands," dashboard-driven operations, knowledge-graph workflows, active releases, and enough adoption to compare beside OpenClaw rather than treat as a fringe experiment.
- **Best for:** builders exploring OS-like abstractions for always-on agents, with a pre-1.0 caveat for production use.

### IronClaw
- **Link:** https://github.com/nearai/ironclaw
- **Why it stands out:** privacy- and security-first Agent OS with local encrypted data, WASM tool sandboxing, credential boundaries, prompt-injection defenses, MCP support, routines, and active signed releases.
- **Best for:** builders comparing always-on PersonalOS runtimes where tool extensibility, local control, and defense-in-depth matter as much as assistant UX.

### VisionClaw
- **Link:** https://github.com/Intent-Lab/VisionClaw
- **Why it stands out:** open-source smart-glasses agent that connects Gemini Live perception to OpenClaw execution, with user-study evidence for faster situated tasks and lower perceived difficulty.
- **Best for:** builders watching PersonalOS move from desktop context stores toward wearable, always-on perception plus action loops.

### AIOS
- **Link:** https://github.com/agiresearch/AIOS
- **Why it stands out:** research-backed AI Agent Operating System that treats scheduling, context switching, memory, storage, tools, and agent SDKs as OS-level services.
- **Best for:** teams exploring kernel-style infrastructure for deploying and managing LLM agents.

### OpenDAN
- **Link:** https://github.com/fiatrete/OpenDAN-Personal-AI-OS
- **Why it stands out:** early but substantial Personal AI OS with Docker-based local deployment, personal knowledge base, agent/workflow concepts, Telegram/email access, and an explicit AIOS shell/kernel roadmap.
- **Best for:** builders comparing full-stack personal AI OS designs, especially where local data control and modular personal agents matter.

### QwenPaw
- **Link:** https://github.com/agentscope-ai/QwenPaw
- **Why it stands out:** self-hostable personal AI assistant with local/cloud deployment, memory, proactive scheduling, multi-channel chat, MCP, skills, and explicit tool/file security controls.
- **Best for:** builders comparing practical PersonalOS products that combine channels, personal memory, cron-like automations, and local control.

### Khoj
- **Link:** https://github.com/khoj-ai/khoj
- **Why it stands out:** mature self-hostable personal AI app that combines document/web answers, custom agents, scheduled automations, multi-surface access, and local or cloud LLM support.
- **Best for:** builders who want a practical personal second-brain / PersonalOS layer rather than just a memory API.

### PyGPT
- **Link:** https://github.com/szczyglis-dev/py-gpt
- **Why it stands out:** cross-platform desktop AI assistant with agents, computer use, tools, MCP, plugins, voice, RAG, memory, web search, and local/Ollama model support in one open-source app.
- **Best for:** builders comparing desktop-native PersonalOS surfaces where chat, automation, files, local models, and everyday tooling share one UI.

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

Agents need to browse, click, extract, fill forms, and operate websites and desktops. This category covers computer-use agents, browser automation, hosted browser infra, and web extraction.

### Agent S
- **Link:** https://github.com/simular-ai/Agent-S
- **Why it stands out:** open-source computer-use framework with research lineage and strong OSWorld results, including reported human-level desktop-agent performance.
- **Best for:** builders comparing agents that operate full computer environments, not just web pages.

### Agent Desktop
- **Link:** https://github.com/lahfir/agent-desktop
- **Why it stands out:** native Rust CLI that exposes desktop apps through accessibility trees, compact snapshots, deterministic element refs, structured JSON, and traceable actions instead of relying only on screenshots and pixel coordinates.
- **Best for:** builders giving coding or operator agents inspectable control of local desktop applications, especially on macOS; Linux and Windows support remain earlier.
- **Evidence:** Apache-2.0, 980+ GitHub stars, and active v0.6 releases with prebuilt binaries and FFI libraries through July 2026. Last checked: 2026-07-30.

### Browser Use
- **Link:** https://github.com/browser-use/browser-use
- **Why it stands out:** popular open-source browser automation layer for AI agents.
- **Best for:** giving agents practical website interaction ability.

### Agent Browser
- **Link:** https://github.com/vercel-labs/agent-browser
- **Why it stands out:** fast Rust CLI that exposes browser snapshots, stable element refs, CDP control, session state, traces, screenshots, and action policies directly to coding agents without requiring a framework.
- **Best for:** Claude Code, Codex, Cursor, and other terminal agents that need a scriptable local browser or one command surface across local and hosted browser providers.

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

### MCP Registry
- **Link:** https://modelcontextprotocol.io/registry/about
- **Why it stands out:** official centralized metadata repository for public MCP servers, with namespace verification, standardized install metadata, and a REST API for downstream marketplaces and clients.
- **Best for:** teams that need MCP tool discovery to move beyond ad hoc GitHub lists without pretending registry metadata is a full security review.

### MCP Servers
- **Link:** https://github.com/modelcontextprotocol/servers
- **Why it stands out:** central collection of MCP servers and examples.
- **Best for:** discovering and wiring tools into MCP-capable agents.

### FastMCP
- **Link:** https://github.com/PrefectHQ/fastmcp
- **Why it stands out:** Pythonic way to build MCP servers, clients, and apps, with strong adoption and production-oriented protocol lifecycle handling.
- **Best for:** Python teams building custom tools for agents.

### mcp-agent
- **Link:** https://github.com/lastmile-ai/mcp-agent
- **Why it stands out:** MCP-native agent framework that pairs server lifecycle management with composable Anthropic-style agent patterns and optional Temporal durability.
- **Best for:** teams that want MCP to be the core runtime for agent workflows, not just a connector bolted onto another framework.

### ContextForge
- **Link:** https://github.com/IBM/mcp-context-forge
- **Why it stands out:** Apache-2.0 gateway that federates MCP, A2A, REST, and gRPC behind one endpoint with centralized discovery, auth, guardrails, plugins, and OpenTelemetry observability.
- **Best for:** platform teams that need a governed tool-and-agent gateway across mixed protocols rather than a local MCP server launcher.
- **Evidence:** 4.1k+ GitHub stars and active v1.0 releases, including OAuth token exchange, vault credentials, dataplane publishing, and security hardening in v1.0.6. Last checked: 2026-07-22.

### Agentgateway
- **Link:** https://github.com/agentgateway/agentgateway
- **Why it stands out:** Linux Foundation, Apache-2.0 proxy that governs agent-to-model, agent-to-tool, and agent-to-agent traffic across LLM, MCP, and A2A protocols, with routing, auth, policy, guardrails, and OpenTelemetry in one data plane.
- **Best for:** platform teams that want one Kubernetes-friendly gateway for model access, MCP tools, and A2A communication instead of separate protocol proxies.
- **Evidence:** 4.1k+ GitHub stars and active v1.4 releases through July 2026. Last checked: 2026-08-01.

### ToolHive
- **Link:** https://github.com/stacklok/toolhive
- **Why it stands out:** Apache-2.0 MCP platform that combines an isolated server runtime, gateway, registry, access policies, audit logs, OpenTelemetry, and a Kubernetes operator instead of leaving production governance as custom glue.
- **Best for:** platform teams that need to run approved MCP servers across developer machines and Kubernetes with centralized security and observability.

### Backlog.md
- **Link:** https://github.com/MrLesk/Backlog.md
- **Why it stands out:** local Markdown task board and MCP/CLI workflow that gives coding agents explicit tasks, acceptance criteria, decisions, and review checkpoints inside the repo.
- **Best for:** teams using Claude Code, Codex, Gemini CLI, Kiro, or Cursor who want agent work to stay spec-driven, reviewable, and offline-friendly.

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

### Daytona
- **Link:** https://github.com/daytonaio/daytona
- **Why it stands out:** open-source, agent-focused sandbox runtime with fast stateful environments, SDKs, CLI/API control, filesystem/process operations, snapshots, and self-hosted or managed deployment paths.
- **Best for:** coding agents and eval workloads that need isolated full-computer sandboxes with persistent state and operational controls.

### Fly.io Sprites
- **Link:** https://fly.io/sprites/
- **Why it stands out:** hardware-isolated Linux computers for agents with durable disks, idle suspend, checkpoint/restore, SDKs, and MCP support instead of disposable execution alone.
- **Best for:** long-running coding and operator agents that need to keep installed tools, files, and working state across sessions.
- **Evidence:** Fly.io reports 8,000+ agent-native customers and made Sprites its core agent-infrastructure focus in July 2026; official Python, JavaScript, Go, Elixir, MCP, and coding-agent integrations are actively maintained. Last checked: 2026-08-05.

### OpenSandbox
- **Link:** https://github.com/opensandbox-group/OpenSandbox
- **Why it stands out:** Apache-2.0 agent sandbox platform with a unified API across Docker and Kubernetes, five language SDKs, network policy, credential injection, MCP, and stronger isolation paths through gVisor, Kata Containers, and Firecracker.
- **Best for:** platform teams that want a self-hosted execution layer spanning coding agents, browser/desktop agents, evals, and large-scale sandbox scheduling.

### Kubernetes Agent Sandbox
- **Link:** https://github.com/kubernetes-sigs/agent-sandbox
- **Why it stands out:** Kubernetes SIG Apps project that standardizes long-running, stateful agent environments as a `Sandbox` CRD, with stable identity, persistent storage, warm pools, lifecycle controls, and pluggable isolation providers.
- **Best for:** platform teams that want to operate agent sandboxes through Kubernetes primitives instead of adopting a separate hosted runtime.
- **Evidence:** Apache-2.0, 3.2k+ GitHub stars, and active v0.5 releases through July 2026; it remains pre-1.0. Last checked: 2026-07-26.

### Microsoft Execution Containers
- **Link:** https://github.com/microsoft/mxc
- **Why it stands out:** policy-driven execution layer that maps one JSON schema and TypeScript SDK onto native process sandboxes, containers, and experimental VM backends across Windows, Linux, and macOS.
- **Best for:** agent builders who want filesystem, network, UI, and lifecycle controls without hard-coding one isolation primitive.
- **Evidence:** Microsoft-backed MIT preview with 1.2k+ GitHub stars, active development, and announced adoption paths for Copilot CLI, OpenClaw, OpenShell, Hermes Agent, Codex, and Manus; its maintainers explicitly warn that current profiles are not yet security boundaries. Last checked: 2026-08-16.

### Microsandbox
- **Link:** https://github.com/superradcompany/microsandbox
- **Why it stands out:** local-first, rootless microVM runtime that embeds hardware-isolated OCI sandboxes directly in Rust, Python, TypeScript, or Go applications, with MCP and coding-agent skill integrations.
- **Best for:** builders who want agent code execution on their own Linux or Apple Silicon machine without operating a sandbox service; it is still beta software.

### AgentScope Runtime
- **Link:** https://github.com/agentscope-ai/agentscope-runtime
- **Why it stands out:** production-oriented runtime framework for agent apps with secure tool sandboxing, Agent-as-a-Service APIs, scalable deployment, full-stack observability, and browser-computer-use support.
- **Best for:** teams that need more than raw sandbox execution: deployment, tool isolation, observability, and service-style agent operations in one runtime layer.

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

### Holistic Agent Leaderboard (HAL)
- **Link:** https://hal.cs.princeton.edu/
- **Why it stands out:** Princeton's third-party leaderboard compares agent systems across nine benchmark families with cost tracking, reproducible runs, full traces, and reliability views instead of flattening evaluation into one accuracy score.
- **Best for:** builders comparing models and scaffolds across coding, web, science, and customer-service tasks while keeping cost and behavioral reliability visible.
- **Evidence:** the ICLR 2026 study reports 21,730 agent rollouts across nine models and nine benchmarks; the live leaderboard now exposes 26k+ rollouts. Last checked: 2026-08-03.

### Artificial Analysis Coding Agent Index
- **Link:** https://artificialanalysis.ai/agents/coding-agents
- **Why it stands out:** independent composite that compares coding-agent variants across long-horizon repository changes, terminal work, and codebase Q&A while exposing harness effects, token use, API cost, and wall time alongside pass rates.
- **Best for:** builders choosing an agent-model-harness combination on real execution efficiency rather than reading model scores as product scores.
- **Evidence:** v1.1 runs 321 public tasks from DeepSWE, Terminal-Bench v2, and SWE-Atlas-QnA three times per variant, with a published scoring and efficiency methodology. Last checked: 2026-08-09.

### Terminal-Bench
- **Link:** https://www.tbench.ai/
- **Why it stands out:** benchmark for terminal-agent performance on realistic terminal tasks.
- **Best for:** comparing terminal-native coding and operator agents.

### Long-Horizon Terminal-Bench
- **Link:** https://github.com/zli12321/LHTB
- **Why it stands out:** extends terminal evaluation to 46 containerized tasks requiring hundreds of dependent actions, with deterministic hidden verifiers and dense partial credit that exposes progress before timeout instead of collapsing hard runs into binary failures.
- **Best for:** comparing whether agents can preserve state, recover, self-verify, and finish sustained engineering, scientific, multimodal, and professional workflows.
- **Evidence:** Apache-2.0 benchmark with a reproducible modified Harbor harness; its July 2026 sweep evaluated 21 frontier models under one 90-minute-per-task setup, and 29 of 46 tasks remained unsolved. Last checked: 2026-08-22.

### SWE-bench
- **Link:** https://www.swebench.com/
- **Why it stands out:** benchmark for resolving real software engineering issues from GitHub repositories.
- **Best for:** evaluating autonomous coding agents and issue-resolution systems.

### ProgramBench
- **Link:** https://github.com/facebookresearch/ProgramBench
- **Why it stands out:** tests whether an agent can reconstruct an entire working program from only its executable and documentation, exposing software-design and specification-discovery failures that issue-resolution benchmarks miss.
- **Best for:** evaluating coding agents that claim to architect and build complete software rather than patch an existing repository.
- **Evidence:** Meta FAIR-led MIT benchmark with 200 programs, behavior-based hidden tests, a reproducible mini-SWE-agent baseline, and active v1.2 releases; its initial nine-model study fully solved no task. Last checked: 2026-08-19.

### mini-SWE-agent
- **Link:** https://github.com/SWE-agent/mini-swe-agent
- **Why it stands out:** Princeton and Stanford's radically small bash-only coding agent pairs an inspectable linear loop with a reported 74%+ SWE-bench Verified score and active v2 releases.
- **Best for:** reproducible coding-agent baselines, model comparisons, fine-tuning, and builders who want to understand the whole scaffold before extending it.

### OSWorld
- **Link:** https://os-world.github.io/
- **Why it stands out:** benchmark and executable environment for multimodal agents doing open-ended desktop and web tasks across real applications.
- **Best for:** evaluating computer-use agents beyond browser-only or coding-only tasks.

### Windows Agent Arena
- **Link:** https://github.com/microsoft/WindowsAgentArena
- **Why it stands out:** Microsoft-backed Windows benchmark with 150+ real OS tasks and parallelized evaluation for multimodal desktop agents.
- **Best for:** teams evaluating whether computer-use agents can reliably operate Windows applications, not just browsers or Linux sandboxes.

### WebArena-Verified
- **Link:** https://github.com/ServiceNow/webarena-verified
- **Why it stands out:** audited, version-controlled 812-task WebArena release with deterministic scoring, offline network-trace replay, reproducible site containers, and a 258-task hard subset.
- **Best for:** comparing browser agents on realistic multi-site workflows without relying on brittle live-web targets or LLM-as-a-judge scoring.

### BrowserGym
- **Link:** https://github.com/ServiceNow/BrowserGym
- **Why it stands out:** open benchmark harness for web agents that unifies MiniWoB, WebArena, WebArena Verified, VisualWebArena, WorkArena, AssistantBench, WebLINX, OpenApps, and TimeWarp-style tasks.
- **Best for:** teams evaluating browser agents across multiple web task suites without wiring every benchmark from scratch.

### WebBench
- **Link:** https://github.com/Halluminate/WebBench
- **Why it stands out:** tests browser agents on 2,454 open tasks across 452 live websites, separating read work from state-changing create, update, delete, and file workflows while exposing infrastructure failures.
- **Best for:** teams checking whether browser agents survive authentication, forms, downloads, pop-ups, and anti-bot friction that static or read-heavy benchmarks miss.
- **Evidence:** MIT-licensed dataset from Halluminate and Skyvern; the broader study covers 5,750 human-validated tasks and publishes task-level results. Last checked: 2026-08-13.

### τ-bench
- **Link:** https://taubench.com/
- **Why it stands out:** benchmark family for tool-agent-user interaction in realistic enterprise workflows, now extending into knowledge and full-duplex voice modes.
- **Best for:** evaluating conversational agents that must follow policy, use tools, and coordinate with users across multi-turn tasks.

### MCPMark Verified
- **Link:** https://github.com/eval-sys/mcpmark
- **Why it stands out:** stress-tests agents against real MCP environments for Notion, GitHub, files, Postgres, and Playwright, with version-pinned dependencies, stabilized verifiers, isolated sandboxes, and reproducible reports.
- **Best for:** comparing model-and-harness reliability on long-horizon tool work instead of synthetic function-calling alone.
- **Evidence:** the ICLR 2026 benchmark covers 127 tasks across five MCP environments; its Verified release supersedes earlier, non-comparable task versions. Last checked: 2026-08-15.

### τ-voice
- **Link:** https://arxiv.org/abs/2603.13686
- **Why it stands out:** open, reproducible extension of τ-bench that scores 278 grounded customer-service tasks under simultaneous speech, interruptions, accents, noise, telephony degradation, and deterministic database outcomes.
- **Best for:** testing whether realtime voice agents still complete the underlying task when clean text assumptions disappear.

### Artificial Analysis Speech to Speech Index
- **Link:** https://artificialanalysis.ai/speech-to-speech
- **Why it stands out:** independent live leaderboard that refuses to reduce native audio models to voice quality, combining speech reasoning, full-duplex turn behavior, and grounded τ-voice task completion while exposing latency and hourly input/output cost.
- **Best for:** choosing a realtime speech-to-speech model or provider on agentic reliability and operating trade-offs rather than demos.
- **Evidence:** the index equally weights Big Bench Audio, Full Duplex Bench, and τ-voice; models need valid results on all three to rank. Last checked: 2026-08-12.

### TRAIL
- **Link:** https://github.com/patronus-ai/trail-benchmark
- **Why it stands out:** open benchmark for trace reasoning and agentic issue localization, with 148 human-annotated long-context traces and 841 reasoning, planning, and execution errors.
- **Best for:** teams debugging complex agent workflows where final-answer grading hides the broken step.

### π-Bench
- **Link:** https://github.com/Simplified-Reasoning/Pi-Bench
- **Why it stands out:** evaluates proactive personal assistants on 100 multi-turn tasks across five personas, with hidden intents, inter-task dependencies, persistent workspaces, and separate proactivity and completeness scores.
- **Best for:** testing whether a PersonalOS can anticipate unstated needs and finish useful work across sessions instead of only recalling context.

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

### Inspect AI
- **Link:** https://github.com/UKGovernmentBEIS/inspect_ai
- **Why it stands out:** UK AI Security Institute framework for reproducible model and agent evaluations, with built-in tooling for agents, custom/MCP tools, sandboxes, and external coding agents.
- **Best for:** teams building serious eval suites for coding, tool-use, cyber, and long-running agent tasks.

### DeepEval
- **Link:** https://github.com/confident-ai/deepeval
- **Why it stands out:** test-style LLM evaluation framework.
- **Best for:** teams that want CI-like evals for LLM apps and agents.

### Promptfoo
- **Link:** https://github.com/promptfoo/promptfoo
- **Why it stands out:** CLI-first eval and red-team harness for prompts, agents, and RAG, with strong CI/CD ergonomics and active open-source releases.
- **Best for:** teams that want declarative regression tests plus security scans before shipping agent changes.

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

### ASPI
- **Link:** https://github.com/scaleapi/aspi
- **Why it stands out:** prompt-injection benchmark that isolates a neglected failure mode: agents becoming vulnerable when their own clarification questions open a trusted-looking channel for malicious follow-up instructions.
- **Best for:** teams testing agents that ask users for missing information before acting, including whether defenses preserve task utility across user- and tool-delivered attacks.
- **Evidence:** 728 task-attack scenarios across workspace, Slack, travel, and banking, an eight-condition matched design, public code and data, and evaluations across ten models. Last checked: 2026-08-07.

### DecodingTrust-Agent
- **Link:** https://github.com/AI-secure/DecodingTrust-Agent
- **Why it stands out:** controllable red-teaming platform with 14 domains, 50+ simulation environments, autonomous attack discovery, and verifiable judges for agent outcomes.
- **Best for:** security teams stress-testing agents against prompt, tool, skill, and environment-level injection paths.

### MCP Security Bench
- **Link:** https://github.com/dongsenzhang/MSB
- **Why it stands out:** ICLR 2026 benchmark for MCP-specific attacks across planning, tool invocation, and response handling, with 2,000+ attack instances across 12 categories.
- **Best for:** teams hardening MCP agents against malicious tool descriptions, parameter abuse, poisoned responses, and retrieval injection.

### AgentDoG
- **Link:** https://github.com/AI45Lab/AgentDoG
- **Why it stands out:** open trajectory-level safety guardrail with lightweight models, fine-grained risk diagnosis, an online intervention path, and ATBench variants for general tool agents, OpenClaw, and Codex-style execution.
- **Best for:** teams that need to inspect and block risky multi-step agent behavior rather than only scan prompts or final responses.

### Snyk Agent Scan
- **Link:** https://github.com/snyk/agent-scan
- **Why it stands out:** security scanner for installed agent components, MCP servers, and skills, with concrete checks for prompt injection, tool poisoning, toxic flows, hidden content, and risky local capabilities.
- **Best for:** teams auditing the agent supply chain on developer machines before trusting MCP configs, IDE agents, or shared skills.

### Agent Governance Toolkit
- **Link:** https://github.com/microsoft/agent-governance-toolkit
- **Why it stands out:** Microsoft-backed, framework-neutral control plane that intercepts agent actions for deterministic policy enforcement, identity, tamper-evident audit, approvals, sandboxing, kill switches, and SRE controls instead of relying on prompt-level guardrails.
- **Best for:** teams moving autonomous tool-using agents into production and needing enforceable governance across frameworks, languages, MCP, and multi-agent delegation.
- **Evidence:** MIT-licensed public preview with 5.5k+ GitHub stars, five language SDKs, formal specifications, and active v4 releases in 2026. Last checked: 2026-08-02.

### PyRIT
- **Link:** https://github.com/microsoft/PyRIT
- **Why it stands out:** Microsoft-backed open-source framework for proactive generative-AI risk identification and red-team automation.
- **Best for:** security teams building repeatable adversarial tests for LLM apps and agentic systems.

### DeepTeam
- **Link:** https://github.com/confident-ai/deepteam
- **Why it stands out:** open-source red-teaming framework built on DeepEval with local attack simulation, 50+ vulnerability checks, and agent-specific risks such as goal theft, indirect instructions, tool orchestration abuse, and autonomous drift.
- **Best for:** teams that want CI-friendly penetration testing for LLM apps, RAG systems, and tool-calling agents before production rollout.

### garak
- **Link:** https://github.com/NVIDIA/garak
- **Why it stands out:** mature LLM vulnerability scanner with active releases and a broad probe/plugin posture.
- **Best for:** teams that want a fast baseline scan before deeper agent-specific red teaming.

### Observability and tracing

### MLflow
- **Link:** https://github.com/mlflow/mlflow
- **Why it stands out:** Apache-2.0 AI engineering platform that now connects the traditional model lifecycle with agent tracing, evaluation, monitoring, prompt management, optimization, and model-access governance.
- **Best for:** teams that want one self-hostable control plane across production agents, LLM applications, and existing ML workflows.
- **Evidence:** 27k+ GitHub stars, active v3 releases through June 2026, and first-party agent tracing and scorer-based evaluation docs. Last checked: 2026-07-28.

### Langfuse
- **Link:** https://github.com/langfuse/langfuse
- **Why it stands out:** open-source LLM engineering platform for observability, metrics, evals, prompt management, datasets, and traces.
- **Best for:** production LLM/agent teams that need traceability and evaluation loops.

### Phoenix
- **Link:** https://github.com/Arize-ai/phoenix
- **Why it stands out:** AI observability and evaluation platform with strong tracing and analysis posture.
- **Best for:** debugging and evaluating complex LLM and RAG systems.

### Opik
- **Link:** https://github.com/comet-ml/opik
- **Why it stands out:** open-source observability and eval platform for LLM apps, RAG, and agentic workflows, with tracing, automated evals, production dashboards, and broad agent-framework integrations.
- **Best for:** teams that want a self-hostable trace-plus-eval loop for production agents without locking into one orchestration stack.

### Laminar
- **Link:** https://github.com/lmnr-ai/lmnr
- **Why it stands out:** open-source, OpenTelemetry-native observability built specifically for AI agents, with traces, evals, natural-language failure signals, SQL access, and self-hosting.
- **Best for:** teams that need to debug agent runs, turn failures into eval datasets, and keep telemetry portable.

### LangSmith
- **Link:** https://www.langchain.com/langsmith
- **Why it stands out:** tracing, evaluation, and observability platform integrated with the LangChain/LangGraph ecosystem.
- **Best for:** teams building on LangGraph or LangChain who want native observability.

### OpenInference
- **Link:** https://github.com/Arize-ai/openinference
- **Why it stands out:** backend-neutral OpenTelemetry conventions and instrumentors for LLM, RAG, agent, tool, and MCP traces across Python, TypeScript, Java, and Go, with adapters for major agent frameworks and existing OpenLLMetry/OpenLIT telemetry.
- **Best for:** teams that want one portable instrumentation layer across agent stacks and OTLP-compatible backends rather than binding telemetry capture to one observability product.
- **Evidence:** Apache-2.0, active August 2026 releases, and an OpenTelemetry-accepted code grant covering its SDK/framework instrumentation; the grant records multimillion-download monthly adoption for core Python packages. Last checked: 2026-08-23.

### OpenLLMetry
- **Link:** https://github.com/traceloop/openllmetry
- **Why it stands out:** Python-first auto-instrumentation for LLM, vector-database, framework, and MCP calls, with a one-line SDK path and broad support for existing OpenTelemetry collectors.
- **Best for:** Python teams that want fast agent tracing into Datadog, Honeycomb, Grafana, or another existing backend rather than a new observability platform.

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
