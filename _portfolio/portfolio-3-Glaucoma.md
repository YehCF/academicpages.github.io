---
title: "Artificial Intelligence-based Early-stage Glaucoma Detection with Fundus Imagess"
excerpt: "The development of an early-detection method for potential patients with Glaucoma with fundus images"<br/><img src='/cfyehprofile/images/Glaucoma_Brief_v.png'>"
collection: portfolio
---

Keywords
---
- Glaucoma, Fundus Image, Visual Field, Optical Coherence Tomography, CNN, AutoEncoder, GAN

Insights
---
- For patients with Glaucoma: To prevent them from blindness, they need to have an easy access to eye health examination and a reliable method to early quantize the retinal nerve fiber lesions.
- For ophthalmologists: how might we help doctors early screen out potential patients with glaucoma from fundus images

Methods
---
Stage 1
- Data Source: Small Public Dataset (15 fundus images from healthy patients; 15 fundus images from patients with Glaucoma)
- Data Annotations: 0 (Healthy), 1 (Glaucoma)
- Deep Learning Framework: Tensorflow (tf-slim)
- Models: <br/>
![CNN model for Glaucoma](/cfyehprofile/images/glaucoma_model.png)

Stage 2
- Data Source: Medical Centers in Taiwan (including fundus images, visual fields, lesion map from optical coherence tomography(OCT))
- Data Annotations: Take visual fields / OCT as lesion annotations for fundus images
- Models: Inception V3 (patch-based detection method), CNN-based Auto-Encoder, VAE-GAN

Results
---
Stage 1
- The results are described in [**_this conference paper_**](/cfyehprofile/files/20180708CVGIP2018_v1.3.pdf)
- Here are the visuals of our model
	- Class Activation Map for Glaucoma  
	- From the ophthalmologist's feedback, the activated regions were close to the retinal nerve fiber layer defects that they saw from the original fundus images.
	<br><img src='/cfyehprofile/images/Glaucoma_CVGIP_v.png'>

Stage 2
- The experiment for using Visual Fields / OCT as the annotations for fundus images is onging. We're using CNN-based Autoencoder and VAE-GAN to build up a model to transform fundus images into probability map of retinal nerve fiber layer defect. The results would be published in the beginning of next year.


## For more information, please contact with me via email