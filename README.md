# Explainable AI on Wireless Capsule Endoscopy

## Introduction
This repository houses the code and resources associated with our research on classifying frames as bleeding or non-bleeding in Wireless Capsule Endoscopy (WCE) images using deep learning (DL) models. We emphasize explainable AI (XAI) by leveraging Grad-CAM for enhanced interpretability, enabling better understanding of model decision-making and facilitating targeted improvement efforts.

## Technologies Used
[![Tech_Used](https://skills.thijs.gg/icons?i=py,tensorflow&theme=dark)](https://skills.thijs.gg)

## Dataset and Proposed Approach
The dataset AutoWCE-BleedGen version-1 consists of 1309 Bleeding and Non-Bleeding images each of more than 30 patients at  AIIMS, New Delhi, India.
We tested two popular deep learning models, ResNET152v2 and MobileNETv2, on the AutoWCE-BleedGen dataset to detect bleeding in images. These pre-trained models along with additional layers were trained on the AutoWCE-BleedGen version-1 dataset to adapt them to our specific task. We implemented Grad-CAM (Gradient Weighted- Class Activation Mapping) from scratch on sample images to analyze the interpretability of the model.

## Results and Discussions
Below is the table comparing the performance of both the models:
![image](https://github.com/Manvith-Prabhu/WCE_XAI/assets/100431364/796a0f30-69d8-407b-8d71-863c410bf38a)

Since ResNet152v2 performed slightly better, we implemented Grad-CAM on the same and the results are as follows:
![image](https://github.com/Manvith-Prabhu/WCE_XAI/assets/100431364/5f4243ea-e7c1-4513-b5ff-edc6507236ee)

In the 1st set of images Grad-CAM on ResNet152v2 highlightes the bleeding region whereas in 2nd set no region is significantly higlighted. Seeing how the AI makes decisions about bleeding pictures helps doctors trust it more, leading to better and more confident diagnoses.

