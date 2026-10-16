# 🧠 Twitter Sentiment Analysis using Transformers

A transformer-based sentiment analysis project using Hugging Face 🤗 models, fine-tuned on the TweetEval `sentiment` dataset. This project allows interactive inference through a Gradio UI and supports CLI-based predictions and full model retraining.

---

## 📌 About the Project

This project explores the use of state-of-the-art transformer models to classify tweets into three sentiment classes:
- **Negative**
- **Neutral**
- **Positive**

The pipeline includes:
- 📊 Exploratory Data Analysis (EDA)
- 🧼 Preprocessing and Tokenization
- 🏋️ Model Training (PyTorch + Hugging Face)
- 🧪 Validation with Accuracy & F1 Score
- 💾 Model Saving & Loading
- 🎯 Inference via CLI & Gradio UI
- 🚀 Hugging Face Spaces-ready Deployment

The initial model used is [`cardiffnlp/twitter-roberta-base-sentiment-latest`](https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment-latest), but the structure supports experimenting with any Hugging Face classification model.

---

## 🚀 Quick Start

### 🔧 Install Dependencies

```bash
pip install -r requirements.txt
```

The trained weights file (`models/sentiment_roberta/model.safetensors`) is excluded from this repository because of its size. Run the training script below to generate the local model weights before using the app.

## Train the Model

```bash
python src/scripts/train.py
```

## Launch Gradio App

```bash
python app.py
```

## Project Structure

```bash
├── models/                         # Trained model + tokenizer
├── notebooks/                      # EDA and exploration
├── reports/                        # Visualizations and results
├── src/
│   ├── config.py
│   ├── dataset.py
│   ├── features.py
│   ├── modeling/
│   │   ├── train.py
│   │   ├── predict.py
│   │   └── app.py
│   ├── scripts/
│   │   ├── train.py
│   ├── services/
│   │   ├── demo.py
├── app.py
├── requirements.txt
└── README.md
```

## 📈 Results
| Model                                   | Accuracy | F1 Score |
| --------------------------------------- | -------- | -------- |
| `twitter-roberta-base-sentiment-latest` | 74.44%    | 74.51%    |