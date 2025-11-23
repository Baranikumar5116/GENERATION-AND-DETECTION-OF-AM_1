# GENERATION-AND-DETECTION-OF-AM_1
## AIM:
To generate and detect the amplitude modulation and demodulation u s i n g S C I L A B and to calculate modulation index of AM.

## EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

## THEORY:
Modulation can be defined as the process by which the characteristics of carrier wave are varied in accordance with the modulating wave (signal). Modulation is performed in a transmitter by a circuit called a modulator.

Need for modulation is as follows:

•	Avoid mixing of signals

•	Reduction in antenna height

•	long distance communication

•	Multiplexing

•	Improve the quality of reception

•	Ease of radiation.

Amplitude Modulation is the process of changing the amplitude of a relatively high frequency carrier signal in proportion with the instantaneous value of the modulating signal. The output waveform contains all the frequencies that make up the AM signal and is used to transport the information through the system. Therefore the shape of the modulated wave is called the AM envelope. With no modulating signal the output waveform is simply the carrier signal. Coefficient of modulation is a term used to describe the amount of amplitude change present in an AM waveform. There are three degrees of modulation available based on value of modulation index.

1)	Under modulation :	m<1, Em < Ec
	
2)	Critical modulation: m-1, Em = Ec
  
3)	Over modulation:	m>1, Em > Ec

Note: Keep all the switch faults in off position

## ALGORITHM
1.	Define Parameters
   
    First, define the parameters for your signals:
    
    •	Carrier frequency (fc)
    
    •	Modulating signal frequency (fm)
    
    •	Sampling frequency (Fs)
    
    •	Duration of the signal (T)

2.	Create a time vector based on the sampling frequency and duration.
 
3.	Create Modulating Signal:Define the modulating signal (message signal).

4.	Create Carrier Signal:Define the carrier signal.

5.	Perform Amplitude Modulation:Multiply the carrier signal by the modulating signal plus 1 (to ensure the modulation depth).

6.	Plot the Signals:Visualize the modulating, carrier, and modulated signals.

7.	Demodulate the AM Signal:To demodulate, you can use envelope detection. One way is to rectify the signal and then apply a low-pass filter.

8.	Plot the Demodulated Signal:Visualize the demodulated signal.

9.	Compare Signals:Compare the original modulating signal with the demodulated signal.

 ## PROCEDURE
•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated waveform using Tabulation and Model Waveform

## MODEL GRAPH:
<img width="600" height="800" alt="image" src="https://github.com/user-attachments/assets/7bc77926-9c2a-42c6-994b-6c67433b11d2" />

## PROGRAM:
'''
Am = 7;
Ac = 14;
fm = 653;
fc = 6530;
fs = 653000;
t = 0:1/fs:2/fm;
m = Am * cos(2*3.14*fm*t);
c = Ac * cos(2*3.14*fc*t);
s = (Ac + m) .* cos(2*3.14*fc*t);
envelope_signal = abs(hilbert(s));
demod = envelope_signal - Ac;
subplot(4,1,1);
plot(t, m, 'b');
title('Message Signal');
xlabel('Time (s)');
ylabel('Amplitude');

subplot(4,1,2);
plot(t, c, 'r');
title('Carrier Signal');
xlabel('Time (s)');
ylabel('Amplitude');

subplot(4,1,3);
plot(t, s, 'k');
title('AM Modulated Signal');
xlabel('Time (s)');
ylabel('Amplitude');

subplot(4,1,4);
plot(t, demod, 'g');
title('Demodulated Signal');
xlabel('Time (s)');
ylabel('Amplitude');
'''

## TABULATION:

<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/b8d3d201-1925-408e-b1c5-5f460ad5e13b" />

## CALCULATION:


<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/01a9ab89-bd1e-473e-9e63-0a51129aa5f3" />


## OUTPUT:

<img width="878" height="748" alt="image" src="https://github.com/user-attachments/assets/076fbb99-4fb7-4763-977c-aae1b756a292" />

## RESULT:
Thus the amplitude modulation and demodulation is experimentally done and the output is verified.
