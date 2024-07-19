# Decision Tree

```
import pandas as pd
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score,confusion_matrix
from sklearn.model_selection import train_test_split


df=pd.DataFrame(data)
df=pd.get_dummies(df,columns=['Price','Maintenance','Airbag'])
X=df.drop('Profitable',axis=1)
y=df['Profitable']
X_train,X_test,y_train,y_test=train_test_split(X,y,test_size=0.2,random_state=42)
clf=DecisionTreeClassifier(criterion='entropy')
clf.fit(X_train,y_train)
y_pred=clf.predict(X_test)
acc=accuracy_score(y_test,y_pred)
print("accuracy:",acc)
cm=confusion_matrix(y_test,y_pred)
cm
```
