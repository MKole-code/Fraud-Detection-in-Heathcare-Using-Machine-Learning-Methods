# Fraud (Overbilling) Detection in Healthcare Using Machine Learning Methods
## Data Science final project (Aug. 2022)

In the United States the cost of healthcare fraud is close to $100 billion a year. Fraud and overbilling in healthcare is a universal challenge and different countries and institutions have different means of fighting it, nowadays a crucial part in this fight is played by artificial intelligence tools including machine learning. 

What can cause overbilling:
<ul>
  <li>fraud (when the service is NOT provided, but the bill is issued)</li>
  <li>abuse of the system (when the service is provided, but it is coded at a HIGHER rate)</li>
  <li>waste of resources (the patient is sent for unnecessary examination)</li>
  <li>errors of personnel or software.</li>
</ul>

After studying 20 scientific publications and more than 150 Internet articles related to the fraud detection problems I chose the following approaches in my project:

<ul>
  <li>Sampling technique to balance classes.</li>
  <li>Popular algorithms for fraud detection: logistic regression, naïve bayes, different variants of gradient boosting and random forest.</li>
  <li>Roc-auc metric to assess the quality of the model</li>
</ul>

### Case study.
Dataset for the experiment was compiled from the database information and financial documentation of a medical clinic. In this case, the victim of fraud is the clinic itself, because it gets overbilled by its business partner. The partner (aggregator) advertises the clinic and schedules patients’ visits. The aggregator bills the clinic for each scheduled visit. 
<br> Current rate of overbilling is 4%.
<br> At the moment the bills are checked for incorrect positions manually by a clinic worker who listens to the phone calls audio recordings and looks through the schedule.
 
### Methods used during the experiment:

<ul>
  <li>SMOTE sampling for class balancing. There are 1068 samples in the dataset. Minority class is only 4%</li>
  <li>timedelta() class in python to make features out of dates in the dataset</li>
  <li>cross-validation for model selection</li>
  <li>geometric mean for calculating decision threshold</li>
  <li>feature importance for feature selection</li>
  <li>log-loss graph for finding the optimal number of iterations</li>
  <li>confusion matrix for evaluating perfomance of the models</li>
</ul>

## Summary:
The XGBoost model identifies 82% cases of fraud in the invoices, without having to analyze audio-recordings of patients’ phone calls and the clinic schedule. 
