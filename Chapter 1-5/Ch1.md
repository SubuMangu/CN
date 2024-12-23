# Chapter 1
**Data Communication:**
---
- Data communications are the exchange of data between two devices via some form of transmission medium such as a wire cable.
-  **Characteristics of Data Communication:**
	1. **delivery:** The system must deliver data to correct destination.
	2. **accuracy:** The system must deliver data accurately.
	3. **timeliness:** The system must deliver data in a timely manner. Timely delivery means delivering data as they are produced, in the same order that they are produced and without significant delay. This kind of delivery is called real –time transmission.
	4. **jitter:** Jitter refers to the variation in the packet arrival time.It is the uneven delay inthe delivery of audio or video packets. For example, let us assume that video packets are sent every 3D ms. If some of the packets arrive with 3D-ms delay and others with 4D-ms delay, an uneven quality in the video is the result. 
 

- A data communications system has five components :Message,Sender,Receiver,Medium,Protocol( Refer to pg no.40-41)
- **Protocol:** A protocol is a set of rules that govern data communications.(Pgno. 41)
- **Standard** ensures authenticity or reliabilty of a network.

**Data Flow(pgno 42-43)**
---
- **Simplex:** In simplex mode, the communication is unidirectional, as on a one-way street. Only one of the two devices on a link can transmit; the other can only receive. Keyboards and traditional monitors are examples of simplex devices. The keyboard can only introduce input; the monitor can only accept output.
- **Half-Duplex:** In half-duplex mode, each station can both transmit and receive, but not at the same time.When one device is sending, the other can only receive, and vice versa.Walkie-talkies and CB (citizens band) radios are both half-duplex systems.
- **Full-Duplex:** both stations can transmit and receive simultaneously.Either the link must contain two physically separate transmission paths, one for sending and the other for receiving; or the capacity of the ch:arillilel is divided between signals traveling in both directions.Eg, telephone network.both can talk and listen at the same time.

<img src="Images/Screenshot 2024-09-24 151642.png" width="" height="">

**Networks**
---
- A network is a set of devices (often referred to as nodes) connected by communication links. A node can be a computer, printer, or any other device capable of sending and/or receiving data generated by other nodes on the network.
- **Distributed Processing:** a task is divided among multiple computers. 
- **Network Criteria:** A network must be able to meet a certain number of criteria- performance, reliability, and security.(44-45)
- **Types of connection** (45)
	- **Point-to-Point:** In point-to-point connection the two devices are connected by a dedicated link. The entire capacity of the link is reserved for transmission between those two devices.
	- **Multipoint:** A multipoint (also called multidrop) connection is one in which more than two specific devices share a single link.In a multipoint environment, the capacity of the channel is shared, either spatially or temporally. If several devices can use the link simultaneously, it is a *spatially shared connection*. If users must take turns, it is a *timeshared* connection

	<img src="Images/Screenshot 2024-09-24 204419.png" width="" height="">

**Network Topology(45-50)**
--- 
- The **topology** of a network is the geometric representation of the relationship of all the link and linking devices (usually called nodes) to one another.
1. **Mesh:** every device has a dedicated point-to-point link to every other device.In other words,we can say that in a mesh topology,we need $\frac{n(n-1)}{2}$ duplex-node links.
- **advantages of mesh(47)**
	1. the use of dedicated links guarantees that each connection can carry its own data load, thus eliminating the traffic problems that can occur when links must be shared by multiple devices.
	2. a mesh topology is **robust**. If one link becomes unusable, it does not incapacitate the entire system.
	3. advantage of privacy or security:As every message travels along a dedicated line only the intended recipient
	4. point-to-point links make fault identification and fault isolation easy
- **Disadvantages of mesh(47)**
	-  The main disadvantages of a mesh are related to the amount of cabling and the
 number of I/O ports required.
	1. because every device must be connected to every other device, installation and reconnection are difficult.
	2. More amount of cabling and the I/O  ports required
	3.  the hardware required to connect each link (I/O ports and cable) can be
 prohibitively expensive.
