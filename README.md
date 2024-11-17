# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import numpy as np
2. From sys package import Guassian
3. Get input from the user
4. Print result 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: SAI KUMAR S
RegisterNumber: 212222240087
import numpy as np
import sys
#reading number of unknowns 
n=int(input())
a=np.zeros((n,n+1))
#making numpy array of n x n+1 size and initializing 
#to zero for storing augmental matrix solution matrix 
x = np.zeros(n)

#reading augmented matrix coefficients
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())

# applying gauss elimination 
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by Zero deteceted!')

    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]

        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]

# back substitution
x[n-1] = a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    for j in range(i+1,n):
        x[i] = x[i] - a[i][j]*x[j]
    
    x[i] = x[i]/a[i][i]

# displaying solution 
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')
*/
```

## Output:

![Gaussian Elimination](https://github.com/Harish2404lll/Gaussian/assets/141472096/6b9c7b8b-bea1-430f-af10-6490dc6ae935)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

