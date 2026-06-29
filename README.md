# 🧠 Multimodal Meme Prediction and Explanation

> **An Explainable Multimodal AI Framework for Meme Sentiment Classification using CLIP and DistilBERT**

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-DeepLearning-red)
![DistilBERT](https://img.shields.io/badge/NLP-DistilBERT-orange)
![CLIP](https://img.shields.io/badge/OpenAI-CLIP-green)

---

## 📖 Overview

Memes are a popular form of online communication that combine visual and textual information to convey emotions, opinions, and humor. Since the meaning of a meme often depends on the interaction between its image and text, traditional unimodal models struggle to accurately interpret their sentiment.

This project presents a **multimodal framework** for meme sentiment prediction by integrating **CLIP** for visual understanding and **DistilBERT** for textual sentiment analysis. The predictions from both modalities are combined using a confidence-based fusion strategy to produce the final sentiment label. Additionally, the framework generates human-readable explanations that improve transparency and interpretability of the model's decisions.

---

## ✨ Features

- 🖼️ Image sentiment prediction using **CLIP ViT-B/32**
- 📝 Text sentiment prediction using **DistilBERT**
- 🔀 Confidence-based multimodal fusion
- 🤖 Automatic explanation generation
- 🔍 Explainable AI (XAI)
- 📊 End-to-end implementation in Jupyter Notebook
- ⚡ Simple inference pipeline

---
## 📂 Dataset

This project uses the **Memotion Dataset 7K**, a benchmark dataset developed for multimodal meme analysis and sentiment understanding. The dataset contains approximately **7,000 internet memes** annotated with multiple affective and semantic labels, making it suitable for multimodal learning tasks.

### Dataset Contents

* 🖼️ Meme images
* 📝 Embedded meme text
* 😊 Sentiment labels (Positive, Neutral, Negative)
* 😂 Humor labels
* 🙃 Sarcasm labels
* 😡 Offensive content labels
* 💥 Motivational labels

The dataset is preprocessed before inference by loading meme images, preparing textual inputs, and organizing annotations for sentiment prediction and explanation generation.

### Dataset Source

The dataset can be downloaded from Kaggle:

🔗 **https://www.kaggle.com/datasets/williamscott701/memotion-dataset-7k**


## 🏗️ Framework Pipeline

```text
                    Input Meme
                        │
        ┌───────────────┴───────────────┐
        │                               │
        ▼                               ▼
   Meme Image                     Meme Text
        │                               │
        ▼                               ▼
  CLIP ViT-B/32                  DistilBERT
        │                               │
        ▼                               ▼
 Image Prediction             Text Prediction
        │                               │
        └───────────────┬───────────────┘
                        ▼
          Confidence-Based Fusion
                        │
                        ▼
         Final Sentiment Prediction
                        │
                        ▼
      Natural Language Explanation
```

---

## 🧠 Methodology

### 1️⃣ Text Analysis

The textual content of the meme is processed using a pre-trained **DistilBERT** sentiment classifier to identify its sentiment and confidence score.

**Output**

- Positive
- Negative
- Confidence Score

---

### 2️⃣ Image Analysis

The image is analyzed using **CLIP (Contrastive Language–Image Pretraining)**.

Instead of directly classifying images, CLIP compares image embeddings with sentiment-related text prompts to determine the most likely visual sentiment.

The visual branch captures:

- Facial expressions
- Objects
- Scene context
- Visual emotions

---

### 3️⃣ Multimodal Fusion

The predictions from both branches are combined using a confidence-based fusion strategy.

The fusion process considers:

- Text prediction confidence
- Image prediction confidence
- Agreement between both modalities

This produces a more reliable final prediction than using either modality independently.

---

### 4️⃣ Explanation Generation

To improve interpretability, the framework generates a natural language explanation describing why a particular sentiment was assigned.

The explanation incorporates information from:

- Text sentiment
- Image sentiment
- Humor annotations
- Sarcasm annotations
- Offensive content annotations

**Example**

> *The meme is classified as positive because both the textual content and visual cues express a humorous, non-offensive message, leading to a high-confidence multimodal prediction.*

---

## 📂 Dataset

The project uses the **Memotion Dataset**, a benchmark dataset designed for multimodal meme understanding.

The dataset contains:

- Meme Images
- Meme Text
- Sentiment Labels
- Humor Labels
- Sarcasm Labels
- Offensive Content Labels

Before inference, the dataset undergoes preprocessing, including image loading, text normalization, and annotation preparation.

---

## 📁 Project Structure

```text
Multimodal-Meme-Prediction/
│
├── Multi_Model_Meme_Prediction_Explanation.ipynb
├── dataset/
├── outputs/
├── requirements.txt
└── README.md
```

---

## 🛠️ Technologies Used

- Python
- PyTorch
- OpenAI CLIP
- DistilBERT
- Pandas
- NumPy
- Pillow
- Matplotlib
- Jupyter Notebook

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/Multimodal-Meme-Prediction.git
```

Navigate to the project directory:

```bash
cd Multimodal-Meme-Prediction
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebook:

```text
Multi_Model_Meme_Prediction_Explanation.ipynb
```

Run all cells sequentially to:

1. Load the dataset
2. Perform text sentiment analysis
3. Perform image sentiment analysis
4. Fuse image and text predictions
5. Generate explanations
6. Visualize the results

---

## 📊 Sample Output

```text
Meme Sentiment: Positive

Text Prediction
---------------
Positive (0.91)

Image Prediction
----------------
Positive (0.84)

Final Prediction
----------------
Positive

Explanation
-----------
The meme conveys a positive sentiment because both the
textual message and visual content express a humorous
and non-offensive context. The agreement between both
modalities results in a high-confidence prediction.
```

---

## 🎯 Applications

- Social Media Analytics
- Meme Sentiment Analysis
- Explainable AI (XAI)
- Content Moderation
- Opinion Mining
- Multimodal Learning
- AI Research

---

## 🚀 Future Work

- Fine-tune CLIP on meme-specific datasets
- Explore transformer-based multimodal fusion techniques
- Integrate Large Language Models (LLMs) for richer explanations
- Extend the framework for multi-class emotion recognition
- Incorporate attention visualization methods
- Develop a web-based interface for real-time inference

---

## ⚠️ Limitations

- Uses pre-trained models without task-specific fine-tuning.
- Explanation generation is template-based.
- Performance depends on the quality of meme text.
- Currently supports binary sentiment prediction.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a new feature branch.
3. Commit your changes.
4. Open a Pull Request.

---

## ⭐ Support

If you found this project useful, consider giving it a **⭐ Star** on GitHub!