-  One practical example of a mesh topology is the connection of telephone regional
 offices in which each regional office needs to beconnected to every other regional office.

<img src="Images/Screenshot 2024-09-24 205025.png" width="300" height="">

2. **Star topology(47-48):**  In a star topology, each device has a dedicated point-to-point link
 only to a central controller, usually called a *hub*. 
- The controller acts as an exchange: If one device wants to send  data to
 another, it sends the data to the controller, which then relays the data to the other connected device.
- **Advantages of star topology(47-48)**
	1. Less expensive than a mesh topology. Each device needs only one link and I/O port to connect with Hub.
	2.  **robustness:** If one link fails, only that link is affected. All other links remain active.
	3. The above factor also lends itself to easy fault identification and  fault isolation. As long as the hub is working, it can be used to monitor link problems and bypass defective links.
- **Disadvantages of star topology(48)**
	-  One big disadvantage of a star topology is the dependency of the whole topology on one single point, the hub. If the hub goes down, the whole system is dead
	-  Although a star requires far less cable than a mesh, each node must be linked to a central hub. For this reason, often more cabling is required in a star than in some other topologies (such as ring or bus).
- The star topology is used in local-area networks (LANs).

<img src="Images/Screenshot 2024-09-24 211030.png" width="300" height="">


3. **Bus topology(48):**  The preceding examples all describe point-to-point connections. A bus
 topology, on the otherhand, is multipoint. One long cable acts as a backbone to link all
 the devices in a network.
- Nodes are connected to the bus cable by *drop lines* and *taps*.
- A **drop line** is a connection running between the device and the main cable.
- A **tap** is a connector that either splices into the main cable or punctures the sheathing of a cable to create a contact with the metallic core.
- As a signal travels along the backbone, some of its energy is transformed into heat. Therefore, it becomes weaker and weaker as it travels farther and farther. For this reason there is a limit on the *number of taps* a bus can support and on the *distance between those taps*.
- **advantages of bus topology(48-49):** 
	- ease of installation
	- less cabling than mesh or star topologies.
- **disadvantages of bus topology(49):** 
	- difficult reconnection and fault isolation
	- difficult to add new devices
	- fault or break in the bus cable stops all transmission

<img src="Images/Screenshot 2024-09-24 211111.png" width="300" height="">

4. **Ring topology(49- 50)**
- Dedicated point-to-point configuration to neighbors 
- A signal is passed along the ring
in one direction, from device to device, until it reaches its destination.
- Each device in the ring incorporates a **repeater**. When a device receives a signal intended for another device, its repeater regenerates the bits and passes them along
- **advantages of ring topology:** 
	- Easy to install and reconfigure.
	- Each device is linked to only its immediate neighbors (either physically or logically). To add or delete a device requires changing only two connections.
	- If one device does not receive the signal within a specified period, it issue an alarm that alerts the network operator to the problem and its location
- **disadvantages of ring topology(49):**
	- A break in the ring breaks the entire network.

<img src="Images/Screenshot 2024-09-24 211244.png" width="350" height="">

5. **Hybrid Topology(50):** A network can be hybrid. For example, we can have a main star topology with each branch connecting several stations in a bus topology.

**Network Models(50)**
---
- Computer networks are created by different entities. Standards are needed so that these
heterogeneous networks can communicate with one another. The two best known standards are 
	- OSI model 
	- Internet model(TCP/IP)

