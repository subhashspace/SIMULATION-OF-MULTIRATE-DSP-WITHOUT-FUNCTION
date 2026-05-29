## EXP 6 : Simulation of Multirate DSP using Decimation and Interpolation

### AIM: 

To perform and verify multirate DSP without function using SCILAB .

### APPARATUS REQUIRED: 
PC installed with SCILAB. 

### PROGRAM : 
```python
clc;
clear;
close;
// Generate sinusoidal signal
n = 0:%pi/20:2*%pi;
x = sin(n);
// Input factors
M = input("Enter the Downsampling factor M = ");
L = input("Enter the Upsampling factor L = ");
// Downsampling
downsampling_x = x(1:M:length(x));
// Upsampling
upsampling_x = zeros(1,length(x)*L);
for i = 1:length(x)
    upsampling_x((i-1)*L + 1) = x(i);
end
disp("Input Signal x(n) = ");
disp(x);
disp("Downsampled Signal = ");
disp(downsampling_x);
disp("Upsampled Signal = ");
disp(upsampling_x);
figure();
subplot(3,1,1)
plot2d3(n,x)
xlabel("n")
ylabel("Amplitude")
title("Original Sinusoidal Signal")
subplot(3,1,2)
plot2d3(1:length(downsampling_x),downsampling_x)
xlabel("n")
ylabel("Amplitude")
title("Downsampled Signal")
subplot(3,1,3)
plot2d3(1:length(upsampling_x),upsampling_x)
xlabel("n")
ylabel("Amplitude")
title("Upsampled Signal")
```

### OUTPUT: 
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/2fb57f3f-6df8-4c95-aac1-7c9a1f0e1ffb" />
<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/aa34365e-4004-4ad2-93a3-5197bd1713b6" />

### RESULT: 
Thus the decimation process by a factor M and interpolation process by a factor L using 
SCILAB was implemented. 
