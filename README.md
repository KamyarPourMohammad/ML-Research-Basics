# Learning-by-Rewriting
### December 2025

---

## 1 Introduction

I began my research by searching for top papers on Google Scholar and reading them to build my foundational knowledge. After familiarizing myself with the field, I attempted to rewrite one of the papers to enhance my understanding and become more comfortable with the subject matter.

In this report, I have documented my research activities in the area of object segmentation in medical images, with a particular focus on chest radiography. My work explores modern segmentation approaches, explainable AI techniques, and large-scale medical datasets.

The ultimate goal of my project was to develop an effective segmentation model for radiological chest images using **limited annotated data**.

---

## 2 Background Study For Getting Started

First, I tried to gain a foundational overview of the key elements required for conducting academic research in a structured format. My focus was on understanding the academic landscape, which includes:

- Types of Scientific Papers
- Major Scientific Publishers
- Reference Structure in Scientific Papers

---

## 3 Selecting the Main Paper

In the second phase, after reviewing the academic landscape, I selected my main paper. The title of my chosen paper is:

**"Explanations of Classifiers Enhance Medical Image Segmentation via End-to-End Pre-training."**

This paper proposes a novel method for generating pseudo-segmentation labels from classification explanations and then using them for segmentation pre-training. The methodology is outlined below:

### Method Overview

1. Train classifiers on the CheXpert dataset
2. Generate pseudo masks using Explainable AI (XAI) techniques
3. Pre-train a segmentation model using these pseudo masks
4. Fine-tune the model on a small ground-truth dataset

---

## 4 Project Goal, Challenges and Proposed Approach

### Goal

The goal was to train a segmentation model for chest radiographs. The authors of the selected paper faced some specific problems.

### Main Challenge in the Selected Paper

Lack of large-scale datasets with accurate segmentation masks. Additionally, most public datasets only contain classification labels, which led to the following approach.

### Proposed Approach

1. Train a chest disease classifier
2. Use XAI (e.g., Grad-CAM) to generate pseudo-masks
3. Pre-train segmentation model on pseudo-labels
4. Fine-tune using limited annotated data

---

## 5 Implementation Progress

Here is my progress so far:

1. Implemented classification model on CheXpert-small
2. Developed Grad-CAM-based heatmap generation
3. Began pseudo-dataset creation

### Major Challenge Encountered

Unfortunately, I encountered one huge challenge: full dataset heatmap generation required 15 hours on a Kaggle T4 GPU. As a solution, I used a subset of 1000 images instead.

---

## 6 Training the Second Model

Finally, after generating the pseudo-dataset, I trained my segmentation model using the generated dataset.
