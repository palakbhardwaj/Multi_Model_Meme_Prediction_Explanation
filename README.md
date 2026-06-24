# Multimodal Meme Prediction and Explanation

## Overview

This project presents a Multimodal Meme Prediction and Explanation framework that combines image understanding and text sentiment analysis to classify memes and generate interpretable explanations. The system leverages state-of-the-art vision-language models and natural language processing techniques to improve meme understanding and explain AI predictions.

## Features

- Multimodal meme sentiment classification
- Image and text-based prediction
- Explainable AI through rationale generation
- Semantic similarity evaluation
- Natural Language Inference (NLI) based explanation validation
- Confidence-based multimodal fusion

## Models Used

| Component | Model |
|------------|--------|
| Image Understanding | CLIP ViT-B/32 |
| Text Sentiment Analysis | DistilBERT SST-2 |
| Semantic Similarity | Sentence-BERT (all-MiniLM-L6-v2) |
| Explanation Verification | BART Large MNLI |

## Methodology

### 1. Text Analysis
The textual content extracted from memes is analyzed using a fine-tuned DistilBERT sentiment classifier to determine positive or negative sentiment.

### 2. Image Analysis
Visual features are extracted using CLIP, which compares meme images against sentiment-related prompts to estimate image sentiment.

### 3. Multimodal Fusion
Predictions from text and image modalities are combined using confidence-weighted fusion to obtain a final sentiment prediction.

### 4. Explanation Generation
The framework generates natural language explanations based on:
- Predicted sentiment
- Humor annotations
- Sarcasm annotations
- Offensive content labels
- Visual context

### 5. Explanation Evaluation
Generated explanations are evaluated using:
- Semantic Similarity (Sentence-BERT)
- Natural Language Inference (BART-MNLI)

## Dataset

The project utilizes the Memotion Dataset containing:
- Meme images
- Meme text
- Sentiment labels
- Humor labels
- Sarcasm labels
- Offensive content annotations

## Project Structure
