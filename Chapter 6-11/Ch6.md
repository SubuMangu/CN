# Ch 6
- Bandwidth utilization is the wise use of available bandwidth to achieve specific goals.
Efficiency can be achieved by multiplexing;
privacy and antijamming can be achieved by spreading

**Multiplexing**
---
- In multiplexing, our goal is efficiency; we combine several channels into one.
- Whenever the bandwidth of a medium linking two devices is greater than the bandwidth needs of the 
devices,  the  link  can  be  shared.  
-  Multiplexing  is  the  set  of  techniques  that  allows  the  (simultaneous) 
transmission  of  multiple  signals  across  a  single  data  link.  As  data  and  telecommunications  use 
increases, so does traffic.

<img src="Images/Screenshot 2024-10-02 111818.png" width="" height="">

- There  are  three  basic  multiplexing  techniques:  frequency-division  multiplexing,  wavelength-division 
multiplexing, and time-division multiplexing. The first two are techniques designed for analog signals, 
the third, for digital signals.

<img src="Images/Screenshot 2024-10-02 111959.png" width="" height="">

<img src="Images/Screenshot 2024-10-02 112254.png" width="" height="">

- The word channel refers to the portion of a link that carries a transmis-
sion between a given pair of lines. One link can have many (n) channels.

**Frequency-division multiplexing (FDM):**
- It is an analog technique that can be applied when the bandwidth of a link (in hertz) is greater than the 
combined bandwidths of the signals to be transmitted.
- 
- The steps carried out in FDM are:
1. **Multiplexing Process:** FDM is an analog multiplexing technique that combines analog signals 

<img src="Images/Screenshot 2024-10-02 114453.png" width="" height="">

2. **Demultiplexing Process:** 
- The demultiplexer uses a series of filters to decompose the multiplexed signal into its
constituent component signals. 
- The individual signals are then passed to a demodulator
that separates them from their carriers and passes them to the output lines. 

- Guard band creates gap between two signals to avoid interference

**The Analog Carrier System**

- The Analog Carrier System is a method used by telephone companies to send multiple phone calls over a single high-bandwidth line. 
- It is made up of groups, super-
groups, master groups, and jumbo groups

**Other Applications of FDM**
- **Telephone systems (analog) –** Combining multiple phone calls into a single high-bandwidth line.
- **Radio broadcasting –** Multiple radio stations use different frequency bands to broadcast simultaneously.

**Wavelength-Division Multiplexing**
- WDM is an analog multiplexing technique to combine optical signals
- Wavelength-division multiplexing (WDM) is designed to use the high-data-rate
capability of fiber-optic cable.
-  The  optical  fiber  data  rate  is  higher  than  the  data  rate  of  metallic  transmission  cable
- The combining and splitting of light sources are easily handled by a prism. 
- Using  this  technique,  a  multiplexer  can  be  made  to  combine  several  input  beams  of  light,  each 
containing a narrow band of frequencies, into one output beam of a wider band of frequencies. A de-
multiplexer can also be made to reverse the process.

<img src="Images/Screenshot 2024-10-02 122632.png" width="" height="">

**Time-Division Multiplexing**
-  each signal gets its own small time slot. These time slots rotate very quickly, so each signal gets sent in turn. This happens so fast that it feels like all the signals are being sent simultaneously, even though they’re actually taking turns using the channel.
- There is no need to have guard band in this type of multiplexing
-  Time-division multiplexing (TDM) is a digital process that allows several 
connections to share the high bandwidth of a link. Instead of sharing a portion of the bandwidth as in 
FDM, time is shared. 

<img src="Images/Screenshot 2024-10-02 123727.png" width="" height="">

- We can divide TDM into two different schemes: synchronous and statistical.
-  In synchronous TDM, each input connection has an allotment in the output even if it is not sending 
data. In synchronous TDM, the data rate of the link is n times faster, and the unit duration is n times 
shorter.
- Statistical TDM gives time slots only to devices that have data to send, instead of giving everyone fixed slots, making it more efficient.
- TDM can be visualized as two fast-rotating switches, one on the multiplexing side and the other on the 
demultiplexing  side.  
- The  switches  are  synchronized  and  rotate  at  the  same  speed,  but  in  opposite 
directions. 
-  On the multiplexing side, as the switch opens in front of a connection, that connection has 
the opportunity to send a unit onto the path. This process is called interleaving. 

**Interleaving**
-  The process of taking a group of bits from each input line for multiplexing is called **interleaving**.

