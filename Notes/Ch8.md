# Ch8:Switching
- Whenever we have multiple devices, we have
the problem of how to connect them to make one-to-one communication possible. One
solution is to make a point-to-point connection between each pair of devices (a mesh
topology) or between a central device and every other device (a star topology). 
- These
methods, however, are impractical and wasteful when applied to very large networks.
- A better solution is switching. A switched network consists of a series of interlinked
nodes, called switches. 
- Switches are devices capable of creating temporary connections
between two or more devices linked to the switch.

**CIRCUIT-SWITCHED NETWORKS**
---
- A circuit-switched network is made of a set of switches connected by physical links.
- Each link is nor-
mally divided into n channels by using FDM or TDM
- each connection uses only one dedicated channel on each link.
- In circuit switching, the resources need to be reserved during the setup phase;
the resources remain dedicated for the entire duration
of data transfer until the teardown phase.

<img src="Images/Screenshot 2024-10-02 172624.png" width="" height="">

**Characteristics**
- Circuit switching takes place at the physical layer.
- Before starting communication, the stations must make a reservation for the resources
to be used during the communication(Setup phase). These resources, such as channels (bandwidth
in FDM and time slots in TDM), switch buffers, switch processing time, and switch
input/output ports, must remain dedicated during the entire duration of data transfer
until the teardown phase
- Data transferred between the two stations are not packetized (physical layer transfer
of the signal). The data are a continuous flow sent by the source station and received
by the destination station, although there may be periods of silence
- There is no addressing involved during data transfer. The switches route the data
based on their occupied band (FDM) or time slot (TDM). Of course, there is end-to-
end addressing used during the setup phase, as we will see shortly

**Three Phases of Circuit Switching**
- **Setup Phase:** Path is decided and resouces coming along the path are reserved.
- **Data Transfer Phase:** After the establishment of the dedicated path, the two parties can transfer data.
- **Teardown Phase:** When one of the parties needs to disconnect, a signal is sent to each switch to release
the resources.

**Efficiency:** Less efficient since resources are still reserved after the setup process even though there is no communication.

**Delay:** Delay is less since a dedicated path is already decided.

**DATAGRAM NETWORKS**
---
- In a packet-switched network, there is no resource reservation;
resources are allocated on demand
- If
the message is going to pass through a packet-switched network, it needs to be divided
into packets of fixed or variable size.
- Datagram switching is normally done at the network layer.Hence,Switching in the Internet is done by using the datagram
approach.
- Packets do not move in a dedicated path since resources are not reserved as shown in the figure below

<img src="Images/Screenshot 2024-10-02 174552.png" width="" height="">

- The datagram networks are sometimes referred to as **connectionless** networks. The
term connectionless here means that the switch (packet switch) does not keep information
about the connection state.
- There are no setup or teardown phases. Each packet is treated
the same by a switch regardless of its source or destination.

**Routing Table**
- Due to no dedicated path, packets Move independently in different routes.
- So the dictagram network uses a **routing table** based on the destination address and the corresponding forward output ports are recorded in the tables.

<img src="Images/Screenshot 2024-10-02 175447.png" width="" height="">

**Destination Address:** The destination address in the header of a packet in a datagram network
remains the same during the entire journey of the packet.

**Efficiency:** More efficient since no path is blocked

**Delay:** Greater delay since no dedicated path

**VIRTUAL-CIRCUIT NETWORKS**
- A virtual-circuit network is a cross between a circuit-switched network and a datagram
network. It has some characteristics of both.

**Characteristics:**
- Resources can be allocated during the setup phase, as in a circuit-switched network,
or on demand, as in a datagram network
- Data are sent in packets
- Packets follow the dedicated path
- Implemented in data link layer

**Addressing**
- In a virtual-circuit network, two types of addressing are involved: global and local
- **Global Addressing:**A source or a destination needs to have a global address-an address that can be unique
in the scope of the network or internationally if the network is part of an international
network. 
- **Virtual-Circuit Identifier:**
- The identifier that is actually used for data transfer is called the virtual-circuit identifie
- unlike a global address, VCI is a small number that has only switch scope; it is used by a frame between two switches
- VCI in a data
frame changes from one switch to another. 

<img src="Images/Screenshot 2024-10-02 181012.png" width="" height="">


