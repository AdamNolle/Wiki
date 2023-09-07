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