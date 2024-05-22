# Emotional Analysis Tool for Psychotherapy using XAI

## Overview

Emotion recognition is crucial in various applications, including psychotherapy, where understanding a patient's emotional state is vital for effective treatment. Traditional unimodal emotion recognition approaches, which rely on a single channel of information (e.g., only audio or only video), may miss critical details necessary for accurate emotion detection.

To address these limitations, our project combines video and audio data to analyze emotions, aiming to identify eight distinct emotional states. By extracting features from both audio and video sources, we employ a fusion approach to predict emotions using cues from both visual and auditory information. This method achieved an accuracy of 70% when tested on the RAVDESS dataset for emotion classification.

## Features

### Multimodal Emotion Recognition
- **Data Sources:** Combines audio and video data to enhance emotion recognition accuracy.
- **Emotion Classes:** Identifies eight distinct emotional states.
- **Dataset:** Tested on the RAVDESS dataset.

### Explainable AI (XAI) Techniques
- **Grad-CAM (Gradient-weighted Class Activation Mapping):** Provides visual insights into the reasoning behind classification decisions by highlighting important features in images.
- **LIME (Local Interpretable Model-agnostic Explanations):** Offers interpretability for audio features by explaining the contribution of specific audio characteristics to the classification process.

## Implementation

### Emotion Classification
- **Feature Extraction:** Extracts relevant features from both audio and video inputs.
<img width="370" alt="Screenshot 2024-05-22 at 2 18 05 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/2c6e1f18-e4f5-4cf5-b695-1e0dd68fb2a4">
<img width="370" alt="Screenshot 2024-05-22 at 2 18 22 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/cb7c720f-ba39-495d-8e8e-c3373eee88ec">

- **Fusion Approach:** Integrates visual and auditory cues to enhance prediction accuracy.
<img width="539" alt="Screenshot 2024-05-22 at 2 13 55 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/fb50840d-0a0b-409e-a1cd-a3e12d5693ec">

### Explainability
- **Grad-CAM:** Grad-CAM uses the gradients of the target class (with respect to the final convolutional layer) to understand the importance of each neuron in the final convolutional layer. It computes the gradient of the target class with respect to the feature maps of the last convolutional layer. These gradients are global average-pooled to obtain the neuron importance weights. The weighted combination of these activation maps highlights the important regions in the input image for the target class. The output obtained is a heatmap which highlights the regions of the input image which were crucial for the network’s decision. By overlapping this heatmap with the input image we get a means for visual interpretation of the decision taken.
  
- **LIME:** We applied the developed system to a set of test audio spectrograms from all emotion classes. For each test spectrogram, we iterated through all emotion classes and applied LIME to generate explanations for each prediction. We visualized the original image alongside LIME heatmaps for each emotion class, facilitating the interpretation of the model's decisions.

## Results

- **Accuracy:** Achieved 70% accuracy on the RAVDESS dataset.
<img width="514" alt="Screenshot 2024-05-22 at 2 18 57 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/da7f8504-aa5b-4c68-b2a5-53fa5bd0418e">
<img width="514" alt="Screenshot 2024-05-22 at 2 19 19 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/2f66c5ef-7f7c-44e7-a66f-d7a0821abe43">

- **Explainability: Grad-CAM** 
<img width="833" alt="Screenshot 2024-05-22 at 2 22 01 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/9c40de5d-184f-4981-b7f1-fc2adf37e78c">

Following heatmap generation, we analyzed the results across all emotion classes to glean insights into the features and patterns deemed most indicative of each emotional state by the model. This iterative exploration allowed us to understand the model's decision-making process comprehensively, shedding light on the discriminative facial cues and visual attributes associated with different emotions. Through this approach, the inferences we got are summarised in table.

<img width="524" alt="Screenshot 2024-05-22 at 2 30 32 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/fd8f65aa-699b-406d-add8-ff17c61d80ec">

- **Explainability: LIME** 
<img width="917" alt="Screenshot 2024-05-22 at 2 22 35 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/92d13e1b-87f2-4261-a2cc-c7ee03d6a5b4">
<img width="917" alt="Screenshot 2024-05-22 at 2 23 25 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/8cbc6b58-776a-43d9-a693-fe81b8b5684f">
<img width="917" alt="Screenshot 2024-05-22 at 2 23 39 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/010b51ed-11f9-4cf1-8403-b827f9cfa017">
<img width="917" alt="Screenshot 2024-05-22 at 2 23 53 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/f412c185-376f-4781-9b6c-a22bf516bda3">

In the emotion classification process, certain emotions exhibit distinct patterns in their spectrograms, aiding in their identification. Moreover, misclassifications may also arise when emotions display overlapping spectrogram features. All the inferences that we observed for each emotion are summarised in table.

<img width="550" alt="Screenshot 2024-05-22 at 2 33 21 PM" src="https://github.com/swetha6116/Multimodal-emotion-analysis/assets/89096691/4df213ad-d6fb-4cd3-adbf-9ef785b93bd5">


## Applications in Psychotherapy

The integration of XAI techniques in our emotion recognition tool has significant implications for psychotherapy. By gaining a deeper understanding of the features driving classification decisions, therapists can better discern subtle nuances in patients' emotional states. This can lead to more effective and personalized therapeutic interventions.




