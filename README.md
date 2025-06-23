# 🎬 YT-MLOps: Complete End-to-End ML Pipeline for YouTube Video Classification

This project demonstrates a **production-ready MLOps pipeline** for classifying YouTube videos as trending or non-trending using a modular, scalable architecture. It includes data ingestion, preprocessing, training, evaluation, version control, CI/CD, and real-time deployment.

---

## 🚀 Project Highlights

- ✅ Built an end-to-end ML pipeline with **95% model accuracy** for YouTube video classification.
- ✅ Automated data ingestion, model training, and evaluation using **DVC**, **MLflow**, and **GitHub Actions**.
- ✅ Deployed the model using **FastAPI** with **<200ms** response time for real-time predictions.
- ✅ Achieved **70% reduction** in deployment time through automated CI/CD workflows.

---

## 🧠 Tech Stack

| Category        | Tools & Frameworks                         |
|----------------|--------------------------------------------|
| Language        | Python                                     |
| Data Versioning | DVC + AWS S3                               |
| Experiment Tracking | MLflow                                 |
| Model Deployment | FastAPI                                   |
| CI/CD           | GitHub Actions                             |
| Workflow Orchestration | Custom shell scripts & modular code  |


---

## ⚙️ Key Features

- **Data Pipeline:** Automates loading, cleaning, and storing datasets.
- **Model Pipeline:** Trains, evaluates, and tracks model versions with hyperparameter tuning.
- **CI/CD Integration:** Automatically retrains and redeploys models on code/data changes.
- **API Deployment:** FastAPI-based interface for serving predictions.
- **Reproducibility:** Every step is versioned using DVC & tracked with MLflow.

---

## 🔧 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/vikashishere/YT-MLOPS-Complete-ML-Pipeline.git
cd YT-MLOPS-Complete-ML-Pipeline

## Setup virtual Environment 
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt

##  Configure DVC & AWS
Link your AWS S3 bucket for data storage
Initialize DVC and pull data:
dvc pull

## Run the ML Pipeline
dvc repro

## Launch the FastAPI App
cd app
uvicorn main:app --reload
