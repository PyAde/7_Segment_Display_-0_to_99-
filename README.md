# 7_Segment_Display_-0_to_99-
This repository contains a Logisim project that uses a 7-segment display to display numbers from 0 to 99

<img width="1127" height="926" alt="image" src="https://github.com/user-attachments/assets/a0a28c27-699b-477b-a863-eee77b20b757" />


I created this circuit as an assignment for my Digital Logic Design course to demonstrate how logic gates can be combined to produce different outputs that can be applied to real electronic devices. In this project, I used Logisim software to design and simulate the circuit.
The circuit consists of two 7-segment displays (one on the left for the tens digit and one on the right for the units digit). It is capable of displaying decimal numbers from 00 to 99. Therefore, this counter operates in decimal (base-10) format, not hexadecimal.
Versi yang lebih ringkas dan sering dipakai di README:
This circuit was designed as a course assignment in Digital Logic Design to show how basic logic gates can be used to control multiple outputs in electronic devices. Using Logisim, I built a two-digit decimal counter (00–99) with two 7-segment displays — one for the tens digit and one for the units digit. The counter works in decimal (base-10), not hexadecimal.



# Decimal to 4-Bit Binary Conversion Table


| Decimal | Binary (4-Bit) | D (Q3) | C (Q2) | B (Q1) | A (Q0) |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **0** | `0000` | 0 | 0 | 0 | 0 |
| **1** | `0001` | 0 | 0 | 0 | 1 |
| **2** | `0010` | 0 | 0 | 1 | 0 |
| **3** | `0011` | 0 | 0 | 1 | 1 |
| **4** | `0100` | 0 | 1 | 0 | 0 |
| **5** | `0101` | 0 | 1 | 0 | 1 |
| **6** | `0110` | 0 | 1 | 1 | 0 |
| **7** | `0111` | 0 | 1 | 1 | 1 |
| **8** | `1000` | 1 | 0 | 0 | 0 |
| **9** | `1001` | 1 | 0 | 0 | 1 |

#BCD to 7-Segment Decoder Truth Table (0-9)

This table outlines the logic for converting 4-bit Binary Coded Decimal (BCD) inputs into 7-segment display outputs. The logic is **Active High** (1 = LED On, 0 = LED Off).

### BCD to 7-Segment Truth Table (With Active Segments)

| Decimal | Input (D C B A) | a | b | c | d | e | f | g | Active Segments |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **0** | `0000` | 1 | 1 | 1 | 1 | 1 | 1 | 0 | **A, B, C, D, E, F** |
| **1** | `0001` | 0 | 1 | 1 | 0 | 0 | 0 | 0 | **B, C** |
| **2** | `0010` | 1 | 1 | 0 | 1 | 1 | 0 | 1 | **A, B, D, E, G** |
| **3** | `0011` | 1 | 1 | 1 | 1 | 0 | 0 | 1 | **A, B, C, D, G** |
| **4** | `0100` | 0 | 1 | 1 | 0 | 0 | 1 | 1 | **B, C, F, G** |
| **5** | `0101` | 1 | 0 | 1 | 1 | 0 | 1 | 1 | **A, C, D, F, G** |
| **6** | `0110` | 1 | 0 | 1 | 1 | 1 | 1 | 1 | **A, C, D, E, F, G** |
| **7** | `0111` | 1 | 1 | 1 | 0 | 0 | 0 | 0 | **A, B, C** |
| **8** | `1000` | 1 | 1 | 1 | 1 | 1 | 1 | 1 | **A, B, C, D, E, F, G** |
| **9** | `1001` | 1 | 1 | 1 | 1 | 0 | 1 | 1 | **A, B, C, D, F, G** |

