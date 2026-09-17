# Ajay S Vasan

<sub>software engineer · backend systems · AI systems · low-level engineering</sub>

I like understanding how things work underneath the abstractions — from data structures and memory management to retrieval systems, databases, and local AI infrastructure.

[GitHub](https://github.com/Ajaysvasan) · [LinkedIn](https://linkedin.com/in/ajay-s-vasan-584111291)

## Projects

### MMRAG — Multi-Model RAG for Searching

[`multi_model_rag_for_searching`](https://github.com/Ajaysvasan/multi_model_rag_for_searching)<br>
<sub>Python · C++ · FastAPI · PostgreSQL · FAISS · llama.cpp · Electron</sub>

Multimodal RAG that doesn't start from scratch on every query. MMRAG keeps a history of past queries and detects when a new one is semantically similar to an earlier query — even when it's phrased differently — so the retrieval work already done can be reused.

```
Electron client ──► FastAPI ──► query processing
                                        │
┌─ retrieval engine ────────────────────▼─────┐   ┌─ data plane ─────────────┐
│  1  topic cache              ┐              │   │  PostgreSQL              │
│  2  history reuse            ┘ cache layers │   │  FAISS HNSW index        │
│  3  FAISS ANN retrieval                     ├───┤  AdapterModule           │
│  4  cross-encoder reranking                 │   │  OCR / ASR / chunk data  │
│  5  relevance gate                          │   └──────────────────────────┘
└──────────────────────┬──────────────────────┘
                       ▼
┌─ generation ────────────────────────────────┐
│  LlamaGenerator · MmapGenerator             │
│  llama.cpp / C++ backend ──► local LLM      │
└─────────────────────────────────────────────┘
```

- **Layered caching** — a topic-level cache and query-history snapshots sit ahead of FAISS HNSW retrieval
- **Relevance gating** — cross-encoder reranking and a relevance gate filter what reaches generation
- **Multimodal data** — OCR and ASR processing, with PostgreSQL-backed data and state
- **Local inference** — llama.cpp and C++ backend components integrated with Python, lazy loading on performance-sensitive paths

<br>

### Project Atlas

[`atlas`](https://github.com/Ajaysvasan/atlas)

A project-aware local RAG system for research. Atlas keeps persistent memory per project, scopes conversational retrieval to that project's context, and handles retrieval orchestration and adaptive knowledge acquisition for structured research workflows.

<br>

<table>
<tbody>
<tr>
<td width="33%" valign="top">

### DSA in C++

[`DSA_in_cpp`](https://github.com/Ajaysvasan/DSA_in_cpp)

Data structures, algorithms, and competitive programming in C++ — the fundamentals underneath the larger projects.

<sub>graphs · trees · dynamic programming · DSU · recursion · STL · LeetCode</sub>

</td>
<td width="33%" valign="top">

### Neovim

[`nvim`](https://github.com/Ajaysvasan/nvim)

Personal Neovim configuration — the editor setup I use for day-to-day development.

</td>
<td width="33%" valign="top">

### Dotfiles

[`.dotfiles`](https://github.com/Ajaysvasan/.dotfiles)

Linux configuration for Kitty, tmux, and Fastfetch, plus custom utilities.

</td>
</tr>
</tbody>
</table>

## Stack

```
languages          C++ · Python · Java · TypeScript · JavaScript
backend & systems  FastAPI · Spring Boot · PostgreSQL · Redis · Linux · Docker
ai / ml            PyTorch · Transformers · RAG · LLMs · FAISS
tools              Git · Neovim · tmux · CMake
```

## Competitions

- Winner – ProjectFest (AI/ML)
- Winner – IEEE Software Competition (Sairam College)
- Participant – IBM Datathon (Global)
- Participant – AIML Challenge, IIT Madras

<br>

<sub>I prefer building fewer projects — and building them deeply and correctly.</sub>
