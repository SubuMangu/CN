# Chapter 4
**Digital to digital conversion**
---
- In this section, we see how we can represent digital data by using digital signals.
- The conversion involves three techniques: line coding, block coding, and scrambling.

**Line Coding**
---
- Line coding is the process of converting digital data to digital signals.
- We assume that data, in the form of text, numbers, graphical images, audio, or video, are stored in computer memory as sequences of bits.
 Line coding converts a sequence of bits to a digital signal. At the sender, digital data are encoded into a digital signal; at the receiver, the digital data are recreated by decoding the digital signal. 

 **Signal element versus data element**

 <img src="Images/Screenshot 2024-09-26 113859.png" width="" height="">

 - A data element is the smallest entity that can represent a piece of information.
 - A signal element is the shortest unit of datra we can send. 
 - r represents the data unit
 - **Data Rate:** The data rate defines the number of data elements (bits) sent in 1s. The unit is bits per sec(bps).
- **Signal rate:** The signal rate is the number of signal elements sent in 1s.The unit is the baud.
- One goal in data communications is to increase the data rate while decreasing the signal rate. 
- Increasing the data rate increases the speed of transmission; decreasing the signal rate decreases the bandwidth(Bandwidth in Bits per Seconds) requirement. In our vehicle-people analogy, we need to carry more people in fewer vehicles to prevent traffic jams.
- bandwidth here is talking about the capacity of the communication channel to carry data
- The minimum bandwidth can be given as

$$B_{min}=c \times N \times \frac{1}{r}$$
- maximum data rate if the bandwidth of the channel is given
$$N_{max}=\frac{1}{c} \times B \times r$$

<img src="Images/Screenshot 2024-09-27 155603.png" width="450" height="">

**Characteristics of digital to digital conversion**
---
**Baseline Wandering** 
- In decoding a digital signal, the receiver calculates a running
average of the received signal power. This average is called the **baseline**. 
- A long string of Os or 1s can cause a drift in the baseline (baseline wandering)
and make it difficult for the receiver to decode correctly.

**DC Components** 
- When the voltage level in a digital signal is constant for a while,
the spectrum creates very low frequencies (results of Fourier analysis). These fre-
quencies around zero, called DC (direct-current) components.
- Problem occurs when the signal passes through a system where low frequencies cannot pass or a system that uses electrical coupling
(via a transformer).
- Eg,For example, a telephone line cannot pass frequencies below 200 Hz. Also a long-distance link may use one or more transformers to isolate
different parts of the line electrically. For these systems, we need a scheme with no
DC component.

**Self-synchronization**
- To correctly interpret the signals received from the sender,the receiver's bit intervals must correspond exactly to the sender's bit intervals.
- If the receiver clock is faster or slower, the bit intervals are not matched and the receiver might misinterpret the signals.Eg,sender sends 10110001, while the receiver receives 110111000011.
- To overcome this we need to have self synchronization system.
- This can be achieved if there are changes in the signal that alert the receiver to the beginning, middle, or end of the pulse. If the receiver's clock is out of synchronization, these points can reset the clock.

**Built-in Error Detection**
- It is desirable to have a built-in error-detecting capability
in the generated code to detect some of or all the errors that occurred during transmis-
sion. 

**Immunity to Noise and Interference**
- Another desirable code characteristic is a code I
that is immune to noise and other interferences. Some encoding schemes that we will
discuss have this capability

**Complexity**
- A complex scheme is more costly to implement than a simple one. For
example, a scheme that uses four signal levels is more difficult to interpret than one that
uses only two levels

**Line Coding Schemes**
---
<img src="Images/Screenshot 2024-09-28 100531.png" width="" height="">

**NRZ(Non return to zero)**
- Here the amplitude of pulse signal doesn't return to zero while a bit is encoded within time period $T_b$.

<img src="Images/Screenshot 2024-09-28 094332.png" width="250" height="">

1. **Unipolar NRZ scheme:**
- In a unipolar scheme, all the signal levels are on one side of the time axis, either above
or below
- Unipolar encoding uses only one polarity.0 is represented by zero voltage and 1 is represented by  positive voltage.

<img src="Images/Screenshot 2024-09-28 100854.png" width="" height="">

**Pros**
- inexpensive to implement.
**Cons**
- Lack of synchronization  
- dc component
- costlier than polar in terms of power consumption: As we will see shortly, the normalized power (power needed to send 1 bit per
unit line resistance) is double that for polar NRZ (In case of polarNRZ normalized power is $V^2$). For this reason, this scheme is nor-
mally not used in data communications today

