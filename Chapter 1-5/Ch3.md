# Chapter 3
**Before u read**
---
- Refer to the diagrams  slide for better understanding.
- Pratice the questions disscused in the slide

**Frequency**
---
- **Frequency** is the rate of change with respect to time. Change in a short span of time means high frequency. Change over a long span of time means low frequency.
- If a signal does not change at all, its frequency is zero.If a signal changes instantaneously, its frequency is infinite.

**Phase**
---
- Phase describes the position of the waveform relative to time zero.

<img src="Images/Screenshot 2024-09-25 212006.png" width="" height="">

**Composite Signals**
---

- A single frequency sine wave is not useful in data communications ;we need to send a composite signal, a signal made of many simple sine waves. Since a single wave signal is more vulnerable to disturbances and sometimes it has no meaning.Eg, If we had only one single sine wave to conversion over the phone, it would make no sense and carry no information. We would just hear a buzz.
- According to **Fourier analysis**, any composite signal is a combination of simple sine waves with different frequencies, amplitudes, and phases.
- If the composite signal is periodic, the decomposition gives a series of signals with discrete frequencies; if the composite signal is non periodic, the decomposition gives a combination of sine waves with continuous frequencies(very imp)
- You can observe it in the diagram below

<img src="Images1/Screenshot 2024-12-10 201702.png" width="" height="">

<img src="Images1/Screenshot 2024-12-10 201927.png" width="" height="">

<img src="Images1/Screenshot 2024-12-10 202019.png" width="" height="">

Basic concepts abot digital signals
---
- **Bandwidth:** It is the difference between the lowest and highest frequency in a composite signal
- If a digital signal has $L$ levels then each level needs $\lceil\log_2{L}\rceil$(Ceiling function over log base 2) bits.Refer the problem given below.

<img src="Images1/Screenshot 2024-12-10 202322.png" width="" height="">


- **Bit Rate:** Bits per second
- **Bit Length:** The bit length is the distance one bit occupies on transmission medium.It is analogous to wavelength in digital signal
 $$\text{Bit length}=\text{propagation speed} \times \text{bit duration}$$
- A digital signal is a composite analog signal with an infinite bandwidth(very imp)


**Transmission of Digital Signals**
---

1. **Baseband Transmission** 
- Baseband transmission means sending a digital signal over a channel without changing the digital signal to an analog signal.
- Baseband transmission requires that we have a **low-pass channel**, a channel with a bandwidth that starts from zero.
- As you can see in the diagram below how a low pass channel with narrow and wide bandwidth look like

<img src="Images1/Screenshot 2024-12-10 204403.png" width="" height="">
 
- a low-pass channel with infinite bandwidth is ideal, but we cannot have such a channel in real life.

**Case 1: Low-Pass Channel with Wide Bandwidth**
- A low-pass channel with a wide bandwidth can be used to accurately communicate between two stations using digital signals. This is possible because the amplitudes of the frequencies at the border of the bandwidth are very small and can be ignored

**Case 2: Low-Pass Channel with Limited Bandwidth**
- In a low-pass channel with limited bandwidth, we approximate the digital signal with an analog signal. The level of approximation depends on the bandwidth available.
- Let us assume that we have a digital signal of bit rate N. 
-  If we want to send analog signals to roughly simulate this signal, we need to consider the worst case, a maximum number of changes in the digital signal.This happens when the signal carries the sequence 01010101 ... or the sequence 10101010
- Show me get our maximum frequency $f=\frac{N}{2}$(first harmonic frequency) and hence the bandwidth is
$$Bandwidth=\frac{N}{2}-0=\frac{N}{2}$$
- You can see the diagram given below how change in bits affect frequency.

<img src="Images1/Screenshot 2024-12-10 202819.png" width="" height="">

- To shape the analog signal more like that of a digital signal we need to add more harmonics to the frequencies to increase the bandwidth.
- Here you can see below how we increase the bandwidth to $3N/2$(third harmonics) and $5N/2$(fifth harmonics)

<img src="Images1/Screenshot 2024-12-10 203727.png" width="" height="">

