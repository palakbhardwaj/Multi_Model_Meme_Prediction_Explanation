# 🧠 Multimodal Meme Prediction and Explanation

> **An Explainable Multimodal AI Framework for Meme Sentiment Classification using CLIP and DistilBERT**

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-DeepLearning-red)
![DistilBERT](https://img.shields.io/badge/NLP-DistilBERT-orange)
![CLIP](https://img.shields.io/badge/OpenAI-CLIP-green)

---

## 📖 Overview

Memes have become one of the most influential forms of online communication, combining images and text to express emotions, opinions, humor, and sarcasm. Understanding meme sentiment is challenging because the intended meaning often emerges from the interaction between visual and textual information rather than either modality alone.

This project presents a **Multimodal Meme Prediction and Explanation Framework** that leverages **CLIP (Contrastive Language–Image Pretraining)** for visual understanding and **DistilBERT** for textual sentiment analysis. Predictions from both modalities are combined using a confidence-based fusion strategy to generate the final sentiment label. Additionally, the framework produces **human-readable explanations** that justify each prediction, improving model transparency and interpretability through Explainable AI (XAI).

---

## ✨ Features

- 🖼️ Visual sentiment prediction using **CLIP ViT-B/32**
- 📝 Text sentiment prediction using **DistilBERT**
- 🔀 Confidence-based multimodal fusion
- 🤖 Automatic explanation generation
- 🔍 Explainable AI (XAI)
- 📊 End-to-end implementation in Jupyter Notebook
- ⚡ Lightweight and easy-to-use inference pipeline
- 📈 Human-readable prediction summaries

---

## 📂 Dataset

This project uses the **Memotion Dataset 7K**, a benchmark dataset designed for multimodal meme understanding and sentiment analysis. The dataset contains approximately **7,000 internet memes** annotated with multiple affective and semantic labels, making it suitable for multimodal learning tasks.

### Dataset Contents

- 🖼️ Meme Images
- 📝 Embedded Meme Text
- 😊 Sentiment Labels (Positive, Neutral, Negative)
- 😂 Humor Labels
- 🙃 Sarcasm Labels
- 😡 Offensive Content Labels
- 💥 Motivational Labels

Before inference, the dataset is preprocessed by loading meme images, preparing textual inputs, and organizing annotations for prediction and explanation generation.

### Dataset Source

The dataset is available on Kaggle:

**https://www.kaggle.com/datasets/williamscott701/memotion-dataset-7k**

---

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

The textual content of each meme is processed using a pre-trained **DistilBERT** sentiment classifier to identify the sentiment expressed in the meme.

**Output**

- Positive
- Negative
- Confidence Score

---

### 2️⃣ Image Analysis

The visual content is analyzed using **CLIP (Contrastive Language–Image Pretraining)**.

Instead of directly classifying images, CLIP compares image embeddings with sentiment-related prompts to estimate the visual sentiment.

The visual branch captures:

- Facial expressions
- Objects
- Scene context
- Emotional cues

---

### 3️⃣ Multimodal Fusion

The outputs of the image and text branches are combined using a confidence-based fusion strategy.

The fusion module considers:

- Image prediction confidence
- Text prediction confidence
- Cross-modal agreement

This improves prediction robustness when either modality alone is ambiguous.

---

### 4️⃣ Explanation Generation

To improve interpretability, the framework generates a natural language explanation describing why a particular sentiment was predicted.

The explanation incorporates information from:

- Text sentiment
- Image sentiment
- Humor annotations
- Sarcasm annotations
- Offensive content annotations

**Example**

> *The meme is classified as positive because both the textual content and visual cues express a humorous, non-offensive message, resulting in a high-confidence multimodal prediction.*

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

## 📈 Results

The proposed multimodal framework demonstrates the effectiveness of combining visual and textual information for meme sentiment prediction.

By integrating **CLIP** and **DistilBERT**, the framework produces more robust predictions than relying on a single modality. The explanation module further enhances transparency by providing human-readable justifications for each prediction, making the decision-making process easier to interpret.

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

- 📱 Social Media Analytics
- 😊 Meme Sentiment Analysis
- 🛡️ Content Moderation
- 🤖 Explainable AI (XAI)
- 📊 Opinion Mining
- 🧠 Multimodal Learning
- 📚 AI Research
- 🌐 Social Media Monitoring

---

## 🚀 Future Work

- Fine-tune CLIP on meme-specific datasets
- Explore transformer-based multimodal fusion techniques
- Integrate Large Language Models (LLMs) for richer explanations
- Extend the framework for multi-class emotion recognition
- Incorporate attention and Grad-CAM visualizations
- Develop a Streamlit-based web application
- Build a real-time inference API
- Evaluate the framework on additional multimodal benchmark datasets

---

## ⚠️ Limitations

- Uses pre-trained models without task-specific fine-tuning.
- Explanation generation is template-based rather than generative.
- Performance depends on the quality of extracted meme text.
- Currently supports sentiment prediction and does not model fine-grained emotional states.

---

## 🤝 Contributing

Contributions are welcome!

If you would like to improve this project:

1. Fork the repository.
2. Create a new feature branch.
3. Commit your changes.
4. Submit a Pull Request.

---

## ⭐ Support

If you found this project useful, consider giving it a **⭐ Star** on GitHub!
