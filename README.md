# Facial Expression Recognition: Models Research on Established and Custom Datasets

## Overview

This repository contains code and models for in-depth research on Facial Expression Recognition (FER). The project evaluates model performance on renowned datasets like FER2013 and CK+, alongside a uniquely crafted dataset from movie scenes. We explore various models, including VGG19, ResNet, Xception, and a state-of-the-art transformer (DAN), to understand their effectiveness on diverse facial datasets.

## Datasets

### FER2013

- Consists of 35888 grayscale images with 7 distinct facial expressions.
- Split into training, testing, and validation sets.

### CK+

- A widely used database with 981 laboratory-controlled facial expression photos in 7 categories (anger, disgust, fear, sad, contempt, happy, neutral).

### Custom Movie Scenes Dataset

- **Creation Method:**
  - Employed a novel approach based on the Distract-Your-Attention-Network (DAN).
  - Components include a Facial Clustering Network (FCN), Multi-Head Cross Attention Network (MAN), and Attention Fusion Network (AFN).
  - Utilized OpenCV for face extraction and DAN's softmax probabilities for expression categorization.
  - Extracted frames from movie scenes using the DAN-based pipeline, creating a diverse dataset.
  - The dataset comprises 3410 images, categorized into 7 classes, sourced from videos featuring high-class actors.

## Model Construction

- 19 models were tested using ImageNet pretrained weights.
- Training on a GPU with 32 GB RAM took ~8 mins per model.
- Early stopping could further reduce training time.
- Flexible learning rates, 15 warm-up, and 15 training epochs were used.

## Testing Models

Extensive tests were performed on all datasets, with ResNet and VGG showing promising results. Confusion matrices for ResNet and VGG on FER2013 are provided in Figure 5.

## Model Evaluation

A comparative analysis of models on CK+ and the custom dataset revealed interesting insights. Xception emerged as the top performer with 68% and 45% accuracy on CK+ and the custom dataset, respectively.

## Conclusion

Despite advancements, FER remains challenging. State-of-the-art transformers struggle to achieve 70% accuracy, and simpler models may perform better. The automated dataset creation process is efficient but prone to overfitting, suggesting room for improvement. The project also highlights the potential to extract general sentiment from videos using the automated dataset pipeline.

## Poster and Visual Results

For detailed information, visual representations, and results, refer to the included [poster](./Poster.pdf)..
