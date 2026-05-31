# AI/ML Integration Cursor Rules

## LLM Integration
- Use structured outputs (JSON mode, function calling)
- Implement retry logic with exponential backoff
- Token counting before API calls
- Streaming responses for long generations
- Caching for identical prompts
- Rate limiting and queue management

## Prompt Engineering
- System prompts define role and constraints
- Few-shot examples in prompt template
- Chain-of-thought for reasoning tasks
- Output format specification (JSON schema)
- Temperature 0 for deterministic, 0.7 for creative

## RAG Pattern
- Chunk documents with overlap
- Embedding model: text-embedding-3-small or similar
- Vector store: pgvector, Pinecone, or Qdrant
- Hybrid search (vector + keyword)
- Reranking for relevance

## AI Safety
- Input sanitization (prompt injection prevention)
- Output validation (schema, content policy)
- Human-in-the-loop for high-stakes decisions
- Fallback to default behavior on AI failure
- Logging all AI interactions for audit
