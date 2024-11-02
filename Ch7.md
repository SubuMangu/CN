# Ch 7: Transmission media
- A transmission media define as anything that can carry information from a source to a destination. 
-  Transmission media are actually located below the physical layer and directly controlled by the 
physical layer.

<img src="Images/Screenshot 2024-10-02 142005.png" width="" height="">

**Guided/Wired media**
---
- Guided media refers to communication channels where data signals are transmitted through a physical medium, such as cables (e.g., twisted pair, coaxial, or fiber-optic cables).

1.  **Twisted-Pair Cable** 
- A  twisted  pair  consists  of  two  conductors  (normally  copper),  each  with  its  own  plastic  insulation, 
twisted together.
- One  of  the  wires  is  used  to  carry  signals  to  the  receiver,  and  the  other  is  used  only  as  a  ground 
reference.  The  receiver  uses  the  difference  between  the  two.
- In  addition  to  the  signal  sent  by  the 
sender  on  one  of  the  wires,  interference  (noise)  and  crosstalk  may  affect  both  wires  and  create 
unwanted signals happens in case of unshielded twisted-
pair (UTP).
- STP cable has a metal foil or braided- mesh covering that encases each pair of insulated 
conductors.  Although  metal  casing  improves  the  quality  of  cable  by  preventing  the  penetration  of 
noise or crosstalk, it is bulkier and more expensive.  

<img src="Images/Screenshot 2024-10-02 142901.png" width="" height="">

<img src="Images/Screenshot 2024-10-02 143710.png" width="" height="">

2. **Coaxial Cable**
-  The outer metallic wrapping serves both as a shield against noise and as the reference wire (ground) for the signal carried by the inner conductor
- This outer conductor is also enclosed in an insulating sheath, and the whole 
cable is protected by a plastic cover
**Advantages**
- Coaxial cable (or coax) carries signals of higher frequency ranges than those in twisted- pair cable
- Less noise or crosstalk
**Diadvantages**
- Attenuation is much higher in coaxial cables than in twisted pair cable.
- Coaxial  cable  has  a  much  higher  bandwidth  the  signal  weakens  rapidly  and  needs  the 
frequent use of repeaters. 

3. **Fiber Optic Cable**
- A fiber optic cable is made of glass or plastic and transmits signals in the form of light. Optical fibers use reflection to guide light through a channel.
- A glass or plastic core is surrounded by a cladding of less dense glass or plastic. The difference in the 
density of the two materials must be such that a beam of light moving through the core is reflected off 
the cladding. 

**Advantages**
- **Higher bandwidth:** It can support higher bandwidth than twisted pair or  coaxial cable.
- **Less  signal  attenuation:** Transmission  distance  is greater  than  that  of other guided media.  Signals 
can be transmitted for 50 km without requiring regeneration.
- **Immunity to electromagnetic Interference:** Electromagnetic noise can not affect fiber-optic cables.

**Disadvantages**
- Installation/Maintenance
- Unidirectional:  Propagation  of  light  is  unidirectional.  Bidirectional  communication  is  achieved  by 
means of two optical fibers.
- Cost
 
**Unguided/Wireless media**
---
- Unguided media transport electromagnetic waves without using a physical conductor. This type of 
communication is often referred to as wireless communication. 

1. **Radiowaves**
- **Frequency** 
- Between 3 KHz – 1 GHz.
- **Application:**
- Radio waves are used for multicast communications,
such as radio and television, and paging systems
- **Advantages:**
- Radio waves, for the most part, are **omnidirectional**. When an antenna transmits
radio waves, they are propagated in all directions. This means that the sending and
receiving antennas do not have to be aligned.
- Radio waves, particularly those waves that propagate in the sky mode, can travel
long distances.
- Radio waves, particularly those of low and medium frequencies, can **penetrate walls**.an AM radio can receive signals inside a closed building.
- **Disadvantages:**
- The
radio wave band is relatively narrow, just under 1 GHz, compared to the microwave
band. When this band is divided into subbands, the subbands are also narrow, leading to a
low data rate for digital communications
- The omnidirectional property has a disadvantage,
too. The radio waves transmitted by one antenna are susceptible to interference by
another antenna that may send signals using the same frequency or band.
- Penetrating walls can be a disadvantage because we cannot isolate communication to just inside or outside a building

2. **Microwaves**
- **Frequency:** between 1 and 300 GHz
- **Properties**
- **Unidirectional:**Microwaves need unidirectional antennas that send out signals in one direction. Two
types of antennas are used for microwave communications: the parabolic dish and the
hom 
- Very high-frequency microwaves cannot penetrate walls. 
- **Application:**
- Microwaves are used for unicast communication such as cellular telephones,
satellite networks, and wireless LANs.
- **Advantages:**
- **High data rate:**The microwave band is relatively wide, almost 299 GHz. Therefore wider subbands
can be assigned, and a high data rate is possible
- Less chance of interference since unidirectional
- **Disadvantages:**
- sending and receiving antennas need to
be aligned properly
- Very high-frequency microwaves cannot penetrate walls. This characteristic can be
a disadvantage if receivers are inside buildings.

3. **Infrared Waves**
- **Frequency:** 300 GHz to 400 THz 
- **Properties**
- Short-range communication
- having high
frequencies, cannot penetrate walls.
- **Application:**
- Remote controls and other short range communications.
- **Advantages:**
- prevents interference between one system and another
- More data rate and bandwidth
- **Disadvantages:**
- Infrared signals useless for long-range communication
- In
addition, we cannot use infrared waves outside a building because the sun's rays contain
infrared waves that can interfere with the communication.

