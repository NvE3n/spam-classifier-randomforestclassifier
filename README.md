# spam-classifier-randomforestclassifier
 
This is a simple machine learning model check emails weather it is spam or non-spam. I used tree classification models, linear models and ensemble models as well.

```python
#import libraries for model development
from sklearn.tree import DecisionTreeClassifier
from sklearn.neighbors import KNeighborsClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.ensemble import AdaBoostClassifier, GradientBoostingClassifier, BaggingClassifier,RandomForestClassifier
```

## Used machiene learning model accuracies

> [!NOTE]
> Below model accuracies will be changed.

### Ensemble Models
```
AdaBoostClassifier         - 0.9112221740038897    
GradientBoostingClassifier - 0.9257498754359741
BaggingClassifier          - 0.9203716026166482
RandomForestClassifier     - 0.9341813330761688
```

### Tree Models
```
DecisionTreeClassifier - 0.8886299564427729
```

### Linear Models
```
LogisticRegression - 0.8823480720703344
```

## Hyperparameter-tuning

- The ***RandomForestClassifier*** model got the highest accuracy. Used it for further model development.

Used parameters :
```python
param_grid = {'n_estimators' : [100, 200, 300],
              'criterion' : ['gini', 'entropy', 'log_loss'],
              'max_depth' : [10,20,30]}
```

### Best Estimator :
```
RandomForestClassifier(criterion='entropy', max_depth=30, n_estimators=300)
```
#### Final accuracy : 0.963608 

Dataset from [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/94/spambase)
Special Thanks for @dineshpiyasamara and @UCI :shipit: 
