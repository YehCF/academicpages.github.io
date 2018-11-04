---
title: "The Development of Medical Devices for COPD Exacerbation Development Monitoring"
excerpt: "The Development of Acute Exacerbation Monitoring for COPD patients at home<br/><img src='/cfyehprofile/images/COPD_CAM_W_r.png'>"
collection: portfolio
---
 
Keywords
---
- COPD, Acute Exacerbation, Abnormal Lung Sound Detection, CNN, RNN

Insights
---
- For patients with COPD: To improve self-efficacy for patients with COPD, they need to objectively judge their symptoms before acute exacerbation occurs.
- For doctors to help COPD detect acute-exacerbations, the service gap is shown below <br/><img src='/cfyehprofile/images/COPD_service_problem.png'>

Methods
--- 
We Develop abnormal lung sound detection system and then build up a model for early-detection of acute-exacerbations
- For Abnormal Lung Sound Detection:
	* Audio Source: We collaborated with medical center in Taiwan to collect lung sounds from patients with COPD
	* Audio Annotation: Normal, Wheeze, Rhonchi, Crackle
	* Audio Preprocessing: (for noisy background) Pre-emphasis with band-pass filter 
	* Stage 1 Modeling: 
		- Audios were transformed into spectrograms.
		- Use Convolutional Neural Network (CNN) for abnormal dectection for each spectrogram
	* Stage 2 Modeling:
		- Audios were transformed into spectrograms.
		- Use Recurrent Neural Network for abnormal detection for the spectrograms from each audio

- For Early Detection of Acute Exacerbation:
	* Use the results from abnormal lung sound detection model and add other data, including respiratory pattern and SpO2
	* Build up a decision tree model to determine the occurrence of acute exacerbation

Results
---
- Abnormal Lung Sound Detection
	* Training Data: ~6.5k, Testing Data: ~1.3k
	* Current Model Performance: Overall, 4-class classification **_accuracy is 87.13%_**. **Precisions for four classes are all above 80%. Recalls for Normal and Wheeze are above 85%. Recalls for Rhonchi and Crackle are near 80%.**
	* The visuals for our model
	![From Audio Clips to Class Activation Maps output from Model](/cfyehprofile/images/COPD_AudioToCAMs.png)

- Eary Detection of Acute Exacerbation:
	* With respiratory pattern features, SpO2 and class probabilities output from abnormal lung sound detection model, we trained a decision tree classifier and **got 80% accuracy on test data**.

- All the experiments above are still ongoing. More data will be included for analysis. 


Discussions
---
- After more abnormal lung sounds (Rhonchi & Crackle) were added to train the model, the precision / recall for the Rhonchi & Crackle were increased. Howevere, adding more data didn't work after the precision / recall of Crackle reached 80%. It might be related to the nature of Crackle - discontinous, intermittent and brief sounds. Currently, I'm experimenting on how bidirectional RNN could help detect Crackle better.

## For more information, please contact with me via email