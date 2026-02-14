# ReliableRAG

ReliableRAG is an enterprise-grade Retrieval-Augmented Generation (RAG) pipeline designed for answering questions over regulatory and technical documents with high faithfulness and minimal hallucination.

The system focuses on **precision, reliability, and explainability**, making it suitable for compliance-heavy domains such as financial services and cloud governance.

---

## 🚀 Key Features

- Semantic document chunking using meaning-based boundaries
- Query rewriting to improve retrieval for vague or underspecified questions
- HyDE (Hypothetical Document Embedding) for improved recall
- Cross-encoder reranking for high-precision retrieval
- Relevance thresholding and no-answer detection
- Contextual compression to remove irrelevant paragraphs
- Explicit context window control to prevent truncation
- Automatic end-to-end pipeline orchestration

---

## 🧠 Architecture Overview

