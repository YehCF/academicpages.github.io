---
title: "LOCALIZATION OF RETINAL NERVE FIBER LAYER DEFECT IN FUNDUS IMAGE BY VISUAL FIELD GUIDED LEARNING NETWORK"
collection: publications
permalink: /publication/2019-08-27-LocalizationOfRNFLD
excerpt: 'Retinal Nerve Fiber Layer Defect (RNFLD) can be an earliest sign to detect the ongoing glaucomatous damage. However, existing measurements, including visual field test and optic cup/disc ratio, fail to reflect RNFLD. Although optical coherence tomography (OCT) may provide information about RNFLD, the field of view (FOV) of OCT is smaller than that of fundus camera. This means early RNFLD may be undetected by OCT. In order to screen out patients with early-stage glaucoma, we propose to build a deep neural network to both predict glaucoma and locate RNFLD in fundus image by constraining its latent space with visual field map (VFM), which has wider FOV than fundus image and indicates visual field loss led by RNFLD. Since VFM does not match fundus image at pixel level, the challenge of this net-work would be to learn the spatial relationship between fundus image and VFM in addition to the prediction of glaucoma. To tackle this challenge, we compared three encoder-decoder convolutional neural network (CNN) with distinctive architectures in this study: (i) encoder-decoder CNN, (ii) encoder-decoder CNN with spatial transformer network (STN) and (iii) generative adversarial network (GAN), whose generator is the same as (i). The main evaluation metrics in this study was the correlation coefficient between predicted VFM and real VFM. Be-sides, accuracy and AUC of each network for the prediction of glaucoma were measured to make sure the predicted VFMs were closely related to glaucoma. The study was conducted on the dataset we collected from a medical center. Our results demonstrated that the correlation coefficient produced from model (iii) was the highest and it also did well in the prediction of glaucoma. This proposed network would be the first one to predict glaucoma and locate RNFLD simultaneously to provide explainable results for ophthalmologists and address the pixel-level mismatch between fundus images and VFM.'
date: 2019-08-27
venue: 'The 32st IPPR Conference on Computer Vision, Graphics and Image Processing'
paperurl: 'http://yehcf.github.io/cfyehprofile/files/2019CVGIP2019-LocalizationOfRNFLD.pdf'
citation: 'Chun-Fu Yeh, Guan-An Chen, Kwou-Yeung Wu, Min-Yu Huang (2019) Localization of Retinal Nerve Fiber Layer Defect in Fundus Image by Visual Field Guided Learning Network. <i>The 32st IPPR Conference on Computer Vision, Graphics and Image Processing</i>, Taitung, Taiwan, August 25-27.'
---

Retinal Nerve Fiber Layer Defect (RNFLD) can be an earliest sign to detect the ongoing glaucomatous damage. However, existing measurements, including visual field test and optic cup/disc ratio, fail to reflect RNFLD. Although optical coherence tomography (OCT) may provide information about RNFLD, the field of view (FOV) of OCT is smaller than that of fundus camera. This means early RNFLD may be undetected by OCT. In order to screen out patients with early-stage glaucoma, we propose to build a deep neural network to both predict glaucoma and locate RNFLD in fundus image by constraining its latent space with visual field map (VFM), which has wider FOV than fundus image and indicates visual field loss led by RNFLD. Since VFM does not match fundus image at pixel level, the challenge of this net-work would be to learn the spatial relationship between fundus image and VFM in addition to the prediction of glaucoma. To tackle this challenge, we compared three encoder-decoder convolutional neural network (CNN) with distinctive architectures in this study: (i) encoder-decoder CNN, (ii) encoder-decoder CNN with spatial transformer network (STN) and (iii) generative adversarial network (GAN), whose generator is the same as (i). The main evaluation metrics in this study was the correlation coefficient between predicted VFM and real VFM. Be-sides, accuracy and AUC of each network for the prediction of glaucoma were measured to make sure the predicted VFMs were closely related to glaucoma. The study was conducted on the dataset we collected from a medical center. Our results demonstrated that the correlation coefficient produced from model (iii) was the highest and it also did well in the prediction of glaucoma. This proposed network would be the first one to predict glaucoma and locate RNFLD simultaneously to provide explainable results for ophthalmologists and address the pixel-level mismatch between fundus images and VFM.