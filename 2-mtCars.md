# 2.MtCars

```
import numpy as np
import pandas as pd
from matplotlib import pyplot as plt
db=pd.read_csv('mtcars.csv')
db

db.keys()



x=db['mpg']
x

plt.figure(figsize=(6,6))
bin=[5,10,15,20,25,30,35,40]
plt.hist(x,bins=bin,color='skyblue',edgecolor='black')
plt.xlabel('Miles per gallon',fontsize=20)
plt.ylabel('Number of Vehicles',fontsize=20)
plt.title('vehicle / Miles per gallon',fontsize=20)
plt.show()
```