- Look at a problem below on first, third and fifth harmonics.

<img src="Images1/Screenshot 2024-12-10 203934.png" width="" height="">

- As we discussed before bandwidth is half of bit rate, implies maximum bit rate is double of bandwidth as shown in the problem below.

<img src="Images1/Screenshot 2024-12-10 204053.png" width="" height="">


2. **Broadband Transmission**

- Broadband transmission or modulation means changing the digital signal to an analog signal for transmission(Modulation).
- Modulation allows us to use a **bandpass channel**-a channel with a bandwidth that does not start from zero as you can see below in the diagram.

<img src="Images1/Screenshot 2024-12-10 204659.png" width="" height="">

- You can see below the mechanism how a digital signal is transmitted through broadband transmission 

<img src="Images/Screenshot 2024-09-25 225641.png" width="" height=""> 

**TRANSMISSION IMPAIRMENT**
---

1. **Attenuation**
- Attenuation means a loss of energy or amplitude over time.
- To compensate for this loss, amplifiers are used to amplify the signal as shown in the diagram below.

<img src="Images1/Screenshot 2024-12-10 205051.png" width="" height="">

- We measure attenuation/amplification in decibel.Refer the problems given below

<img src="Images1/Screenshot 2024-12-10 205318.png" width="" height="">

<img src="Images1/Screenshot 2024-12-10 205547.png" width="" height="">

<img src="Images1/Screenshot 2024-12-10 205742.png" width="" height="">

<img src="Images1/Screenshot 2024-12-10 205845.png" width="" height="">

2. **Distortion**
- Distortion means that the signal changes its form or shape.
- Distortion can occur in a composite signal made of different frequencies. Each signal component has its own
propagation speed (see the next section) through a medium and, therefore, its own delay in arriving at the final destination. Differences in delay may create a difference in phase if the delay is not exactly the same as the period duration.

<img src="Images1/Screenshot 2024-12-10 210036.png" width="" height="">

3. **Noise**

- Noise is a wave in transmission medium interfering with the signal resulting in error signal at receiver side.
  
<img src="Images/Screenshot 2024-09-25 230931.png" width="" height="">

- Noise is measured in terms of SNR

**Signal-to-Noise Ratio (SNR):**
$$SNR=\frac{average\: signal\:power}{average\: noise\:power}$$
$$SNR_{dB}=10\log_{10}{SNR}$$

- More the value of SNR, more the channel is noiseless.
- A complete noiseless channel has SNR value infinity.

<img src="Images1/Screenshot 2024-12-10 210455.png" width="" height="">

**DATA RATE LIMITS**
---

**Noiseless Channel: Nyquist Bit Rate**

- For a noiseless channel, the Nyquist bit rate formula defines the theoretical maximum
bit rate
$$BitRate=2 \times bandwidth \times 10\log_2L$$
$$\text{L: No of levels}$$
- According to the formula, we might think that, given a specific bandwidth, we can
have any bit rate we want by increasing the number of signa11eve1s. Although the idea
is theoretically correct, practically there is a limit. 
- When we increase the number of sig-
nal1eve1s, we impose a burden on the receiver. Ifthe number of levels in a signal is just 2,
the receiver can easily distinguish between a 0 and a 1. If the level of a signal is 64, the
receiver must be very sophisticated to distinguish between 64 different levels.
- Increasing the levels of a signal may reduce the reliability of the system.

**Noisy Channel: Shannon Capacity**
-  Shannon capacity, to determine the
theoretical highest data rate for a noisy channel:
$$Capacity=bandwidth \times \log_2(1+SNR)$$
- Shannon formula there is no indication of the signal level, which means that no matter
how many levels we have, we cannot achieve a data rate higher than the capacity of the
channel.
- In other words, the formula defines a characteristic of the channel, not the method
of transmission.

**Using both limits**
- The Shannon capacity gives us the upper limit;
the Nyquist formula tells us how many signal levels we need.

<img src="Images/Screenshot 2024-09-25 233605.png" width="" height="">
