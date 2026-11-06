# Retrieval-Augmented Generation (RAG)

## 1. What is RAG?

Retrieval-Augmented Generation is a technique that grounds a large
language model (LLM) in external, up-to-date knowledge by retrieving
relevant documents before generating an answer.

Instead of relying only on the model's internal weights, RAG:

- Fetches context from a knowledge base at query time.
- Feeds that context into the prompt alongside the question.
- Lets the model answer using the retrieved evidence.

This reduces hallucination and keeps answers current without retraining.

## 2. Why RAG matters

- **Freshness** — knowledge can be updated without fine-tuning.
- **Grounding** — answers cite real sources instead of guessing.
- **Control** — you decide which documents the model may use.
- **Cost** — cheaper than retraining a large model on new data.
- **Traceability** — each answer can point back to its evidence.

## 3. Core components

1. **Indexing pipeline** — turns documents into searchable chunks.
2. **Retriever** — finds the most relevant chunks for a query.
3. **Generator** — the LLM that writes the final answer.
4. **Orchestrator** — ties retrieval and generation together.

## 4. The indexing pipeline

### 4.1 Loading
Read documents from files, databases, or APIs.

### 4.2 Chunking
Split long documents into smaller pieces.

- Fixed-size chunks (e.g. 512 tokens).
- Sentence- or paragraph-based splits.
- Semantic or structure-aware splits.

### 4.3 Embedding
Convert each chunk into a dense vector.

- Use an embedding model (e.g. text-embedding-3, bge, e5).
- Store vectors in a vector database.

### 4.4 Storage
Persist chunks and their vectors.

- Vector stores: Pinecone, Weaviate, Qdrant, Milvus, pgvector.
- Also keep the raw text and metadata for later use.

## 5. Retrieval

### 5.1 Query embedding
Embed the user's question with the same model used for chunks.

### 5.2 Similarity search
Find the top-k nearest chunks to the query vector.

- Cosine similarity is the most common metric.
- Dot product and Euclidean distance are alternatives.

### 5.3 Reranking (optional)
Improve precision with a cross-encoder reranker.

- Retrieval is fast but coarse.
- Reranking is slower but more accurate.
- Common pattern: retrieve 50, rerank to top 5.

## 6. Generation

### 6.1 Prompt assembly
Combine the question with retrieved context.


### 6.2 Answering
The LLM produces a grounded answer.

- Ask the model to cite which chunks it used.
- Ask it to say "I don't know" when context is insufficient.

## 7. Common failure modes

- **Irrelevant retrieval** — wrong chunks lead to wrong answers.
- **Lost in the middle** — models ignore context in the middle.
- **Chunk fragmentation** — splitting breaks meaning across chunks.
- **Stale index** — documents change but the index does not.
- **Over-trusting context** — bad context still produces confident answers.

## 8. Improving retrieval quality

- Tune chunk size and overlap.
- Add metadata filters (date, source, category).
- Use hybrid search: dense + sparse (BM25).
- Add a reranker.
- Query rewriting or expansion before retrieval.

## 9. Evaluation

- **Retrieval metrics** — recall@k, precision@k, MRR, nDCG.
- **Generation metrics** — faithfulness, answer relevance.
- **End-to-end** — does the final answer match ground truth?
- Use a golden dataset of question–answer pairs.

## 10. Advanced patterns

- **Parent-child retrieval** — retrieve small chunks, feed larger context.
- **Multi-hop RAG** — answer questions needing several steps.
- **Self-RAG** — the model decides when to retrieve.
- **Graph RAG** — retrieve over knowledge graphs, not just text.
- **Agentic RAG** — an agent plans, retrieves, and verifies.

## 11. When not to use RAG

- The model already knows the answer reliably.
- The data is tiny and fits in the prompt directly.
- Latency is critical and retrieval adds too much delay.
- The knowledge changes rarely and fine-tuning is acceptable.

## 12. Quick checklist

- [ ] Choose an embedding model and keep it consistent.
- [ ] Pick a chunking strategy that fits your documents.
- [ ] Store vectors with metadata for filtering.
- [ ] Add a reranker if precision matters.
- [ ] Evaluate retrieval and generation separately.
- [ ] Refresh the index when source data changes.
- [ ] Log queries and answers for debugging.

