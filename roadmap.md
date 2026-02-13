# 📋 Roadmap: Learning Generative AI

## Overview
**Goal:** Gain comprehensive understanding of GenAI — from fundamentals to building applications
**Timeline:** 3-6 months (depending on pace and prior background)
**Success criteria:** Can explain GenAI concepts, use APIs effectively, fine-tune models, and build GenAI-powered applications

---

## Phase 1: Foundations
**Duration:** 2-3 weeks
**Objective:** Understand what GenAI is and how it works conceptually

### Milestone 1.1: Core Concepts
- [ ] Understand ML basics — supervised vs unsupervised, training vs inference *(~4 hours)*
- [ ] Learn what neural networks are — layers, weights, activation functions *(~3 hours)*
- [ ] Grasp the Transformer architecture — attention mechanism, encoder/decoder *(~4 hours)*
- [ ] Understand tokenization — BPE, vocabulary, context windows *(~2 hours)*

### Milestone 1.2: GenAI Landscape
- [ ] Learn the difference: LLMs vs image models vs multimodal *(~2 hours)*
- [ ] Survey major models: GPT, Claude, Gemini, Llama, Mistral, Stable Diffusion *(~3 hours)*
- [ ] Understand model sizes, parameters, and what they mean *(~1 hour)*
- [ ] Learn about training data, RLHF, and alignment *(~3 hours)*

**Resources:**
- 3Blue1Brown: Neural Networks series (YouTube)
- Andrej Karpathy: "Let's build GPT from scratch" (YouTube)
- Jay Alammar: "The Illustrated Transformer"

---

## Phase 2: Hands-On with APIs
**Duration:** 2-3 weeks
**Objective:** Build practical skills using GenAI through APIs

### Milestone 2.1: API Fundamentals
- [ ] Set up OpenAI API account and make first call *(~1 hour)*
- [ ] Understand API parameters: temperature, top_p, max_tokens *(~2 hours)*
- [ ] Learn prompt engineering basics — system/user/assistant roles *(~3 hours)*
- [ ] Experiment with different models (GPT-4, Claude, Gemini) *(~4 hours)*

### Milestone 2.2: Prompt Engineering
- [ ] Master few-shot prompting with examples *(~3 hours)*
- [ ] Learn chain-of-thought prompting *(~2 hours)*
- [ ] Practice structured output (JSON mode, function calling) *(~4 hours)*
- [ ] Build a simple chatbot with conversation memory *(~4 hours)*

### Milestone 2.3: First Projects
- [ ] Build: Text summarizer *(~3 hours)*
- [ ] Build: Q&A system over documents *(~4 hours)*
- [ ] Build: Content generator (blog posts, emails) *(~3 hours)*

**Resources:**
- OpenAI Cookbook (GitHub)
- Anthropic Prompt Engineering Guide
- LangChain documentation

---

## Phase 3: RAG & Embeddings
**Duration:** 2-3 weeks
**Objective:** Learn retrieval-augmented generation and vector search

### Milestone 3.1: Embeddings
- [ ] Understand what embeddings are — semantic vectors *(~2 hours)*
- [ ] Learn about embedding models (text-embedding-3, Cohere, etc.) *(~2 hours)*
- [ ] Experiment with similarity search *(~3 hours)*

### Milestone 3.2: Vector Databases
- [ ] Set up a vector DB (Pinecone, Weaviate, Chroma, or pgvector) *(~3 hours)*
- [ ] Index documents and perform semantic search *(~4 hours)*
- [ ] Understand chunking strategies for documents *(~2 hours)*

### Milestone 3.3: Build RAG System
- [ ] Implement end-to-end RAG pipeline *(~6 hours)*
- [ ] Handle different doc types (PDF, web, markdown) *(~4 hours)*
- [ ] Optimize retrieval with hybrid search, reranking *(~4 hours)*

**Resources:**
- LangChain RAG tutorials
- LlamaIndex documentation
- Pinecone learning center

