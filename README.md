CE_Soldering_Practice
=====================

A board for learning how to solder without breaking anything.  This one is supposed to act as a little example circuit to show the amplication effect of a 741 opamp on an oscillating signal.  The 555 outputs a squarewave at around 100hz, which then passes through an RC filter to soften the edges of the square and then another capacitor to remove the DC component of the signal.

Because the signal that is fed into the 741 isn't a true square anymore, you can actually see when the amp gets saturated, and see the variations in amplification due to changing the resistor values more easily on an oscilloscope.

As of 27-JAN-2014, the headers are designed as follows...

Middle board 3 socket header: +9v, -9v and Ground (two 9v batteries in series, with the center as ground reference).

End Board 7 pin header: 
1. Oscilloscope test point: pre-amp
2. 2. Oscilloscope test point: post-amp
3. Oscilloscope Ground
4. Signal Resistor IN 
5. Signal Resistor OUT 
6. Feedback Resistor IN 
7. Feedback Resistor OUT 

## Bill of Materials


[Bill of Materials]
| Value |  Qty | Part Number | Manufacturer  |  Package | Reference | Description |  Digi-Key P/N  |  Min Qty | Cost  |
-------- | :-----------:     | :------:  | :------:  | :------:  | :------:  | :------:  |:------:  |:------:  |:------:  |
.1uF  |  1      |     SM0603 | | | C9    |      1 |  0.1  |   
.1uF   | 3  | CC0603KRX7R9BB104  | Yageo  | SM0805 | C1 C2 C5  |  CAP CER 0.1UF 50V 10% X7R 0603 | 311-1344-1-ND               
1uF | 1 |  C0805C105K4RACTU   | Kemet  | SM0805 |  C3 |  CAP CER 1UF 16V 10% X7R 0805  |  399-1284-1-ND |  1 |  0.12  |        
10uF  |  1   |   CC0805KRX7R7BB104 | Yageo |      SM0805 | C4    | CAP CER 10UF 6.3V 10% X5R 0805 | 311-1459-2-ND | 1 | 0.02905                      
.33uF  | 1    | 0805YC334KAT2A |  AVX Corporation   |     SM0805 | C6    | CAP CER 0.33UF 16V 10% X7R 0805 | 478-1402-1-ND | 1 | 0.24000                   
.01uF  | 1    | CC0805KRX7R9BB103 |  Yageo   |     SM0805 | C7   | CAP CER 10000PF 50V 10% X7R 0805 | 311-1136-1-ND | 1 | 0.10                       
LED | 1 |  |   |  LED-0603  |  D1  | 
CONN_3 | 1    | |     |     SIL-3  | K1    |                    
CONN_7 | 1    | |     |     SIL-7  | P1    |                    
330 ohm | 1    |  RC0603JR-07330RL   |   Yageo   |      SM0603 | R9    | RES 330 OHM 1/10W 5% 0603 SMD | 311-330GRCT-ND | 1 | 0.10                     
1K ohm  | 3   | RC0805JR-071KL |  Yageo    |      SM0805 | R2 R3 R5    | RES 1.0K OHM 1/8W 5% 0805 SMD | 311-1.0KARCT-ND | 1 | .10                       
2K ohm  | 1    | |    |      SM1206 | R6   |                     
4K ohm  | 1    | |    |     SM0603 | R7    |                    
10K ohm | 1    | |    |      SM1206 | R4    |                    
68K ohm | 1    | |    |      SM1206 | R1     |                   
180K ohm |   1  | |    |        SM0603 | R8     |                   
7555   | 1     | |     |    SO8E  |  U1      |                  
7555   | 1    | |      |    TSSOP-8 | U4    |                    
7805-REG  |  1  | |    |        DPAK3 |  U3   |                     
TL082  | 1    | |      |    MSOP_8 | U5     |                   
LM741  | 1     | |     |    SO8E   | U2    |                    