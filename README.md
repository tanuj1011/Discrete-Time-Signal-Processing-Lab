# EXP 1 B :  ANALYSIS OF DFT WITH AUDIO SIGNAL

# AIM: 

  To analyze audio signal by removing unwanted frequency. 

# APPARATUS REQUIRED: 
   
   PC installed with SCILAB/Python. 

# PROGRAM: 
```
clc;
clear;

// Generate audio-like signal
Fs = 8000;
t = 0:1/Fs:1-1/Fs;

// Desired + unwanted frequency
x = sin(2*%pi*500*t) + 0.5*sin(2*%pi*1500*t);

N = length(x);

// DFT of audio signal
X = fft(x);

// Frequency axis
f = (0:N-1)*(Fs/N);

// Display DFT
plot(f(1:N/2), abs(X(1:N/2)));
xlabel("Frequency (Hz)");
ylabel("Magnitude");
title("DFT Analysis of Audio Signal");
xgrid();

// Remove unwanted frequency
X(1501) = 0;
X(N-1500) = 0;

// Inverse DFT
y = real(ifft(X));

disp("Sampling Frequency = ");
disp(Fs);

disp("Number of Samples = ");
disp(N);
```

# OUTPUT: 
<img width="762" height="699" alt="image" src="https://github.com/user-attachments/assets/aba0de83-ae57-4bcc-ae66-cdfc1ae93b33" />


# RESULTS
Thus, the audio signal was successfully analyzed using DFT, and the unwanted frequency component was removed successfully.
