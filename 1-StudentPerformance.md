# 1. Student Performance

```
from matplotlib import pyplot as plt

x=[10,9,2,15,10,16,11,16]
y=[95,80,10,50,45,98,38,93]
plt.plot(x,y,color='r',marker='*',linestyle='solid')
plt.title("Student Performance")
plt.ylabel("Marks scored")
plt.xlabel("Number of hours spent for study")
plt.show()



paired = list(zip(x,y))
paired_sorted=sorted(paired)
x_sorted,y_sorted=zip(*paired_sorted)
x_sortred=list(x_sorted)
y_sortred=list(y_sorted)
print("Sorted x:",x_sorted)
print("Sorted y:",y_sorted)


from matplotlib import pyplot as plt
plt.plot(x_sorted,y_sorted,color='r',marker='*',linestyle='solid')
plt.title("Student Performance")
plt.ylabel("Marks scored")
plt.xlabel("Number of hours spent for study")
plt.show()

```
