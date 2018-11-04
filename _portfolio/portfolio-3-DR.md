---
title: "Artificial Intelligence-based Diabetics Fundus Image Decision Support"
excerpt: "The Development of CNN models for Primary Doctors to refer patients with DR to ophthalmologists<br/><img src='/cfyehprofile/images/DR_L2.gif'>"
collection: portfolio
---

Keywords
---
- Diabetic Retinopathy, Fundus Image, CNN, Class Activation Map

Insights
---
Primary doctors need to be enabled with ability to refer potential patients with diabetic retinopathy (DR) to prevent patients with DR from blindness

Methods
---
Stage 1
- Data Source: Kaggle DR Dataset (Images for Training: ~35k, Testing: ~51k)
- Data Annotations: 0, 1, 2, 3, 4 (Ranging from No DR to Proliferative DR)
- Deep Learning Framework: Tensorflow (tf-slim)
- Models: Inception V3, Inception V4, Inception-Resnet V2, DenseNet-121, DenseNet-169

Stage 2
- Data Source: Medical Centers in Taiwan
- Data Annotations: DR Severity (Similar to Kaggle) + Lesions related to DR (Microanuerysm, Hemorrhage, Exudate, Neovascularization, etc)
- Image Preprocessing Method: Adaptive Histogram Equalization (AHE) as basis
- Deep Learning Framework: Tensorflow (tf-slim)
- Models: Inception V3 (patch-based detection method), YOLO (object-detection method)

Results
---
Stage 1
- Just 1 Model: Quadratic Kappa - **_84.15% (Rank 3th, in comparion with results in Kaggle Competition)_**
- Here are the visuals of our model
	- Class Activation Map for Moderate DR (level: 2) 
	<img src='/cfyehprofile/images/DR_L2.gif'>
	- Class Activation Map for Severe DR (level: 3)
	<img src='/cfyehprofile/images/DR_L3.gif'>
	- Class Activation Map for Proliferative DR (level: 4)
	<img src='/cfyehprofile/images/DR_L4.gif'>

Stage 2
- The model for lesion detection is still under development 


Discussions
---
- From the experiments in Stage1, it seemed image preprocessing method  just helped a little bit for the performance of our deep-learning model(about 0.5% in kappa). However, from the feedback of the ophthalmologists we collaborated with, this image preproceesing method based on AHE could benefit ophthalmologists if it is embedded in current service flow in ophthalmology.
- As the class activation maps for each level of DR were plotted, we found out that our model took laser spots as important features for classification. However, laser spots were the signs appearing following the laser operation, not really the signs for level 4 (Proliferative DR). In the later experiment, we should build up a model not to take laser spot as a determinant feature for level 4. (This would be addressed in stage 2)


## For more information, please contact with me via email