2. **Polar Encoding Schemes**
- In polar schemes, the voltages are on the both sides of the time axis. 
- Under it three encoding schemes comes:
    - NRZ(NRZ-L,NRZ-I)
    - RZ
    - Biphase

**NRZ-L**
- In NRZ-L the level of the voltage determines the value of the bit.
- The
voltage level for 0 can be positive and the voltage level for 1 can be negative.

**NRZ-I**
-  In NRZ-I
the inversion or the lack of inversion determines the value of the bit.
- It comes under differential coding.
- It starts with positive voltage

<img src="Images/Screenshot 2024-09-28 102242.png" width="" height="">

**NRZ-L vs NRZ-I**
- NRZ-I is more preferable than NRZ-L because of the following reasons
    - Baseline wandering,synchronization problem and DC component occurs in NRZ-L if there is a long sequence of Os or 1s , but in case of NRZ-I it only occurs when there is longer sequence of 0s.
    - NRZ-L is vulnerable to sudden change in polarity whereas NRZ-I is not.
- NRZ-L and NRZ-I both have problem if there is longer sequence of 0s.
- Bandwidth of both the signals is $\frac{N}{2}$.

**RZ(Return to zero)**
- Here the amplitude of pulse signal return to zero while a bit is encoded within time period $T_b$ at $T_b/2$.


<img src="Images/Screenshot 2024-09-28 110905.png" width="" height="">

- uses three values: positive, negative, and zero.
- The first half of the signal respond to the input and the next half is zero 

<img src="Images/Screenshot 2024-09-28 112036.png" width="" height="">

**Pros:**
- no DC component problem Since number of changes per signal is doubled

**Cons**
- Bandwidth requirement is double of NRZ i.e, $N$.
- Still vulnerable to change in polarity
- RZ uses three levels of voltage, which is more complex to create

**Biphase**
- Here, the amplitude of the signal reverses in the mid of signal i.e, at $T_b/2$. This improves synchronisation.

<img src="Images/Screenshot 2024-09-28 112633.png" width="250" height="">

- It is of two types:  Manchester and Differential Manchester.

<img src="Images/Screenshot 2024-09-28 113651.png" width="" height="">

- The Manchester scheme overcomes several problems associated with NRZ-L, and
differential Manchester overcomes several problems associated with NRZ-I. 
 
**Pros:**
- No baseline wandering,synchronisation error and DC component

**Cons**
- Double bandwidth required

3. **Bipolar Schemes**
- In bipolar encoding (sometimes called multilevel binary), there are three voltage lev-
els: positive, negative, and zero.
- RZ is not a bipolar scheme because here voltage level is zero in between signal, but in bipolar, voltage level can be zero throughout the signal.
- It is of two types: AMI(alternate mark inversion) and pseudoternary.
- In AMI, the signal alternates when input is 1 and the signal is zero when the input is zero. Pseudoternary is opposite of AMI.

<img src="Images/Screenshot 2024-09-28 114927.png" width="" height="">

- synchronisation problem occurs when there is long sequence of 0s in AMI and 1s in pseudo ternary

4. **Multi level schemes**
- In mBnL schemes, a pattern ofm data elements is encoded as a pattern ofn signal
elements in which $2^m\le L^n$, where
$$L:\text{No of Levels}$$
$$n:\text{Size of signal in bits}$$
$$m:\text{Size of data in bits}$$
-  A letter is often used in place of L: B
(binary) for $L =2$, T (ternary) for $L = 3$, and Q (quaternary) for $L =4$. Note that the first
two letters define the data pattern, and the second two define the signal pattern.
- If $2^m=L^n$ , then each data pattern is
encoded into one signal pattern.
- If $2^m \lt L^n$  ,data patterns occupy only a subset of signal
patterns. The rest of signal patterns are known as **Redundant Signals** which carefully designed to prevent baseline wandering, to pro-
vide synchronization, and to detect errors that occurred during data transmission.
- If $2^m \gt L^n$ , data
encoding is not possible because some of the data patterns cannot be
encoded.

**2B1Q**
- There are no redundant signal patterns in this
scheme because $2^2=4^1$.
- Bandwidth requirement is half of NRZ i.e,$N/4$.

<img src="Images/Screenshot 2024-09-28 120931.png" width="" height="">

5. **Multiline Transmission: MLT-3** 
- Generally in differential coding techniques like NRZ-I and Differential Manchester we have two transitions:no inversion, inversion.
- If we have a signal with more than
2 levels, we can design a differential encoding scheme with more than 2 transition
rules.
- MLT-3 is one of them. The multiline transmission, three level (MLT-3) scheme
uses three levels (+V, 0, and - V) and three transition rules to move between the levels:

