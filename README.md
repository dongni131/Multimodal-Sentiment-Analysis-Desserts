# Multimodal-Sentiment-Analysis-Desserts
This project investigates the intersection of computer vision and natural language processing by analyzing dessert reviews and evaluating how effectively AI-generated captions (from food images) reflect human sentiment.

## 🎯 Project Overview
The goal of this research is to evaluate the potential of AI-generated content in review systems and recommendation engines. We analyze the semantic similarity and sentiment consistency between original user reviews and automated captions generated from images.

## 📊 Dataset
The study is based on a specialized dataset consisting of:
* **49 Dessert Restaurants**: Hand-picked locations with high-quality review data.
* **Multimodal Data**: Paired human-written reviews (from Yelp) and corresponding food images.
* **AI-Generated Text**: Captions produced using the **BLIP-2 (Flan T5-xxl)** model based on food photos.

## 🛠️ Technical Workflow
1. **Preprocessing**: Text normalization including lowercasing, tokenization, and stopword removal.
2. **Feature Engineering**: Text was converted into vector space using **DistilBERT embeddings**.
3. **Image-to-Text**: Leveraging **BLIP-2** to translate visual food cues into descriptive text.
4. **Sentiment Classification**: Comparison of multiple machine learning models (Logistic Regression, Random Forest, MLP, and XGBoost).
5. **Semantic Evaluation**: Using **BERTScore** and **Cosine Similarity** to measure the alignment between human and AI text.

## 📈 Key Results

### Sentiment Classification
We compared model performance for binary sentiment classification (Positive vs. Negative). **Logistic Regression** achieved the best balance of accuracy and fairness.

| Model | Accuracy | Macro F1 |
| :--- | :---: | :---: |
| **Logistic Regression** | **0.86** | **0.80** |
| Random Forest | 0.81 | 0.64 |
| MLP | 0.82 | 0.69 |
| XGBoost | 0.82 | 0.69 |

### Semantic Alignment (BERTScore)
The AI-generated captions showed a high degree of semantic similarity to user reviews:
* **Precision**: 0.812
* **Recall**: 0.779
* **F1 Score**: 0.795

## 🔍 Major Observations
* **High Alignment**: Generated texts and user reviews demonstrate strong semantic consistency.
* **Sentiment Bias**: AI models tend to simplify emotional expression and occasionally show a "positive bias," struggling to capture the nuanced negativity found in some 1-star human reviews.
* **Utility**: The best-performing sentiment classifier can be effectively applied to AI-generated texts, proving their utility in automated systems.

## 🚀 Future Scope
* **Customized Generation**: Integrating specific user preferences to generate personalized review drafts from photos.
* **Emotional Depth**: Enhancing the vividness and emotional layers of AI-generated food descriptions.

## 👥 Contributors
* Yen Jo (Sally) Lee
* Dongni Li
* Chen Hsu
* Pin Tzu Tseng
