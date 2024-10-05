# Source 1
**source** : chatgpt
###### Key Considerations

1. **Business Objectives**: The selection of modeling techniques should align with the business goals established in the earlier phases. Understanding the specific problem to be solved will guide which models are most suitable
2. **Data Characteristics**: Analysts must consider the nature of the data, including:
    
    - Types of variables (categorical, continuous)
    - Distribution of data
    - Presence of missing values
    - Data quality and completeness
    
3. **Model Interpretability**: Organizations often prefer models that are easy to interpret. For instance, decision trees or logistic regression may be favored over more complex models like neural networks, especially in contexts where stakeholders need to understand the decision-making process
4. **Available Tools and Techniques**: The choice of modeling techniques may also depend on the tools available within the organization. Certain software packages may offer specific algorithms that are easier to implement or more suited to the data at hand

###### Steps in Selecting Techniques

1. **Review Project Goals**: Revisit the objectives outlined during the Business Understanding phase to ensure alignment with selected modeling techniques
2. **Explore Available Techniques**: Identify a range of potential modeling techniques suitable for the data type and business problem. Common techniques include:
    
    - Regression analysis
    - Classification algorithms (e.g., decision trees, SVM)
    - Clustering methods (e.g., k-means)
    - Ensemble methods (e.g., random forests)
    
3. **Document Assumptions**: Each modeling technique comes with underlying assumptions (e.g., linearity for regression). Document these assumptions to ensure that they are met during model application
4. **Prototype Models**: Build initial prototypes using selected techniques to evaluate their performance against predetermined metrics (e.g., accuracy, precision). This step often involves creating baseline models for comparison
5. **Iterate and Refine**: Based on performance assessments, iterate on model selection and refinement. This may involve returning to earlier phases for additional data preparation or exploring alternative techniques if initial models do not meet expectations

###### Deliverables from the Modeling Phase

- **Modeling Technique Report**: A document specifying the chosen modeling techniques, including rationale and assumptions.
- **Test Design**: A plan outlining how models will be trained and tested, ensuring that training and testing datasets are appropriately managed to avoid overfitting
- **Model Descriptions**: Detailed descriptions of each model built, including parameters used and any challenges encountered during development

In summary, selecting modeling techniques in CRISP-DM is a structured yet flexible process that requires careful consideration of business objectives, data characteristics, interpretability, and available tools. The iterative nature of this phase allows for continuous improvement and adaptation throughout the data mining project lifecycle.

# Source 2
souce: 


Modelling Phase (Fase Pemodelan) 
a. Pilih dan aplikasikan teknik pemodelan yang sesuai b. Kalibrasi aturan model untuk mengoptimalkan hasil. 
c. Perlu diperhatikan nahwa beberapa teknik mungkin digunakan untuk permasalahan data mining yang sama. 
d. Jika diperlukan, prses dapat kembali ke fase pengolahan data ke dalam bentuk yang sesuai dengan spesifikasi kebutuhan teknik data mining tertentu. 


# Source 3: Modelling asumption
source: chatgpt
When choosing a modeling technique in machine learning, it's essential to consider various modeling assumptions. These assumptions can significantly impact the performance and interpretability of the model. Here are some key assumptions to keep in mind:

1. **Linearity**:
    
    - Some models, like linear regression, assume a linear relationship between features and the target variable. If this assumption is violated, a non-linear model might be more appropriate.
2. **Independence of Errors**:
    
    - Many models assume that the residuals (errors) are independent and identically distributed. If there's correlation in the errors (as in time series data), this assumption may not hold.
3. **Normality of Errors**:
    
    - Techniques like linear regression assume that the residuals follow a normal distribution. If the errors are not normally distributed, it could affect hypothesis testing and confidence intervals.
4. **Homoscedasticity**:
    
    - This assumption states that the variance of the residuals should be constant across all levels of the independent variables. If the variance changes (heteroscedasticity), it can lead to inefficient estimates.
