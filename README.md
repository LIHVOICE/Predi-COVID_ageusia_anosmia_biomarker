# Discovery and analytical validation of a vocal biomarker to monitor anosmia and ageusia in patients with Covid-19

## Background
Ageusia and anosmia are frequent symptoms in people with COVID-19 that could help to early identify the disease and prevent its spread. An automatic assessment tool would also help to follow the Long-Covid syndrome symptoms and understand the whole specter of the disease. Our objective was to develop an artificial intelligence pipeline to predict the presence of ageusia and anosmia, identify a vocal biomarker for these symptoms and internally validate it.

## Content
1. Audio concatenation
    - Concatenates the audios of type1 and type 2 to further feature extraction.
  
2. OpenSMILE features extraction
    - Feature extraction using OpenSMILE package. Changing the _features_subset_ parameter one can choose between the Functional subset or the Low-level descriptors one.

3. Recursive Feature Elimination (RFECV)
    - Recursive feature elimination for 3gp and m4a formats.

4. ML algorithms
    - All classifiers that used structured data are fine-tuned and trained on this script.
  
5. Final results and biomarkers
    - Given the chosen model, it extracts biomarkers as the probability of classifying the sample as positive. After the probability is taken, it is plotted according to the true label of the sample, and a Student's t-test is performed to confirm that the distribution of the probabilities of each class is different. It is important to notice that the AUC used to differentiate the models is the weighted one.

## Dependencies

- Pandas 1.1.5
- Numpy 1.19.5
- Matplotlib 3.2.2
- Opensmile 2.2.0
- Librosa 0.8.1
- Sklearn 0.22.2
- Seaborn 0.11.2
- Scipy 1.4.1
