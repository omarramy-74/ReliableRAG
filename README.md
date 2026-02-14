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

User Query
↓
Query Rewrite
↓
Vector Retrieval (Top-K)
↓
Cross-Encoder Reranking
↓
Relevance Threshold Filtering
↓
Contextual Compression
↓
Context Window Control
↓
LLM Answer OR Abstain


---

## 📦 Data Sources

- PDF documents (regulatory and technical reports)
- CSV files (structured reference data)

Documents are cleaned to remove headers, footers, and noise before indexing.

---

## 🔬 Design Principles

- **Faithfulness over fluency**: answers must be grounded in retrieved context
- **Abstention over hallucination**: the system explicitly refuses to answer when evidence is insufficient
- **Separation of concerns**: retrieval, ranking, compression, and generation are independent stages
- **Production realism**: avoids brittle abstractions and unstable library dependencies

---

## ⚙️ Implementation Details

### Retrieval
- Embedding-based vector search for candidate retrieval
- Semantic chunking using percentile-based thresholds

### Query Enhancement
- LLM-based query rewriting
- HyDE for embedding hypothetical answers instead of raw queries

### Precision Control
- Cross-encoder reranking (`ms-marco` style models)
- Relevance score thresholding to filter weak matches

### Context Control
- Query-aware contextual compression
- Token-based context window enforcement

---

## 🧪 Evaluation Strategy

- Qualitative evaluation using real regulatory queries
- Comparison before and after reranking and compression
- Verification of hallucination-free behavior
- Explicit testing of no-answer scenarios

---

## 📈 Example Use Case

**Query:**
> "Effective risk assessment and governance controls"

**Behavior:**
- Retrieves relevant regulatory sections
- Filters irrelevant vendor descriptions
- Compresses content to core compliance requirements
- Produces a grounded, faithful answer
- Abstains when information is missing

---

## 🛡️ Limitations

- No multi-hop reasoning across documents
- Evaluation is qualitative (metrics can be added later)
- Optimized for text-based documents only

---

## 🔮 Future Improvements

- Automated evaluation using DeepEval or RAGAS
- Multi-hop and graph-based retrieval
- Query decomposition for complex questions
- Multimodal document support

---

## 🧑‍💻 Author

Built as a hands-on project to deeply understand and implement reliable, production-style RAG systems beyond tutorial-level implementations.