5. **No Multicollinearity**:
    
    - Some models assume that features are not highly correlated with each other. Multicollinearity can make coefficient estimates unstable and difficult to interpret.
6. **Sufficient Sample Size**:
    
    - Certain models require a minimum amount of data to ensure robust training and generalization. Smaller datasets can lead to overfitting, especially in complex models.
7. **Data Distribution**:
    
    - Some algorithms assume specific distributions of the input data (e.g., Gaussian distribution in Naive Bayes). Understanding your data's distribution can guide your choice of model.
8. **Feature Scaling**:
    
    - Many models (like K-nearest neighbors or support vector machines) are sensitive to the scale of input features. Ensuring proper scaling or normalization may be necessary.
9. **Outliers**:
    
    - Some techniques are sensitive to outliers, which can skew results. It's essential to identify and handle outliers appropriately based on the chosen model.
10. **Time Dependencies**:
    
    - In time series forecasting, it's crucial to consider that observations may be dependent over time. Models like ARIMA specifically account for these dependencies.

By carefully considering these assumptions, you can choose a modeling technique that aligns well with your data and the specific problem you are addressing, leading to better performance and interpretability.

# Source 4: all by perplex
## Overview of CRISP-DM Modeling Phase

The CRISP-DM (CRoss Industry Standard Process for Data Mining) methodology is a widely recognized framework for managing data mining projects. It is structured into six phases, with each phase serving distinct purposes while allowing for flexibility and iteration throughout the project lifecycle. The **Modeling Phase** is the fourth step in this process, focusing on selecting and applying modeling techniques to address the defined business problem.

## Phases of CRISP-DM

1. **Business Understanding**: Define project objectives and requirements from a business perspective.
2. **Data Understanding**: Collect, explore, and verify the data.
3. **Data Preparation**: Clean and prepare the data for modeling.
4. **Modeling**: Select and apply modeling techniques.
5. **Evaluation**: Assess the model's effectiveness against business objectives.
6. **Deployment**: Implement the model in a production environment.

## Key Aspects of the Modeling Phase

The Modeling Phase involves several critical tasks aimed at developing a robust model based on the prepared dataset:

