# Large Language Models (LLMs)

Large Language Models (LLM) như GPT-4, Claude, LLaMA, và PaLM đã tạo nên cuộc cách mạng cho việc hiểu và sinh ngôn ngữ tự nhiên. Hiểu cách LLM hoạt động — và cách xây dựng, fine-tune, hoặc sử dụng chúng — là chìa khóa cho AI engineering hiện đại.

## Mục Tiêu Học Tập

Sau khi hoàn thành module này, bạn sẽ có thể:

- Hiểu kiến trúc và cách train đứng sau LLM dựa trên transformer
- Dùng LLM API và model mã nguồn mở cho nhiều bài toán (chatbot, tóm tắt, hỏi-đáp)
- Đánh giá, fine-tune, và deploy LLM trong môi trường production
- Hiểu các cân nhắc về đạo đức và an toàn khi dùng LLM

## Vì Sao Điều Này Quan Trọng

LLM là cốt lõi của các ứng dụng AI hiện đại. Chúng mang lại khả năng từ sinh code đến nghiên cứu pháp lý, tóm tắt y tế, và AI agent. Các kỹ sư am hiểu LLM đang rất được săn đón trong mọi ngành.


## Chủ Đề Cốt Lõi & Tài Nguyên

### 1. Foundations of Large Language Models

- [The Illustrated Transformer – Jay Alammar](https://jalammar.github.io/illustrated-transformer/) — **Miễn phí**
- [Transformers From Scratch – YouTube (Andrej Karpathy)](https://www.youtube.com/watch?v=kCc8FmEb1nY) — **Miễn phí**
- [Attention Is All You Need (Paper gốc)](https://arxiv.org/abs/1706.03762) — **Miễn phí**

Bao gồm:
- Kiến trúc Transformer (self-attention, encoder-decoder)
- Positional encoding, masked attention
- Pre-training và fine-tuning

### 2. Using LLMs via APIs

- [OpenAI GPT API Quickstart](https://platform.openai.com/docs/quickstart) — **Có gói miễn phí**
- [Anthropic Claude API Guide](https://docs.anthropic.com/) — **Có gói miễn phí**
- [LangChain for LLM Workflows](https://docs.langchain.com/) — **Miễn phí**

Bao gồm:
- Kỹ thuật Prompting (zero-shot, few-shot, chain-of-thought)
- Xây dựng chatbot, agent, và công cụ
- Prompt injection và an toàn

### 3. Open-Source LLMs

- [Hugging Face Transformers Course](https://huggingface.co/learn/nlp-course/) — **Miễn phí**
- [Running LLaMA or Mistral on Local Hardware – Guides](https://huggingface.co/blog/llama2) — **Miễn phí**

Bao gồm:
- Làm việc với model như LLaMA 2, Mistral, Falcon
- Load model qua `transformers` và `transformers.js`
- Tokenizer, tốc độ inference, quantization

### 4. Fine-Tuning & Retrieval-Augmented Generation (RAG)

- [Fine-tuning LLMs with LoRA – Hugging Face](https://huggingface.co/blog/lora) — **Miễn phí**
- [RAG with Haystack or LangChain – Tutorials](https://www.youtube.com/watch?v=Lk4TzDNsCzU) — **Miễn phí**
- [Full-Stack LLM Bootcamp – Cohere](https://fullstackdeeplearning.com/llm-bootcamp/) — **Miễn phí**

Bao gồm:
- Fine-tuning với LoRA/QLoRA
- Embedding và vector store (FAISS, ChromaDB)
- Hybrid search và chèn tài liệu (document injection)

### 5. LLM Security, Ethics & Evaluation

- [AI Security & Safety (DeepMind)](https://deepmind.com/research/publications/2023/ai-safety-and-security) — **Miễn phí**
- [Responsible AI Practices (Google)](https://ai.google/responsibilities/responsible-ai-practices/) — **Miễn phí**
- [LLM Security Risks (OWASP)](https://owasp.org/www-community/attacks/LLM_Attacks) — **Miễn phí**
- [Responsible AI with LLMs – DeepLearning.AI Short Course](https://www.deeplearning.ai/short-courses/responsible-llms/) — **Miễn phí**
- [Red Teaming LLMs – Anthropic Blog](https://www.anthropic.com/index/2023/07/red-teaming-ai/) — **Miễn phí**
- [Prompt Injection Guide – OWASP](https://owasp.org/www-community/attacks/Prompt_Injection) — **Miễn phí**

Bao gồm:
- Rủi ro bảo mật khi deploy LLM
- Prompt injection, jailbreak, và prompt đối kháng (adversarial prompting)
- Thiên lệch (bias), công bằng, hallucination, và độc hại
- Đánh giá model và công cụ an toàn
- Chiến lược giảm thiểu và thực hành AI có trách nhiệm

## Gợi Ý Dự Án & Thực Hành

- Xây dựng bot hỏi-đáp dùng OpenAI hoặc Claude API
- Fine-tune một LLM mã nguồn mở trên dữ liệu chuyên ngành
- Triển khai RAG trên một tập tài liệu (vd: knowledge base công ty)
- So sánh các model (GPT-4 so với LLaMA) trên cùng một bài toán prompt

## Checkpoint: Trước Khi Qua Phần Tiếp Theo

Bạn sẽ có thể:

- Dùng và prompt LLM hiệu quả qua API hoặc thư viện mã nguồn mở
- Fine-tune và deploy LLM cho bài toán riêng
- Hiểu rủi ro và giới hạn cốt lõi của hệ thống dựa trên LLM

🔗 Tiếp theo: [Agentic AI →](./02_agentic-ai.md)
