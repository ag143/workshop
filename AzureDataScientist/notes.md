**Machine Learning** is the subfield of computer science that gives computers the ability to learn without being explicitly programmed
- process:
    - extraction of knowledge from data
    - learns from past behavior and make predictions or decisions
- benefits
    - faster decisions
    - Develop insights beyond human capabilities
    - Act at the right time and take advantage of opportunities , converting them into closed deals.
- 3 types:
    - **supervised** learning (solutions provided by parents)
        - Data is labelled
        - Input (set of) variable "X" and output variable "Y"
            - *y = f(x)*
        - the function is approximated to predict new values of Y given X
        -Examples
            - **Regression** - Output variable is a real value such as Amount, Height, Weight etc
            - **Classification** - Output variable is a category, such as Yes, No, Red, Blue, Yellow etc
    - **unsupervised** learning (make your own decision)
        - Only X or input variable is known
        - The goal is to model the underlying structure or distribution in the data in order to learn more about the data
        - Algorithms are left on their own to discover and present the interesting structure in the data
        - e.g.
            - Clustering Customer behaviour grouping
            - Association Recommendation model. (how a series of items can determine/incur another series of items)
    - **reninforement** learning
        - rewards good behavior and peranlizes bad ones
        - to maximise the gain or reward

====

aspects of data
- Types of variables
    - predictor/independent
    - target/dependent
- data type
    - character/string
    - numeric
- category
    - categorical
    - continuous

common terms
- **mean**
- **median**: Numerical Middle value of the sorted observations with
equal number of observations on both sides,
- **mode**: The value that appears most often in a set of data (众数)
- **range**: The difference of highest and lowest values in a sample of observations

**probability** is a numerical way of describing how likely something isgoing to happen.
- Sammple Space

Types of Models
1. Classification. (Identification of category of data)
    - Binary/Two Class Classification Either/Or, Yes or No type
    - Multi Class Classification One of the many alternatives
    - e.g.
        - Assigning a given email into "spam" or "non spam" classes Or Primary, Social or Promotionalemails
        - Will this customer default on loan repayment?
        - Will this customer buy my product?
1. Regression Analysis. (Estimating the relationships among variables)
    - Predictor is a continuous variables
    - e.g.
        - predicting the future sale of products
        - Computing fair price of the product or service
    - one of the most common methods used in Maching Learning
    - Infer causal realtionships between dependent and independent variable
    - if data is far/near to the Regression line, it is strong/weak realtion
1. Clustering. grouping a set of objects in such a way that objects in the same group (called a cluster) are more similar (in some sense or another) to each other than to those in other groups (clusters)
    - Unsupervised Learning model
    - e.g. Customers who make lot of long distance calls and don’t have a job. Who are they?
1. Anomaly Detection is the identification of items, events or observations which do not conform to an expected pattern or other items in a dataset.
    - e.g.
        - Bank fraud
        - Credit Card Fraud
        - Structural defect
        - Medical problems
    - also refered as outliers, novelties, noise, deviations and exceptions

workflow of Azure ML
1. Get the data
1. prepare the data
1. feature selection
    - Filter Based Feature Selection
    - Fisher Linear Discrminant Analysis
    - Permutation Feature Importance
1. choose and apply learning algorithms
1. train and evaluate the model
    1. train model
    1. score mode
    1. evaluate model

