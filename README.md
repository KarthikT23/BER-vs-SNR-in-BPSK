# BER-vs-SNR-in-BPSK
Bit Error Rate vs Signal to Noise Ratio in Binary Phase Shift Keying using Simulink
# Abstract
In a binary phase shift keying (BPSK) system, the bit error rate (BER) performance is dependent on the signal-to-noise ratio (SNR) of the received signal. Simulink, a simulation tool in MATLAB, can be used to analyze the BER versus SNR performance of a BPSK system.

The simulation model includes a Random Integer Generator, BPSK modulator, Rayleigh SISO Fading Channel, a math function, an additive white Gaussian noise (AWGN) channel, a product, BPSK demodulator and an Error Rate Calculation.

The transmitted signal is modulated using BPSK and passed through the AWGN channel to simulate the effects of noise. The received signal is demodulated using BPSK and compared to the original transmitted signal to calculate the BER.

By varying the SNR of the received signal, the simulation can generate a BER versus SNR plot. The plot shows the relationship between the BER and the SNR, where the BER decreases as the SNR increases. The plot can be used to evaluate the performance of the BPSK system and to determine the minimum required SNR for a specific BER.
