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
```

import numpy as np
import matplotlib.pyplot as plt


x=np.array(eval(input()))
y=np.array(eval(input()))

x_mean=np.mean(x)
y_mean=np.mean(y)

print(x_mean)
print(y_mean)

num,denom=0,0
for i in range(len(x)):
    num+= ((x[i]- x_mean)*(y[i]-y_mean))
    denom+= ((x[i]-x_mean)*(x[i]-x_mean))
    
m= num/denom
b= y_mean - m*(x_mean)

print("m= ",m)
print("b= ",b)

y_pred= m*x+b
y_pred

plt.scatter(x,y,color='black')
plt.plot(x,y_pred,color='yellow')
plt.show()

print(m*3+b)

#example x=10
y_ans= m*10+b
y_ans


/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: HARIPRASHAAD RA
RegisterNumber: 212223040060
*/
```

## Output:
![image](https://github.com/user-attachments/assets/fa4ace51-d2b2-494b-b15b-32924c586f56)
![image](https://github.com/user-attachments/assets/d2fa33a0-de77-4c68-a5f7-d3ffb1859d81)
![image](https://github.com/user-attachments/assets/abedb607-4ca0-4382-90ca-243870f0320a)
![image](https://github.com/user-attachments/assets/1fd672ed-1f03-4cce-ae96-d2eaed92a74f)
![image](https://github.com/user-attachments/assets/55055038-a06e-4785-84a7-2cb09de91ef4)
![image](https://github.com/user-attachments/assets/34479ab8-6a1d-4ce2-9fb3-c9f9bb0dbc20)





## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
