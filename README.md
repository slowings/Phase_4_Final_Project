# Phase_4_Final_Project
Image classification using CNN

## Our Client
Our client, a national non-profit healthcare provider called WeCare, is developing a virtual doctor, or vMD to aid in opening a series of clinics to service under-resourced areas. To miinimize costs, they'll staff these with technicians and Nurse Practitioners, who will be able to test, diagnose and perscribe with the additional assistance of vMD. Our small part of this monumental task is building a deep neural network that detects pediatric pnuemonia with a significant degree of precision and recall.

## The Problem With Pneumonia
Over the last 20 years, pneumonia has been a leading cause of death for children under 5 worldwide, and it is the 6th most common cause of childhood death in the US. In 2019 pneumonia caused the death of 1.9 million children worldwide.  In the U.S., children younger than 5 years of age accounted for 70 percent of pneumonia hospitalizations, at an economic cost of about 1 billion dollars. 

Developing models to quickly and accurately diagnose pneumonia from xrays is one meaningful step towards lessening the toll of this disease, both human and economic.

## Our Data
To train our model we'll be using a publically available database, "Chest X-Ray Images (pnuemonia)" from Kaggle, which consists of 5,863 entries, or xrays, split into 3 sections: train (entries), test (entries), and val (entries). These xrays were taken of anonyomous pediatric patients, aged one to five years old, from Guangzhou, China. These images have been screened for quality control, with unreadable and low quality scans discarded.

## Our Models
We employed an iterative approach to designing a deeply connected neural network that is progressively tuned from a vanilla classifier with few hidden layers towards our goal, a Convolutional Nueral Network, or CNN to train and test our data. Ultimately a PNet with image augmentation and class weights was our best model for maximizing our identification of true positives (precision) and minimizing false negatives (recall).

### PNet Model:
<img width="602" alt="Screenshot 2023-09-13 at 3 10 57 PM" src="https://github.com/slowings/Phase_4_Final_Project/assets/113614318/afb6bbc2-bb0f-48aa-a848-e8081db2fd67">


## Outcomes
With 179 TP (actual normal) and 55 FP (predicted normal), and 42 FN(predicted pneumonia), and 348 TN(actual pneumonia), out Pnet model produced the best metrics. 

However, it should be noted that these rates are far better than at least one NIH study of human diagnosis, where only 59% of x-rays of patients with pneumonia were accurately diagnosed and 14% of normal x-rays were misdiagnosed as having pneumonia.

