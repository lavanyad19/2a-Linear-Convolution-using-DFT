EXPT 2a: LINEAR CONVOLUTION-USING-DFT
### AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

### APPARATUS REQUIRED
PC installed with SCILAB

### PROGRAM:
LINEAR CONVOLUTION
```
clc;
clear;
x = [1 1 1 1];
h = [1 2 3 4];
m = length(x);
n = length(h);
a=0:1:m-1;
b=0:1:n-1;
subplot(3,1,1);
plot2d3(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b,h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
for i = 1: n+m-1
conv_sum = 0;
for j = 1:i
if (((i-j+1) <= n)&(j <=m))
conv_sum = conv_sum + x(j)*h(i-j+1);
end;
y(i) = conv_sum;
end;
end;
disp(y,'Convolution Sum using Direct Formula Method = ')
subplot(3,1,3);
plot2d3(y)
title('Graphical Representation of output Signal y');
```
### CALCULATIONS:

<img width="322" height="615" alt="image" src="https://github.com/user-attachments/assets/ed1791e9-b316-4dd5-87d1-7d294e6382f2" />
<img width="327" height="596" alt="image" src="https://github.com/user-attachments/assets/aad9b68a-2da3-4819-a3da-20d22027e9d0" />

### SAMPLE OUTPUT:

<img width="346" height="377" alt="image" src="https://github.com/user-attachments/assets/cf7156c1-4b89-43a3-8162-a55e98a6fac4" />

### RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
