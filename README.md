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
#Program for Univariate linear regression using the least squares method.
#Developed by: Keerthika N 
#RegisterNumber: 21000385
import numpy as np
import matplotlib.pyplot as plt
# Preprocessing Input data

X = np.array(eval(input()))
Y = np.array(eval(input()))

# Building the model
# write your code here
Xmean=np.mean(X)
Ymean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-Xmean)*(Y[i]-Ymean)
    den+=(X[i]-Xmean)**2
m=num/den
c=Ymean-m*Xmean
print (m, c)

#Predict the output
Y_pred=m*X+c
print (Y_pred)
plt.scatter(X,Y)
plt.plot(X,Y_pred,color='red')
plt.show()



```
## input
![uni sam](https://github.com/vinodhini-17/Univariate-Linear-Regression/assets/145742741/908da1cd-8e07-4df5-8c21-03d558d7003e)


## Output

![uni out](https://github.com/vinodhini-17/Univariate-Linear-Regression/assets/145742741/805c0539-8b74-4c0b-8446-2799dc668e93)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
