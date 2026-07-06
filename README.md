## Tang Simu

Graduate student at the **University of Electronic Science and Technology of China** (Chengdu), working on **retrieval-augmented generation and retrieval systems** for large language models — dense retrieval, reranking, and grounded RAG pipelines.

My work leans toward small, readable, **offline-first** implementations: dependency-light cores you can run in a unit test, read end to end, and reproduce on a laptop or in CI — no model downloads, no network calls, no hidden state. Grounding and evaluation are treated as first-class concerns rather than afterthoughts.

![Focus](https://img.shields.io/badge/focus-retrieval--augmented%20generation-4c6ef5)
![Also](https://img.shields.io/badge/also-dense%20retrieval%20%C2%B7%20reranking-495057)
![Python](https://img.shields.io/badge/python-3.10%2B-3776ab?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/core-NumPy-013243?logo=numpy&logoColor=white)
![PyTorch](https://img.shields.io/badge/optional-PyTorch-ee4c2c?logo=pytorch&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-2f9e44)

---

### Featured projects

#### 🔎 [ragcite](https://github.com/ivyw960/ragcite)
A pure-Python **retrieval-augmented generation** pipeline that retrieves passages, reranks them, generates an answer, and ties every sentence back to its supporting passages with inline `[1]` citations. Ships with an offline extractive generator, so the whole thing runs with no model, no network, and no third-party dependencies — plus an evaluation harness for retrieval, answer quality, and citation grounding. Each stage (retrieve → rerank → generate → ground) is a small, swappable object, and you can bring your own LLM by wrapping any `str -> str` callable.

`retrieval-augmented-generation` · `reranking` · `citations` · `information-retrieval`

#### 📐 [densekit](https://github.com/ivyw960/densekit)
An offline-first **dense retrieval and embedding toolkit** built on a pure-NumPy core: deterministic hashing / random-projection encoders, exact `FlatIndex` plus approximate `IVFIndex`, `LSHIndex`, and `PQIndex` behind one `search` API, and IR metrics (recall@k, precision@k, nDCG@k, MRR, MAP) that mirror `trec_eval` conventions. An optional PyTorch backend trains bi-encoders with in-batch InfoNCE, and any index serializes to a plain `.npz` archive. Reproducible on a laptop or in CI, with a `densekit encode | build | search | evaluate` CLI for file-based pipelines.

`dense-retrieval` · `approximate-nearest-neighbors` · `embeddings` · `information-retrieval`

---

### Research interests

| Area | What I'm exploring |
| --- | --- |
| Retrieval-augmented generation | Grounded generation with faithful, sentence-level citation attribution |
| Dense retrieval | Bi-encoder training, ANN indexing (IVF / LSH / PQ), and embedding methods |
| Reranking & fusion | Lexical / MMR reranking and reciprocal rank fusion over hybrid retrieval |
| Evaluation | Reproducible IR and answer-quality measurement that runs offline and in CI |

### How I like to build

- **Offline-first & reproducible** — dependency-light cores, no network calls, deterministic by default.
- **Readable over clever** — code you can follow in an afternoon; every stage a small, swappable piece.
- **Evaluation as a first-class citizen** — grounding and metrics built in, not bolted on afterward.

<sub>Tooling: Python · NumPy · PyTorch (optional). Both projects are MIT-licensed.</sub>
