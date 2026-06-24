# Multimodal Meme Prediction and Explanation

A multimodal AI framework that combines visual and textual understanding to predict meme sentiment and generate human-readable explanations for model decisions.

---

## Overview

Memes communicate meaning through a combination of images and text, making them challenging for traditional unimodal models. This project addresses that challenge by integrating computer vision and natural language processing techniques to perform sentiment classification on memes while providing interpretable explanations for the predictions.

The framework utilizes CLIP for visual understanding and DistilBERT for textual sentiment analysis. Predictions from both modalities are fused to produce a final sentiment label, and an explanation module generates a rationale describing the decision.

---

## Key Features

- Multimodal meme sentiment classification
- Visual sentiment prediction using CLIP
- Text sentiment prediction using DistilBERT
- Confidence-based fusion of image and text predictions
- Automatic explanation generation
- Explainable AI for transparent decision-making
- End-to-end notebook implementation

---

## Architecture

### Step 1: Text Analysis
The textual content of memes is processed using a pre-trained DistilBERT sentiment classifier.

**Model Used**
- DistilBERT SST-2

**Output**
- Positive sentiment
- Negative sentiment
- Confidence score

---

### Step 2: Image Analysis

The meme image is analyzed using CLIP (Contrastive Language-Image Pretraining).

**Model Used**
- CLIP ViT-B/32

The model compares image features against sentiment-related prompts and predicts the visual sentiment of the meme.

---

### Step 3: Multimodal Fusion

Predictions from both modalities are combined using confidence-based fusion to obtain the final sentiment classification.

This allows the framework to utilize both:
- Visual cues
- Textual context

for more robust meme understanding.

---

### Step 4: Explanation Generation

The framework generates a natural language explanation describing why a particular sentiment was assigned.

The explanation is constructed using:
- Text sentiment
- Image sentiment
- Humor information
- Sarcasm information
- Offensive content annotations

This improves model transparency and interpretability.

---

## Dataset

The project uses the **Memotion Dataset**, which contains:

- Meme images
- Meme captions/text
- Sentiment annotations
- Humor annotations
- Sarcasm annotations
- Offensive content labels

The dataset is preprocessed before inference and analysis.

---

## Project Structure

```text
Multimodal-Meme-Prediction/
│
├── Multi_Model_Meme_Prediction_Explanation.ipynb
├── dataset/
├── outputs/
├── images/
├── requirements.txt
└── README.md
```

---

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- CLIP
- Pandas
- NumPy
- Pillow
- Matplotlib

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/Multimodal-Meme-Prediction.git
cd Multimodal-Meme-Prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Usage

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Multi_Model_Meme_Prediction_Explanation.ipynb
```

Run all cells sequentially to:

1. Load the dataset
2. Perform text sentiment analysis
3. Perform image sentiment analysis
4. Fuse predictions
5. Generate explanations
6. Visualize results

---

## Sample Output

```text
Meme Sentiment: Positive

Text Prediction:
Positive (0.91)

Image Prediction:
Positive (0.84)

Final Prediction:
Positive

Explanation:
The meme conveys a positive sentiment because both the textual content and visual context express a humorous and non-offensive message.
```

---

## Applications

- Social Media Analytics
- Meme Understanding
- Content Moderation
- Sentiment Analysis
- Explainable AI Research
- Multimodal Learning

---

## Future Enhancements

- Fine-tuning CLIP on meme-specific datasets
- Advanced multimodal fusion techniques
- LLM-based explanation generation
- Multi-class emotion recognition
- Attention visualization for explainability
- Real-time meme analysis system

