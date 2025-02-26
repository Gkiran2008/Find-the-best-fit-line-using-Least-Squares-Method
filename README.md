# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:


```PYTHON

Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: KIRAN G
RegisterNumber:  212223040095
```

```PYTHON

import numpy as np
import matplotlib.pyplot as plt

#INPUT ARRRAY A AND Y
x=np.array(eval(input()))
y=np.array(eval(input()))


x_mean=np.mean(x)
y_mean=np.mean(y)
print(x_mean)
print(y_mean)



num,denom=0,0
for i in range(len(x)):
    num+=((x[i]-x_mean)*(y[i]-y_mean))
    denom+=(x[i]-x_mean)**2
m=num/denom
b=y_mean - m*x_mean
print(m,b)


y_prediction=m*x+b
y_prediction

plt.scatter(x,y,color='orange')
plt.plot(x,y_prediction,color='green')
plt.show()

print(m*3+b)
```

## Output:


![{FFBC5711-2574-44A8-8D25-E222179066C2}](https://github.com/user-attachments/assets/c5655750-b5f1-427a-9478-d7da7916dbac)


![{EF3788C7-2203-487F-8D98-F12B49785607}](https://github.com/user-attachments/assets/a4028ebd-4cfa-43f8-99c5-e09e1a54c205)


![{1490A683-2A81-4510-970B-40FE27FBD447}](https://github.com/user-attachments/assets/63824c44-b8fa-4e64-8341-70b686d18ddd)


![{63FE1A24-DB70-457A-8D42-A9D3136328BB}](https://github.com/user-attachments/assets/c47507c7-ba27-4fe9-8a9e-bf3005361ff0)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
