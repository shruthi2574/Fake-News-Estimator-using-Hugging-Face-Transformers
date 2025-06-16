# 📰 Fake News Estimator using Hugging Face Transformers

A lightweight and intelligent tool to estimate whether a news article is **fake or real** using **pretrained NLP models** — no datasets, no training required.

This project uses Hugging Face's sentiment analysis model to evaluate the **tone** of user-provided news content. Based on sentiment polarity, it classifies the article as:
- 🟢 REAL (credible tone)
- 🔴 FAKE (sensational/misleading tone)
- ⚠️ UNCERTAIN (neutral or unclear tone)

---

## 📌 Key Features

- 🔍 Accepts custom news headlines as input
- 🤖 Uses `nlptown/bert-base-multilingual-uncased-sentiment` model
- 📊 Predicts fake/real status based on star rating (1–5)
- 💬 No training or dataset required
- ✅ Works directly in Google Colab or local Python

---

## 🧰 Tech Stack

| Tool              | Description                              |
|-------------------|------------------------------------------|
| Python            | Core programming language                |
| Hugging Face      | Access to pretrained NLP models          |
| Transformers      | Inference pipeline (`sentiment-analysis`)|
| Google Colab      | Cloud-based environment (optional)       |

---

## 🚀 Getting Started

### 📍 Prerequisites

- Python 3.x
- Internet connection (to fetch model from Hugging Face)

### 🟢 Run in Google Colab (Recommended)

1. Open [Google Colab](https://colab.research.google.com)
2. Run each code block in separate cells in the notebook:

   ```bash
 # Example format
# 1st Cell
from transformers import pipeline
classifier = pipeline("sentiment-analysis", model="nlptown/bert-base-multilingual-uncased-sentiment")

# 2nd Cell
text = input("Enter a news article: ")
result = classifier(text)[0]
# etc...

   ```

## 💡 Example Output

```
Enter a news article: Scientists confirm COVID-19 vaccine causes brain control

🔍 Sentiment: 1 star | Confidence: 0.96  
📊 Prediction: 🔴 FAKE (low credibility)
Enter a news article: ISRO successfully launches new satellite into orbit

🔍 Sentiment: 5 stars | Confidence: 0.89  
📊 Prediction: 🟢 REAL (credible tone)

```

---

## 📂 Project Structure

```
fack_news-estimator/
├── fack_news_estimator.ipynb
└── README.md
```

---

## 🙋‍♀️ Author

Gugulothu Shruthi 
B.Tech,CSE—Narayanamma Institute of Technology  
✉️ [gugulothushruthi@gmail.com](mailto:gugulothushruthi@gmail.com)

---

