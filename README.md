# News-Article-Classification

**📰 News Article Classification Project with Web Crawling and Fine-Tuned LLM (Qwen2.5)**

---

## 📘 Project Description

This project implements a fully automated **news classification pipeline** — from data crawling and text extraction to machine learning model training and evaluation.
It automatically collects articles from multiple online sources, cleans the data, labels it, and fine-tunes a **Qwen2.5-0.5B transformer** model to classify news articles by category (e.g., sports, politics, technology, etc.).

---

## ⚙️ Key Components

- ### 🔍 Web Crawling:

  - Developed a **custom crawler** using the universalapi.thordata.com API to scrape article HTML content from given URLs.

  - Extracted **clean text** content from **HTML**  using BeautifulSoup.

  - Collected up to 100 articles per category dynamically with pagination.

- ### 🧹 Data Cleaning & Preprocessing:

  - Cleaned HTML tags, whitespace, and unwanted characters using regex and BeautifulSoup.

  - Encoded categorical labels (news categories) using LabelEncoder.

  - Saved and reloaded the dataset as a structured CSV (articles.csv).

- ### 🤖 Model Training (Qwen2.5-0.5B):

  - Utilized the **Hugging Face transformers** and datasets libraries.

  - **Tokenized** articles with automatic padding and truncation.

  - **Fine-tuned** the **Qwen2.5-0.5B** model for text classification with bfloat16 precision, gradient accumulation, and layer freezing for optimization.

  - Used the Trainer API for efficient training, validation, and evaluation.

- ### 📈 Evaluation:

  - Measured accuracy and generated classification reports on both train and test splits.

  - Achieved robust results with proper label mapping and metric computation.

- ### 🚀 Deployment-Ready Inference:

  - Exported the fine-tuned model and tokenizer for easy reuse.

  - Built an inference pipeline using transformers.pipeline for real-time text classification.

 ---

## 🧩 Tech Stack

- Python
- Hugging Face Transformers
- BeautifulSoup
- Pandas / Scikit-learn
- HTTP Client API
- Evaluate Library
