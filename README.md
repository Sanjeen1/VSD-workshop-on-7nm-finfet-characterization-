# VSD-workshop-on-7nm-finfet-characterization-
This repository contains my work from the VLSI System Design (VSD) Workshop on 7nm FinFET Circuit Design and Characterization using the ASAP7 PDK.

<p align="center"> <img width="330" height="168" alt="image" src="https://github.com/user-attachments/assets/434affcd-3498-41f0-99c0-bd2af91d7556" /> </p>


## 🚀 Objectives
- Gain a deep understanding of **7nm FinFET device physics**  
- Perform **SPICE-based circuit simulations** using the ASAP7 PDK  
- Characterize a **CMOS inverter** in terms of:  
  - Voltage Transfer Characteristics (VTC)  
  - Delay and Transition time  
  - Power, gain , transconductance, drain current 
  - Noise Margins  
- Bandgap reference Circuit design and simulation
  - Note down the reference voltage for change in supply and change in temperature.
 
# Why do we need FinFET ?

The transition from planar MOSFETs to FinFETs was driven by the scaling limitations faced at advanced technology nodes, especially below 22nm. In planar MOSFETs, as the channel length shrinks, short-channel effects such as drain-induced barrier lowering (DIBL) and threshold voltage roll-off become significant, leading to higher leakage currents and poor gate control. FinFETs address this issue by introducing a three-dimensional “fin”-shaped channel with the gate wrapping around it on multiple sides. This structure provides much stronger electrostatic control over the channel, which suppresses leakage and improves subthreshold slope. In addition, the fin geometry increases the effective channel width per unit area, allowing FinFETs to deliver higher drive current and better performance without increasing footprint. This leads to improved switching speed and higher energy efficiency, making them ideal for low-power and high-performance applications. Moreover, FinFETs demonstrate superior scalability compared to planar MOSFETs, enabling continued Moore’s law progression. Overall, FinFET technology offers a balance of high performance, low power consumption, and robust scalability, which makes it far superior to planar MOSFETs in deep nanometer regimes

<img width="1179" height="508" alt="image" src="https://github.com/user-attachments/assets/82b33d5b-8868-49ea-9f18-131fb66a7aad" />

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

# Propogation delay - 

<img width="550" height="84" alt="image" src="https://github.com/user-attachments/assets/c9ac9269-4d4f-4339-9447-60d1457bf9cf" />

tpr is time when input reaches to 50 percent of vdd and tpf is time when output voltage reaches to 50 percent of vdd. 

# Observation 

---> When Pfet width (no of fins increaded ) increases the VTC Curve shifts towards right side.

---> When Nfet width (Nfin) increases the VTC curve shifts left side.

---> When width of any device nfet or pfet is increased then drain current will get increased also. 

---> When Nfet size increased then gain increases.

---> Gain decreases when pfet size increases.

---> Power is increased in both case.

# Bandgap Reference circuit Design and Simulation using Xschem

<img width="923" height="447" alt="image" src="https://github.com/user-attachments/assets/1b224e4e-a84a-4e69-b403-362626788fc4" />

A Bandgap Reference Circuit (BGR) is an analog integrated circuit block that generates a constant DC reference voltage (typically around 1.2 V) which is:

- Independent of supply voltage (VDD variations)

- Stable over temperature changes

- Robust against process variations
  
**CTAT (Complementary-To-Absolute-Temperature)**

-The base–emitter voltage (Vbe) of a BJT (or diode-connected transistor).

-Decreases with increasing temperature (≈ –2 mV/°C).

**PTAT (Proportional-To-Absolute-Temperature)**

- Generated from the difference of Vbe between two BJTs of different emitter areas, scaled by a resistor.

- Increases with temperature (≈ +0.085 mV/°C).

The different plot by sweaping temperature.

<img width="1185" height="548" alt="image" src="https://github.com/user-attachments/assets/e9108e88-7162-4928-a99f-f536ef8498b3" />

<img width="1181" height="597" alt="image" src="https://github.com/user-attachments/assets/daaa37dc-6034-4439-a9e9-eb144c29e9fd" />

**Methods to calculate reference voltage -**

<img width="533" height="365" alt="image" src="https://github.com/user-attachments/assets/72c12d04-3ccf-43a5-86b3-a4a5540e84e0" />

**Here sweaping the temperature from -45 to 125 with step size of 1, and print Vref value by "print Vref" command.**

<img width="582" height="50" alt="image" src="https://github.com/user-attachments/assets/e87a8865-4320-43f8-a34a-709e15dd9744" />

**at vdd 0.8 , temp = 27 then Vref is 213 mV**

**Methods to calculate startup time -**

<img width="468" height="148" alt="image" src="https://github.com/user-attachments/assets/32a5057b-0077-4b26-b07c-3aab41834531" />

<img width="699" height="511" alt="image" src="https://github.com/user-attachments/assets/1e4d8ebf-db93-4a7e-8dee-cf3249f47923" />

**Temperature is varied by .temp command.**

**For this run transient analysis**

# Acknowledgements

I would like to express my sincere gratitude to **Kunal Sir** and **Soundarya Madhuri Mam** for their valuable guidance and support. 

 

 


















