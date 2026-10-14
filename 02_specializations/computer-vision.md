# Computer Vision cho AI Engineering

Computer Vision (CV) giúp máy móc diễn giải và hiểu thế giới hình ảnh. Đây là động lực đứng sau các công nghệ như nhận diện khuôn mặt, xe tự lái, phân tích ảnh y tế, và nhiều hơn nữa.


## Mục Tiêu Học Tập

Sau khi hoàn thành module này, bạn sẽ có thể:

- Hiểu các khái niệm chính trong xử lý ảnh (image processing) và computer vision
- Xây dựng và train model deep learning (CNN) cho phân loại hình ảnh, object detection, và segmentation
- Làm việc với OpenCV và các framework deep learning cho bài toán CV
- Áp dụng transfer learning dùng các model pre-trained như ResNet và EfficientNet


## Vì Sao Điều Này Quan Trọng

Computer Vision là một chuyên môn cốt lõi trong AI. Từ y tế đến xe tự lái, nó giúp AI "nhìn" và hiểu thế giới. Học CV trang bị cho bạn khả năng xây dựng model tương tác với môi trường hình ảnh.


## Chủ Đề Cốt Lõi & Tài Nguyên

### 1. Introduction to Computer Vision

- [Python & OpenCV for Computer Vision – FreeCodeCamp](https://www.youtube.com/watch?v=oXlwWbU8l2o) — **Miễn phí**
- [Computer Vision Basics – Coursera (UMich)](https://www.coursera.org/learn/computer-vision-basics) — **Miễn phí (audit)**

Bao gồm:
- Ảnh số (digital images) và pixel
- Không gian màu (RGB, HSV, Grayscale)
- Bộ lọc ảnh, biến đổi ảnh, edge detection

### 2. Image Classification với CNN

- [CS231n: Convolutional Neural Networks – Stanford](http://cs231n.stanford.edu/) — **Miễn phí**
- [Intro to Deep Learning for Computer Vision – Coursera (DeepLearning.AI)](https://www.coursera.org/learn/convolutional-neural-networks) — **Miễn phí (audit)**
- [Fast.ai Part 1](https://course.fast.ai/) — **Miễn phí**

Bao gồm:
- CNN (lớp Conv, Pooling, Fully Connected)
- Kiến trúc: LeNet, AlexNet, ResNet
- Transfer learning và fine-tuning

### 3. Object Detection

- [Object Detection with YOLOv5 – Roboflow Guide](https://blog.roboflow.com/how-to-train-yolov5-on-a-custom-dataset/) — **Miễn phí**
- [TensorFlow Object Detection API Tutorial](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/) — **Miễn phí**

Bao gồm:
- Sliding window so với region proposal so với YOLO
- Anchor box, confidence score, IOU
- Object detection thời gian thực và ứng dụng

### 4. Image Segmentation

- [Image Segmentation – Coursera (DeepLearning.AI)](https://www.coursera.org/learn/convolutional-neural-networks) — **Miễn phí (audit)**
- [U-Net: Convolutional Networks for Biomedical Image Segmentation (Paper)](https://arxiv.org/abs/1505.04597) — **Miễn phí**

Bao gồm:
- Semantic segmentation so với instance segmentation
- Kiến trúc U-Net và Mask R-CNN
- Ứng dụng trong y tế, ảnh vệ tinh

### 5. Advanced & Real-World CV Projects

- [Build a Face Recognition System – PyImageSearch](https://pyimagesearch.com/2021/04/26/opencv-face-recognition/) — **Trả phí**
- [Autonomous Driving with Computer Vision – Udacity](https://www.udacity.com/course/introduction-to-self-driving-cars--ud513) — **Miễn phí (audit)**

Bao gồm:
- Phát hiện và nhận diện khuôn mặt
- Phát hiện làn đường và phân loại biển báo giao thông
- An toàn và triển khai trên edge device

### 6. Advanced Computer Vision Resources

- [Awesome Computer Vision (GitHub)](https://github.com/jbhuang0604/awesome-computer-vision) — Danh sách tổng hợp paper, dataset, và thư viện
- [Papers With Code – Computer Vision](https://paperswithcode.com/area/computer-vision) — Nghiên cứu mới nhất và code triển khai
- [MMDetection (OpenMMLab)](https://github.com/open-mmlab/mmdetection) — Bộ công cụ object detection mã nguồn mở mạnh mẽ
- [Albumentations](https://albumentations.ai/) — Thư viện augmentation ảnh nhanh
- [CVPR Conference Proceedings](https://openaccess.thecvf.com/CVPR2023?day=all) — Paper nghiên cứu hàng đầu
- [Roboflow Universe](https://universe.roboflow.com/) — Dataset công khai và model pre-trained cho CV

Bao gồm:
- Model và benchmark SOTA
- Data augmentation và tiền xử lý
- Bộ công cụ mã nguồn mở cho detection, segmentation, và nhiều hơn
- Truy cập dataset và nghiên cứu mới nhất

## Gợi Ý Thực Hành & Dự Án

- Xây dựng bộ phân loại hình ảnh cho loài động vật hoặc thực vật
- Phát hiện khuôn mặt hoặc vật thể thời gian thực dùng OpenCV + YOLO
- Phân đoạn (segment) ảnh y tế (phổi, khối u) với U-Net
- Tạo AI phân loại ngôn ngữ ký hiệu từ cử chỉ tay

## Checkpoint: Trước Khi Qua Phần Tiếp Theo

Bạn sẽ có thể:

- Dùng CNN cho classification, detection, và segmentation
- Áp dụng OpenCV cho bài toán xử lý ảnh
- Train và deploy model cho ứng dụng vision thực tế

🔗 Tiếp theo: [Reinforcement Learning →](./reinforcement-learning.md)
