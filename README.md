# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
am=5.7;
fm=474;
ac=11.4;
fc=4740;
fs=47400;
b=5.5;
t=0:1/fs:3/fm;

m=am*cos(2*3.14*fm*t);
subplot(3,1,1);
plot(t,m);
title('Message signal');

c=ac*cos(2*3.14*fc*t);
subplot(3,1,2);
plot(t,c);
title('Carrier signal');

efm= ac*cos((2*3.14*fc*t)+b*sin(2*3.14*fm*t));
subplot(3,1,3);
plot(t,efm);
title('Frequency modulated signal');


Output Waveform
<img width="756" height="683" alt="image" src="https://github.com/user-attachments/assets/2a759d43-4df0-4b30-ba5a-1339a7f7e62f" />


Tabular Column
<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/05e08de9-0c1a-4926-94e0-50b0e83b433f" />



Calculation




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