<img src="Images/Screenshot 2024-09-28 122046.png" width="" height="">

<img src="Images/Screenshot 2024-09-28 122139.png" width="" height="">

**Summary**

<img src="Images/Screenshot 2024-09-28 122323.png" width="" height="">


**Block Coding**
---
- In general, block coding changes a block of m bits into a block
of n bits, where n is larger than m. Block coding is referred to as an mB/nB encoding
technique.
- It involves three steps
1. **Division:** In the
division step, a sequence of bits is divided into groups of m bits. For example, in 4B/5B encoding, the original bit sequence is divided into 4-bit groups.
2. **Substitution:** In this step, we substitute an m-bit group for an n-bit group.
For example, in 4B/5B encoding we substitute a 4-bit code for a 5-bit group.
3. **Combining:** the n-bit groups are combined together to form a stream.

<img src="Images/Screenshot 2024-09-28 151454.png" width="" height="">

**4B/5B**
- This block coding scheme is designed to solve the synchronisation problem of NRZ-I.
- We know that long sequence of 0s is the cause of this problem.
- The block-coded stream does not have more that three consecutive
0s as you can see in the Encoded sequence column in table below.

<img src="Images/Screenshot 2024-09-28 154530.png" width="" height="">
- 
<img src="Images/Screenshot 2024-09-28 154846.png" width="" height="">

**Disadvantages:**
- The redundant bits add 20 percent more baud.
- does
not solve the DC component problem of NRZ-I.

**8B/10B**
- The most five significant bits of a 10-bit block is fed into the 5B/6B encoder; the
least 3 significant bits is fed into a 3B/4B encoder.
- To prevent a long run of consecutive Os or 1s, the code uses a disparity
controller which keeps track of excess Os over 1s (or 1s over Os).  
- The coding has $2^{10} - 2^8 = 768$ redundant groups that can be used for disparity checking
and error detection.
- **Advantages over 4B/5B:**
In general, the technique is superior to 4B/5B because of better
**built-in error-checking** capability and better **synchronization**

<img src="Images/Screenshot 2024-09-28 155553.png" width="" height="">

**Scrambling**
---
- The combination of block coding and NRZ line coding is not suitable for long-distance
encoding either, because of the DC component.
- Bipolar AMI encoding, on the other
hand, has a narrow bandwidth and does not create a DC component. 
- However, a long
sequence of Os upsets the synchronization
- So **scrambling** is a modification of AMI encoding where consecutive sequences of 0s substituted with a combination of other levels to provide synchronization without compromising with change in bit rate.

**R8ZS**
- In
this technique, eight consecutive zero-level voltages are replaced by the sequence OOOVBOVB. 
- The V(Violation) means the same polarity as the polarity of the previous nonzero pulse,since it breaks the rule of AMI Encoding.
- B(bipolm)
means the polarity opposite to the polarity of the previous nonzero pulse,Since it follows the rule of AMI.

<img src="Images/Screenshot 2024-09-28 161947.png" width="" height="">

**HDB3**
-  In this
technique, which is more conservative than B8ZS, four consecutive zero-level voltages are
replaced with a sequence of OOOV or BOOV
- The reason for two different substitutions is to
 maintain the even number of nonzero pulses after each substitution.

- The rules for the same are-
1. If the number of nonzero pulses after the last substitution is odd, the substitution
pattern will be OOOV, which makes the total number of nonzero pulses even.
2. If the number of nonzero pulses after the last substitution is even, the substitution
pattern will be BOOV, which makes the total number of nonzero pulses even

<img src="Images/Screenshot 2024-09-28 162324.png" width="" height="">

**ANALOG-TO-DIGITAL CONVERSION**
---

**Pulse Code Modulation (PCM)**
---
-  PCM encoder has three processes
1. **Sampling:**
- Sampling refers measuring the amplitude of the signal at equal intervals. 
- There are three
sampling methods-ideal, natural, and flat-top-as 
- **Ideal sampling:**
    -  It is a sampling where each instance of analog signal is sampled to capture the exact form of analogue signal.
    - Here, the sampling rate is infinite.
    - It is practically not possible
- **Natural sampling:** 
    - a high-speed
switch is turned on for only the small period of time when the sampling occurs. 
    - The
result is a sequence of samples that retains the shape of the analog signal.

<img src="Images/Screenshot 2024-09-28 164011.png" width="250" height="">

