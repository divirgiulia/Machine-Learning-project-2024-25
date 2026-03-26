# Machine Learning 2025 Course - Homework

## Francesco Trovò, Aleksandra Zec, Stefano Samele

## {francesco1.trovo, aleksandra.zec, stefano.samele}@polimi.it

## May 2025

## 1 Background

The SUPPORT2 (Study to Understand Prognoses Preferences Outcomes and
Risks of Treatment) dataset comprises 9105 individual critically ill patients
across 5 United States medical centers, accessioned throughout 1989-1991 and
1992-1994. Each row concerns hospitalized patient records who met the inclu-
sion and exclusion criteria for nine disease categories: acute respiratory failure,
chronic obstructive pulmonary disease, congestive heart failure, liver disease,
coma, colon cancer, lung cancer, multiple organ system failure with malignancy,
and multiple organ system failure with sepsis. The goal is to determine these
patients’ short-term and mid-term survival rates based on several physiologic,
demographic, and disease severity factors. It is an important problem because
it addresses the growing national concern over patients’ loss of control near the
end of life. It enables earlier decisions and planning to reduce the frequency of
a mechanical, painful, and prolonged dying process.

## 2 Dataset

An accurate description of the dataset features can be found athttps://
archive.ics.uci.edu/dataset/880/support2.
Remark 1The dataset contains information about previously developed
models. Variable aps, sps, surv2m, surv6m, prg2m, prg6m, dnr, and dnrday
contain information that could heavily influence your model predictions and
should thus be excluded.
Remark 2. Due to the high percentage of missing values, there are a
couple of recommended imputation values. According to the HBiostat Reposi-
tory (https://hbiostat.org/data/repo/supportdesc, Professor Frank Har-
rell) the following default values have been found to be useful in imputing miss-
ing baseline physiologic data in Table 1.
Moreover, there are 159 patients surviving 2 months for whom there were
no patient or surrogate interviews. These patients have missing sfdm2.


```
Table 1: Reference default values.
Baseline Variable Normal Fill-in Value
Serum albumin (alb) 3.
PaO2/FiO2 ratio (pafi) 333.
Bilirubin (bili) 1.
Creatinine (crea) 1.
bun 6.
White blood count (wblc) 9 (thousands)
Urine output (urine) 2502
```

## 3 Requests

The dataset is provided as is. It is part of the project to develop a fully struc-
tured and correct analysis based on Machine Learning techniques and method-
ologies provided during lessons and laboratories.

### 3.1 Tasks

The project will consist of the following tasks:

- Perform a preliminary analysis of the data. For instance, but not limited
    to, visualize samples, identify if features are correlated, determine which
    are most correlated with the target class (for the regression task), and
    inspect the distribution of samples among classes;
- Develop a regression model to estimate the target variabletotcst. Compare
    different regression algorithms for this task, and eventually perform feature
    selection procedures;
- Develop a classification model to predict whether the patient has died by
    the end of 1994. Identify with a domain analysis which information can
    represent the target variable for this task. Compare different classification
    models, choosing the appropriate metrics.
- Perform a clustering analysis to understand whether we can identify sev-
    eral degrees of severity in the patients’ conditions based on the ordinal
    functional disability variablesfdm2. Compare the performance of different
    clustering algorithms and distance measures using the metrics presented
    during the course.

### 3.2 Submission

The final report should be sent by mail (to both the TAs and the lecturer)
before the student takes the written exam. You should:

- Create a Jupyter notebook to answer all the requests, using the libraries
    presented during the laboratory classes;


- Include Name, Surname, and Student ID in the notebook;
- You are free to use the structure that you prefer within the notebook.
    However, please use markdown cells (Cell>Cell Type>Markdown) to
    insert section titles and clearly identify the different requests. You are free
    to add subsections to make the notebook more readable;
- dd text cells (markdown) to briefly explain what you did and why, and to
    help you answer the requests;
- Check that the notebook can execute correctly before submitting your
    work. Press Kernel>Restart & Run All, and check that all cells execute
    correctly without errors;
- The output of notebook cells should be included in the submitted note-
    book.

## 4 Evaluation

The project evaluation is not performed based on the (clustering, classification,
and regression) scores you obtain in each request, but rather on the soundness
of your analysis and the choices you made to solve issues (if any) you may
encounter. A good project follows the evaluations discussed during the lectures
and lab sessions, while also adapting and integrating the analysis based on the
project. The following is the evaluation criterion used in the previous year’s
project. Notice that it may slightly vary in this year’s evaluation, but you can
use it as a rough reference.
Points for each task: Clustering, Classification, Regression.

- 0:Completely wrong, or one key concept is not taken into account;
- 1:Ok, but poorly discussed, e.g., just a copy-paste of labs with no comments,
or some conceptual errors;
- 2:Well done, good comments and analysis, adapted code/analysis, and in-
terpreted the results.


Penalties:
- 0:Does compile with no error;
- 0.5:Does not compile, but it is an easy fix to make it work;
- 1:Does not compile, and it would require more than 10 minutes of debugging
to fix the errors.