**Categories of Networks(50-52)**
---
1. **LAN**
- Usually privately owned and links the devices in a single office, building, or campus 
- LAN size is limited to a few kilometers.
- LANs are designed to allow resources to be shared (hardware , software and data )
- Today LANs to have data rates of 100 Mbps to 10Gbps 
- LANs are designed to allow resources to be shared between personal computers or
workstations. The resources to be shared can include hardware (e.g., a printer), software
(e.g., an application program), or data.
- One of the computers may be given a large-
capacity disk drive known as **Server**.
- Software can be stored on this
central server and used as needed by the whole group
- The size of the
LAN may be determined by licensing restrictions on the number of users per copy of software, or by restrictions on the number of users licensed to access the operating system
2. **MAN**
- A MAN is designed to cover an entire city.
- May be a single network such as cable TV network
- May be a means of connecting  a number of  LANs into a larger network   
- MANs  have data rates of 1 Mbps to 100 Mbps 
- Resources may be shared  LAN to LAN as well as device to device 
- A company can use a MAN to connect the LANs in all its offices throughout a city. 
- A MAN can be owned by a private company or it may be a service provided by a public company 
,such as local telephone company 
- Telephone companies provide a popular MAN service called (SMDS) Switched Multi-megabit Data 
Services.
3. **WAN**
- WAN provides long distance transmission of data, voice, image, and video information over large 
geographical areas  
- Comprise a country, a continent, or even the whole world (Interlink age of many LANs and MANs) 
- Low data transmission rate (below 1 Mbps) 
- Unlimited number of miles  example: Internet Network
- A WAN can be as complex as the backbones that connect the Internet or as
simple as a dial-up line that connects a home computer to the Internet. We normally refer
to the first as a switched WAN and to the second as a point-to-point WAN.
- The **switched WAN** connects the end systems, which usually comprise a router (internet-
working connecting device) that connects to another LAN or WAN.
- The **point-to-point WAN** is normally a line leased from a telephone or cable TV provider that connects a
home computer or a small LAN to an Internet service provider (lSP).

<img src="Images/Screenshot 2024-11-03 171456.png" width="" height="">

<img src="Images/Screenshot 2024-09-24 221619.png" width="400" height="">

**Internetwork**
---
- Connection of two or more networks by the use of internetworking devices which include routers 
and gateways 
- Internet is a generic term used to mean an interconnection of networks  
- The Internet is the name of a specific worldwide network

**Example of Internetwork**
- As an example, assume that an organization has two offices, one on the east coast
and the other on the west coast.
- The established office on the west coast has a bus topology
LAN; the newly opened office on the east coast has a star topology LAN.
- The president of
the company lives somewhere in the middle and needs to have control over the company from her home.
- To create a backbone WAN for connecting these three entities (two
LANs and the president's computer), a switched WAN (operated by a service provider
such as a telecom company) has been leased.
- To connect the LANs to this switched
WAN, however, three point-to-point WANs are required. These point-to-point WANs
can be a high-speed DSL line offered by a telephone company or a cable modern line
offered by a cable TV provider as shown in Figure


<img src="Images/Screenshot 2024-11-03 171643.png" width="" height="">

<img src="Images/Screenshot 2024-09-24 221942.png" width="300" height="">



**Internet(54-56)**
---
- History
- TCP/IP
- ISP

**Protocols and Standard(56-)**
- **Protocols**:
	- **Syntax:** The term syntax refers to the **structure** or **format** of the data, meaning the order in which they are presented. For example, a simple protocol might expect the first 8 bits of data to be the address of the sender, the second 8 bits to be the address of the receiver, and the rest of the stream to be the message itself 
	- **Semantics:** The word semantics refers to the meaning of each section of bits. For example, does an address identify the route to be taken or the final destination of the message?
	- **Timing:** The term timing refers to two characteristics: when data should be sent and how fast they can be sent.
- **Standards**
    - **De facto(by fact/convention):** Standards that have not been approved by an organized body but have
been adopted as standards through widespread use are de facto standards. 
	- **De Jure(by law):** Those standards that have been legislated by an officially recognized body
are de jure standards
- https://chatgpt.com/c/67270634-fdcc-800c-8707-8474f8d1d762


