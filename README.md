# BER-vs-SNR-in-BPSK
Bit Error Rate vs Signal to Noise Ratio in Binary Phase Shift Keying using Simulink
# Abstract
In a binary phase shift keying (BPSK) system, the bit error rate (BER) performance is dependent on the signal-to-noise ratio (SNR) of the received signal. Simulink, a simulation tool in MATLAB, can be used to analyze the BER versus SNR performance of a BPSK system.

The simulation model includes a Random Integer Generator, BPSK modulator, Rayleigh SISO Fading Channel, a math function, an additive white Gaussian noise (AWGN) channel, a product, BPSK demodulator and an Error Rate Calculation.

The transmitted signal is modulated using BPSK and passed through the AWGN channel to simulate the effects of noise. The received signal is demodulated using BPSK and compared to the original transmitted signal to calculate the BER.

By varying the SNR of the received signal, the simulation can generate a BER versus SNR plot. The plot shows the relationship between the BER and the SNR, where the BER decreases as the SNR increases. The plot can be used to evaluate the performance of the BPSK system and to determine the minimum required SNR for a specific BER.
# Binary Phase Shift Keying
BPSK is a digital modulation technique used in communication systems to transmit binary information over a channel. In BPSK, the information to be transmitted is represented by a binary sequence of 1s and 0s. The binary sequence is then modulated onto a carrier wave by shifting the phase of the carrier signal by 180 degrees for each binary symbol.

Mathematically, BPSK can be represented as:
s(t) = Acos(2πfct + π(1-m(t)))
where s(t) is the modulated signal, Ac is the amplitude of the carrier signal, fc is the frequency of the carrier signal, m(t) is the binary sequence of 1s and 0s, and π(1-m(t)) represents the phase shift of the carrier signal.

![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/93f5d297-6fb5-41cc-9db1-9b66934176fc)

![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/3e5f44c1-6bed-4c0d-bb8a-3cb8b8da6a5d)

![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/77e12f13-1c8c-4b34-b25a-c75711fd06ee)

# Bit Error Rate
It is a performance metric used to measure the quality of a digital communication system. BER represents the percentage of received bits that are in error compared to the transmitted bits.

In Binary Phase Shift Keying (BPSK) modulation, the BER represents the number of bit errors that occur in the received signal compared to the transmitted signal. The BER performance of a BPSK system is affected by various factors such as noise, interference, and fading in the communication channel.

The BER performance of a BPSK system can be mathematically expressed as:
BER = 0.5 * erfc(sqrt(Eb/N0))
where erfc is the complementary error function, Eb is the energy per bit, and N0 is the noise power spectral density.

The equation shows that the BER performance of a BPSK system is inversely proportional to the square root of the SNR. As the SNR increases, the BER decreases, and the quality of the received signal improves.

# Signal to Noise Ratio
The SNR represents the ratio between the signal power and the noise power in the received signal. The SNR performance of a BPSK system is an important factor in determining the quality and reliability of the communication system.
The SNR can be mathematically expressed as:
SNR = (Eb / N0) * Rb
where Eb is the energy per bit, N0 is the noise power spectral density, and Rb is the bit rate.
![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/8d34d2d5-da7f-4c9a-8da3-fbe684c60bec)

# Simulink
![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/1e3049bb-2049-4c22-b288-91bb3dd3f0c5)
![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/918efc4b-cedb-4d92-8837-9a979c94470e)
https://www.mathworks.com/products/simulink.html

# Simulation
![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/7567d52e-b127-4fef-a75a-71b3bd813cb0)
a) The model is set up as shown in the figure.

b) The "Random Integer" block generates random integers within a specified range.

c) Initial Seed is set as 73 on Rayleigh SISO Fading Channel.

d) The math function can be set to any function required.

e) Initial Seed is set as 67 on AWGN Channel.

f) In the Error Rate Calculation block, the Target number of errors is set as 100 and Maximum number of symbols as 1e4.

Write the command ‘bertool’ in the MATLAB command window to open the ‘Bit Error Rate Analysis Tool’ and set the parameters in the Monte Carlo Window for Eb/No as 1:0.5:20, link the correct Simulink model file, mention the BER variable name as given in the model, and set the simulation limits to Number of errors as 100 and Number of bits as 1e4. 

Leave the Theoretical Window as the default parameters
![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/e5955df6-007b-479c-94d7-17b591b45c95)

# Results
Theoretical Graph for BER vs SNR


![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/0c604190-f8ed-4f16-a30d-c812e9974ff6)

BER vs SNR for EbNo=20 with a 10^u math function block in the model
![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/c614f5dd-be19-439f-9398-b6cac1d0f2d8)
BER vs SNR for EbNo=50 with a 10^u math function block in the model
![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/42791421-f008-4a7a-be08-13ba90ded99f)
BER vs SNR for EbNo=1000 with a log u math function block in the model
![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/4857a13f-52f1-476a-950f-b2569ae0196e)
BER vs SNR for EbNo=20 with e^u math function block in the model
![image](https://github.com/KarthikT23/BER-vs-SNR-in-BPSK/assets/119528503/11e96ba4-0c5a-47c5-baa5-3c5c788856e3)

# References
[1] https://www.tutorialspoint.com/digital_communication/digital_communication_phase_shift_keying.htm

[2] https://www.mpirical.com/glossary/bpsk-binary-phase-shift-keying

[3] https://www.youtube.com/watch?v=vtJ6mAy3xMc&t=440s

[4] https://www.youtube.com/watch?v=HXPzqhKO3X0

[5] https://www.mathworks.com/matlabcentral/fileexchange/79224-bpsk-system-modeled-and-benchmarked-against-ber-snr

[6] https://www.divilabs.com/2015/04/ebno-snr-vs-ber-curve-plotting-for-bpsk.html

[7] Bit Error Rate (BER) Comparison of AWGN Channels for Different Type’s Digital Modulation Using MATLAB Simulink by Md. Golam Sadeque, Lecturer, Dept. of EEE, PUST, Bangladesh

[8] Performance Analysis of BER and SNR of BPSK in AWGN Channel by Promise Elechi, Rivers State University and Bodunrin Isa Bakare, Rivers State University of Sciences









