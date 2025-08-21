# Full-Wave Rectifier with Capacitor Filter

## Objective
The goal of this project was to design and simulate a full-wave rectifier using LTSpice. A full-wave rectifier converts both halves of an AC waveform into pulsating DC. By adding a capacitor filter, the DC output is smoothed, reducing the ripple voltage.

## Project Files
- LTSpice circuit files are included in the `circuit_files` folder  
- Simulation output images are included in the `images` folder  

## Circuit Diagram
<img width="1920" height="1080" alt="Full Wave Rectifier" src="https://github.com/user-attachments/assets/0e523fa1-72d7-4092-b05c-c39c4048d447" />

## Circuit Description
The circuit consists of:
- AC voltage source (sinusoidal input)  
- Four diodes arranged in a bridge configuration  
- Two inductors (used in some configurations to limit current spikes)  
- Load resistor  
- Smoothing capacitor  

The AC source was connected to the bridge rectifier. The diodes allow both positive and negative halves of the AC waveform to pass through, but only in one direction across the load. A capacitor placed in parallel with the load resistor filters the output, reducing ripple.

## Simulation and Observations

### Without Capacitor
<img width="1920" height="1080" alt="Without Capacitor" src="https://github.com/user-attachments/assets/157b4750-25e9-41af-9635-a778851d68f7" /> 
The rectified output showed significant ripple without filtering.

### With Capacitor (5uF, R=1k)
<img width="1920" height="1080" alt="With capacitor at 5u and R=1k" src="https://github.com/user-attachments/assets/46e01887-d21d-4622-819a-aa53598c9952" />
Adding a 5uF capacitor reduced ripple but some fluctuations were still present with a lower load resistance.

### With Capacitor (5uF, R=10k)
<img width="1920" height="1080" alt="With capacitor at 5u and R=10k" src="https://github.com/user-attachments/assets/a787e7c9-69f4-4d3d-a401-27b39acde277" />
With higher load resistance, the ripple reduced further since the capacitor discharged more slowly.

### With Capacitor (20uF, R=10k)
<img width="1920" height="1080" alt="With capacitor at 20u and R=10k" src="https://github.com/user-attachments/assets/a2843c09-4535-46b6-8527-2410645478a0" />
A larger capacitor provided even better filtering, producing a smoother DC waveform.

## Conclusion
The simulation shows that a full-wave rectifier with a capacitor filter produces a smoother DC output compared to a simple rectifier. The quality of smoothing depends on both the load resistance and the capacitor value. Higher resistance and larger capacitance reduce ripple effectively, providing a more stable DC supply.
