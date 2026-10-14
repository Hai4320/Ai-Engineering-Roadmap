# Reinforcement Learning (RL) cho AI Engineering

Reinforcement Learning (RL) là một hướng tiếp cận của machine learning, nơi agent học cách ra quyết định bằng cách tương tác với môi trường (environment). Nó vận hành các bước đột phá trong robotics, chơi game (AlphaGo), hệ thống gợi ý, và hệ thống tự hành.

## Mục Tiêu Học Tập

Sau khi hoàn thành module này, bạn sẽ có thể:

- Hiểu nền tảng của RL, bao gồm agent, environment, reward, và policy
- Triển khai phương pháp value-based và policy-based (Q-learning, REINFORCE)
- Làm việc với framework như OpenAI Gym và Stable Baselines
- Áp dụng RL vào bài toán và môi trường thực tế

## Vì Sao Điều Này Quan Trọng

RL là nền tảng để xây dựng AI agent học qua thử và sai (trial and error) — từ xe tự lái đến bot chơi game. Thành thạo RL giúp bạn xây dựng hệ thống tự hành có khả năng thích nghi và tối ưu hành vi trong môi trường biến động.

## Chủ Đề Cốt Lõi & Tài Nguyên

### 1. Fundamentals of Reinforcement Learning

- [Reinforcement Learning Specialization – Coursera (University of Alberta)](https://www.coursera.org/specializations/reinforcement-learning) — **Miễn phí (audit)**
- [Reinforcement Learning Explained – YouTube (Welch Labs)](https://www.youtube.com/watch?v=2pWv7GOvuf0) — **Miễn phí**
- [Reinforcement Learning: An Introduction (Sutton & Barto)](http://incompleteideas.net/book/the-book.html) — **Miễn phí**

Bao gồm:
- Markov Decision Process (MDP)
- Agent, state, action, và reward
- Exploration so với exploitation

### 2. Value-Based Methods

- [Deep Q-Learning with PyTorch – FreeCodeCamp](https://www.youtube.com/watch?v=wc-FxNENg9U) — **Miễn phí**
- [Q-Learning Tutorial – Towards Data Science](https://towardsdatascience.com/simple-reinforcement-learning-q-learning-fcddc4b6fe56) — **Miễn phí**

Bao gồm:
- Q-learning và chiến lược epsilon-greedy
- Phương trình Bellman
- DQN (Deep Q-Networks)

### 3. Policy-Based Methods & Actor-Critic

- [Policy Gradient Methods – OpenAI Spinning Up](https://spinningup.openai.com/en/latest/spinningup/rl_intro.html) — **Miễn phí**
- [Deep Reinforcement Learning with TensorFlow & PyTorch – Udacity](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893) — **Trả phí**

Bao gồm:
- Thuật toán REINFORCE
- Phương pháp actor-critic
- Advantage Actor-Critic (A2C), PPO, DDPG

### 4. Tools & Frameworks

- [OpenAI Gym](https://www.gymlibrary.dev/) — Bộ môi trường RL chuẩn  
- [Stable Baselines3](https://stable-baselines3.readthedocs.io/en/master/) — Triển khai RL cấp cao, dễ dùng  
- [RLlib (Ray)](https://docs.ray.io/en/latest/rllib/index.html) — Framework RL phân tán

Bao gồm:
- Xây dựng môi trường tùy chỉnh
- Train model RL với thuật toán có sẵn
- Logging và đo hiệu năng (benchmark)

### 5. Advanced & Real-World Applications

- [Multi-Agent RL – DeepMind Blog](https://www.deepmind.com/blog/the-emergent-behaviours-of-multi-agent-systems) — **Miễn phí**
- [Self-Driving Cars in Simulation – Carla + RL](https://carlasimulator.org/) — **Miễn phí**
- [AI for Robotics – Georgia Tech (Udacity)](https://www.udacity.com/course/artificial-intelligence-for-robotics--cs373) — **Miễn phí**

Bao gồm:
- Môi trường multi-agent
- RL trong môi trường mô phỏng (CARLA, MuJoCo, Unity)
- Ứng dụng thực tế: robotics, game, tự động hóa

### 6. Advanced RL Resources

- [Awesome Reinforcement Learning (GitHub)](https://github.com/aikorea/awesome-rl) — Danh sách tổng hợp paper, thư viện, và môi trường RL
- [Papers With Code – RL](https://paperswithcode.com/area/reinforcement-learning) — Nghiên cứu RL mới nhất và code triển khai
- [RL Baselines3 Zoo](https://github.com/DLR-RM/rl-baselines3-zoo) — Bộ sưu tập agent RL và benchmark train
- [DeepMind x UCL RL Course](https://www.deepmind.com/learning-resources/-deep-reinforcement-learning-lecture-series-2021) — Bài giảng và tài liệu RL nâng cao
- [OpenAI Spinning Up](https://spinningup.openai.com/en/latest/) — Tài nguyên học tập và triển khai cho RL
- [RL Conference Proceedings (NeurIPS, ICML, ICLR)](https://papers.nips.cc/) — Paper nghiên cứu RL hàng đầu

Bao gồm:
- Thuật toán và benchmark RL SOTA
- Bộ công cụ và thư viện RL mã nguồn mở
- Truy cập dataset và nghiên cứu mới nhất
- Tài nguyên do cộng đồng tổng hợp

## Gợi Ý Thực Hành & Dự Án

- Giải CartPole và MountainCar dùng Q-learning và DQN
- Xây dựng môi trường OpenAI Gym tùy chỉnh (vd: robot kho hàng)
- Train agent chơi video game hoặc mô phỏng bay drone
- Triển khai PPO để dạy robot đi trong môi trường mô phỏng

## Checkpoint: Trước Khi Qua Phần Tiếp Theo

Bạn sẽ có thể:

- Triển khai Q-learning và phương pháp policy gradient
- Dùng thư viện như Gym và Stable Baselines3
- Hiểu thách thức của RL và train agent trong thực tế

🔗 Tiếp theo: [Modern AI →](../../modern-ai/01_llms.md)
