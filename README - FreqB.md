# Prac-1
This repository includes the code developed for Prac 1

# Question 4.2.2 - Frequency B
The Problem I faced for the synchroniser based on the correlator principle: 

After having frequency shifted the received sequence, I convolve it with the preamble (which is BPSK modulated as required). 
Afterwards, I try to find the start of the signal (the QPSK symbols) by looking for peaks in the result of the convolution. 
In fact, the convolution delivers a sequence with an interesting pattern. However, I couldn't relate this pattern to the 
actual sequence we have (128 bits: preamble / 640 bits : signal / 128 bits preamble / ... and so on). The pattern that the convolution's result shows is the following: The first peak is at 3436, after exactly 896 symbols (896 = 640 + 128*2) another peak arises. The next peak is at 7148. 

Furthermore, I am not quite sure about the decoder I implemented, although it was totally fine for the previous question (frequency A), and I can't see how to further improve it. 
