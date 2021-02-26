# Titanic
    
This notebook tries to figure out who survives on the Titanic. See the Kaggle challenge at https://www.kaggle.com/c/titanic/overview for more information on the competition related to this project.

The data have 891 observations with 10 features:

<ul>
<li>Pclass: Class of passenger (1st, 2nd, 3rd)</li>
<li>Name</li>	
<li>Sex</li>	
<li>Age</li>	
<li>SibSp: Number of siblings / spouses on board</li>	
<li>Parch: Number of parents / children on board</li>	
<li>Ticket</li>	
<li>Fare</li>	
<li>Cabin</li>	
<li>Embarked: Destination</li>
</ul>

From these features, I engineered new features:
<ul><li>Salutation: Status of passenger (i.e. Mr., Mrs., Miss). This was used for imputing missing ages.</li>
<li>Deck: Determined given the first letter of cabin number.</li>
<ul>

Six different machine learning models were chosen:
<ul>
    <li>Logistic Regression: Logistic models assign each observation to a binary outcome, which is helpful given our problem statement.</li>
    <li>Random Forest: Random forests are a series of decision trees with randomly chosen subsets of features. This takes the classic decision tree model and provides a more robust prediction.</li>
    <li>K-Nearest Neighbors: K-Nearest Neighbors is a classification algorithm that assigns classes based on observing the classes of other neighbors. It is useful in this dataset because similar observations are likely to have similar survival rates.</li>
    <li>Gradient Boosting Classifier: Gradient boosting models take a bunch of weak decision trees and builds on them iteratively, instead of growing full trees at once like in a random forest.</li>
    <li>Support Vector Machine</li>: Support vector machines produce a boundary vector with a maximum amount of separation between positive and negative classes. 
    <li>XGBoost</li>: XGBoost takes the gradient boosting classifier model with additional hyperparameters.
</ul>

The models were then combined to create a stacked classifier that ended up having a better prediction on the Kaggle test set than any of the individual models.


