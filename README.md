## Tang Simu

Grad student at **UESTC** (Chengdu) · retrieval-augmented generation & retrieval systems.

> Good generation starts with good retrieval. I work on the pieces that put the right context in front of an LLM — and prove it did.

**The pipeline I build toward**

`query → [dense retrieval] → [rerank] → [grounded, cited generation]`

**Projects**

- **[densekit](https://github.com/ivyw960/densekit)** — the retrieval half
  Bi-encoder training, ANN indexing (IVF / LSH / PQ), and IR evaluation on a NumPy core. Offline-first.

- **[ragcite](https://github.com/ivyw960/ragcite)** — the generation half
  A pure-Python RAG pipeline with grounded, citation-aware generation and an evaluation harness.

Everything runs offline, no GPU required — NumPy core with an optional PyTorch backend, CI green.
