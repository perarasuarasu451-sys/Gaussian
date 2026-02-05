# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy module to use the built-in functions for calculation 
2. Prepare the lists from each linear equations and assign in np.array() 
3. Using the np.zeros() and seprate them and use it in the for loops so we can find the solutions. 
4. End the program 

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: PERARASU K 25004665
RegisterNumber: 212225100034
'''
import sys
n=int(input())
a=[[float(input()) for j in range(n+1)] for i in range(n)]
x=[0]*n

for i in range(n):
    if a[i][i]==0:
        sys.exit("Divide by zero detected!")
    for j in range(i+1,n):
        r=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]-=r*a[i][k]
            
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]-=a[i][j]*x[j]
    x[i]/=a[i][i]
    
for i in range(n):
    print("X%d = %0.2f"%(i,x[i]),end=" ")
```

## Output:
![OUTPUT OF PROGRAM](<Screenshot 2026-02-05 211448.png>)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

