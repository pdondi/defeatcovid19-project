# Project description and synopsis

*Development of a model of analysis of clinical images for purposes of supporting medical diagnosis*

17 March 2020


## Revisions

| Version | Date       |  Notes         |
|:-------:|:----------:|:---------------|
|     1.0 | 2020-03-17 | Document draft |
|     2.0 | 2020-03-25 | Document revision |


## Index

- [Revisions](#revisions)
- [Index](#index)
- [Purpose of the document](#purpose-of-the-document)
- [State of the art](#state-of-the-art)
  * [Artificial Intelligence (AI) and clinical analysis](#artificial-intelligence-ai-and-clinical-analysis)
  * [Screening and diagnosis of patients with COVID19](#screening-and-diagnosis-of-patients-with-covid19)
- [Synopsis of the studies](#synopsis-of-the-studies)
  * [Study 1: Analysis of pulmonary radiological images](#study-1-analysis-of-pulmonary-radiological-images)
    + [Objectives of the study](#objectives-of-the-study)
    + [Study Population](#study-population)
    + [Period of study](#period-of-study)
    + [Analyzed data](#analyzed-data)
    + [Expected results](#expected-results)
  * [Study 2: Analysis of cardiac (and lung) ultrasound images](#study-2-analysis-of-cardiac-and-lung-ultrasound-images)
    + [Objectives of the study](#objectives-of-the-study-1)
    + [Study Population](#study-population-1)
    + [Study period](#study-period)
    + [Analyzed data](#analyzed-data-1)
    + [Expected results](#expected-results-1)
- [Notes](#notes)


## Purpose of the document

This document has the purpose to illustrate the research project that the working group #defeatcovid19 intends to carry out in order to develop a support system for diagnosing lung diseases. The scope of this document will be to present the state of the art in research, in machine learning and to demonstrate the potential of the tool that will be developed including the development path of the research plan.


## State of the art

### Artificial Intelligence (AI) and clinical analysis

Modern medical imaging techniques are able to offer the doctors valuable information in the early diagnosis of pneumonia with bilateral interstitial infiltrate, typical of serious new coronavirus infections. The use of tools such as radiological analysis during hospitalization and the course of the disease, combined with ultrasound monitoring can provide a clinical picture of the patient, allowing the doctor to take advantage of his experience in order to assess the situation in order to increase the possibility of a favorable prognosis.

The acquisition of images using radiological and ultrasound instruments also allows the doctor to have a scoreboard which, combined with the patient's clinical data, can allow the timely adoption of certain therapy protocols, and monitor their impact over time.

In the field of image processing, artificial intelligence has produced extremely significant results in recent years. By exploiting the localized nature of the images provided to the machine learning model, it is possible to identify the presence of patterns of interest with a precision that, in the best cases, can go beyond human analysis capacity. Such techniques make extensive use of analytical tools known as neural networks. Such tools (in the generalized mathematical representation) are known as “universal learners”, mathematical models capable of approximating, theoretically, any unknown function. These techniques are effectively applied to classification processes, where the function to be estimated is that of a complex mathematical structure that links the acquired image to the determination of the presence (or absence) of a specific object within it. Neural networks find application in various aspects of the technological frontier: from the simple recognition of the content of an image, to the autonomous driving of vehicles, to the construction of tools capable of "learning" human experience, modeling its behavior. In particular, the latter allow to obtain, through a phase called "training", a machine learning model capable of behaving in front of an image in a similar way to an expert in extracting the information it contains.

In the medical field, numerous applied research projects have emerged in recent years in which machine learning techniques (or, more generally, artificial intelligence) are used effectively to support the specialist, for the identification and diagnosis of images obtained for the purposes diagnostics from patients, extensively using systems such as computed tomography (CT) <sup id="a1">[[1]](#f1)</sup> <sup id="a2">[[2]](#f2)</sup> and Positron Emission Tomography (PET) <sup id="a3">[[3]](#f3)</sup>.

Recently, research has focused its efforts on the use of radiological images <sup id="a4">[[4]](#f4)</sup> and ultrasound <sup id="a5">[[5]](#f5)</sup> <sup id="a6">[[6]](#f6)</sup> which, unlike the previous techniques, are extensively adopted to support the diagnosis, not requiring huge financial investments or posing risks for the patient's health.

### Screening and diagnosis of patients with COVID19

Following the recent epidemic of new coronavirus, hospitals are under considerable pressure which reaches its peak in the stages of screening for new potentially infected and diagnosis of the course for hospitalized patients, with consequent difficulty for the medical staff in diagnosing both the main situation and any patient's comorbidities. Added to this is the ever increasing need to identify the areas of impact of the virus's action and the course of organs that, although not directly affected, suffer the strong stress induced by the COVID 19 infection. In this scenario, two techniques are present in the diagnostic and monitoring protocols of hospitals: pulmonary radiography and cardiac ultrasound (sometimes also pulmonary). These are techniques aimed at determining the correct physiological functioning of the organs or at assessing the damage in order to be able to reach a prognosis.


## Synopsis of the studies
The main goal of the project is to analyze the applicability of machine learning models to the analysis of radiological and ultrasound images, in order to build a valid support for medical diagnosis, thus allowing  extending screening procedures to a larger number of patients. As a consequence, the work of radiology technicians and specialized doctors would be streamlined, reducing the waiting time for medical reports and thus, increasing the diagnostic capacity of the hospital wards.

The secondary aim is to identify which other parameters (for now on features) can influence the onset or development of the pathology. In this case, a supervised learning approach will be applied, through which a set of patient's clinical and demographic features (which, in a different way, can be linked to the presence of the considered pathology)  are introduced into the network, so that the network can identify a rule to associate the data of the incoming subjects with the presence or absence of the pathology. In this context, instead of using the network to extract the image parameters, additional features are explicitly added, so that the network can learn the rule to distinguish the subjects in the two classes, and use it in similar tasks. As a consequence, it is possible to identify which are the most meanighful features, among those collected, to recognize the patology. This would make it possible to profile the subjects more prone to the insurgence of COVID19 and the prevention of the aggravation of the pathology. The feasibility of this third goal is supported by the "If Available" data collection of the two studies detailed below.

Given the fortunately small number of patients suffering from severe forms of COVID19 and the numbers usually necessary for the construction of a sufficient dataset to train a new model, we will proceed in this study with the use of previous images available at the hospital representing healthy situations and situations with known pathologies (for example pneumonia) and then the models identified will be specialized by using the available images of COVID19 patients.

This project aims to conduct two parallel investigations on different types of images and then consolidate the two models identified in a later phase in order to clarify the correlation between cases with similar prognosis.

### Study 1: Analysis of pulmonary radiological images

#### Objectives of the study

A first application of image analysis models regards the radiographs of a population made by: healthy patients; lung disease patients; identified (or suspect) COVID19 patients, suffering from pneumonia. By constructing a dataset of images obtained by X-ray and comparing them to the resulting diagnosis, it would be possible to train the model to recognize pathological situations of serious pneumonia. Furthermore, during the course of the disease for hospitalized patients, the use of this analysis model could allow constant monitoring even in conditions of reduced availability of staff, offering feedback to support diagnostic activity.

This practice would help to promptly provide a clinical picture of the patient resulting in:

- Increase in the possibility of a favorable outcome
- Decrease of waiting times
- Quick detection of indispensable hospitalizations, making intensive care stations more accessible
- Accuracy of an independent operator tool
- Less use of other operator dependent diagnostic methods (which are already scarce in the region) with consequent simplification and lightening of the workload of the analysis laboratories

#### Study Population

**Required:** Anonymized lung radiographic image of healthy patients, lung disease patients, identified (or suspect) COVID19 patients suffering from pneumonia in DICOM format or equivalent.

**If available,** data of clinical relevance relating to patients such as age, gender, presence of previous pathologies, etc.

**If available,** data on COVID19 treatment therapies administered to patients and outcome of the prognosis.

#### Period of study

March 2020 - December 2020

#### Analyzed data
The chest and lung x-ray of healthy patients, lung disease patients, identified (or suspect) COVID19 patients suffering from pneumonia will be analyzed, together with the report information, so as to build a dataset useful for training the machine learning model.

#### Expected results

A binary classification-model of the probability of favorable or unfavorable diagnosis will be produced, based on the images supplied to the system. The probabilities expressed by the machine learning model can be interpreted as the confidence interval of belonging to one of the two possible diagnosis outcomes. The data will be analyzed con deep neural network computational models using a specific architecture to analyze images. For the analysis of the models the following specific metrics will be used:

- Precision & Recall
- F1 score
- Thresholds evalution in funtion of the importance of false negative/false positives
- ROC (Receiver Operating Characteristic) curve
- AUC (Area Under Curve)

Expressed outcome and probability will be the two values that can be integrated into the diagnostic evaluation.

More in detail, the study aims to carry out a first overall analysis identifying the data certainly incompatible with the clinical picture of pneumonia caused by COVID-19, which will be hospitalized and/or treated in different ways and structures; and doubtful or highly compatible cases with the clinical picture under examination, validated with further diagnostic methods by the Healthcare Facility and/or by the ISS. 

### Study 2: Analysis of cardiac (and lung) ultrasound images

#### Objectives of the study

The use of ultrasound techniques allows the analysis of the physiological behavior of the organ during examination. In this phase, to build a machine learning model capable of identifying pathological behaviors, we will proceed to acquire data produced by an ultrasound machine in use at the hospital for a population composed by: healty patients; heart disease patients; identified (or suspect) COVID19 patients, suffering of heart diseases.

The availability of time-varying images relating to the physiology of the cardiac organs of patients will allow training of a machine learning model capable of accurately recognizing a situation of healthy or pathological behavior of the heart muscle.

This practice would help to promptly provide a clinical picture of the patient resulting in:

- Increase in the possibility of a favorable outcome
- Decrease of waiting times
- Quick detection of indispensable hospitalizations, making intensive care stations more accessible
- Accuracy of an independent operator tool
- Less use of other operator dependent diagnostic methods (which are already scarce in the region) with consequent simplification and lightening of the workload of the analysis laboratories


#### Study Population

**Required:** Anonymized images of cardiac ultrasound scans of healthy patients, heart disease patients, identified (or suspect) COVID19 patients suffering of heart diseases in DICOM format or equivalent.

**If available,** data of clinical relevance relating to patients such as age, gender, presence of previous pathologies, family history and ongoing drug therapies.

**If available,** data on COVID19 treatment therapies administered to patients and outcome of the prognosis.

#### Study period

March 2020 - December 2020

#### Analyzed data

The ultrasound images relating to the cardiac function of healthy patients, heart disease patients, identified (or suspect) COVID19 patients suffering of heart diseases will be analyzed, together with the medical report information, so as to build a dataset useful for training the machine learning model.

#### Expected results

A binary classification-model of the probability of favorable or unfavorable diagnosis will be produced, based on the images supplied to the system. The probabilities expressed by the machine learning model can be interpreted as the confidence interval of belonging to one of the two possible diagnosis outcomes. The data will be analyzed con deep neural network computational models using a specific architecture to analyze images. For the analysis of the models the following specific metrics will be used:

- Precision & Recall
- F1 score
- Thresholds evalution in funtion of the importance of false negative/false positives
- ROC (Receiver Operating Characteristic) curve
- AUC (Area Under Curve)

Expressed outcome and probability will be the two values that can be integrated into the diagnostic evaluation.

More in detail, the study aims to carry out a first overall analysis identifying the data certainly incompatible with the clinical picture of pneumonia caused by COVID-19, which will be hospitalized and/or treated in different ways and structures; and doubtful or highly compatible cases with the clinical picture under examination, validated with further diagnostic methods by the Healthcare Facility and/or by the ISS. 

## Treatment of personal data and results achieved

The data will be processed in compliance with the principles set out in article 5 of Regulation (EU) 2016/679, anonymously and for the purposes expressly stated in this document.

The results of the studies will be free of charge for all national medical staff and will therefore be usable in private and public structures in the departments responsible for identifying and treating COVID-19.

The data will be saved in DICOM format and processed in a protected folder on the Neosperience S.p.A. servers.

Neosperience S.p.A and Looptribe S.r.l. guarantee the treatment and conservation of the data used and collected during the study for a period of 2 years (reference period 2020-2021).

## Notes
1. <b id="f1">[^](#a1)</b> S. Chen *et al.*, "Automatic Scoring of Multiple Semantic Attributes With Multi-Task Feature Leverage: A Study on Pulmonary Nodules in CT Images," in *IEEE Transactions on Medical Imaging*, vol. 36, no. 3, pp. 802-814, March 2017.
2. <b id="f2">[^](#a2)</b> Y. Chunran, W. Yuanvuan and G. Yi, "Automatic Detection and Segmentation of Lung Nodule on CT Images," *2018 11th International Congress on Image and Signal Processing, BioMedical Engineering and Informatics (CISP-BMEI)*, Beijing, China, 2018 , pp. 1-6.
3. <b id="f3">[^](#a3)</b> G. Nalbantov, A. Dekker, D. De Ruysscher, P. Lambin and EN Smirnov, "The Combination of Clinical, Dose-Related and Imaging Features Helps Predict Radiation-Induced Normal-Tissue Toxicity in Lung-cancer Patients - An in-silico Trial Using Machine Learning Techniques" *2011 10th International Conference on Machine Learning and Applications and Workshops*, Honolulu, HI, 2011, pp. 220-224.
4. <b id="f4">[^](#a4)</b> [https://www.pyimagesearch.com/2020/03/16/detecting-covid-19-in-x-ray-images-with-keras-tensorflow-and-deep-learning/](https://www.pyimagesearch.com/2020/03/16/detecting-covid-19-in-x-ray-images-with-keras-tensorflow-and-deep-learning/)
5. <b id="f5">[^](#a5)</b> Y. Liang, R. He, Y. Li and Z. Wang, "Simultaneous segmentation and classification of breast lesions from ultrasound images using Mask R-CNN," 2019 *IEEE International Ultrasonics Symposium (IUS)*, Glasgow, United Kingdom, 2019, pp. 1470-1472.
6. <b id="f6">[^](#a6)</b> L. Zhang, H. Zhu and T. Yang, "Deep Neural Networks for fatty liver ultrasound images classification," *2019 Chinese Control And Decision Conference (CCDC)*, Nanchang, China, 2019, pp. 4641-4646.