- **flat-top-as sampling/sample and hold:**
    - the top portion of the waveform is truncated horizontally, resulting in a flat or level top
    - Most commonly used sampling method.

<img src="Images/Screenshot 2024-09-28 164400.png" width="250" height="">

- According to the Nyquist theorem, the sampling rate must be
at least 2 times the highest frequency contained in the signal.
- The sampling rate must be at least 2 times the highest frequency, not the bandwidth.
- If the analog signal is low-pass, the bandwidth and the
highest frequency are the same value.
- If the analog signal is bandpass, the bandwidth
value is lower than the value of the maximum frequency.

<img src="Images/Screenshot 2024-09-28 164739.png" width="350" height="">

2. **Quantization**
- Process of assigning integral values in a specific range to the long range 
of sampled instances. 
- The following steps in quantization are:

<img src="Images/Screenshot 2024-09-28 165226.png" width="" height="">

<img src="Images/Screenshot 2024-09-28 165311.png" width="" height="">

3. **Encoding** 
-  After each sample is quantized and the number of
bits per sample is decided, each sample can be changed to an bit code word.
- This binary data are converted into digital signals by line coding.

**Delta Modulation (DM)**
---
- PCM is a very complex technique.The simplest is delta modulation. 
- PCM finds the value of the
signal amplitude for each sample; DM finds the change from the previous sample.
- It has two components modulator and demodulator.

**Modulator**
---
- It converts the analogue signal to digital data.
- The process records the small positive or negative changes, called delta $\delta$.
- If the delta is
positive, the process records a 1; if it is negative, the process records a O. 
- However, the
process needs a base against which the analog signal is compared. The modulator
builds a second signal that resembles a staircase.
- The modulator, at each sampling interval, compares the value of the analog signal
with the last value of the staircase signal.
- If the amplitude of the analog signal is larger,
the next bit in the digital data is 1; otherwise, it is O. 
- If the next bit is I, the staircase maker moves the
last point of the staircase signal 0 up; it the next bit is 0, it moves it 0 down. 

<img src="Images/Screenshot 2024-09-28 181737.png" width="" height="">

<img src="Images/Screenshot 2024-09-28 181836.png" width="" height="">

**TRANSMISSION MODES**
---

<img src="Images/Screenshot 2024-09-28 182133.png" width="" height="">

1. **Parallel transmission:**
- The  advantage  of  parallel  transmission  is  speed. 
-  All  else  being  equal,  parallel  transmission  can 
increase  the  transfer  speed  by  a  factor  of  n  over  serial  transmission.
-  But  there  is  a  significant 
disadvantage: cost. Parallel transmission requires n communication lines (wires in the example) just 
to  transmit  the  data  stream. 
-  Because  this  is  expensive,  parallel  transmission  is  usually  limited  to 
short distances. 

<img src="Images/Screenshot 2024-09-28 182445.png" width="" height="">

2. **Serial transmission**
- In  serial  transmission  all  the  data  bits  are  transmitted  across  a  single  wire  in  sequence. 
- The 
advantage of serial over parallel transmission is that with only one communication channel, serial 
transmission reduces the cost of transmission over parallel by roughly a factor of n.

<img src="Images/Screenshot 2024-09-28 184634.png" width="" height="">

**Asynchronous transmission** 
- Asynchronous transmission is so named because the timing of a signal is unimportant.
- We send 1 
start bit (0) at the beginning and 1 or more stop bits (1s) at the end of each byte.  
- There may be a gap between each byte. 
- The 
addition  of  stop  and  start  bits  and  the  insertion  of  gaps  into  the  bit  stream  make  asynchronous 
transmission  slower  than  forms  of  transmission  that  can  operate  without  the  addition  of  control 
information.  
- But  it  is  cheap  and  effective, that  make  it  an  attractive  choice  for 
situations such as low-speed communication.

<img src="Images/Screenshot 2024-09-28 190042.png" width="" height="">

**Synchronous transmission**
- In synchronous transmission, we send bits one after another without start or stop bits or gaps.
- It is 
the  responsibility  of  the  receiver  to  group  the  bits. 
- The  advantage  of 
synchronous transmission is speed. With no extra bits or gaps, synchronous transmission is faster 
than asynchronous transmission.

<img src="Images/Screenshot 2024-09-28 190310.png" width="" height="">

**Isochronous**
- used for sending real time audio and video. 
-  uneven  delays  between  frames  are  not  acceptable, 
synchronous transmission fails.
-  The 
isochronous transmission guarantees that the data arrive at a fixed rate.  
 
 
 

 

















