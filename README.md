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
1.Case 1: 180nm
![Screenshot (52)](https://github.com/user-attachments/assets/27b8c5d5-b466-4acf-8f70-b0dd35515b21)
### Procedure:

1. Build the circuit as per the circuit diagram using LTspice.
2. Set the Vdd as 1.8V.
3. Download the library file [tsmc018 (1).txt](https://github.com/user-attachments/files/18785407/tsmc018.1.txt)
4. Create a folder. Save the library file and LTspice file to the folder.
5. Import the library file to LTspice using spice directive(.op).
6. Find the current value for the given power rating.
7.  Set the mosfet model name CMOSN for NMOSFET and CMOSP for PMOSFET as given in the library file, length as 180nm and vary the width  of NMOSFET till you get the exact Q point. Set the gate volatge of NMOSFET as 0.5V. 
8. DC analysis: In edit simulation option, change to dc offset to get list of values obtained from the circuit. We should get the calculated current value in the simulation result.So that we need to vary the value of width since width is directly proportional to Drain current(Id) keeping other parameters constant. Since we are doing current mirroring the current of both mosfets should be same as the reference current even the output also should match too. 
9. Transient analysis: In edit simulation option, change from dc offset to transient. Set the dc offset as 0.5V, Amplitude 1mV, frequency 1KHz. Keep stop time for 3ms and run to get the expected waveform.find the maximum output swing.
10. AC analysis : In edit simulation option, change from transient to ac analysis. Set type of sweep as decade, number of points per decade as 20, start and stop frequency as 0.1Hz and 1THz to get the expected ac waveform. Note down the 3dB gain of the circuit and its bandwidth.

<br>
### Simulation Results:
### DC analysis:
1.Case 1: 180nm

![Screenshot (53)](https://github.com/user-attachments/assets/72e273d9-5d62-4f27-9125-c1db2cdeaf64)
PMOSFET = length is 180nm, width is 10um\
NMOSFET = length is 180nm, width is 114.025um\
V<sub>out</sub>= 0.967276V\
V<sub>x</sub>= 0.967276V\
I<sub>ref</sub> = 0.277mA\
2.Case 2: 500nm
![Screenshot (55)](https://github.com/user-attachments/assets/bd84ea81-4e48-49b2-84fa-a12b26cd7257)
PMOSFET = length is 500nm, width is 10um\
NMOSFET = length is 500nm, width is 207.617um\
V<sub>out</sub>= 0.644713V\
V<sub>x</sub>= 0.644703V\
I<sub>ref</sub> = 0.277mA\
![Screenshot (54)](https://github.com/user-attachments/assets/170f5a2a-983d-4db6-a1a9-90ea032678d5)
3.Case 3: 1umm
PMOSFET = length is 1um, width is 10um\
NMOSFET = length is 1um, width is 251.54um\
V<sub>out</sub>= 0.293193V\
V<sub>x</sub>=  0.293177V\
I<sub>ref</sub> = 0.277mA
![Screenshot (56)](https://github.com/user-attachments/assets/8c23cae5-d399-4874-8be1-5f36e064382a)
### Tabular column:
|  Length  |            Width           |   V<sub>x</sub>  | V<sub>out</sub>  |   I<sub>ref</sub>|
|----------|----------------------------|------------------|------------------|------------------|
|   180nm  | pmos= 10u; nmos=114.025u   |    0.967276V     |     0.967276V    |    0.277mA       |
|   500nm  | pmos= 10u; nmos=207.617u   |    0.644703V     |     0.644713V    |    0.277mA       |
|    1um   | pmos= 10u; nmos=251.54u    |    0.293177V     |     0.293193V    |    0.277mA       |

1.Case 1: 180nm
![Screenshot (57)](https://github.com/user-attachments/assets/4ef039d5-4c1b-4196-bbbf-bb19735038ec)

* Peak to Peak volatge = 1.934V
* Maximum output swing = Vdd-Vov2+Vov3 = 1.8-(-0.00847-0.36)+(0.5-0.36)= 2.29V

2.Case 2: 500nm
![Image](https://github.com/user-attachments/assets/8786450e-c70e-4efd-8edf-bf6ba5d635ee)
* Peak to Peak volatge = 1.28V
* Maximum output swing = Vdd-Vov2+Vov3 = 1.8-(-0.00000907-0.36)+(0.5-0.36)= 2.29V

<br>
3.Case 3: 1um

![Screenshot (58)](https://github.com/user-attachments/assets/c4058a2f-7682-4df8-b4b0-b3e27c13d6dd)

* Peak to Peak volatge = 0.607V
* Maximum output swing = Vdd-Vov2+Vov3 = 1.8-(0.0000165-0.36)+(0.5-0.36)= 2.29V

<br>
### AC analysis:
1.Case 1: 180nm

![screenshot 1 1](https://github.com/user-attachments/assets/5ebb55c5-2f2b-497c-9766-524839fd9245)

* 3dB gain = 27dB
* 3dB bandwidth= 265.18509MHz

<br>

2.Case 2: 500nm
![screenshot1 2](https://github.com/user-attachments/assets/28777c88-bf55-4ec8-a1b9-e604b2907808)

* 3dB gain = 36dB
* 3dB bandwidth= 52.464564MHz

<br>

3.Case 3: 1um
![screenshot 1 3](https://github.com/user-attachments/assets/206e1623-ffdc-4ead-8473-91d8fa8b88fe)

* 3dB gain = 35.75dB
* 3dB bandwidth= 39.494824MHz
* ### Circuit 1: for 1:2 ratio
![Screenshot (59)](https://github.com/user-attachments/assets/bdcff76e-db31-44e6-8da7-d4fa961e14bc)
### Calculations:
* Power <= 1mW
* Vdd = 1.8V
* I<sub>total</sub> = power/Vdd = 1mW/1.8 = 55.5mA
* I<sub>D</sub>= I<sub>total</sub>/3 = 0.185mA.
* 1:2 ratio = 0.185mA : 0.37mA.

### Components :
PMOSFET-2, NMOSFET- 1, supply volatage-2, current source-1.

### Procedure:

1. Build the circuit as per the circuit diagram using LTspice.
2. Set the Vdd as 1.8V.
3. Download the library file [tsmc018 (1).txt](https://github.com/user-attachments/files/18785407/tsmc018.1.txt)
4. Create a folder. Save the library file and LTspice file to the folder.
5. Import the library file to LTspice using spice directive(.op).
6. Find the current value for the given power rating.
7.  Set the mosfet model name CMOSN for NMOSFET and CMOSP for PMOSFET as given in the library file, length as 180nm and vary the width  of NMOSFET till you get the exact Q point. Set the gate volatge of NMOSFET as 0.5V. 
8. DC analysis: In edit simulation option, change to dc offset to get list of values obtained from the circuit. We should get the calculated current value in the simulation result.So that we need to vary the value of width since width is directly proportional to Drain current(Id) keeping other parameters constant. Since we are doing current mirroring the current of both mosfets should be same as the reference current even the output also should match too. 
9. Transient analysis: In edit simulation option, change from dc offset to transient. Set the dc offset as 0.5V, Amplitude 5mV, frequency 1KHz. Keep stop time for 3ms and run to get the expected waveform.Find the maximum output swing.
10. AC analysis : In edit simulation option, change from transient to ac analysis. Set type of sweep as decade, number of points per decade as 20, start and stop frequency as 0.1Hz and 1THz to get the expected ac waveform. Note down the 3dB gain of the circuit and its bandwidth.

<br>
### Simulation Results:
### DC analysis:
1.Case 1: 180nm

![Screenshot (60)](https://github.com/user-attachments/assets/324933d0-73a6-4585-9f50-3af334ea0b92)

PMOSFET 1 = length is 180nm, width is 70um : PMOSFET 2 = width is 140um\
NMOSFET = length is 180nm, width is 135.867um\
V<sub>out</sub>=  1.20094V\
V<sub>x</sub>=  1.20934V\
I<sub>ref</sub> = 0.185mA\

2.Case 2: 500nm
![Screenshot (62)](https://github.com/user-attachments/assets/31ba8dc0-be6a-4d52-abb1-36007fc77555)


PMOSFET 1 = length is 180nm, width is 70um : PMOSFET 2 = width is 140um
NMOSFET = length is 500nm, width is 256.773um\
V<sub>out</sub>=  1.1V\
V<sub>x</sub>=  1.2\
I<sub>ref</sub> = 0.185mA\

3.Case 3: 1um
![Screenshot (64)](https://github.com/user-attachments/assets/83fe172a-5b67-49d2-8abb-d30e952c3e30)


PMOSFET 1 = length is 180nm, width is 70um : PMOSFET 2 = width is 140um
NMOSFET = length is 1um, width is 307.294um\
V<sub>out</sub>=  1.1V\
V<sub>x</sub>=  1.2V\
I<sub>ref</sub> = 0.277mA
### Tabular column:
|  Length  |                Width            |   V<sub>x</sub>  | V<sub>out</sub> | I<sub>ref</sub>  |
|----------|---------------------------------|------------------|-----------------|------------------|
|   180nm  | pmos= 70u,140u; nmos=135.867um  |     1.20934V     |     1.20094V    | 0.185mA : 0.37mA |
|   500nm  | pmos= 70u,140u; nmos=256.773um  |     1.2V         |     1.1V        | 0.185mA : 0.37mA |
|    1um   | pmos= 70u,140u;nmos=307.294um   |    1.2V          |     1.1V        | 0.185mA : 0.37mA |

### Transient analysis:
1.Case 1: 180nm
![Screenshot (61)](https://github.com/user-attachments/assets/96d7193f-4f05-4716-a468-54db80ecc0f0)

* Peak to Peak volatge = 2.39V
* Maximum output swing = Vdd-Vov2+Vov3 = 1.8-(-0.00847-0.36)+(0.5-0.36)= 2.30V

<br>

2.Case 2: 500nm
![Screenshot (63)](https://github.com/user-attachments/assets/088a6a41-6d32-47cc-8dfb-57175bce937f)
* Peak to Peak volatge = 2.25V
* Maximum output swing = Vdd-Vov2+Vov3 = 1.8-(-0.0015-0.36)+(0.5-0.36)= 2.3015V

<br>

3.Case 3: 1um
![Screenshot (65)](https://github.com/user-attachments/assets/f404c7bc-0559-4a9e-b950-d9d72811c9a9)
* Peak to Peak volatge = 2.048V
* Maximum output swing = Vdd-Vov2+Vov3 = 1.8-(0.000575-0.36)+(0.5-0.36)= 2.2V

### AC analysis:
1.Case 1: 180nm
![screenshot2 1](https://github.com/user-attachments/assets/b07c43c8-3df2-4a13-9d1a-dd7d3784953a)
* 3dB gain = 26.212dB
* 3dB bandwidth= 105.81654MHz

<br>

2.Case 2: 500nm
![screenshot 2 2](https://github.com/user-attachments/assets/e21326be-aa17-4962-96b2-44fd6e356f24)
* 3dB gain = 34.71dB
* 3dB bandwidth= 29.731326MHz

<br>

3.Case 3: 1um
![screenshot 2 3](https://github.com/user-attachments/assets/a7feb13e-7433-4876-b0c7-00c1d01f919d)
* 3dB gain = 37dB
* 3dB bandwidth= 18.6247MHz


### Circuit 3: 
### Aim : Design the diffrential amplifier having VDD=2V, P<=1mW, Vicm =1V as per the 3rd experiment and perform DC, Transient , AC analysis
### Circuit Diagram:





