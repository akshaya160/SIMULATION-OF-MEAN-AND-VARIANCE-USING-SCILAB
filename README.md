# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB
## AIM
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB


## ALGORITHM
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation
   
## PROCEDURE
•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated results


## PROGRAM
```

clear;
clc;
clear;
function z = f(x)
z = 3*(1-x)^3;
endfunction
a = 0;
b = 1;
EX = intg(a, b, f);
function z = c(y)
z = 3*(1-y)^3; 
EY = intg(a, b, c);
disp(EX, "i) Mean of X =");
disp(EY, "Mean of Y =");
function z = g(x)
z = 3*(1-x)^3 * x^2; 
endfunction
EX2 = intg(a, b, g);
function z = h(y)
z = 3*(1-y)^3 * y^2; 
endfunction
EY2 = intg(a, b, h);
vX2 = EX2 - (EX)^2; 
vY2 = EY2 - (EY)^2; 
disp(vX2, "ii) Variance of X");
disp(vY2, "Variance of Y");
x = input("Type in the reference sequence = ");
y = input("Type in the second sequence = ");
n1 = max(size(y)) - 1;
n2 = max(size(x)) - 1;
r = corr(x, y, n1);
plot2d3('gnn', r);

```

## CALCULATION

<img width="817" height="817" alt="image" src="https://github.com/user-attachments/assets/ed03cb5f-f140-4bfd-a1a2-57c5fcf2c8bb" />
<img width="295" height="871" alt="image" src="https://github.com/user-attachments/assets/69b827fe-2f4e-4411-97c3-69e3fc0cad75" />
<img width="303" height="813" alt="image" src="https://github.com/user-attachments/assets/83a88d49-0c36-4a1a-80af-a039b04839a2" />
<img width="287" height="820" alt="image" src="https://github.com/user-attachments/assets/8cdaa32a-fa4e-467b-9481-34cf7d930434" />
<img width="551" height="663" alt="image" src="https://github.com/user-attachments/assets/890dd14f-61b6-4ffa-b136-233dc2724bfe" />



## OUTPUT
```
Mean Values
Mean of X = 0.3011687
Mean of Y = 0.25
Variance Values
Variance of X = 0.0092974
Variance of Y = 0.0375000
Cross-Correlation Input Example
Reference sequence: [1, 2, 3, 4, 5, 6, 7, 8]
Second sequence: [2, 1, 3, 5, 6, 3, 5, 9]
```
<img width="610" height="460" alt="image" src="https://github.com/user-attachments/assets/b6db4972-7fca-41fe-9700-83f44e1f8f8c" />
```

## RESULT
```
Thus the mean , variance and cross correlation are executed in Scilab and output is verified
```
