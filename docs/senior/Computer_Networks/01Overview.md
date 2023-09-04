[Source](https://www.cnsr.dev/index_files/Classes/Networking/Content/00-Inspiration.html)

# 01 - Overview  

## Perspective 1: Physical and information infrastructure 
**Billions of connected computing devices:**
- Hosts = end systems
- running networks apps
- smart devices 

**Communication links:**
- fiber, copper, radio, satellite
- transmission rate: bandwidth

**Packet switches:**
- forward packets (chunks of data)
- routers and switches 

**Inter-networked networks:**
- Interconnected ISPs

**Protocols:**
- control sending, receiving of messages
- e.g., TCP, IP, HTTP, 802.11

**Internet standards:**
- RFC: Request for comments 
- IETF: Internet Engineering Task Force

## Perspective 2: Service
**Infrastructure that provides services to applications:**
- Web, VoIP, games, e-commerce, social nets,...

**Provides programming interface to apps:**
- hooks that allow sending and receiving app programs to "connect" to Internet 
- Provides service options, analogous to postal service

## Human protocols versus Network protocols 
A network protocol is similar to a human protocol, except that the entities exchanging messages and taking actions are hardware or software components of some device (fro example, computer, smartphone tablet, router, or other network-capable device). 

A protocol defines the format and the order of messages exchanged between two or more communicating entities, as well as the actions taken on the transmission and/or receipt of a message or other event. 

All communication activity in Internet governed by protocols, public or proprietary. 

## Packet order
**Arrival order packet joke! is a critical to good a make

## Network edge
** Network edge:
- hosts: clients and servers
- servers often in data centers

**Access networks, physical media:**
- wired, wireless communication links

**Network core:**
- interconnected routers network of networks 

## End systems
Hosts = end systems, BOTH clients and servers
Routers - core

## DSL ISP
- Use existing telephone line to central office DSLAM
    - Data over DSL phone line goes to Internet 
    - Voice over DSL phone line goes to telephone net
- < 2.5 Mbps upstream transmission rate (typically < 1 MBbps)
- < 24 Mbps downstream transmission rate (typically < 10 Mbps)

## Cable ISP 
- HFC: hybrid fiber coax
    - asymmetric: up to 30 Mbps downstream transmission rate, 2 Mbps upstream transmission rate
- Network of cable, fiber attaches homes to ISP router
    - Homes share access network to cable head-end
    - Unlink DSL, which has dedicated access to central office 

frequency division multiplexing: different channels transmitted in different frequency bands

## Ethernet (like campus)
- Typically used in companies, universities, etc. 
- 10 Mbps, 100 Mbps, 1 Gbps transmission rates 
- Today, end systems typically connect into Ethernet switch 

## Wireless
Two uses of the term:

1. **Shared wireless access** network connects end system to router 
    - via base station aka "access point"

2. **Wide-area wireless access**
    - provided by telco (cellular) operator, 10's km 
    - between 1 and 10 Mbps
    - 3G, 4G, LTE, 5G, etc. 

## Terms
**Computer networks are often classified in function of the geographical area that they cover.**

- **LAN:** a local area network typically interconnects hosts that are up to a few or maybe a few tens of kilometers apart. 
- **MAN:** a metropolitan area network typically interconnects devices that are up to a few hundred kilometers apart
- **WAN:** a wide area network interconnect hosts that can be located anywhere on Earth. 

## Topology 
- Another classification fo computer networks is based on their physical topology. 
    - Full Mesh
        - To allow any host to send messages to any other host in the network, the easiest solution is to organize them as a full-mesh, with a direct and dedicated link between each pair of hosts. 
        - Such a physical topology is sometimes used, especially when high performance and high redundancy is required for a small number of hosts. 
        - However, it has two major drawbacks. 
        - For a network containing n hosts, each host must have n-1 physical interfaces. 
        - In practice, the number of physical interfaces on a node will limit the size of a full-mesh network that can be built. 
    - Bus
        - The second possible physical organization, which is also used inside computers to connect different extension cards, is the bus. 
        - In a bus network , all hosts are attached to a shared medium, usually a cable through a single interface. 
        - When one host sends an electrical signal on the bus, the signal is received by all hosts attached to the bus. 
        - A drawback of bus-based networks is that if the bus is physically cut, then the network is split into two isolated networks. 
        - For this reason, bus-based networks are sometimes considered to be difficult to operate and maintain, especially when the cable is long and there are many places where it can break. 
        - Such a bus-based topology was used in the early Ethernet networks. 
    - Star
        - A third organization of a computer network is a star topology. 
        - In such topologies, hosts have a single physical interface and there is one physical link between each host and the center of the star. 
        - The node at the center of the star can be either a piece of equipment that amplifies an electrical signal, or an active device, such as a piece of equipment that understands the format of the messages exchanged through the network. 
        - However, if one physical link fails (e.g. because the cable has been cut), then only the node is disconnected from the network. 
        - In practice, star-shaped networks are easier to operate and maintain than bus-shaped networks. 
        - Many network administrators also appreciate the fact that they can control the network from a central point. 
        - Administered from a Web interface, or through a console-like connection, the center of the star is a useful point of control (enabling or disabling devices) and an excellent observation point (usage statistics). 
    - Ring
        - A fourth physical organization of a network is the Ring topology. 
        - Like the bus organization, each host has a single physical interface connecting it to the ring. 
        - Any signal sent by a hot on the ring will be received by all hosts attached to the ring. 
        - From a redundancy point of view, a single ring is not the best solution, as the signal only travels in one direction on the ring; 
            - Thus if one of the links composing the ring is cut, the entire network fails. 
        - In practice, such rings have been used in local area networks, but are now often replaced by star-shaped networks. 
        - In metropolitan networks, rings are often used to interconnect multiple locations. 
        - In this case, two parallel links, composed of different cables, are often used for redundancy. 
        - With such a dual ring, when one ring fails all the traffic can be quickly switched to the other ring. 
    - Tree
        -  A fifth physical organization of a network is the tree. 
        - Such network are typically used when a large number of customers must be connected in a very cost-effective manner. 
        - Cable TV networks are often organized as trees. 
    - Hybrid 
        - In practice, most real networks combine part of these topologies. 
        - For example, a campus network can be organized as a ring between the key buildings, while smaller buildings are attached as a tree or a star to important buildings. 
        - An ISP network may have a full mesh of devices in the core of its network, and trees to connect remote users. 

## Physical Media 
- Bits: propagates between transmitter/receiver pairs
- Physical link: what lies between transmitter & receiver 
- Guided media:
    - Signal propagate in solid media: copper, fiber, coax 
- Unguided media:
    - Signals propagate freely, e.g., radio

## Wire 
- Coaxial cable:
    - Two concentric copper conductors 
    - Bidirectional 
    - Broadband:
        - Multiple channels on cable 
- Twisted pair (TP)
    - Two insulated copper wires 
        - Category 5: 100 Mbps, 1 Gbps Ethernet 
        - Category 6: 10 Gbps
    - Fiber optic cable:
        - Glass fiber carrying light pulses, each pulse a bit
        - High-speed operation:
            - High-speed point-to-point transmission (e.g., 10's-100's Gbps transmission rate)
        - Low error rate:
            - Repeaters spaced far apart 
            - Immune to electromagnetic noise 

## Radio
  - Signal carried in electromagnetic spectrum 
  - No physical "wire"
  - Bidirectional 
  - Propagation environment effects:
      - Reflection
      - Obstruction by objects
      - Interference
  - Radio link types:
      - Terrestrial microwave
          - e.g. up to 45 Mbps channels
      - LAN (e.g., WiFi)
          - 54 Mbps
      - Wide-area (e.g., cellular)
          - 4G cellular: ~ 10 Mbps
      - Satellite 
          - Kbps to 45 Mbps channel (or multiple smaller channels)
          - 270 msec end-end delay
          - geosynchronous versus low altitude 

## Network core
- Mesh of interconnected routers
- Packet-switching:
    - Hosts break application-layer messages into packets
    - Forward packets from one router to the next, across links on path from source to destination 
    - Each packet transmitted at full link capacity 

## Two key network-core functions 
**Routing:**
- Determines source-destination route taken by packets 
- A variety of routing algorithms 
- Operates on longer time-scales 

**Forwarding:**
- Move packets from router's input to appropriate router output 
- Chooses instant path of packet 


## Packet Switching 
- In a network application, end systems exchange messages with each other. 
- Messages can contain anything the application designer wants. 
- Messages may perform a control function (for example, the "Hi messages in our handshaking example in or can contain data, such as an email message, a JPEG image, or an MP3 audio file.)
- To send a message from a source end system to a destination end system, the source breaks long messages into smaller chunks of data known as packets. 
- Between source and destination, each packet travels through communication links and packet switches (for which there are two predominant types, routers and link-layer switches). 

## To whom?
**Broadcast**

In TV and radio transmission, broadcast is often used to indicate a technology that send a video or radio signal to all receivers in a given geographical area. Broadcast is sometimes used in computer networks, but only in local area networks where the number of recipients is limited. 

**Unicast**
The first and most widespread transmission mode is called unicast. In the unicast transmission mode, information is sent by one sender to one receiver. The example shows a network with two types of devices: hosts (drawn as computers) and intermediate nodes (drawn as cubes). Hosts exchange information via the intermediate nodes. In the example below when host S uses unicast to send information, it send it via three intermediate nodes. Each of these nodes receives the information from its upstream node or hosts, then processes and forwards it to its downstream node or host. This called store and forward and we will see later that his concept is key in computer networks. 

**Multicast** 
A second transmission mode is multicast transmission mode. This mode is used when the same information must be sent to a set of recipients. It was first used in LANs but later became supported in wide area networks. When a sender uses multicast to send information to N receivers, the send sends a single copy of the information and the network nodes duplicate this information necessary, so that it can reach all recipients belonging to the destination group. 

**Anycast**
The last transmission mode is the anycast transmission mode. It was initially defined in RFC 1542. When a source sends information towards this set of receivers, the network ensures that the information is delivered to one receiver that belongs to this set. 

## Routing and forwarding 
- Every end system has an address called an IP address. 
- Source includes the destination's IP address in the packet's header. 
- Address had a hierarchial structure. 
- Router examines a portion of the packet's destination address and forwards the packet to the best adjacent router. 
- Each router has a forwarding table that maps destination addresses (or portions of the destination addresses) to the router's outbound links. 
- When a packet arrives at a router, the router examines the address and searches its forwarding table, using this destination address, to find the appropriate outbound link. 
- Multiple routing protocols that are used to automatically develop the forwarding tables themselves. 
- E.g., determine the shortest path from each router to each destination and use the shortest path results to configure the forwarding tables in the routers. 

## Store-and-forward packet switching
- Takes L/R seconds to transmit (push out) L-bit packet into link at R bps
- Store and forward: entire packet must arrive at router before it can be transmitted on next link 
- End-end delay = 2L/R (assuming zero propagation delay)

one-hop numerical example: 
 L = 7.5 Mb
 R = 1.5 Mb/s 
 one-hop transmission delay = 5 sec

## Packet queuing and loss
- If arrival rate (in bits) to link exceeds transmission rate of link for a period of time, packets will queue, wait to be transmitted on link. 
- Packets can be dropped (lost) if memory (buffer) fills up

## Circuit switching 
- End-end resources allocated to, reserved for "call" between source & dest: 
- In diagram, each link has four circuits. 
    - A call gets 2nd circuit in top link and 1st circuit in right link. 
- Dedicated resources: no sharing 
    - Circuit-like (guaranteed) performance
- Circuit segment idle if not used by call (no sharing)
- Commonly used in traditional telephone networks. 

A circuit in a link is implemented with either:
- Frequency-division multiplexing (FDM) or
- Time-division multiplexing (TDM)

## Packet versus circuit switching 
- Example: 
    - 1 Mb/s link 
    - Each user: 
        - 100 kb.s when "active" 
        - Active 10% of time 
- Circuit-switching: 
    - 10 users 
- Packet switching:
    - With 35 users, probability > 10 active at same time is less than .0004

Packet switching 
- Great for bursty data 
    - Resource sharing 
    - Simpler, no call setup (reserving a line)
- Excessive congestion possible: packet delay and loss
    - Protocols needed for reliable data transfer, congestion control


## Global network structure 
**Internet structure: network of networks**
- End systems connect to Internet via access ISPs (Internet Service Providers)
    - Residential, company, and university ISPs
- Access ISPs in turn must be interconnected. 
    - So that any two hosts can send packets to each other 
-  Resulting network of networks is very complex. 
- Evolution was driven by economics and national policies
- Let's take a step-wise approach to describe current Internet structure 

**Network of ISPs**
Not just technical considerations: corporate, historical, collusive, regulatory 
- At center: small number of well-connected large networks
    - "Tier-1" commercial ISPs (e.g., Level 3, Sprint, ATT, NTT), national and international coverage
    - Content provider network (e.g., Google): 
        - Private network that connects its data centers to Internet, often bypassing tier-1, regional ISPs, 
    - Internet Exchange Point (IXP) is a meeting point where multiple ISPs can peer together. 
        - An IXP is typically in a stand-alone building with its own switches. 
        - There are well over 400 IXps in the Internet "today" (may be out of date)

## Nodal delay at router A 
- Packets queue in router buffers 
    - Packet arrival rate to link (temporarily) exceeds output link capacity 
    - Packets queue, wait for turn 

All delay is not the same. 
If we let ```d_proc, d_queue, d_trans, and d_prop``` denote the processing, queuing, transmission, and propagation delays, then the total nodal delay is given by: 

```d_nodal = d_proc + d_queue + d_tans + d_prop```

**Network load**
The impact of increasing network load is super-linear on delay
R: link bandwidth (bps)
L: packet length (bits)
a: average packet arrival rate

La/R ~ 0: avg. queueing delay small
La/R -> 1: avg. queueing delay large
La/R > 1: more "work" arriving than can be serviced, average delay infinite!

## What do "real" Internet delay and loss look like? 
The ```traceroute``` program delay measurement from source to router along end-end Internet towards destination. 

For all i:
- Sends three packets that will reach router i on path towards destination 
- Router i will return packets to sender 
- Sender times interval between transmission and reply. 

## Commands to try  
(watch with Wireshark too):

```
$ traceroute mst.edu
$ traceroute www.mst.edu 
$ traceroute efp1.ch
$ traceroute www.epf1.ch
```

Alternative fancier program
```$ mtr epfl.ch```

## Dropped packets 
With no place to store such a packet, a router will drop that packet; that is, the packet will be lost. 

## Throughput
- In addition to delay and packet loss, another critical performance measure in computer networks is end-to-end throughput. 
- To define throughput, consider transferring a large fle from Host A to Host B across a computer network. 
- This transfer might be, for example, a large video clip from one peer to another in a P2P file sharing system. 
- The instantaneous throughput at any instant of time is the rate (in bits/sec) at which the Host B is receiving the file. 

Bottleneck throughput limitations tend to be servers and local ISPs (edge), not the backbone (core). 

## Protocol layers, service models 
- Networks are complex, with many "pieces":
  - hosts
  - routers
  - links of various media 
  - applications 
  - protocols 
  - hardware, software 

## Layered protocols 
- To provide structure to the design of network protocols, network designers organize protocols, and the networks hardware and software that implement the protocols, in layers. 
- In a theoretical vacuum, each protocol belongs to one of the layers, just as a each function in the airline architecture. 
- A protocol layer can be implemented in software, in hardware, or in a combination of the two. 
- When taken together, the protocols of the various layers are called a networking protocol stack. 
- The Internet protocol stack can be oversimplified to **five layers:**
    - **1. physical**,
    - **2. link**, 
    - **3. network**,
    - **4. transport**, 
    - **5. application**, 

## Layering 
**Why layering?** 

- Explicit structure allows identification, relationship of complex system's pieces 
- Modularity eases maintenance, updating of system. 
- Change of implementation of layer's service transparent to rest of system. 
    - E.g., change in gate procedure doesn't affect rest of system 

Internet protocol stack 

- **1. Application:** 
    - Supporting network applications 
    - FTP, SMTP, HTTP
- **2. Transport:**
    - OS-process to OS-process data transfer 
    - TCP, UDP, and some more rare others
- **3. Network:**
    - Routing of datagrams from source to destination 
    - IP, routing protocols 
- **4. Link:** 
    - Data transfer between neighboring network elements 
    - Ethernet, 802.111 (WiFi), ppp, etc. 
- **5. Physical:**
    - Bits "on the wire" or "over the airwaves" 

## Application 
**Supporting network applications** 
- Network applications and their application-layer protocols reside here
- Examples:
    - **HTTP** Hypertext Transfer Protocol provides for Web document request and transfer
    - **SMTP** Simple Mail Transfer Protocol provides for the transfer of e-mail messages
    - **FTP** (which provides for the transfer of files between two end systems).
    - **DNS** provides translation of human-friendly names for Internet systems to a 32-bit network address (ipv4). This is also done with the help of a specific application-layer protocol, namely, the Domain Name System (DNS). 
- An application-layer protocol is distributed over multiple end systems, with the application in one end system using the protocol to exchange packets of information with the application in another end system. 
- Packet of information at application layer is a **message.**    
- Encryption often implemented at this layer (though it should at least as low as the Network/IP layer).

The upper layer of our architecture is the Application layer. This layer includes all the mechanisms and data structures that are necessary for the applications. Our big-picture book calls these packets ADUs. 

## Transport 
**OS-Process to OS-process data transfer** 
- Transports application-layer messages between application endpoints
- In the current Internet, there are two primary transport protocols, TCP and UDP, either of which can transport application-layer messages. 
- **TCP** (Transmission Control Protocol) provides a connection-oriented service to its applications. 
    - Guaranteed delivery of application-layer messages to the destination
    - Flow control (that is, sender/receiver speed matching). 
    - Congestion-control mechanism, so that a source throttles its transmission rate when the network is congested. 
- **UDP** (User Datagram Protocol) protocol provides a connectionless service to its applications. 
    - No-frills service that provides no reliabiluty, no flow control, and no congestion control. 
- Transport-layer packet is a **segment**. 
- Most realizations of the network layer, including the internet, do not provide a reliable service. 
- However, many applications need to exchange information reliably, and so using the network layer service directly would be very difficult for them 
- Ensuring the reliable delivery of the data produced by application is the task of the transport layer. 
- Transport layer entities exchange segments. 
- A segment is a finite sequence of bytes that are transported inside one or more packets. 
- A transport layer entity issues segments (or sometimes part of segments) as requests to the underlying network layer entity. 
- The most widely used transport layers on the Internet are TCP, that provides a reliable connection-oriented bytestream transport service, and USP, that provides an unreliable connection-less transport service. 
- There are some other interesting transport layer protocols, though they are not as common. 

## Network
**Routing of datagrams from source to destination 
- Responsible for moving network-layer packets known as **datagrams** from one host to another. 
- Transport-layer protocol (TCP to UDP) from source host passes a transport-layer segment and a destination address to the network layer 
- Network layer then provides the service of deliverign the segment to the transport layer in the destination host. 
- Network layer includes the celebrated IP, which defines the fields in the datagram as well as how the end systems and routers act on these fields. 
- There is only one IP protocol (or two...), and all Internet components that have a network layer must run it. 
- Network layer also contains many routing protocols that determine the routes
- The network layer is built above the datalink layer. 
- The Datalink layer (below) allows directly connected hsts to exchange information, but it is often necessary to exchange information between hosts that are no attached to the same physical medium. 
- This is the task of the network layer. 
- Network layer entities exchange packets. 
- A packet is a finite sequence of bytes that is transported by the datalink inside one or more frames. 
- A packet usually contains information about its origin and its destination, and usually passes through several intermediate devices called routers on its way from its origin to its destination. 

## Link / datalink
**Data transfer between adjacent nodes**

- At each node, the network layer passes the datagram down to the link layer, which delivers the datagram to the next nod along the route. 
- At this next node, the link layer passes the datagram up to the network layer. 
- Some link-layer protocols provide reliable delivery, from transmitting node, over one link, to receiving node. 
- Examples of link-layer protocols include: Ethernet, WiFi, the cable access network's DOCSIS protocol, and more
- A datagram may be handled by Ethernet on one link and by WiDi on the next link. 
The network layer (above) will receive a different service from each one of the different link-layer protocols. 
- Link-layer packets are **frames**
- The Datalink layer builds on the service provided by the underlying physical layer. 
- The Datalink layer allows two hosts that are directly connected through the physical layer to exchange information. 
- The unit of information exchanged between two entities in the Datalink layer is a frame. 
- A frame is a finite sequence of bits. 
- Some Datalink layers use variable-length frames while others only use fixed-length frames. 
- Some Datalink layers provide a connection-oriented service while other provide a connectionless service. 
- Some Datalink layers provide reliable delivery while others do not guarantee the correct delivery of the information. 
- An important point to note about the Datalink layer is that although the figure below indicates that two entities of the Datalink layer exchange frames directly, in reality this is slightly different. 
- When the Datalink layer entity on the left needs to transmit a frame, it issues as many requests to the underlying physical layer as there are bits in the frame. 
- The physical layer will then convert the sequence of bits in an electromagnetic or optical signal that will be sent over the physical medium. 
- The physical layer on the right hand side of the figure will decode the received signal, recover the bits and issue the corresponding Data. Indication primitives to its Datalink layer entity. 
- If there are no transmission errors, this entity will receive the frame sent earlier. 

## Physical 
**Bits "on the wire"**
- The protocols in this layer are again link dependent and further depend on the actual transmission medium of the link (for example, twisted-pair copper wire, single-mode fiber optics).
- For example, Ethernet has many physical-layer protocols: one for twisted-pair copper wire, another for coaxial cable, another for fiber, and so on. 
- In each case, a **bit** is moved across the link in a different way. 

An important point to note about the Physical layer is the service that it provides. This service is usually an unreliable connection-oriented service that allows the users of the Physical layer to exchange bits. The unit of information transfer in the Physical layer is the bit. The Physical layer service is unreliable because:
- The Physical layer may change, e.g. due to electromagnetic interferences, the value of a bit being transmitted 
- The Physical layer may deliver more bits to the receiver than the bits sent by the sender 
- The Physical layer may deliver fewer bits to the receiver than the bits sent by the sender
- The physical layer allows this two or more entities that are directly attached to the same transmission medium to exchange bits. 
- Being able to exchange bits is important as virtually any information can be encoded as a sequence of bits. 
- Electrical engineers are used to processing streams of bits, but computer scientists usually prefer to deal with higher level concepts. 


## OSI 
- **Presentation:** allow applications to interpret meaning of data, e.g., encryption, compression, machine-specific conventions
- **Session:** synchronization, checkpointing, recovery of data exchange 
- Internet stack "missing" these layers. 
- These services, if needed, myst be implemented in application. 

## Network security 
- Internet not originally designed with (much) security in mind 
- Original vision: "a group of mutually trusting users attached to a transparent network"
- Internet protocol designers playing "catch-up"
- Security considerations in all layers!
- Field of network security:
    - How bad guys can attack computer networks 
    - How we can defend networks against attacks 
    - How to design architectures that are immune to attacks 

**Types of attack**
- DoS (Denial of Service) - the most common attack, often easy
- Packet "sniffing": broadcast media (shared Ethernet, wireless), promiscuous network interface reads/records all packets (e.g., including passwords!) passing by
- Masquerading
- and more!

## Malware
- Malware can get into host from: 
    - virus: self-replicating infection by receiving/executing objects (e.g., e-mail attachment)
    - worm: self-replicating infection by passively receiving object that gets itself executed 
- Spyware malware can record keystrokes, web sites visited, upload info to collection site
- Infected host can be rolled in botnet, used for spam. DDoS attacks 

## Attack server, network infrasturcture 
Denial of Service (DoS): attackers make resources (server, bandwidth) unavailable to legitimate traffic by overwhelming resource with bogus traffic 

1. Select target
2. Break into hosts 
3. Send packets to target from compromised hosts

## Sniffing packets 
- Packet "sniffing": 
- Broadcast media (shared Ethernet, wireless)
- Promiscuous network interface reads/records all packets (e.g., including passwords!) passing by
- Wireshark software is a packet sniffer
- Malicious infrastructure. 
    - A trustless "Distrust the infrastructure" is a good policy, even when you don't think it's corrupt. 

## Faking addresses
IP spoofing: send packet with false source address