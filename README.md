# Iterative Detection and Decoding for RIS-Assisted Multiuser Multiple-Antenna Systems #

This code package is related to the following scientific article:
Roberto C. G. Porto; Rodrigo C. de Lamare, "Iterative Detection and Decoding for RIS-Assisted Multiuser Multiple-Antenna Systems," 2024 19th International Symposium on Wireless Communication Systems (ISWCS).

# Abstract of the Article

We present a novel iterative detection and decoding (IDD) scheme for Reconfigurable Intelligent Surface (RIS)assisted multiuser multiple-antenna systems. The proposed approach introduces a joint iterative detection strategy that integrates Low-Density Parity-Check (LDPC) codes, RIS processing and iterative detection and decoding. In particular, we employ a minimum mean square error receive filter that performs truncation at the RIS and soft interference cancelation at the receiver. Simulation results evaluate the system’s overall capacity and bit error rate, and demonstrate substantial improvements in bit error rate across block-fading channels.

# Content of Code Package

### This code was developed using MATLAB Live Script and consists of two main scripts: ###

- **iddMIMO.mlx:** In this script, the number of packets remains the same for all SNR (Signal-to-Noise Ratio) values.
- **iddMIMO_fast.mlx:** This alternative script allows you to specify a different number of packets for each SNR value.

### Performance Tips: ###
To improve execution speed, especially for large-scale simulations, it is highly recommended to run the code in parallel. To do this, follow these steps:

- Replace the inner for loop with a parfor loop.
- Set the variable useParallel to false.

### Data Tracking: ###
For each SNR value, the code saves the results in the file data/iddMIMO.mat. This enables users to monitor the progress of the simulation in real-time.

### Speed Optimization: ###
If you want to accelerate the simulation further, you can comment out the methods you don't need (e.g., 'iddWOris()'). The generatePlots function automatically generates plots for only the active methods.

# License and Referencing

This code package is licensed under the GPLv2 license. If you in any way use this code for research that results in publications, please cite our original article listed above.
