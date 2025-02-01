# Conversational AI Model Ranking using TOPSIS

This project uses the **TOPSIS** (Technique for Order of Preference by Similarity to Ideal Solution) method to rank pre-trained conversational AI models based on their performance in a simple conversational dataset. We evaluate three lightweight pre-trained models and rank them using **cosine similarity**, **inference speed**, and **model size**.

### Table of Contents
1. [Description](#description)
2. [Models Evaluated](#models-evaluated)
3. [Evaluation Metrics](#evaluation-metrics)
4. [Methodology](#methodology)
5. [Results](#results)
6. [Flowchart](#flowchart)
7. [Screenshots](#screenshots)

## Description

In this project, we evaluate three pre-trained conversational models:
- **DistilGPT-2**
- **Facebook BlenderBot-90M** 
- **Microsoft DialoGPT-small** 

We use a simple conversational dataset and apply the **TOPSIS** method to rank these models based on:
1. **Mean Similarity**: Cosine similarity of embeddings produced by the model during conversations.
2. **Inference Speed**: Simulated inference speed (for the sake of comparison).
3. **Model Size**: Simulated model size (for storage efficiency).

## Models Evaluated

The three pre-trained models used in this evaluation are:

1. **DistilGPT-2**: A smaller version of GPT-2, providing a lightweight option with relatively good performance.
2. **Facebook BlenderBot-90M**: A conversational agent designed for multi-turn conversations.
3. **Microsoft DialoGPT-small**: A smaller version of DialoGPT trained for conversations.

## Evaluation Metrics

We used the following evaluation metrics to rank the models:

- **Mean Similarity**: The cosine similarity between model-generated embeddings for each conversation.
- **Inference Speed**: A simulated inference speed metric.
- **Model Size**: A simulated model size in terms of storage required.

## Methodology

1. **Cosine Similarity**: We calculate cosine similarity between the embeddings produced by each model for a set of predefined conversations.
2. **TOPSIS Ranking**: We apply the TOPSIS method to rank the models based on their cosine similarity, inference speed, and model size.
3. **Ranking**: The model with the highest TOPSIS score is considered the best, followed by the rest in descending order.

## Results

The ranking of models based on the **TOPSIS score** is displayed below in a table format:

| Rank | Model                           | Mean Similarity | Inference Speed | Model Size | TOPSIS Score |
|------|---------------------------------|-----------------|-----------------|------------|--------------|
| 2    | **DistilGPT-2**                 | 0.999768        | 0.976021        | 0.885133   | 0.851193     |
| 3    | **Facebook/BlenderBot-90M**     | 0.518769        | 0.906980        | 0.976280   | 0.148761     |
| 1    | **Microsoft/DialoGPT-small**    | 0.999947        | 0.909961        | 0.939018   | 0.872414     |

> Note: Values for inference speed and model size are simulated for comparison purposes.

### Screenshot of the Results Table
![WhatsApp Image 2025-02-01 at 14 59 44_8db4dc45](https://github.com/user-attachments/assets/ae2a3571-ad44-4e7b-9ab9-12e02e70cfac)


### Screenshot of the Results Graph
![WhatsApp Image 2025-02-01 at 14 59 32_b9e36eb2](https://github.com/user-attachments/assets/6af8a25e-d27e-4733-ba9f-080353f18e49)

## Flowchart

Below is a flowchart that illustrates the methodology used in this project:

```plaintext
+-------------------+
| Pre-trained Models|
+-------------------+
         |
         v
+-------------------+
| Evaluate Models   |
| (Cosine Similarity)|
+-------------------+
         |
         v
+-------------------+
| Normalize Scores  |
+-------------------+
         |
         v
+-------------------+
| Calculate Ideal   |
| Best & Worst      |
+-------------------+
         |
         v
+-------------------+
| Compute Distances |
| (from Ideal Best &|
| Worst)            |
+-------------------+
         |
         v
+-------------------+
| Calculate TOPSIS  |
| Scores            |
+-------------------+
         |
         v
+-------------------+
| Rank Models       |
+-------------------+
