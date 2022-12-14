# Machine Learning - Supervised Learning
## Project: Finding Donors for CharityML

### Project Description
This is the supervised learning (2.0.0) project for the Udacity Data Analyst Nanodegree. In this project, I used sklearn and supervised learning techniques on data collected from the U.S. census to help a fictitious charity organization (CharityML) identify people most likely to donate based on their income. I start by exploring the data to understand the type of data being used. I then prepare the data by transforming skewed continuous features, normalizing numerical features, and converting non-numeric features (catagorical variable) into numerical values. I then split the data, 80% for training and 20% for testing.

I then investigate four different algorithms (Naive Predictor, Gradient Boosting, K-Nearest Neighbors, and Logistic Regression) to determine which is best at modeling the data. Based on model accuracy, F-score and training/testing speed, I decide to use Gradient Boosting as my algorithm. I improve the results by using GridSearchCV and adjusting the parameters of the algorithm. Finally, I explore what happens to model accuracy and F-score if I reduce the amount of training data to save time.

### Install
This project requires Python 3 and the following Python libraries to be installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)

You will also need to have software installed to run and execute an [iPython Notebook](http://ipython.org/notebook.html)

### Code
The main code for this project is located in the `finding_donors.ipynb` notebook file. Supporting code for visualizing the necessary graphs can be found in `visuals.py`. The `Report.html` file contains a snapshot of the main code in the jupyter notebook with all code cells executed.

### Run
In a terminal or command window, navigate to the top-level project directory `finding_donors/` (that contains this README) and run one of the following commands:

```bash
ipython notebook finding_donors.ipynb
```  
or
```bash
jupyter notebook finding_donors.ipynb
```
This will open the iPython Notebook software and project file in your browser.

### Data
The modified census dataset (`census.csv`) consists of approximately 32,000 data points, with each datapoint having 13 features. This dataset is a modified version of the dataset published in the paper "Scaling Up the Accuracy of Naive-Bayes Classifiers: a Decision-Tree Hybrid", by Ron Kohavi. You may find this paper [online](https://www.aaai.org/Papers/KDD/1996/KDD96-033.pdf), with the original dataset hosted on [UCI](https://archive.ics.uci.edu/ml/datasets/Census+Income).

### Features
- `age`: Age
- `workclass`: Working Class (Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked)
- `education_level`: Level of Education (Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool)
- `education-num`: Number of educational years completed
- `marital-status`: Marital status (Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse)
- `occupation`: Work Occupation (Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces)
- `relationship`: Relationship Status (Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried)
- `race`: Race (White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other, Black)
- `sex`: Sex (Female, Male)
- `capital-gain`: Monetary Capital Gains
- `capital-loss`: Monetary Capital Losses
- `hours-per-week`: Average Hours Per Week Worked
- `native-country`: Native Country (United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands)

### Target Variable

- income: Income Class (<=50K, >50K)
