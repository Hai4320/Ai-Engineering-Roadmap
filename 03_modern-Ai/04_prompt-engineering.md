# Prompt Engineering

Prompt engineering là nghệ thuật thiết kế input (prompt) hiệu quả để dẫn dắt large language model (LLM) sinh ra kết quả chính xác, hữu ích, hoặc sáng tạo. Khi model ngày càng mạnh, prompt tốt chính là chìa khóa để khai thác hết tiềm năng của chúng.

## Mục Tiêu Học Tập

Sau khi hoàn thành module này, bạn sẽ có thể:

- Hiểu các định dạng và chiến lược prompt khác nhau
- Áp dụng kỹ thuật prompting như zero-shot, few-shot, và chain-of-thought
- Dùng structured prompting, template, và prompt chaining
- Đánh giá và lặp lại (iterate) prompt để có kết quả nhất quán

## Vì Sao Điều Này Quan Trọng

Prompting thường mạnh hơn cả fine-tuning. Nó giúp bạn khai thác model pre-trained hiệu quả mà không cần chỉnh sửa chúng — lý tưởng cho prototyping, RAG, và hệ thống dựa trên agent.

## Chủ Đề Cốt Lõi & Tài Nguyên

### 1. Foundations of Prompting

- [Prompt Engineering Guide](https://www.promptingguide.ai/) — **Miễn phí**
- [OpenAI Prompt Examples](https://platform.openai.com/examples) — **Miễn phí**
- [Google Prompt Engineering Crash Course (YouTube)](https://www.youtube.com/watch?v=qw1pV_q3-ZA) — **Miễn phí**

Bao gồm:
- Cấu trúc prompt cơ bản
- Model instruct so với completion
- Ví dụ few-shot và định dạng prompt

### 2. Prompting Techniques

- [Chain of Thought Prompting Paper](https://arxiv.org/abs/2201.11903) — **Miễn phí**
- [ReAct Prompting (Reason + Act)](https://arxiv.org/abs/2210.03629) — **Miễn phí**
- [Guidelines for Iterative Prompting](https://github.com/dair-ai/Prompt-Engineering-Guide) — **Miễn phí**

Kỹ thuật:
- **Zero-shot prompting**  
- **Few-shot prompting**
- **Chain-of-thought reasoning**
- **Self-consistency** prompting
- **Toolformer-style** tool-aware prompting

### 3. Prompt Tools & Frameworks

- [PromptLayer](https://www.promptlayer.com/) — Logging và debug prompt  
- [LangChain Prompt Templates](https://docs.langchain.com/docs/components/prompts/) — **Miễn phí**
- [Prompt Engineering in LangChain (Docs)](https://docs.langchain.com/docs/guides/prompts) — **Miễn phí**

Bao gồm:
- Template hóa prompt và chèn biến (variable injection)
- Prompt chaining (output làm input cho prompt tiếp theo)
- Đánh giá prompt ở quy mô lớn

### 4. Evaluation & Safety

- [Evaluating Prompt Quality (Google DeepMind)](https://arxiv.org/abs/2302.09604) — **Miễn phí**
- [OpenAI Moderation API](https://platform.openai.com/docs/guides/moderation) — **Miễn phí**

Bao gồm:
- Debug prompt và đảm bảo tính nhất quán của output
- Độ nhạy của prompt, thiên lệch (bias), hallucination
- Chấm điểm output và A/B testing

### 5. Advanced Prompt Engineering Resources

- [Awesome Prompt Engineering (GitHub)](https://github.com/promptslab/awesome-prompt-engineering) — **Danh sách tổng hợp**
- [Prompt Engineering Papers (arXiv)](https://arxiv.org/search/?query=prompt+engineering&searchtype=all) — **Miễn phí**
- [Prompt Engineering for Developers (DeepLearning.AI)](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) — **Miễn phí**
- [Prompt Engineering Leaderboard (Hugging Face)](https://huggingface.co/spaces/mteb/leaderboard) — **Miễn phí**

Bao gồm:
- Paper nghiên cứu và leaderboard
- Thiết kế và đánh giá prompt nâng cao
- Tài nguyên do cộng đồng tổng hợp

## Gợi Ý Dự Án & Thực Hành

- Xây dựng prompt giải thích một khái niệm ở cả mức cơ bản lẫn chuyên sâu
- Thiết kế prompt sinh câu hỏi kiểm tra từ tài liệu
- So sánh output giữa zero-shot và chain-of-thought
- Dùng LangChain để tạo luồng prompt nhiều bước


## Checkpoint: Trước Khi Qua Phần Tiếp Theo

Bạn sẽ có thể:

- Viết prompt hiệu quả cho nhiều loại bài toán khác nhau
- Dùng chiến lược prompting nâng cao để cải thiện chất lượng output
- Tích hợp prompt vào chain và hệ thống RAG
- Đánh giá và debug prompt một cách có hệ thống

🔗 Tiếp theo: [AI Tooling →](./05_ai-tooling.md)
