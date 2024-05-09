# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```

'''
Program to implement univariate Linear Regression to fit a straight line using least square
Developed By: G. Pradeep Kumar
Register Number: 212223230150
'''

import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)


plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()

```
## Output

</br>![Screenshot 2024-05-09 201225](https://github.com/pradeep23014186/Univariate-Linear-Regression/assets/152294642/720342e6-e144-44ed-add3-e419a6593bc0)

</br>![Screenshot 2024-05-09 201249](https://github.com/pradeep23014186/Univariate-Linear-Regression/assets/152294642/55a7428e-1dcb-46cb-9de8-733f4a6364d4)

</br>![Screenshot 2024-05-09 201308](https://github.com/pradeep23014186/Univariate-Linear-Regression/assets/152294642/9f171ff7-114f-4cdf-aeb5-6e522a51f49e)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
