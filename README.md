# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB-
__AIM:__

To write a program for mean, variance and cross correlation in SCILAB and verify the output. 

__EQUIPMENTS NEEDED:__

.Computer with i3 Processor 

.SCI LAB 

__ALGORITHM:__

1. Define the Function: Specify the function you want to simulate. For example, 
f(x)=sin⁡(x)f(x)=sin(x) or any other function. 
2. Generate Sample Points: Decide on the range and the number of sample points. Generate 
these sample points within the desired range. 
3. Evaluate the Function: Compute the function values at each of these sample points. 
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the 
mean and variance of the computed function values. 
5. Display Results: Output the computed mean variance and Cross Correlation 

__PROCEDURE:__ 

1.Refer Algorithms and write code for the experiment. 

2.Open SCILAB in System 

3.Type your code in New Editor 

4.Save the file 

5.Execute the code If any Error, correct it in code and execute again 
  
6.Verify the generated results

__PROGRAM:__
```
clear;
clc;

function z = f(x)
    z = 3*(1-x)^2;
endfunction

a = 0;
b = 1;
EX = intg(a, b, f);

function z = c(y)
    z = 3*(1-y)^2;
endfunction

EY = intg(a, b, c);

disp(EX, "Mean of X = ");
disp(EY, "Mean of Y = ");

function z = g(x)
    z = 3*(1-x)^2;
endfunction

EX2 = intg(a, b, g);

function z = h(y)
    z = 3*(1-y)^2;
endfunction

EY2 = intg(a, b, h);

vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;

disp(vX2, "Variance of X = ");
disp(vY2, "Variance of Y = ");

x = input("Enter reference sequence x = ");
y = input("Enter second sequence y = ");

n1 = max(size(y)) - 1;
r = corr(x, y, n1);

clf;
plot2d3(1:length(r), r);
```

__OUTPUT GRAPH:__
<img width="573" height="439" alt="image" src="https://github.com/user-attachments/assets/3560c340-7417-4eb8-8963-21ccf3911678" />

<img width="757" height="560" alt="image" src="https://github.com/user-attachments/assets/53d6115a-f1c0-42e9-8381-709ba43009b7" />

__RESULT:__

