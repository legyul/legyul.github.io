---
layout: page
title: AutoML Web App
date: 2025-03-27 17:39:00
description: AutoML Web App
category: work
---

# 🤖 AutoML Web App with Clustering, Classification, and AI Q&A (RAG + LoRA)
## 🔍 Overview  
  
This project is a full-stack **AutoML web application** designed to make machine learning easier and more accessible for everyone - even for those without coding experience.  
  
▶️ **Watch Demo**  
{% include video.liquid path="assets/video/ML_web_app.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}  
  
This video shows:  
- Dataset upload  
- Clustering & classification execution  
- Report and result download  
  
Users can:  
- Upload their own dataset  
- Select between **Clustering** or **Classification**  
- Automatically train models  
- Ask questions about the data using **AI-powered Q&A** with **RAG (Retrieval-Augmented Generation)** and **LoRA-tuned LLM**  
  
The entire system runs on **Dockerized Flask** backend and is deployed using **AWS EC2 and S3**.  
  

---
  
## 📌 Introduction
  
This project is a full-featured AutoML web application designed to enable users to interact with machine learning workflows—without writing a single line of code.  
  
Through an intuitive interface, users can upload their own datasets and choose between clustering or classification tasks. The system automatically processes the data, trains appropriate models, and generates visualizations, downloadable reports, and structured results.  
  
What sets this platform apart is its integration of a **natural language question-and-answer system**, powered by **LLM fine-tuning (LoRA)** and **Retrieval-Augmented Generation (RAG)**. Users can ask questions about their uploaded data and model results, and receive contextual, AI-generated answers.  
  
This application was built with a strong focus on:  
- **Accessibility** (no-code interaction)  
- **Automation** (AutoML workflows and reporting)  
- **Scalability** (cloud deployment on AWS using Docker)  
- **Extendability** (custom ML models and integrated LLMs)  

It demonstrates real-world implementation of a no-code AI platform with end-to-end capabilities, from data upload to intelligent insight delivery.  
  
---
  
## 📦 Architecture

Here's a simplified view of the system flow:  
  
User → Web UI (Flask) → Model Selector → ML Training/Prediction  
          ↓                     ↓  
      AI Q&A (RAG)        S3: Model, Logs, Results  
          ↓  
   TinyLlama + LoRA  
  
<div class="row mt-3">
	<div class="col-sm mt-3 mt-md-0">
	{% include figure.liquid loading="eager" path="/assets/img/automl_detailed_architecture.png" class="img-fluid rounded z-depth-1" %}
	</div>
</div>
  
---
  
## 🎯 Goals
- Build a user-friendly AI platform with **no-code interaction**  
- Support both unsupervised and supervised ML tasks  
- Integrate a **natural language interface** so users can ask questions about their data and results  
- Deploy a scalable version using **cloud infrastructure (AWS)**  
  
---  
  
## ⚙️ Features
  
### 📊 Clustering (Unsupervised Learning)
- Algorithms: K-Means, Agglomerative Clustering  
- Automatic cluster number detection (Elbow & Silhouette)  
- Dimensionality reduction using PCA  
- Generates visualizations and PDF reports  
- Allows CSV export of cluster results  
  
### 🧠 Classification (Supervised Learning)
- Model choices:  
    - Naive Bayes  
    - Decision Tree  
    - Random Forest  
    - Logistic Regression (auto hyperparameter tuning)  
- Users can choose a specific model or let the system auto-select the best one based on **ROC-AUC**  
- Trained models can be **downloaded**  
- **Log files** are viewable and downloadable  
- A **PDF report** is auto-generated  
- Predictions are not directly shown in CSV - instead, users can ask the AI via the Q&A system  
  
### 💬 AI-Powered Q&A (RAG + LoRA)
- Users can interact with the results using natural language  
- Built using **TinyLlama** fine-tuned via **LoRA (Low-Rank Adaptation)**  
- Uses **ChromaDB** for vector storage and fast retrieval  
- Allows users to ask about patterns, predictions, and insights based on their own uploaded dataset  
  
---
  
## 🧱 Tech Stack
- **Frontend**: HTML, JavaScript  
- **Backend**: Flask, PyTorch, LangChain, Hugging Face, Transformers  
- **ML Models**: Custom implementation (no scikit-learn used for classification models)  
- **LLM**: TinyLlama + LoRA (fine-tuned on EC2)  
- **Database**: ChromaDB (local vector store)  
- **Deployment**: Docker, AWS EC2, S3  
- **CI/CD**: Crontab-based GitHub auto-pull every hour  
  
---  
  
## 🌐 Live Demo & Source Code
  
- 🚀 **Live Web App**: [https://automlplatform.tech/](https://automlplatform.tech/)  
- 📦 **GitHub Repository**: [https://github.com/namdarine/ML_web_app](https://github.com/namdarine/ML_web_app) (MIT Licensed)
  
---
  
## 🚀 Outcome

This project demonstrates the development of a production-ready, full-stack AutoML web platform.  
Key accomplishments include:

- ✅ Designed and implemented a user-facing application supporting both **clustering** and **classification** workflows with automated model training, selection, and reporting.  
- ✅ Developed **custom machine learning models** (Naive Bayes, Decision Tree, Random Forest, Logistic Regression) without relying on external libraries such as scikit-learn.  
- ✅ Integrated a scalable, cloud-based pipeline using **AWS EC2 and S3** to manage user data, model storage, and logs.  
- ✅ Deployed the application in a containerized environment using **Docker**, with automated updates via **crontab-based CI/CD**.  
- ✅ Extended functionality with an **LLM-based Q&A system**, built using **RAG (Retrieval-Augmented Generation)** and **LoRA fine-tuning** on **TinyLlama**, enabling interactive insight retrieval from uploaded datasets.  
- ✅ Delivered task-specific result pages:  
    - Classification includes downloadable reports, logs, and AI-assisted insights  
    - Clustering provides downloadable visual reports and cluster outputs  
- ✅ Emphasized **accessibility and usability**, allowing non-technical users to leverage machine learning and LLM technologies without writing code.  
  
This project reflects practical experience in end-to-end AI system design, custom model implementation, cloud deployment, and LLM integration. It serves as a foundation for future work in no-code AI tools and AI automation platforms.  
  
---
  
## 🌍 Vision & Future Direction
This project is more than a technical implementation - it's a step toward democratizing AI.  
  
My philosopy is simple:  
> **"AI should be for everyone."**  
  
Instead of building AI that only experts can use, I aim to create tools that allow anyone to design, deploy, and interact with AI - without writing code.  
  
This philosophy is reflected in:  
- The no-code design of this platform  
- The emphasis on explainability and interaction (via AI Q&A)  
- The long-term goal to establish **AI citizenship as a right**, not a privilege  
  
### 🔭 Future Plan
  
| Phase | Goal | Approach |
|-------|------|----------|
| 1 | Internalize AI deployment skills | Built with LoRA, RAG, Lambda, Docker, EC2 |
| 2 | Launch a no-code AI web platform | Fully automated model training and inference pipeline |
| 3 | Brand and publish the philosophy | Mini whitepapers, blog series on Medium, strengthen **namdarine** |
| 4 | Expand into a service or open-source platform | Build a SaaS ecosystem or accessible education tool |
| 5 | Design social-AI structures | Bridge ethics, governance, and everyday AI use in society |
  
This is not just a project - it's a foundation for the world I want to build.  
  
---
  
## 🧗 Key Challenges & Solutions
  
- **Deploying LLMs under resource constraints**  
    → Initially attempted using AWS Lambda, but due to model size limitations, switched to EC2 with the local caching strategy for model loading.  
  
- **Designing the classification flow with only custom ML models**  
    → Chose to implement Naive Bayes, Decision Tree, Random Forest, and Logistic Regression from scratch as part of a self-study effort.  
  
- **Handling latency in AI Q&A system**  
    → Implemented system-level feedback and result caching to reduce user-facing delays and prevent timeouts (504 errors).  
  
---
  
## 🎓 What I Learned

While I learned core machine learning algorithms through university classes, the rest of this project-from infrastructure to LLM integration-was fully self-taught. Key areas include:  
  
- End-to-end web app development using Flask and Docker  
- Managing AWS services (EC2, S3) for cloud-based ML workflows  
- Integrating LLMs (TinyLlama) with RAG and LoRA fine-tuning  
- Custom ML model implementation and evaluation pipelines  
- Building a minimal CI/CD system using crontab  
- Enhancing UX for interactive AI systems