# Retrieval-Augmented Generation (RAG)

Retrieval-Augmented Generation (RAG) nâng cấp LLM bằng cách kết hợp chúng với nguồn dữ liệu bên ngoài. Thay vì chỉ dựa vào kiến thức nội tại của model, RAG cho phép truy cập động vào nội dung cập nhật hoặc chuyên ngành ngay trong lúc sinh câu trả lời.

## Mục Tiêu Học Tập

Sau khi hoàn thành module này, bạn sẽ có thể:

- Hiểu kiến trúc RAG và các thành phần của nó (retriever + generator)
- Xây dựng pipeline RAG đơn giản dùng vector database và LLM
- Fine-tune hệ thống retrieval với embedding
- Áp dụng RAG vào bài toán thực tế (hỏi-đáp, chatbot, trợ lý tri thức)

## Vì Sao Điều Này Quan Trọng

LLM có context window giới hạn và dữ liệu train tĩnh. RAG giải quyết vấn đề này bằng cách cho phép model *lấy* thông tin liên quan ngay tại thời điểm inference, phù hợp cho hệ thống AI cần thông tin cập nhật, chính xác, hoặc chuyên biệt cho doanh nghiệp.


## Chủ Đề Cốt Lõi & Tài Nguyên

### 1. RAG Fundamentals

- [Retrieval-Augmented Generation – YouTube (AssemblyAI)](https://www.youtube.com/watch?v=qbIk7-JPB2c) — **Miễn phí**
- [Hugging Face RAG Architecture Overview](https://huggingface.co/blog/rag) — **Miễn phí**
- [RAG Explained – Zilliz](https://zilliz.com/blog/retrieval-augmented-generation-explained) — **Miễn phí**

Bao gồm:
- Vector store, retriever, và generator
- RAG khác fine-tuning ở điểm nào
- Tổng quan hệ thống RAG in-memory so với persistent

### 2. Building a RAG Pipeline

- [LangChain RAG Tutorial](https://docs.langchain.com/docs/use-cases/question-answering/) — **Miễn phí**
- [Haystack RAG Implementation](https://docs.haystack.deepset.ai/docs/rag) — **Miễn phí**
- [ChromaDB + OpenAI Demo](https://www.youtube.com/watch?v=GkZrTgV0nrw) — **Miễn phí**

Bao gồm:
- Tạo và dùng vector store (Chroma, FAISS, Weaviate)
- Embedding model (OpenAI, Hugging Face, SentenceTransformers)
- Chunking, retrieval, và tích hợp vào prompt

### 3. Embeddings & Vector Databases

- [OpenAI Embedding Guide](https://platform.openai.com/docs/guides/embeddings) — **Có gói miễn phí**
- [Intro to FAISS – Facebook AI](https://github.com/facebookresearch/faiss) — **Miễn phí**
- [ChromaDB Quickstart](https://docs.trychroma.com/) — **Miễn phí**

Bao gồm:
- Chunking văn bản, tạo embedding
- Lưu trữ và tìm kiếm vector
- Semantic similarity so với tìm kiếm từ khóa

### 4. Evaluation & Optimization

- [RAG Best Practices – Cohere](https://docs.cohere.com/docs/rag-best-practices) — **Miễn phí**
- [Prompt Engineering for RAG](https://www.promptingguide.ai/techniques/rag) — **Miễn phí**
- [Context Re-ranking with BGE/ColBERT](https://huggingface.co/spaces/mteb/leaderboard) — **Miễn phí**

Bao gồm:
- Độ chính xác (precision) và độ bao phủ (recall) của retrieval
- Chiến lược re-ranking
- Tối ưu kích thước chunk, temperature, context của prompt

### 5. Advanced RAG Resources

- [Awesome RAG (GitHub)](https://github.com/0xpayne/awesome-rag) — **Danh sách tổng hợp**
- [RAG End-to-End Tutorial (YouTube, Pinecone)](https://www.youtube.com/watch?v=Vv0bKz0j7uY) — **Miễn phí**
- [RAG with OpenAI and ChromaDB (Blog)](https://blog.langchain.dev/rag-openai-chromadb/) — **Miễn phí**
- [RAG Evaluation and Metrics (Cohere)](https://docs.cohere.com/docs/rag-evaluation) — **Miễn phí**

Bao gồm:
- Pipeline RAG end-to-end
- Đánh giá và chỉ số cho RAG
- Công cụ và framework RAG mã nguồn mở

## Gợi Ý Dự Án & Thực Hành

- Xây dựng công cụ "Chat with Docs" dùng LangChain và FAISS
- Tạo trợ lý tri thức chạy bằng RAG cho ghi chú hoặc PDF của bạn
- So sánh hiệu năng tìm kiếm từ khóa so với semantic search
- Dùng Haystack hoặc Chroma để deploy bot hỏi-đáp bằng RAG

## Checkpoint: Trước Khi Qua Phần Tiếp Theo

Bạn sẽ có thể:

- Giải thích RAG hoạt động thế nào và vì sao được dùng
- Xây dựng pipeline RAG đầy đủ từ tài liệu đến kết quả truy vấn
- Dùng vector database và embedding hiệu quả
- Tối ưu RAG để tăng độ liên quan và hiệu năng

🔗 Tiếp theo: [Prompt Engineering →](./04_prompt-engineering.md)
