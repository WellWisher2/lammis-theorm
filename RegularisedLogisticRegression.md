# 4.RegularisedLogisticRegression.md

```

from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.preprocessing import StandardScaler
from sklearn.pipeline import make_pipeline
from sklearn.metrics import confusion_matrix



iris=load_iris()
x=iris.data
y=iris.target



x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=42) 
pl=make_pipeline(StandardScaler(), LogisticRegression(C=1e4,max_iter=1000)) pl.fit(x_train,y_train)

acc=pl.score(x_test,y_test)11 print('Classification accuracy:', acc)

y_pred=pl.predict(x_test) cm=confusion_matrix(y_test,y_pred)

cm
```
