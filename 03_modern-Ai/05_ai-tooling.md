# AI Tooling

AI tooling chỉ các phần mềm, thư viện, và nền tảng giúp tinh gọn việc phát triển, thử nghiệm, deploy, và cộng tác trong workflow AI/ML. Công cụ đúng có thể tăng đáng kể năng suất và hiệu năng model của bạn.

## Mục Tiêu Học Tập

Sau khi hoàn thành module này, bạn sẽ có thể:

- Thiết lập môi trường hiệu quả cho phát triển AI
- Dùng công cụ để theo dõi thử nghiệm (experiment tracking), deploy model, và cộng tác
- Hiểu cách đóng gói và phục vụ (serve) model
- Khám phá công cụ no-code/low-code cho prototyping nhanh

## Vì Sao Điều Này Quan Trọng

AI hiện đại không chỉ là xây dựng model — mà còn là **deploy**, **giám sát**, và **mở rộng quy mô** chúng trong thực tế. Tooling chính là cách để biến ý tưởng hay thành sản phẩm AI thực sự.

## Chủ Đề Cốt Lõi & Tài Nguyên

### 1. Development Environments

- [Jupyter Notebooks](https://jupyter.org/) — Coding tương tác  
- [VS Code + Python AI Extensions](https://code.visualstudio.com/) — IDE phổ biến  
- [Google Colab](https://colab.research.google.com/) — Truy cập **GPU miễn phí**

Bao gồm:
- Môi trường local so với cloud
- Notebook so với IDE
- Tăng tốc phần cứng (GPU/TPU)

### 2. Experiment Tracking & Workflow

- [Weights & Biases (WandB)](https://wandb.ai/) — **Miễn phí cho cá nhân**  
- [MLflow](https://mlflow.org/) — Theo dõi thử nghiệm mã nguồn mở  
- [Neptune.ai](https://neptune.ai/) — **Có gói miễn phí**

Bao gồm:
- Theo dõi metric, loss, và config
- So sánh các lần chạy model và hyperparameter tuning
- Khả năng tái lập (reproducibility) của thử nghiệm

### 3. Model Deployment

- [FastAPI + Uvicorn Tutorial](https://fastapi.tiangolo.com/) — **Miễn phí**  
- [Gradio](https://www.gradio.app/) — Demo ứng dụng no-code cho model ML  
- [Hugging Face Spaces](https://huggingface.co/spaces) — Deploy miễn phí

Bao gồm:
- Phục vụ (serve) model qua API hoặc web app
- Tạo demo tương tác
- Deploy local so với cloud

### 4. Model Packaging & Versioning

- [Docker for AI](https://docs.docker.com/get-started/overview/) — Đóng gói ứng dụng ML vào container  
- [DVC (Data Version Control)](https://dvc.org/) — Theo dõi dataset và model  
- [ONNX](https://onnx.ai/) — Model có thể chuyển đổi, tương thích đa nền tảng

Bao gồm:
- Theo dõi model và dataset xuyên suốt các dự án
- Pipeline ML có thể tái lập
- Chia sẻ và deploy model dễ di chuyển (portable)

### 5. Collaboration & Open Source

- [Git & GitHub](https://github.com/) — Quản lý version và cộng tác  
- [Hugging Face Model Hub](https://huggingface.co/models) — Model pre-trained + chia sẻ  
- [Kaggle](https://www.kaggle.com/) — Cuộc thi + notebook cộng đồng

Bao gồm:
- Cách đóng góp cho công cụ AI mã nguồn mở
- Chia sẻ model, dataset, và dự án với người khác
- Tìm thành phần tái sử dụng cho AI stack của bạn

### 5. Advanced AI Tooling Resources

- [Awesome MLOps (GitHub)](https://github.com/visenger/awesome-mlops) — **Danh sách tổng hợp**
- [AI Tooling Landscape (Papers with Code)](https://paperswithcode.com/area/ai) — **Miễn phí**
- [MLOps Community](https://mlops.community/) — **Cộng đồng**
- [Best Practices for ML Engineering (Google)](https://developers.google.com/machine-learning/guides/rules-of-ml) — **Miễn phí**

Bao gồm:
- MLOps và AI trong production
- Xu hướng tooling và best practice
- Tài nguyên cộng đồng và mã nguồn mở

## Gợi Ý Dự Án & Thực Hành

- Deploy một model thành web app dùng Gradio hoặc FastAPI
- Theo dõi và so sánh thử nghiệm train với WandB hoặc MLflow
- Đóng gói dự án bằng Docker để dùng local + cloud
- Dùng Hugging Face Spaces để host một demo hoạt động

## Checkpoint: Trước Khi Qua Phần Tiếp Theo
Bạn sẽ có thể:

- Thiết lập môi trường phát triển AI
- Theo dõi, đóng gói, và deploy model của bạn
- Dùng công cụ để cộng tác và chia sẻ công việc
- Chọn công cụ phù hợp theo từng giai đoạn dự án AI

🔗 Tiếp theo: [Capstone Projects →](../capstone-project/07_capstone-projects.md)
