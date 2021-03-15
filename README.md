# 699 Final Project

Hello, my name is Matthew Hui and I am a current Master's student at the University of San Francisco studying data science. This repository is for my Machine Learning Lab class where we explored the various functionalities of scikit-learn and how to use it in the data science life cycle.

- You can find a link to the [data here](https://www.kaggle.com/arashnic/hr-analytics-job-change-of-data-scientists)
- You can find a link to my code in [DeepNote here](https://deepnote.com/project/3d577cd0-4e74-4b55-beaf-ba4ec1241d48#%2Fnotebook.ipynb) or download it from the repository.

# Data
This dataset contains information on various candidates who signed up for a company's Data Science course. The  company is trying to figure out which of these candidates took the course to learn new skills and which ones are looking for a new job. The dataset contains ~19,000 rows and 14 columns.

# Feature Engineering
The dataset contains missing values so I used a simple imputer (impute median values for continuous variables and impute 'unknown' for discrete variables). I also used both ordinal encoding and one hot encoding on the data.

# Algorithms
I performed a hyperparameter search using randomized search. The hyperparameters I tried tuning are:
- Criterion: The two criterion are two different functions that determine how good a split is.
- Max Depth: Limits the number of splits each tree can have (prevents overfitting)
- Min Samples Split/Min Samples Leaf: Have similar uses: once a leaf node is small enough stop fitting (prevents overfitting)
- Max Features: The amount of features the tree can consider (by taking a subset it prevents all trees to look the same)
- Class Weight: Takes into account the proportion of the target (deals with the slight data imbalance problem)
- N Estimators: Number of trees produced gives better generalization to the model

# Final Model
- RandomForestClassifier
- class weight: balanced
- max depth: 200
- min samples leaf: 3
- min samples split: 5
- number of estimators: 200

# Evaluation Metrics
Accuracy: 79% | Precision: 56% | Recall: 75%

# Conclusion
Model functionality:
- Reduce time and resouces spent on hiring process
- With accurate predictions, company will not reach out to people who are not interested

Next steps:
- create more features
- sacrifice some recall for better precision





