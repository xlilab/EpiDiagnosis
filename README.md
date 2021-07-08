# PhenoDiagnosis
PhenoDiagnois is a machine learning diagnosis model based on lightgbm algorithm. Here we show that the indicators obtained from blood tests were used as features, and a balanced data set containing 15,950 samples in UK Biobank was used to diagnose and predict the risk of gastrointestinal cancer through machine learning model——LightGBM[1].
In terms of processing missing values and capturing nonlinear relationships, LightGBM shows better performance compared with other models, with a maximum ROC of 0.7940.

## Running PhenoDiagnosis
The two LightGBM models(LightGBM-Full63, LightGBM-Blood61) shown below (https://github.com/xlilab/PhenoDiagnosis) are based on 61 characteristics (including 30 blood biochemistry indicators and 31 blood count indicators) and 63 characteristics (age and sex are added) as input for training and evaluating.

## Model Explaination
We then used TreeExplainer[2] to explain the output of the model, get the SHAP values for each feature, sort the top 20 features, and draw a heat map of the SHAP interaction values. Based on the SHAP summary plot and the SHAP interaction value plot，some features were selected as instances so as to show the relationship between SHAP value and characteristic value, and the interaction between features in detail.

## Reference
[1] Ke G L, Meng Q, Finley T, et al. LightGBM: A Highly Efficient Gradient Boosting Decision Tree[A]. In: Guyon I, Luxburg U V, Bengio S, et al. Advances in Neural Information Processing Systems 30[C]. La Jolla:Neural Information Processing Systems (Nips),2017.1-9.
[2]Lundberg S M, Erion G, Chen H, et al.From Local Explanations to Global Understanding with Explainable AI for Trees[J].Nat Mach Intell,2020, 2 (1): 56-67.

## Datasets for model construction
UK Biobank

## Dependencies and Testing environment
* python 3.7.6
* jupyter lab 1.2.6

## Author
**Shijia Yu** -- [Lydiaeve](https://github.com/Lydiaeve)
