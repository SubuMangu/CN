# Chapter 5

**DIGITAL-TO-ANALOG CONVERSION**
---
<img src="Images/Screenshot 2024-10-01 204858.png" width="" height="">

**Carrier Signal**
- In analog transmission, the sending device produces a high-frequency signal that acts
as a base for the information signal.
-  This base signal is called the carrier signal or carrier frequency
- Digital information then changes the carrier signal by modify-
ing one or more of its characteristics (amplitude, frequency, or phase).This kind of
modification is called **modulation** (shift keying) 

$$N=S \times r$$
$$N:\text{bit rate}$$
$$S:\text{baud rate}$$
$$r:\text{Maximun data element to signal element ratio}$$

<img src="Images/Screenshot 2024-10-02 103516.png" width="" height="">

<img src="Images/Screenshot 2024-10-01 210112.png" width="" height="">

- In the analog transmission of digital data, the baud rate is less than or equal to the bit rate. 

**Amplitude Shift Keying(ASK)**
- In amplitude shift keying, the amplitude of the carrier signal is varied to create signal
elements.
- Both frequency and phase remain constant while the amplitude changes.

**Binary ASK (BASK)**

<img src="Images/Screenshot 2024-10-01 212331.png" width="" height="">

- a digital “1” could not affect the signal, whereas a digital “0” would, by making 
it zero.
- The value of d is between 0 and 1. This
means that the bandwidth can be expressed as shown, where S is the signal rate and the B
is the bandwidth
$$B=\left(1+d\right)\times S$$

<img src="Images/Screenshot 2024-10-01 213044.png" width="" height="">

**Frequency Shift Keying**
- In frequency shift keying, the frequency of the carrier signal is varied to represent data.

**Binary FSK (BFSK)**

<img src="Images/Screenshot 2024-10-01 223638.png" width="" height="">

<img src="Images/Screenshot 2024-10-01 223947.png" width="" height="">

**Multilevel FSK**
$$B=\left(1+d\right)\times S + \left(L-1\right)2\Delta f \implies B = L \times S $$

<img src="Images/Screenshot 2024-10-01 224755.png" width="" height="">

<img src="Images/Screenshot 2024-10-01 225600.png" width="" height="">

**Phase Shift Keying**

- In phase shift keying, the phase of the carrier is varied to represent two or more differ-
ent signal elements. 

**Binary PSK (BPSK)**

- The simplest PSK is binary PSK, in which we have only two signal elements, one with
a phase of 0°, and the other with a phase of 180°.

<img src="Images/Screenshot 2024-10-01 230035.png" width="" height="">

- The bandwidth is the
same as that for binary ASK, but less than that for BFSK. No bandwidth is wasted for
separating two carrier signals.

**Quadrature PSK (QPSK)**
- Instead of just two phase shifts like in regular PSK, QPSK uses four different phase shifts (45°, -45°, 135°, and -135°). This allows QPSK to transmit two bits of data per symbol instead of one.
- This makes QPSK more efficient, as it can carry twice as much data with the same bandwidth.
- There are four
kinds of signal elements in the output signal (L = 4), so we can send 2 bits per signal
element (r = 2).

<img src="Images/Screenshot 2024-10-02 091416.png" width="" height="">


**Constellation Diagrams**
- A constellation diagram helps us to define the amplitude and phase of a signal when we 
are using two carriers, one in quadrature of the other.
- The X-axis represents the in-phase carrier and the Y-axis represents quadrature carrier
$$M=2^r$$
$$r:\text{No of bits per symbol}$$
$$M:\text{No of points in constellation diagrams}$$

<img src="Images/Screenshot 2024-10-02 090719.png" width="" height="">

**Quadrature Amplitude Modulation**
- Quadrature amplitude modulation is a combination of ASK and PSK
- The minimum bandwidth required for QAM transmission is the same as that required
for ASK and PSK transmission. QAM has the same advantages as PSK over ASK

<img src="Images/Screenshot 2024-10-02 091203.png" width="" height="">

**ANALOG-TO-ANALOG CONVERSION**
---
- Analog-to-analog conversion, or analog modulation, is the representation of analog
information by an analog signal.
- Analog-to-analog conversion can be accomplished in three ways: amplitude
modulation (AM), frequency modulation (FM), and phase modulation (PM).

**Amplitude Modulation**
- In AM transmission, the carrier signal is modulated so that its amplitude varies with the
changing amplitudes of the modulating signal. 
- The modulating signal is the envelope of the carrier.

<img src="Images/Screenshot 2024-10-02 092226.png" width="" height="">

- The modulation creates a band-
width that is twice the bandwidth of the modulating signal and covers a range centered
on the carrier frequency.
$$B_{AM}=2B$$

**Standard bandwidth allocation for AM radio**
- n fact, the Federal Communications
Commission (FCC) allows 10 kHz for each AM station.
- AM stations are allowed carrier frequencies anywhere between 530 and 1700 kHz
- If one
station uses a carrier frequency of 1100 kHz, the next station's carrier frequency cannot
be lower than 1110 kHz 

<img src="Images/Screenshot 2024-10-02 092910.png" width="" height="">


**Frequency Modulation**
- In FM transmission, the frequency of the carrier signal is modulated to follow the chang-
ing voltage level (amplitude) of the modulating signal.
- FM is normally implemented by using a voltage-controlled
oscillator as with FSK

<img src="Images/Screenshot 2024-10-02 093007.png" width="" height="">

- The total bandwidth required for FM can be determined from
the bandwidth of the audio signal: 
$$B_{FM}=2\left(1+\beta \right)B$$
- $\beta$ is a factor depends on modulation technique
with a common value of 4

**Standard bandwidth allocation for FM radio**
- The FCC allows 200 kHz (0.2 MHz) for each station.
- FM stations are allowed carrier frequencies anywhere between
88 and 108 MHz. 

**Phase Modulation**
- In PM transmission, the phase of the carrier signal is modulated to follow the changing
voltage level (amplitude) of the modulating signal. 
- In FM, the
instantaneous change in the carrier frequency is proportional to the amplitude of the modulating signal; in PM the instantaneous change in the carrier frequency is proportional to the derivative of the amplitude of the modulating signal.

<img src="Images/Screenshot 2024-10-02 093901.png" width="" height="">

- Although, the formula shows the same bandwidth for FM and PM, the
value of $\beta$ is lower in the case of PM (around 1 for narrowband and 3 for wideband).
$$B_{PM}=2\left(1+\beta\right)B$$