- **Model Selection**: Choose appropriate modeling techniques based on the understanding gained from previous phases. Common techniques include regression, classification, clustering, and decision trees[2](https://datalabnotes.com/crisp-dm-model-building/)[4](https://www.datascience-pm.com/crisp-dm-2/).
- **Building Models**: Construct models using selected techniques. This includes:
    
    - Developing baseline models
    - Experimenting with additional models to improve performance
    - Tracking experiments to compare results[2](https://datalabnotes.com/crisp-dm-model-building/).
    
- **Parameter Tuning**: Optimize model parameters to enhance accuracy and performance. This may involve adjusting settings or conducting statistical hypothesis testing to validate assumptions about the data[2](https://datalabnotes.com/crisp-dm-model-building/)[4](https://www.datascience-pm.com/crisp-dm-2/).
- **Model Assessment**: Evaluate the models using predefined metrics to determine their effectiveness in solving the business problem. This includes analyzing performance indicators such as accuracy, precision, recall, and F1 score[2](https://datalabnotes.com/crisp-dm-model-building/)[4](https://www.datascience-pm.com/crisp-dm-2/).

## Outputs of the Modeling Phase

The outputs produced during this phase are essential for documenting the modeling process and guiding subsequent evaluations:

1. **Modeling Technique Documentation**: Record details about the chosen modeling techniques, including rationale and underlying assumptions[2](https://datalabnotes.com/crisp-dm-model-building/).
2. **Test Design**: Outline plans for training, testing, and evaluating models, including hypotheses being tested[2](https://datalabnotes.com/crisp-dm-model-building/).
3. **Model Evaluation Reports**: Generate reports summarizing model performance and insights gained during testing[2](https://datalabnotes.com/crisp-dm-model-building/)[4](https://www.datascience-pm.com/crisp-dm-2/).

## Iterative Nature of CRISP-DM

One of the defining features of CRISP-DM is its iterative nature. It is common for data scientists to revisit earlier phases based on findings during modeling. For instance, insights gained may necessitate further data preparation or adjustments in understanding data characteristics[1](https://www.scielo.org.mx/scielo.php?pid=S1405-55462023000300675&script=sci_arttext)[4](https://www.datascience-pm.com/crisp-dm-2/). This flexibility allows teams to refine their approach continually until they achieve satisfactory model performance.

## Conclusion

The Modeling Phase of CRISP-DM is pivotal in transforming prepared data into actionable insights through effective modeling techniques. By systematically selecting, building, and evaluating models, practitioners can ensure that their solutions align with business objectives while remaining adaptable to new findings throughout the project lifecycle.


# source 5
source : [Crisp DM methodology - Smart Vision Europe](https://www.sv-europe.com/crisp-dm-methodology/#four)
## STAGE FOUR – MODELLING

### Select modeling technique

As the first step in modelling, you’ll select the actual modelling technique that you’ll be using. Although you may have already selected a tool during the business understanding phase, at this stage you’ll be selecting the specific modelling technique e.g. decision-tree building with C5.0, or neural network generation with back propagation. If multiple techniques are applied, perform this task separately for each technique.

- **Modelling technique** – Document the actual modelling technique that is to be used.
- **Modelling assumptions** – Many modelling techniques make specific assumptions about the data, for example that all attributes have uniform distributions, no missing values allowed, class attribute must be symbolic etc. Record any assumptions made.

### Generate test design

Before you actually build a model you need to generate a procedure or mechanism to test the model’s quality and validity. For example, in supervised data mining tasks such as classification, it is common to use error rates as quality measures for data mining models. Therefore, you typically separate the dataset into train and test sets, build the model on the train set, and estimate its quality on the separate test set.

- **Test design** – Describe the intended plan for training, testing, and evaluating the models. A primary component of the plan is determining how to divide the available dataset into training, test and validation datasets.

### Build model

Run the modelling tool on the prepared dataset to create one or more models.

- **Parameter settings** – With any modelling tool there are often a large number of parameters that can be adjusted. List the parameters and their chosen values, along with the rationale for the choice of parameter settings.
- **Models** – These are the actual models produced by the modelling tool, not a report on the models.
- **Model descriptions** – Describe the resulting models, report on the interpretation of the models and document any difficulties encountered with their meanings.

### Assess model

Interpret the models according to your domain knowledge, your data mining success criteria and your desired test design. Judge the success of the application of modelling and discovery techniques technically, then contact business analysts and domain experts later in order to discuss the data mining results in the business context. This task only considers models, whereas the evaluation phase also takes into account all other results that were produced in the course of the project.

At this stage you should rank the models and assess them according to the evaluation criteria. You should take the business objectives and business success criteria into account as far as you can here. In most data mining projects a single technique is applied more than once and data mining results are generated with several different techniques. 

- **Model assessment** – Summarise the results of this task, list the qualities of your generated models (e.g.in terms of accuracy) and rank their quality in relation to each other.
- **Revised parameter settings** – According to the model assessment, revise parameter settings and tune them for the next modelling run. Iterate model building and assessment until you strongly believe that you have found the best model(s). Document all such revisions and assessments.


# source 6
source: [CRISP-DM, Phase 4: Model Building - Data Lab Notes](https://datalabnotes.com/crisp-dm-model-building/#)

## Review of CRISP-DM

CRISP-DM stands for the [CRoss Industry Standard Process for Data Mining](https://datalabnotes.com/crisp-dm-101-what-is-it/). It is a 6-phase process model for data mining projects developed in the late 1990s and early 2000s by a consortium of companies funded by the European Union. The goal of the consortium was to develop a standardized process for data mining that could be used across industries.

Fast forward to today, the CRISP-DM model has received only minor updates since it was first developed, yet remains the most cited data science lifecycle model in academic papers and among practitioners.

Here are some links to previous posts on CRISP-DM:

- [Why is CRISP-DM important for Data Scientists](https://datalabnotes.com/data-science/crisp-dm/crisp-dm-a-data-scientists-secret-weapon/) to learn?
- [CRISP-DM Phase 1: Business/Problem Understanding](https://datalabnotes.com/data-science/crisp-dm/business-understanding-for-data-professionals/)
- [CRISP-DM Phase 2: Data Understanding](https://datalabnotes.com/data-science/crisp-dm/data-understanding-crisp-dm/)
- [CRISP-DM Phase 3: Data Preparation](https://datalabnotes.com/data-science/crisp-dm/data-preparation-crisp-dm/)
- [All the CRISP-DM Things](https://www.datalabnotes.com/crisp-dm)

## Overview of data modeling

Data Modeling is the fourth phase of CRISP-DM. This is the point in the project where you fit a mathematical or visual model to the data to accomplish a task, answer a question, or solve a specific problem.

If you’re following the CRISP-DM model, then you will already have a clear idea of the business problem, an understanding of the datasets and how they were generated, and some preprocessed data.

Specifically, you have

✅ Gained a solid understanding of the problem and how it is generally solved

✅ Talked to SMEs about variables and built some initial features in the data prep phase

✅ Explored the dataset and have an understanding of the distribution of the variables

✅ Quantified how much complete data you have, and some initial ideas about the limitations and biases of the datasets

✅ Verified that the data is accurate, complete, and consistent

Because of the work up to this point, you have confidence in the results gathered here and you are ready to build some models!

### Steps

![Process diagram of Phase 4: Model Building](https://i0.wp.com/datalabnotes.com/wp-content/uploads/CRISP-DM-Model-Building.jpg?resize=1024%2C576&ssl=1 "CRISP-DM Model Building")

In the image above, you can see the original subtasks and outputs for the Modeling Phase of CRISP-DM as outlined in 1999. I’ve deviated slightly from these subtasks in the steps below by adding some more specificity, but generally, the steps are the same.

Here are some general steps if you are building a machine learning model:

1. Revisit the stated project goals from Phase 1
2. Select the models for experiments based on your data understanding
3. Build a baseline model
4. Experiment with additional models and complexity
5. Track experiments
6. Assess the models

These steps can be framed differently if you are building a data visualization or a dashboard.

### Iteration

You can still expect some back and forth between the data preparation and model building phases. It’s likely that you will run into some questions and need to go back to the data understanding phase to fill in the gaps.

Even though we come to expect this as data professionals, this is one of the reasons that traditional software development methodologies, like SCRUM and Kanban, sometimes fail to support the data science process.

Sometimes, the data needs to be formatted differently to work with a model, i.e. through one-hot encoding, vectorizing text, discretizing ranges, etc. Other times, you may have follow-up questions about the behavior of certain variables. This is the iterative nature of data science and the CRISP-DM model allows for this iteration.

## Data Modeling Tasks

When working through the data modeling tasks, consider the following questions:

- What assumptions have been made about the data that are driving your analysis?
- What hypotheses will you be testing?
- What data will be used to test the models? Have you partitioned the data into train/test sets? (This is a commonly used approach in modeling.)
- Are there best practices established for creating train/test sets with the data you are using?
- In supervised learning, make sure to keep a validation set as well–this set is not used in the model development process and acts as “unseen” data to help evaluate how the model might perform once deployed.
- How many times are you willing to rerun a model with adjusted settings before attempting another type of model?

### 1. Revisit project goals

During the [Business Understanding Phase](https://datalabnotes.com/data-science/crisp-dm/business-understanding-for-data-professionals/), we discussed the goals of the project, including the type of problem we are solving: regression, classification, or clustering model. We also identified target variables and use-case-specific data mining goals.

Are we determining the probability that a part will fail within the next 1000 miles? Are we trying to predict monthly sales revenue? Are we trying to gain insights into our customer base?

When designing the experiment, determine how to report on metrics related to the business goals. If the goal is to predict the probability of part failure within the next 1000 miles, do you have enough historical data to create a robust train/test set that will actually contain failures? Will you need to wait for parts to fail to determine the goodness of your model?

### 2. Select modeling techniques

When making your model selection, it is important to take into account the potential impact of the following issues on your decision:

- Does the model require the data to be split into test and training sets? Is there a process in place for this or do you need to design the test/train/validation split? If so, try to design representative test/train sets and avoid data leakage.
- Do you have enough data to produce reliable results for a given model? In statistical analysis, you can consider the Power of the results. In machine learning, you need to generate confidence intervals or probabilities of likelihood to accompany predictions.
- Does the model require a certain level of data quality? Can you meet this level with the current data?
- Are your data the proper type for a particular model?
- What are the underlying assumptions of the chosen modeling technique? Some models require normally distributed data. Most time-series forecasting models require a constant frequency.
- Do you need to balance the data for rare events? This is common in fault prediction, fraud prediction and generally working with data that contains underrepresented groups.

### 3. Baseline model or benchmark?

Sometimes the term “baseline model” is confused with “benchmark”. So what is the difference?

A baseline model is a low-complexity model that you use to measure the effect and potentially justify the use of a more complex model.

A benchmark is usually used to compare your results to industry standards. In data science, you will often hear about benchmark datasets that are designed to measure model performance for a certain task.

For example, the MNIST data set is a benchmark dataset for the task of image and number recognition in computer vision. For time series anomaly detection, the NAB dataset is used as a benchmark to measure the accuracy of various anomaly detection models.

#### 

Baseline models are starting points

An important first step is to build a baseline model. This is a low-complexity model that is used to measure performance gains by more complex models. As you iterate through the model-building process, you perform experiments and build from low complexity to high complexity.

But, beware of the Complexity Tradeoffs! They go by many names:

- [Accuracy-Efficiency trade-off](https://arxiv.org/pdf/2007.02203.pdf)
- [Complexity-Interpretability trade-off](https://www.sciencedirect.com/science/article/pii/S016792362100066X)
- [Accuracy-Explainability trade-off](https://dl.acm.org/doi/fullHtml/10.1145/3531146.3533090)
- [Bias-Variance trade-off](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff)
- etc.

Additionally, adding too much complexity can be computationally inefficient, creating waste in the form of additional time and energy required to complete training or inference of the model. In a nutshell, when you add too much complexity to a machine learning model, you risk a number of things, so it is often preferred to start with the lowest complexity model possible.

Key things to keep in mind regarding the complexity of a model:

- How much data is required to train?
- How many parameters are included in the model?
- How many computational steps are required to train the model?
- How much computation is required to score new data?

#### 

Benchmarks are measuring sticks

Unlike baseline models, benchmarks are used to assess models and methods on how well they solve a general task such as digit identification or image recognition. In CRISP-DM, if it is your goal to create a state-of-the-art model to perform well on a general task, then keeping track of benchmarks would be important.

If you need to create or beat an existing benchmark, this should be discussed with stakeholders and documented in the project plan as a stated objective of the project.

Most of the time, companies and applied research projects are not focusing on developing general use case models and are more interested in how their models perform on the specific use case identified in phase one. For specific use cases, benchmarks are typically not useful, though you might be able to take a pre-trained, open-source model and fine-tune it for your use case.

### 4. Experiment with models & complexity

Plan ahead on how you will test the goodness of your model. Consider factors such as interpretability, accuracy, and efficiency.

The scientific method needs to be part of the model building process: Make a hypothesis about the underlying nature of the data, build a model that supports the hypothesis, starting with the baseline model and adding complexity from there.

Evaluate the pre-determined model “goodness” metrics to drive the scientific process.

### 5. Track experiments

Make sure to keep track of all of the metrics and hyperparameter information for each version of the model.

As you iterate through different modeling techniques, it is important to keep track of the models, the data used, the parameter settings, and the resulting metrics.

In the past, people used spreadsheets to keep track of these, but there are some open-source and automated tools that you can use now:

- [Weights and Biases](https://wandb.ai/)
- [Neptune.AI](https://neptune.ai/)
- [ML Flow](https://mlflow.org/)
- [TensorBoard](https://www.tensorflow.org/tensorboard)
- and many more.

This step is critical for creating reproducible results and for the next step: model evaluation.

### 6. Assess the models

You can assess the goodness of your model using different evaluation metrics. There are different metrics for different use cases, but they can generally be grouped based on the task: Regression or Classification.

#### Regression Metrics

In regression, we try to predict a numeric output. There are several statistical measures for quantifying the error of the predictions. Here are a few:

- **MSE**: Mean Squared Error (MSE) is the mean difference between the predicted and actual values.
- **RMSE**: Root Mean Squared Error (RMSE) is the square root of the MSE.
- **MAE**: Mean Absolute Error (MAE) between the predicted and actual values. This value is easy to interpret in business terms. If you are predicting a $12,000 outcome and the MAE is $500, that is easy to talk about with business stakeholders: Is the model good enough?
- **MAPE**: Mean Absolute Percentage Error (MAPE) is the mean absolute value percentage error between the predicted and actual values.
- **MSLE**: Mean Squared Logarithmic Error (MLSE) is the mean squared logarithmic error between the actual and predicted values.

#### Classification Metrics

In classification tasks, we predict labels for inputs. There are many ways to measure a classifier’s performance. Here are just a few:

- **Accuracy**: A simple ratio between # Correct / # Predicted.
- **Precision**: The ratio of True Positives to predicted positives, or the accuracy of the positive predictions.
- **Recall**: The ratio of true positives to predicted positives and false negatives. This is sometimes called the True Positive Rate and is used to assess the sensitivity of the model. It is a good measure for assessing an imbalanced dataset.
- **F1 score**: A harmonic mean of the Precision and Recall. This is a way to assess and compare classification models that takes both precision and recall into account.
- **Log-loss**: A value between 0 and 1 that provides a measure of how close the predicted value is to the actual value.

There are also some visual tools to evaluate these metrics for classification tasks:

- **Confusion Matrix**: A chart that shows the numbers of correct and incorrect labels per class.
- **Precision-Recall Curve**: A plot of precision versus recall for a range of k values where k is the number of predictions made.
- **AUC-ROC Curve**: This is the Area Under the ROC Curve. It shows the performance of the classifier across all possible decision thresholds.

#### Caveats

There are some caveats to using the metrics listed above. To avoid these pitfalls, it is crucial to understand your data and be on the lookout for a few things:

**Unbalanced datasets**: These datasets have rare events or imbalanced classes. Rare events are common in fraud detection and predictive maintenance. Imbalanced classes are very common in data about people where groups are underrepresented.

**Overfitting**: Be skeptical when metrics are too good. It is possible that the model is overfitted to the training data, making the metrics look great. The consequence of this is usually poor performance on real data.

**Outliers**: Outliers can have an impact on your model metrics, but it’s not always necessary or recommended to remove them. Sometimes, there are alternative modeling methods that are robust to outliers that can be used.

**Training versus Evaluation Metrics**: During training, we use a loss function to optimize the model. Then, we assess the model using evaluation metrics. It’s best to keep these more or less the same.

## Model building phase outputs

Each task in the CRISP-DM model building phase has recommended outputs. In the Model Building phase, these are the recommended outputs:

### 1. Modeling technique

Document the actual modeling technique or techniques that you have chosen. Include your rationale about why the techniques were chosen.

Include information about any underlying assumptions that are made in order to use the techniques. Did you conduct any statistical hypothesis testing to validate your assumptions? What was your hypothesis about the nature of the data that led to the model choice? Make sure to include the details here.

### 2. Test design

Describe the plan for training, testing, and evaluating the models. Include the hypotheses that are being tested and the results.

### 3. Parameter settings

When using a modeling tool, there are typically numerous parameters that can be customized. Keep track of the selected parameter values and explain the reasoning behind each choice.

### 4. Models

The models are an important output of this phase. These may be saved within a modeling tool, or saved to a file system, but should have a clear naming convention.

### 5. Model description

Begin developing both technical and non-technical descriptions of the models. The descriptions help promote transparency of the models and aid end-users, stakeholders, and developers in understanding the models.

The descriptions should include the strengths and weaknesses of the models, experiment metrics, and information about any biases or blindspots in the model.

Researchers at Google developed Model Cards to help standardized transparent [documentation of machine learning models](https://modelcards.withgoogle.com/about).

## Next step: model evaluation

Once you have preformed the experiments and tracked the model metadata, it is time for [Model Evaluation, Phase 5 of CRISP-DM](https://datalabnotes.com/crisp-dm-model-business-evaluation/).

Get ready to evaluate the goodness of the model, evaluation of how well the model solves the business problem, and perform an internal Audit of the model.

## Conclusion

In this post, we looked at the model building process from a very high level and walked through some specific tasks and considerations that should be made at this step. You should have enough information to make a model development game plan for your project!

Developing the Machine Learning model during a data science project sometimes seems like the main event, but experience and research will tell that building ML models can actually be a very [small part of the whole project lifecycle](https://papers.nips.cc/paper_files/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html).

[![image depicting various sized boxes representing parts of the machine learning ecosystem. the smallest box in the middle is called "ML Code". The Caption reads: "Figure 1: Only a small fraction of real-world ML systems is composed of the ML code, as shown by the small black box in the middle. The required surrounding infrastructure is vast and complex."](https://i0.wp.com/datalabnotes.com/wp-content/uploads/Screen-Shot-2023-05-02-at-8.56.07-AM.png?resize=1130%2C440&ssl=1)](https://i0.wp.com/datalabnotes.com/wp-content/uploads/Screen-Shot-2023-05-02-at-8.56.07-AM.png?ssl=1 "hidden_debt_of_ML_systems")

From a 2015 paper by Google researchers called "Hidden Technical Debt in Machine Learning Systems."

New tools spring up constantly to help automate time-consuming parts of data science, but automation does not remove the necessity of the time spent in understanding the problem and the data before diving into modeling.


# Source 7
source: [What is CRISP DM? - Data Science Process Alliance](https://www.datascience-pm.com/crisp-dm-2/)

### IV. Modeling

What is widely regarded as data science’s most exciting work is also often the shortest phase of the project. Here you’ll likely build and assess various models based on several different modeling techniques. This phase has four tasks:

1. **Select modeling techniques:** Determine which algorithms to try (e.g. regression, neural net).
2. **Generate test design:** Pending your modeling approach, you might need to split the data into training, test, and validation sets.
3. **Build model:** As glamorous as this might sound, this might just be executing a few lines of code like “reg = LinearRegression().fit(X, y)”.
4. **Assess model:** Generally, multiple models are competing against each other, and the data scientist needs to interpret the model results based on domain knowledge, the pre-defined success criteria, and the test design.

Although the [CRISP-DM Guide](https://web.archive.org/web/20220401041957/https://www.the-modeling-agency.com/crisp-dm.pdf) suggests to “iterate model building and assessment until you strongly believe that you have found the best model(s)”, in practice teams should continue iterating until they find a “good enough” model, proceed through the CRISP-DM lifecycle, then further improve the model in future iterations.


# Modeling

| A                | B                 | C                       |
| ---------------- | ----------------- | ----------------------- |
| Model Selection  | Choose model      | Select Model technieque |
| Building Models  | Model calibration | Generate test design    |
| Parameter Tuning | business goals    | build model             |
| Model Assessment | iteration         | asses model             |
|                  |                   |                         |