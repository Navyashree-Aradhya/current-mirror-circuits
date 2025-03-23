# current-mirror-circuits
### **CURRENT MIRROR**
**What is Current Mirror?**

A current mirror is an electronic circuit used in analog and mixed-signal applications to replicate or mirror the current flowing through one active device and produce an identical current in another device. The primary purpose of a current mirror is to maintain a consistent current in multiple parts of a circuit, ensuring that different components receive the same current for precise operation.

**Use of Current Mirror**
A current mirror circuit is used in electronic circuits to replicate or mirror a current from one part of the circuit and provide an identical current in another part. The primary purpose of a current mirror is to ensure that different components or branches of a circuit receive the same current, maintaining consistency and precision in the operation of the circuit.


![image](https://github.com/user-attachments/assets/59fc7f4d-74b0-4257-aa40-af025154484a)

Explaination: This simplest form of a current mirror consists of two transistors, where the current is replicated (or mirrored) by ensuring that the transistors are matched in their characteristics. Typically, one transistor is configured to set a reference current, and the other transistor mirrors this current, maintaining an equivalent current in its branch.

**Applications of Current Mirror**
Biasing Circuits
Current Sources
Differential Amplifiers
Cascode Amplifiers

**Advantages**
Simple and easy to design.
Minimal transistor count.

**Disadvantages**
Poor output impedance.
Limited accuracy due to channel-length modulation.
## Procedure:
1. Create a new experiment file.
2. Build the respective circuit diagram as per the design question and set the length and wisth of the corresponding n and p channel mosfets as per the current mirror ratio fopr Part A and only to the current mirror circuit to set the DC operating point for Circuit Part 2 with the previous simulation file .
3. Vary the length and width by maintaing the constant current mirror ratio as peer the requirement and note the corresponding changes in the current flowing through the circuit . Compare and plota comparision table .
4. Perform the transient analysis and observe the gain , variations in input and output waveform.
5. Perform the AC analysis and analyze the frequency response of the circuiit and calculate the 3dB Bandwidth

### **AIM:Design and analyis current mirror circuit as active load in amplifier circuit**
## Design Calculation:
wkt It=Iref+Ix\
Therefore, for 1:1 ratio Iref=Ix\
So,Iref=It/2\
It=P/Vdd\
It=1mW/1.8V\
It=0.555mA.\
Therefore,Iref=0.2778mA.
