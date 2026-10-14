# Thuật Ngữ

Các thuật ngữ kỹ thuật dưới đây được giữ nguyên tiếng Anh xuyên suốt repo (đúng với cách cộng đồng AI Việt Nam thường dùng). Danh sách này giải thích ngắn gọn từng thuật ngữ bằng tiếng Việt, nhóm theo chủ đề.

## Foundation (01_foundation)

- **Machine Learning (ML)** — Máy học: nhánh AI dạy máy tính học từ dữ liệu thay vì lập trình luật cứng.
- **Deep Learning** — Học sâu: nhánh con của Machine Learning dùng neural network nhiều lớp.
- **OOP (Object-Oriented Programming)** — Lập trình hướng đối tượng: tổ chức code quanh các class và object.
- **Linear Algebra** — Đại số tuyến tính: nền tảng toán cho vector, ma trận, vận hành trong mọi model AI.
- **Supervised Learning** — Học có giám sát: train model bằng dữ liệu đã có nhãn (label).
- **Unsupervised Learning** — Học không giám sát: tìm cấu trúc trong dữ liệu không có nhãn.
- **Overfitting / Underfitting** — Model học quá khớp (mất khả năng tổng quát) / học chưa đủ (chưa nắm được quy luật).
- **CNN (Convolutional Neural Network)** — Kiến trúc neural network chuyên xử lý ảnh, dùng phép convolution.
- **RNN (Recurrent Neural Network)** — Kiến trúc neural network xử lý dữ liệu tuần tự (văn bản, chuỗi thời gian).
- **LSTM (Long Short-Term Memory)** — Biến thể của RNN, xử lý tốt phụ thuộc dài hạn trong chuỗi dữ liệu.
- **GAN (Generative Adversarial Network)** — Hai mạng (generator/discriminator) thi đấu với nhau để sinh dữ liệu giả.
- **VAE (Variational Autoencoder)** — Kiến trúc sinh dữ liệu dựa trên việc học phân phối xác suất tiềm ẩn.

## Specializations (02_specializations)

- **Computer Vision (CV)** — Thị giác máy tính: giúp máy "nhìn" và hiểu ảnh/video.
- **NLP (Natural Language Processing)** — Xử lý ngôn ngữ tự nhiên: giúp máy hiểu và sinh ngôn ngữ con người.
- **RL (Reinforcement Learning)** — Học tăng cường: agent học qua thử-sai dựa trên reward từ môi trường.
- **Object Detection** — Phát hiện vật thể: xác định vị trí và loại vật thể trong ảnh.
- **Image Segmentation** — Phân đoạn ảnh: gán nhãn từng pixel theo vùng/đối tượng.
- **Tokenization** — Tách văn bản thành các đơn vị nhỏ (token) để xử lý.
- **NER (Named Entity Recognition)** — Nhận diện thực thể có tên (người, địa điểm, ngày tháng...) trong văn bản.
- **Transformer** — Kiến trúc neural network dùng cơ chế attention, nền tảng của hầu hết LLM hiện nay.
- **Q-learning / DQN (Deep Q-Network)** — Thuật toán Reinforcement Learning dựa trên ước lượng giá trị hành động (value-based).
- **Policy Gradient / Actor-Critic (PPO, A2C, DDPG)** — Nhóm thuật toán RL học trực tiếp policy thay vì value.
- **MDP (Markov Decision Process)** — Khung toán học mô tả bài toán RL: state, action, reward.

## Modern AI (03_modern-Ai)

- **LLM (Large Language Model)** — Model ngôn ngữ lớn (GPT-4, Claude, LLaMA...), nền tảng của AI hiện đại.
- **Agent / Agentic AI** — Hệ thống AI hoạt động tự hành: tự lập kế hoạch, dùng công cụ, ra quyết định nhiều bước.
- **RAG (Retrieval-Augmented Generation)** — Kỹ thuật kết hợp LLM với truy xuất dữ liệu ngoài để trả lời chính xác, cập nhật hơn.
- **Prompt / Prompt Engineering** — Câu lệnh đầu vào cho LLM / nghệ thuật thiết kế prompt hiệu quả.
- **Fine-tuning** — Huấn luyện tiếp một model đã pre-trained trên dữ liệu chuyên biệt để chuyên hóa nó.
- **Embedding** — Biểu diễn văn bản/dữ liệu dưới dạng vector số để máy so sánh được ngữ nghĩa.
- **Vector Database** — Cơ sở dữ liệu lưu và tìm kiếm embedding theo độ tương đồng (vd: FAISS, ChromaDB).
- **Zero-shot / Few-shot** — Cho model làm bài toán không có ví dụ mẫu / chỉ với vài ví dụ mẫu trong prompt.
- **Chain-of-Thought** — Kỹ thuật prompt yêu cầu model trình bày từng bước suy luận trước khi trả lời.
- **Function Calling / Tool Use** — Khả năng LLM gọi công cụ/API bên ngoài để thực hiện hành động.

## Capstone & Tooling

- **MLOps** — Thực hành vận hành, triển khai, và giám sát model ML trong production.
- **CI/CD** — Continuous Integration/Continuous Deployment: tự động hóa kiểm thử và triển khai code.
- **Docker** — Công cụ đóng gói ứng dụng thành container để chạy nhất quán ở mọi môi trường.
