[Source](https://www.cnsr.dev/index_files/Classes/Networking/Content/02-Application.html)

# 02 - Application 

## Network applications 
- Classic text-based applications that became popular in the 1970s and 1980s: 
    - text email. remote access to computers, file transfers, and newsgroups. 
- Killer application of the mid-1990s:
    - The World Wide Web, encompassing Web surfing, search, and electronic commerce. 
- Instant messaging and P2P file sharing, the two killer applications introduced at the end of the millennium. 
- Since 2000, voice-over-IP (VoIP), YouTube, Netflix, World of Warcraft, Facebook, and Twitter. 

**Goal** write program that: 
- run on (different) end systems
- communicate over network
- e.g., web server software communicates with browser software

No need (or desire) to write software for network-core devices: 
- network-core devices do not (and SHOULD not) run user applications!
- applications on end systems allows for rapid app development, propagation, innovation
- this is changing somewhat, which could impede the development of new protocols. 

## Server
- Always-on host, called the server, which services requests from many other hosts, called clients. 
- permanent address
    - IP address
    - Overlay/hash address of some kind in the case of IP-anonymizing networks 
- Web server services requests from browsers running on client hosts. 
- When a Web server receives a request for an object from a client hosts, it responds by sending the requested object to the client host. 
- Now in data centers for scaling 

## Client 
- Communicate with server
- Maybe be intermittently connected
- May have dynamic IP addresses (or dynamically changing overlay addresses)
- Do not usually communicate directly with each other (unless hybrid client-server/p2p with p2p). 

## P2P architecture 
- Minimal (or no) reliance on dedicated servers in data centers. 
- Direct communication between pairs of intermittently connected hosts, called peers. 
- The peers are not owned by the service provider, but are instead desktops and laptops controlled by users, with most of the peers residing in homes, universities, and offices.
- Peers request service from other peers, provide service in return to other peers 
    - Self-scalability: each peer adds service capacity to the system by distributing files to other peers. 
- Cost effective, since they normally don't require significant server infrastructure and server bandwidth (in contrast with clients-server designs with data centers)
- Peers often exchange IP addresses (or overlay address, e.g., onion, garlic routing and crypto addresses).
    - Complex management, implementation, debugging? 

## Processes 
- It's not actually programs, but **processes** that communicate with each other. 
- A process is assigned by OS to a program that is running within an end system. 
- WHen processes are running on the same end system, they can communicate with each other with inter-process communication (IPC)
- Processes on two different end systems communicate with each other by exchanging **messages** across the computer network. 
- A sending process creates and sends messages into the network 
- A receiving process receives these messages and possibly responds by sending messages back. 
- Processes that initiates that communication (that is, initially contacts the other process at the beginning of the session) is nominally, if not substantially, labeled as the **client**. 
- The process that waits to be contacted to begin the session is nominally the **server** 

## Sockets
- Any message sent from one process to another must go through the underlying network. 
- A process sends messages into, and receives messages from, the network through an OS-defined software interface called a **socket**.
- A socket is the interface between the application layer and the within a host OS. 
- It is also referred to as the Application Programming Interface (API) between the application and the network, since the socket is the programming interface with which network applications are built. 

## Addresses
- To receive messages, process must have identifier 

Q: Does the IP address of a host, on which a process runs, suffice for identifying the process? 

A: No, many processes can be running on one host 

- In order for a process running on one host to send packets to a process running on another host, the receiving process needs to have an **address** with: 
    - address of the host OS itself (IP)
    - Identifier that specifies the specific receiving process in the destination host OS 
    - Popular applications have been assigned specific port numbers, e.g., 
        - A Web server (using the HTTP protocol) is usually identified by port number 80. 
        - A mail server process (using the SMTP protocol) is usually identified by port number 25.
        - An SSH server is usually identified on port number 22. 


For example, to send HTTP message to gaia.cs.umass.edu web server: 

  IP address: 128.119.245.12
  port number: 80

Hosts are often identified by IP address
- **IP address** is a 32-bit quantity uniquely identifying the host, in ipv4.
    - Addresses are 128 bit for ipv6. 
    - We ran out of ipv4 addresses...
- The sending process must also identify the receiving process (more specifically, the receiving socket) running in the host. 
    - This is information is needed because in general a host could be running many network applications. 
    - A destination port number serves this purpose. 

## Preview of transport services 
**Data integrity** 
- Some apps (e.g., file transfer, web transactions) require 100% reliable data transfer 
- Other apps (e.g., audio) can tolerate some loss

**timing** 
- Some apps (e.g., Internet telephony, interactive games) require low delay to be "effective" 
- Some apps (e.g., file download) tolerate delay 

**throughput** 
- Some apps (e.g., multimedia) require minimum amount of throughput to be "effective"
- Other apps ("elastic apps") make use of whatever throughput they get 

**security** 
- Encryption, data integrity, ...

## Multiple types of service: 

**Application usually choose between TCP and UDP** 
- TCP and UDP are transport layer 
- Employed by most application layer programs
- Other Transport layer, or pseudo-transport layer protocols exist. 
    - SCTP (stream control transmission protocol), SSU (I2P app), DCCP, RUDP, UDP-lite, etc. 
- An application designer could design their own transport layer protocol, since Transport layer and up runs on end hosts, as opposed to network infrastructure. 
    - Could build into the core/kernel of end operating systems and languages as new socket type. 
    - Could also just begin the features into the application layer, rather than actually get a transport protocol built into the kernel of an OS. 
    - UDP lets you build new things!

## TCP
**Connection-oriented service** 
- TCP has the client and server exchange transport-layer control information with each other, before the application-level messages begin to flow. 
- This so-called handshaking procedure alerts the client and server, allow them to prepare for an onslaught of packets. 
- After the handshaking phase, a TCP connection is said to exist between the sockets of the two processes. 
- The connection is a full-duplex connection, in that the two processes can both send messages to each other over the connection at the same time, bi-directionally
- When the application finishes sending messages, it must tear down the connection. 

**TCP has a reliable data transfer service** 
- The communicating process can rely on TCP to deliver all data sent without error and in the proper order. 

**TCP also includes a congestion-control mechanism** 
- The TCP congestion-control mechanism throttles a sending process (client or server) when the network is congested between sender and receiver. 

Summary

- **reliable transport:** between sending and receiving process
- **flow control:** sender won't overwhelm receiver 
- **congestion control:** throttle sender when network overloaded
- **does ot provide:** timing, minimum throughput guarantee, security 
- **connection-oriented:** setup required between client and server process 

## UDP 
- UDP is a no-fills, lightweight, transport protocol, providing minimal services. 
- UDP is a connectionless, so there is no handshaking before the two processes start to communicate. 
- UDP provides an unreliable data transfer service
- When a process sends a message will ever reach the receiving process. 
- Messages that do arrive at the receiving process may arrive out of order. 
- UDP does not include a congestion-control mechanism, so the sending side of UDP can attempt to pump data into the layer below (the network layer) at any rate ot pleases

UDP service: 
- Unreliable data transfer between sending and receiving process
- Does not provide: reliability, flow control, congestion control, timing, throughput guarantee, security, or connection setup. 

## Encryption 

Neither base TCP nor UDP provide any encryption!

An Enhancement for TCP provides: 

1. encryption,
2. data integrity, and 
3. end-point authentication. 

**The great thing about a TLS joke, is that you can tell if it's not the original...**

- This security enhancement used to be called **Secure Sockets Layer (SSL)**
- Transport layer security **(TLS)** is just a newer version of SSL. 
    - SSL was the name of now-defunct versions of what is now modern TLS. 
- TLS is not a third Internet transport protocol, on the same level as TCP and UDP, but an enhancement of TCP, at the application layer. 
- Applications needs to include TLS code (existing libraries) in both the client and server sides of the application. 
- TLS has its own socket API that is similar to the traditional TCP socket API. 
- Sending process passes cleartext data to the SSL socket.
- TLS in the sending host then encrypts the data and passes the encrypted data to the TCP socket. 
- Encrypted data travels over the Internet to the TCP socket in the receiving process. 
- Receiving socket passes the encrypted data to SSL, which decrypts the data.
- TLS passes the cleartext data through its SSL socket to the receiving process. 
- TLS socket API is like that of a TCP socket (just important and use).

Tunneling:
    Inner-most ->  Outer-more... > Outer-most 
    Application -> TLS -> TCP -> MAC -> Ethernet -> Physical 

## Application-layer protocols 
An **application-layer protocol** defines how an application's processes, running on different end systems, pass messages to each other, for exmaple:

- The **type of messages** exchanged, for example, request messages and response messages
    - E.g., request, response 
- The **syntax** of the various message types, such as the fields in the message and how the fields are delineated
- The **semantics** of the fields
    - Meaning of the information in the fields
- **Rules** for determining when and how a process sends messages and responds to messages, and change state. 

**Open protocols:**
defined in RFCs
allows for interoperability 
e.g., HTTP, SMTP
**Proprietary protocols:**
e.g., Skype (sued to be open, fun story)

## Web and HTTP
