# Java LLM Toolbelt

A modular Java-first AI toolkit for experimenting with LLM-based tools and agents.  
Built with Maven, LangChain4j, and pure JVM technologies.

Inspired by the book [*Ollama in Action: Building Safe, Private AI with LLMs, Function Calling and Agents*](https://leanpub.com/ollama) by Mark Watson

Goal: Build a flexible, production-ready foundation to develop AI assistants and agents in Java, comparable to Python’s LangChain / OpenAI tool ecosystems, but JVM-first.

---

## Vision

My long-term goals are to:
- Understand how to architect LLM-powered systems.
- Create reusable tools that perform real tasks (file reading, web fetching, summarization, etc.).
- Compose them into autonomous agents (research bots, document Q&A, Jira assistant, etc.).
- Benchmark and compare Java ML frameworks: DJL, ONNX Runtime, and DL4J.

---

## Project Structure

```
java-llm-toolbelt/
├── tool-spi/ → Tool interface, registry, DTOs
├── tools/ → Aggregator of concrete tool modules
│ ├── tool-dir/ → List files in a directory
│ ├── tool-fileio/ → Read/write text files
│ └── tool-webfetch/ → Fetch and clean web pages
└── examples/
  └── research-agent/ → Runnable demo app and dispatcher
```


---

## Tools Overview (Planned)

| Tool | Description | Status |
|------|--------------|--------|
| Directory Tool | Lists files and subdirectories. | Done |
| File I/O Tool | Reads text files safely. | Done |
| Web Fetch Tool | Fetches a URL and extracts readable text. | Done |
| Summarizer Tool | Summarizes text (DJL / ONNX / Azure). | Planned |
| SQLite NLQ Tool | Executes LLM-generated SQL safely. | Planned |
| Memory Store Tool | Embedding-based vector search (Qdrant / Milvus). | Planned |
| Graph Tool | Neo4j integration for knowledge graphs. | Planned |
| Judge Tool | Evaluates LLM outputs for quality and hallucination. | Planned |

---

## Prerequisites
- Java 21 or later
- Maven 3.9 or later

# Roadmap / Progress Checklist

## Core Infrastructure
- [ ] Multi-module Maven project
- [ ] GitHub Actions CI
- [x] Codespaces Dev Container
- [ ] SPI (Tool interface + DTOs)
- [ ] Dispatcher for JSON-validated tool execution

## Core Tools
- [ ] tool-dir — Directory listing
- [ ] tool-fileio — File read/write
- [ ] tool-webfetch — Fetch and clean HTML
- [ ] tool-summarize — DJL + ONNX comparison
- [ ] tool-sqlite — Natural language to SQL
- [ ] tool-memory — Vector search / retrieval
- [ ] tool-judge — Output evaluation

## Integrations
- [ ] LangChain4j + OpenAI tool-calling demo
- [ ] Local Ollama / Azure integration
- [ ] Docker deployment example
- [ ] Monitoring (Micrometer + Prometheus)

## Stretch Goals
- [ ] Research Agent with autonomous workflow
- [ ] Local Notebook QA assistant

