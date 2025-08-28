# VSD-workshop-on-7nm-finfet-characterization-
This repository contains my work from the VLSI System Design (VSD) Workshop on 7nm FinFET Circuit Design and Characterization using the ASAP7 PDK.

## 🚀 Objectives
- Gain a deep understanding of **7nm FinFET device physics**  
- Perform **SPICE-based circuit simulations** using the ASAP7 PDK  
- Characterize a **CMOS inverter** in terms of:  
  - Voltage Transfer Characteristics (VTC)  
  - Delay and Transition time  
  - Dynamic & Leakage Power  
  - Noise Margins  

---

**For my user name Sanjeen the ASCII sum in mv is 0.516**

<img width="553" height="133" alt="image" src="https://github.com/user-attachments/assets/8462416d-9ae2-41b0-91f1-4d005192d84c" />

<img width="553" height="133" alt="image" src="https://github.com/user-attachments/assets/abb77b4d-5835-4de5-9802-0d9b4c307f8d" />

# VTC Curve -

<img width="465" height="68" alt="image" src="https://github.com/user-attachments/assets/da74719d-63a4-4bc4-b7d6-1352e6153dfb" />

![VTC Curve](https://github.com/user-attachments/assets/e02f6983-248e-4d1b-ba77-f99eb9e7f45f)

Y axis is output voltage (nfet_out) and X axis is input voltage (nfet_in). The point where input voltage is equal to output voltage or the point where blue line intersects red line is known as switching threshold (denoted here by v_th).

# Drain current -

![Drain current](https://github.com/user-attachments/assets/2cd9e509-ed71-44df-aa22-9cf7946c95bb)

# Transconductance - 

![gm](https://github.com/user-attachments/assets/a02d5ae1-6da8-4a4a-ae1f-c079425fb355)

In digital switching,Transconductance measures how strongly the input voltage (V_{in}) can control the output current.High gm ensures fast and sharp switching.

# Output resistance -

![Rout](https://github.com/user-attachments/assets/fce444a6-5475-43b9-8e32-a5b967cf476f)

# Calculation of power -

<img width="652" height="51" alt="image" src="https://github.com/user-attachments/assets/0e5f13f7-d4f4-4bb3-8615-3bdf682a5971" />

<img width="719" height="251" alt="image" src="https://github.com/user-attachments/assets/a43a2e2f-4241-4217-a6ac-07d0d31345d1" />

<img width="757" height="603" alt="image" src="https://github.com/user-attachments/assets/f60c36d1-c4ea-40f1-92db-f7dfc7943249" />

Power = Energy / Time period , Energy is the voltage multiply with the area falls under the Idt plot. If we divide by Ton which is done here that gives us the average power only during the time the circuit is switching, not over the full clock cycle.

# Noise margin analysis- 

<img width="781" height="274" alt="image" src="https://github.com/user-attachments/assets/2ba78de2-f2ea-478a-9a86-ba9a66c5f7d3" />

<img width="841" height="409" alt="image" src="https://github.com/user-attachments/assets/d1375ef8-2847-46df-b8be-96dab2582801" />

# Observation 

---> When Pfet width (no of fins increaded ) increases the VTC Curve shifts towards right side.

---> When Nfet width (Nfin) increases the VTC curve shifts left side.


















