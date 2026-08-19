# EXP 1 B :  ANALYSIS OF DFT WITH AUDIO SIGNAL

# AIM: 

  To analyze audio signal by removing unwanted frequency. 

# APPARATUS REQUIRED: 
   
   PC installed with SCILAB/Python. 

# PROGRAM: 
```
clc;
clear;

Fs = 8000;             
t = 0:1/Fs:1-1/Fs;     


x = sin(2*%pi*500*t) + 0.5*sin(2*%pi*1500*t);


N = length(x);
X = fft(x);


f = (0:N-1)*(Fs/N);

// Plot DFT
plot(f(1:N/2), abs(X(1:N/2)));
xlabel("Frequency (Hz)");
ylabel("Magnitude");
title("DFT Analysis of Audio Signal");
xgrid();

disp("Sampling Frequency = ");
disp(Fs);

disp("Number of Samples = ");
disp(N);

```


# OUTPUT: 
<img width="760" height="718" alt="image" src="https://github.com/user-attachments/assets/663f5bf1-e5b1-4aa5-9b92-550eb9f1ad68" />


# RESULTS
Thus, the audio-like signal was successfully analyzed using DFT, and the frequency components present in the signal were identified.
