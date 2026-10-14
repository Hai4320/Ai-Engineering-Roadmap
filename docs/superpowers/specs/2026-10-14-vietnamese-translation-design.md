# Thiết kế: Dịch toàn bộ repo sang tiếng Việt

## Mục tiêu

Dịch toàn bộ nội dung 18 file `.md` của repo (roadmap học AI mã nguồn mở) từ tiếng Anh sang tiếng Việt, ghi đè trực tiếp lên file gốc.

## Phạm vi

File cần dịch (1655 dòng tổng):

- `README.md`
- `CONTRIBUTING.md`
- `CODE_OF_CONDUCT.md`
- `SECURITY.md`
- `CHANGELOG.md`
- `07_capstone-projects_README.md`
- `01_foundation/01_programming.md`
- `01_foundation/02_math.md`
- `01_foundation/03_machine-learning.md`
- `01_foundation/04_deep-learning.md`
- `02_specializations/computer-vision.md`
- `02_specializations/nlp.md`
- `02_specializations/reinforcement-learning.md`
- `03_modern-Ai/01_llms.md`
- `03_modern-Ai/02_agentic-ai.md`
- `03_modern-Ai/03_rag.md`
- `03_modern-Ai/04_prompt-engineering.md`
- `03_modern-Ai/05_ai-tooling.md`
- `04_capstone-project/capstone-projects.md`

File mới: `GLOSSARY.md` (thư mục gốc).

## Quyết định thiết kế

1. **Ghi đè, không song ngữ.** File gốc tiếng Anh bị thay thế hoàn toàn bằng bản dịch. Bản Anh vẫn truy xuất được qua git history.
2. **Tên riêng (khóa học, sách, video, công cụ) giữ nguyên tiếng Anh**, kèm link gốc không đổi. Chỉ dịch câu mô tả/ghi chú xung quanh.
3. **Thuật ngữ kỹ thuật chuyên ngành (Machine Learning, Deep Learning, Agent, Prompt, Fine-tuning, Embedding, RAG, LLM, Transformer...) giữ nguyên tiếng Anh** trong toàn bộ nội dung — không dịch, không chua tiếng Việt trong ngoặc lặp lại nhiều lần.
4. **File `GLOSSARY.md` mới** tổng hợp các thuật ngữ giữ tiếng Anh ở trên, mỗi thuật ngữ kèm giải thích ngắn bằng tiếng Việt, nhóm theo chủ đề (Foundation, Specializations, Modern AI...). README thêm link trỏ tới file này.
5. **Heading dịch toàn bộ sang tiếng Việt.** Mục lục (TOC) trong README dùng link nội bộ kiểu `#why-this-exists` — các anchor này đổi theo heading mới, TOC phải được cập nhật khớp lại (không giữ tương thích ngược với anchor cũ).
6. **Giữ nguyên không đổi:** cấu trúc thư mục/tên file, code block, bảng Markdown (cấu trúc bảng, chỉ dịch nội dung ô chữ), badge, số liệu, link URL.

## Thực thi

Dịch trực tiếp từng file (đọc → dịch → ghi đè), không cần subagent/song song vì quy mô nhỏ (~1655 dòng, 18 file) — làm tuần tự để giữ thuật ngữ nhất quán xuyên suốt dễ hơn. Tạo `GLOSSARY.md` sau khi dịch xong các file khác để gom đúng danh sách thuật ngữ thực tế xuất hiện.

## Ngoài phạm vi

- Không dịch comment trong code (không có code thực thi trong repo, chỉ doc).
- Không đổi tên file/thư mục sang tiếng Việt.
- Không tạo bản song ngữ hay thư mục `/vi/`.
