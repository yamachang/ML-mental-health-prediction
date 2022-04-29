# Prediction-of-Mental-Wellbeing-among-Transgender-Individuals
A quantitative study predicting 12-month non-suicidal self injury (NSSI) among gender diverse individuals using LASSO Regularized Regression

<p align="center">
  <img src="https://github.com/yamachang/NSSI_LONGITIDUNAL/blob/master/NSSI_LONGITIDUNAL_files/cover-photo.jpg" width=50% >
</p>

<hr>

## RESEARCH-QUESTION

`What factors would prospectively predict non-suicidal self-injurious behaviors among gender diverse individuals?`

## OBJECTIVE 

Gender diverse individuals (i.e., identifying their gender as different from the sex assigned at birth) demonstrate higher rates of non-suicidal self-injury (NSSI) compared to other sexual and gender minority (SGM) populations. Despite the importance of identifying prospective risk factors for NSSI, few studies have examined the longitudinal predictors of NSSI among gender diverse individuals. To address this gap, the current study investigated which factors would prospectively predict past-year non-suicidal self-injurious behaviors among gender diverse individuals.

## METHOD

A supervised machine model based on 10-fold cross-validation of LASSO regularized logistic regressions was built using 31 baseline characteristics. Model features included self-injurious thoughts and behaviors (SITB) related factors, minority stress-related factors, protective factors, mental health factors, and the factors of gender-affirming treatment. Training goal of the model consisted of discriminatory accuracy of presence/absence of NSSI engagement during the 12-month follow-up period.

## WORKFLOW

```
    0. Data cleaning and feature engineering
    1. Exploratory Data Analysis - Correlation analysis
    2. LASSO regularized logistic regressions
        - a. Data Modelling
        - b. Division of dataset into: train and test set
        - c. Find the best lambda using cross-validation
          - Find the optimal value of lambda that minimizes the cross-validation error
        - d. Model evaluation on the test data
        - e. Use AREA UNDER THE CURVE (AUC) to assess the prediction accuracy 
```

## RESULT

The model mean cross-validation estimate of the Area Under the Receiving Operating Characteristics Curve suggested an overall good prediction accuracy (AUC, 0.85). Our model suggested the optimal value of tuning parameter “lambda” as 0.03, and selected 8 variables with the strongest association with NSSI: past-year NSSI, past-year NSSI frequency, past-year suicidal ideation, enacted stigma, sense of safety, BSI-GSI, anxiety, and somatization. Lifetime engagement in NSSI, suicidal ideation and suicidal attempts did not emerge as longitudinal predictors in 12-month NSSI.

<p align="center">
  <img src="https://github.com/yamachang/NSSI_LONGITIDUNAL/blob/master/NSSI_LONGITIDUNAL_files/figure-gfm/unnamed-chunk-6-1.png" width=50% >
</p>

<p align="center">
  <img src="https://github.com/yamachang/NSSI_LONGITIDUNAL/blob/master/NSSI_LONGITIDUNAL_files/figure-gfm/unnamed-chunk-7-1.png" width=50% >
</p>

> Regularized regression model showed 85% prediction accuracy and suggested 8 predictors with the strongest association

<p align="center">
  <img src="https://github.com/yamachang/NSSI_LONGITIDUNAL/blob/master/NSSI_LONGITIDUNAL_files/figure-gfm/unnamed-chunk-8-1.png" width=50% >
</p>

> EDA helps in giving a preliminary glimpse on how various factors are associated with 12-month non-suicidal self injury

<hr>

## CONCLUSION

Our model suggested the risk of 12-months NSSI behavior to be strongly associated with past-year risk factors, including suicidal ideation, NSSI engagement, and higher NSSI frequency, suggesting the importance of continued clinical monitoring as a prevention strategy. Among minority-stress-related factors, enacted stigma, the actual experiences of rejection and discrimination, emerged as a predictor towards future NSSI engagement. This finding indicates that gender diverse individuals suffering from enacted stigma might have a higher risk of developing NSSI behaviors. LASSO regularized logistic regressions provided the advantage of effectively improving model interpretability by selecting relevant variables and avoiding overfitting. 

## FUTURE-WORK

Future studies are needed to collect more longitudinal data points, in order to establish more accurate trajectories of NSSI across the lifespan among gender diverse individuals. 