---

## Phase 4: Local Models & Fine-tuning
**Duration:** 3-4 weeks
**Objective:** Run models locally and customize them

### Milestone 4.1: Local Inference
- [ ] Set up Ollama or LM Studio *(~2 hours)*
- [ ] Run Llama, Mistral, Phi locally *(~3 hours)*
- [ ] Understand hardware requirements (GPU, VRAM, quantization) *(~2 hours)*
- [ ] Compare local vs API: speed, cost, privacy tradeoffs *(~2 hours)*

### Milestone 4.2: Fine-tuning Basics
- [ ] Understand when and why to fine-tune *(~2 hours)*
- [ ] Learn about LoRA and QLoRA — efficient fine-tuning *(~3 hours)*
- [ ] Set up fine-tuning environment (Hugging Face, Axolotl) *(~4 hours)*
- [ ] Fine-tune a small model on custom data *(~6 hours)*

### Milestone 4.3: Evaluation
- [ ] Learn evaluation metrics (perplexity, BLEU, human eval) *(~3 hours)*
- [ ] Build evaluation datasets for your use case *(~4 hours)*
- [ ] Compare base vs fine-tuned performance *(~3 hours)*

**Resources:**
- Hugging Face course
- Sebastian Raschka: "LLMs from Scratch" (book)
- Unsloth fine-tuning tutorials

---

## Phase 5: Agents & Advanced Patterns
**Duration:** 2-3 weeks
**Objective:** Build autonomous AI systems

### Milestone 5.1: Tool Use & Function Calling
- [ ] Implement function calling with OpenAI/Anthropic *(~4 hours)*
- [ ] Build agents that use external tools (search, calculator, APIs) *(~6 hours)*
- [ ] Handle errors and retries gracefully *(~3 hours)*

### Milestone 5.2: Agent Frameworks
- [ ] Explore LangGraph for stateful agents *(~4 hours)*
- [ ] Build a ReAct-style reasoning agent *(~4 hours)*
- [ ] Implement multi-step planning agents *(~4 hours)*

### Milestone 5.3: Production Patterns
- [ ] Learn about guardrails and safety *(~3 hours)*
- [ ] Implement caching and cost optimization *(~3 hours)*
- [ ] Add observability (logging, tracing, evaluation) *(~4 hours)*

**Resources:**
- LangGraph documentation
- Anthropic tool use guide
- AI Engineer resources (latent.space)

---

## Phase 6: Image & Multimodal
**Duration:** 2 weeks (optional track)
**Objective:** Expand beyond text to images and multimodal

### Milestone 6.1: Image Generation
- [ ] Understand diffusion models conceptually *(~3 hours)*
- [ ] Use DALL-E, Midjourney, Stable Diffusion APIs *(~4 hours)*
- [ ] Learn image prompting techniques *(~3 hours)*

### Milestone 6.2: Multimodal
- [ ] Use vision models (GPT-4V, Claude Vision, Gemini) *(~4 hours)*
- [ ] Build image-to-text applications *(~4 hours)*
- [ ] Explore video and audio models *(~4 hours)*

---

## Dependencies & Risks

- **Dependency:** Basic Python proficiency required before Phase 2
- **Dependency:** GPU access helpful (but not required) for Phase 4
- **Risk:** API costs can add up → **Mitigation:** Use free tiers, local models, or set spending limits
- **Risk:** Field moves fast → **Mitigation:** Follow key people on X/Twitter, subscribe to newsletters

## Recommended Follows

- **Twitter/X:** @karpathy, @swyx, @simonw, @emollick
- **Newsletters:** The Batch (Andrew Ng), Ben's Bites, Latent Space
- **Podcasts:** Latent Space, Practical AI

---

## Next Actions

1. **Today:** Watch 3Blue1Brown neural network video (~20 min)
2. **This week:** Complete Phase 1 Milestone 1.1
3. **Set up:** OpenAI API account (free tier)
