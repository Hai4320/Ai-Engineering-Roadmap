# Agentic AI

Agentic AI chỉ các hệ thống hoạt động tự hành, tự ra quyết định và hành động hướng tới mục tiêu mà không cần giám sát liên tục từ con người. Đây là một mảng cốt lõi của AI hiện đại, nơi các model như LLM được nhúng vào trong các agent có khả năng lập kế hoạch, suy luận, và tương tác với công cụ và môi trường.

## Mục Tiêu Học Tập

Sau khi hoàn thành module này, bạn sẽ có thể:

- Hiểu AI agent là gì và khác gì so với việc dùng LLM một lần (single-shot)
- Xây dựng agent có thể dùng công cụ, truy xuất dữ liệu, và hoàn thành tác vụ qua nhiều bước
- Hiểu các framework như LangChain, Auto-GPT, và CrewAI
- Thiết kế hệ thống multi-agent và luồng điều phối tác vụ (task orchestration)

## Vì Sao Điều Này Quan Trọng

Hệ thống agentic là chìa khóa để biến LLM thực sự *hữu ích* trong ứng dụng thực tế — từ trợ lý nghiên cứu tự hành đến bot chăm sóc khách hàng và AI đồng hành (co-pilot). Chúng mở khóa khả năng suy luận liên tục, ghi nhớ, lập kế hoạch, và ra quyết định.


## Chủ Đề Cốt Lõi & Tài Nguyên

### 1. What Are AI Agents?

- [LangChain: Agents & Tools Docs](https://docs.langchain.com/docs/components/agents/) — **Miễn phí**
- [What are AI Agents? – YouTube (AssemblyAI)](https://www.youtube.com/watch?v=JQkjhoq92JE) — **Miễn phí**
- [Agent Models in AI – A Short Introduction](https://www.microsoft.com/en-us/research/blog/the-emergence-of-agentic-ai/) — **Miễn phí**

Bao gồm:
- Kiến trúc Agent: lập kế hoạch, ghi nhớ, thực thi
- Phân rã tác vụ và quy trình nhiều bước
- Hành vi phản tư (reflection) và tự phục hồi

### 2. Tool Use & Environments

- [Toolformer Paper (Meta AI)](https://arxiv.org/abs/2302.04761) — **Miễn phí**
- [OpenAI Function Calling Examples](https://platform.openai.com/docs/guides/gpt/function-calling) — **Miễn phí**
- [LangChain Tools + Agents Guide](https://python.langchain.com/docs/modules/agents/tools) — **Miễn phí**

Bao gồm:
- Cách agent gọi API bên ngoài, dùng máy tính, trình duyệt web, hoặc code interpreter
- Hành động đa phương thức: text + code + công cụ
- Định tuyến công cụ (tool routing), fallback, và xử lý lỗi

### 3. Agentic Frameworks

- [LangChain Agents](https://docs.langchain.com/docs/components/agents/) — **Miễn phí**
- [Auto-GPT](https://github.com/Torantulino/Auto-GPT) — **Miễn phí, Mã nguồn mở**
- [CrewAI (Multi-Agent Framework)](https://github.com/joaomdmoura/crewAI) — **Miễn phí**

Bao gồm:
- Khác biệt giữa agent kịch bản (scripted) so với agent vận hành bởi LLM
- Module lập kế hoạch + ghi nhớ (vd: ReAct, BabyAGI, AutoGPT)
- Chạy agent cục bộ hoặc qua API

### 4. Multi-Agent Systems & Advanced Topics

- [AutoGen (Microsoft)](https://github.com/microsoft/autogen) — Điều phối multi-agent với LLM  
- [CAMEL: Communicative Agents Paper](https://arxiv.org/abs/2303.17760) — **Miễn phí**
- [Multi-Agent Simulations (Stanford)](https://crfm.stanford.edu/2023/04/19/ghost-in-the-machine.html) — **Miễn phí**

Bao gồm:
- Agent theo vai trò (vd: planner, executor, verifier)
- Giao tiếp giữa các agent
- Hành vi nổi sinh (emergent behavior) trong môi trường mô phỏng

### 5. Advanced Agentic AI Resources

- [Awesome AI Agents (GitHub)](https://github.com/veritable-tech/awesome-ai-agents) — **Danh sách tổng hợp**
- [AgentBench: Benchmarking Foundation Model Agents](https://arxiv.org/abs/2308.07258) — **Miễn phí**
- [LLM Agents: Open Problems and Opportunities (arXiv)](https://arxiv.org/abs/2307.10169) — **Miễn phí**
- [OpenAgents (GitHub)](https://github.com/openagents/openagents) — **Mã nguồn mở**

Bao gồm:
- Benchmark và đánh giá cho hệ thống agentic
- Framework agentic mã nguồn mở
- Hướng nghiên cứu và thách thức

## Gợi Ý Dự Án & Thực Hành

- Xây dựng Research Agent: nhận câu hỏi và trả về câu trả lời đã tóm tắt
- Tạo luồng multi-agent (vd: PM → Dev → Reviewer → Tester)
- Tích hợp LLM agent với API (vd: Notion, Google Search, máy tính)
- Dùng CrewAI hoặc AutoGen để mô phỏng một đội ngũ startup

## Checkpoint: Trước Khi Qua Phần Tiếp Theo

Bạn sẽ có thể:

- Giải thích và xây dựng agent dựa trên LLM với bộ nhớ, công cụ, và mục tiêu
- Dùng framework như LangChain, CrewAI, và AutoGen
- Thiết kế luồng agent hoặc hệ thống multi-agent của riêng bạn

🔗 Tiếp theo: [RAG →](./03_rag.md)
