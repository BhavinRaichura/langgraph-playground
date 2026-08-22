# LangGraph Playground

A hands-on repository for learning and experimenting with **LangGraph, LangChain, LLM workflows, memory, persistence, context management, tools, RAG, and Human-in-the-Loop (HITL) systems**.

## 📚 Topics

### 1. Graph Workflows

- [Sequential Graph — Basic](./1_sequencial_graph_basic.ipynb)
- [Sequential Graph with LLM](./2_sequencial_graph_with_llm.ipynb)
- [Parallel Graph Workflow](./3_parallel_graph_workflow.ipynb)
- [Conditional Graph](./4_conditional_graph.ipynb)
- [Looping Graph Workflow](./5_looping_graph_workflow.ipynb)
- [Subgraph](./11_subgraph.ipynb)
- [Dynamic Routing](./15_dynamic_routing.ipynb)

### 2. Memory & Persistence

- [Memory History Chatbot](./6_memory_history_chatbot.ipynb)
- [Persistent Memory](./7_persistant_memory.ipynb)
- [SQLite Storage](./8_sqlite_storage.ipynb)
- [Short-Term Memory (STM) Implementation](./16_STM_implementation.ipynb)

### 3. Context Memory Management

- [Context Memory Overflow Problem](./17_context_memory_overflow_problem.ipynb)
- [Solution 1 — Message Trimming](./18_context_overflow_sol_1_trim_messages.ipynb)
- [Solution 2 — Summarization](./19_context_coverflow_sol_2_summarization.ipynb)

### 4. Tools & Agents

- [Tool Calling](./10_tool_calling.ipynb)
- [Agentic RAG](./12_agentic_RAG.ipynb)

### 5. Human-in-the-Loop

- [HITL — Human in the Loop](./13_HTIL_human_in_the_loop.ipynb)
- [HITL — Parallel Multiple Interrupts](./14_HITL_parallel_multiple_interrupts.ipynb)

### 6. Observability

- [LangSmith Integration & Tracing](./9_trace_langsmith_integration.ipynb)

---

## 🧠 STM Architecture

The STM implementation uses **LangGraph + PostgreSQL** for persistent, thread-based state.

```text
User
 │
 ▼
LangGraph
 │
 ▼
Thread ID
 │
 ▼
PostgreSQL Checkpointer
 │
 ▼
Checkpoint / State