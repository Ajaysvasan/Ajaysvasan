<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Ajaysvasan/Ajaysvasan/main/assets/header-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Ajaysvasan/Ajaysvasan/main/assets/header-light.svg">
  <img alt="Ajay S Vasan — software engineer: backend systems, AI systems, low-level engineering" src="https://raw.githubusercontent.com/Ajaysvasan/Ajaysvasan/main/assets/header-light.svg" width="100%">
</picture>

I like understanding how things work underneath the abstractions — from data structures and memory management to retrieval systems, databases, and local AI infrastructure. I prefer building fewer projects, and building them deeply and correctly.

[GitHub](https://github.com/Ajaysvasan) &nbsp;·&nbsp; [LinkedIn](https://linkedin.com/in/ajay-s-vasan-584111291)

## Projects

### MMRAG — Multi-Model RAG for Searching

[`Ajaysvasan/multi_model_rag_for_searching`](https://github.com/Ajaysvasan/multi_model_rag_for_searching)

**Multimodal RAG that doesn't start from scratch on every query.** MMRAG keeps a history of past queries and detects when a new one is semantically similar to an earlier query — even when it's phrased differently — so retrieval work that was already done can be reused.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Ajaysvasan/Ajaysvasan/main/assets/mmrag-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Ajaysvasan/Ajaysvasan/main/assets/mmrag-light.svg">
  <img alt="MMRAG architecture: Electron client → FastAPI → query processing → retrieval engine (topic cache, history reuse, FAISS ANN retrieval, cross-encoder reranking, relevance gate) → generation (LlamaGenerator, MmapGenerator, llama.cpp / C++ backend, local LLM), with a data plane of PostgreSQL, FAISS HNSW index, AdapterModule and OCR / ASR / chunk data" src="https://raw.githubusercontent.com/Ajaysvasan/Ajaysvasan/main/assets/mmrag-light.svg" width="100%">
</picture>

- **Layered caching** — a topic-level cache and query-history snapshots sit in front of FAISS HNSW retrieval
- **Relevance gating** — cross-encoder reranking and a relevance gate filter what reaches generation
- **Multimodal data** — OCR and ASR processing, with PostgreSQL-backed data and state
- **Local inference** — llama.cpp and C++ backend components integrated with Python, lazy loading on performance-sensitive paths

<br>

<table>
<thead>
<tr>
<td colspan="3">

**[Project Atlas](https://github.com/Ajaysvasan/atlas)**

A project-aware local RAG system for research. Atlas keeps persistent memory per project, scopes conversational retrieval to that project's context, and handles retrieval orchestration and adaptive knowledge acquisition for structured research workflows.

</td>
</tr>
</thead>
<tbody>
<tr>
<td width="33%" valign="top">

**[DSA in C++](https://github.com/Ajaysvasan/DSA_in_cpp)**

Data structures, algorithms, competitive programming and LeetCode in C++ — the fundamentals underneath the larger projects.

`graphs` `trees` `DP` `DSU` `recursion` `STL`

</td>
<td width="33%" valign="top">

**[Neovim](https://github.com/Ajaysvasan/nvim)**

Personal Neovim configuration — the editor setup I use for day-to-day development.

</td>
<td width="33%" valign="top">

**[Dotfiles](https://github.com/Ajaysvasan/.dotfiles)**

Linux configuration and custom utilities.

`kitty` `tmux` `fastfetch`

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

**Winner** — ProjectFest (AI/ML) · IEEE Software Competition (Sairam College)<br>
**Participant** — IBM Datathon (Global) · AIML Challenge, IIT Madras
