[Source](https://www.cnsr.dev/index_files/Classes/Networking/Content/00-Inspiration.html)

# 00 - Inspiration 

## Before the internet, there was the ARPANET
- Precursor to the modern internet ARPANET was an academic research project funded by the **Advanced Research Projects Agency** which was a branch of the military known for funding projects without commercial or military applications. 
- Originally the network only connect the University of Utah with three research centers in California. 
- ARPANET used new technology called **packet-switching** which breaks data into smaller _packets_ so that they can be transmitted efficiently across the network. 
- Also had the goal of making expensive computing resources more efficient. 
- Computer scientists sometimes used ARPA money to buy computers, and the agency hoped that ARPANET would allow universities to share these expensive resources more efficiently. 
- One of the first applications of ARPANET was **Telnet** which allowed a researcher at one ARPANET site to _log into_ a computer at another site. 


## 1970: ARPANET expands 
- By the end of 1970 ARPANET had grown to 13 nodes which included East Coast schools like Harvard and MIT. 
- Some of the other early nodes where Bolt, Beranek, and Newman (BBN) - an engineering consulting company that did the engineering work to build ARPANET. 
- Each ARPANET site used a **router** known as an **Interface Message Prcoessor** costing $82,200 or half a million in today's money. 


## 1973: ARPANET goes international 
- In 1973 the ARPANET became international, with a satellite link connecting Norway and London to the other nodes in the U.S. 
    -  Hawaii also joined by satellite. 
-  Network not at around 40 nodes.
- ARPANET _applications_ had begun to emerge: 
    - **Email** was invented in 1971 by a BBN engineer named Ray Tomlinson, who also invented the use of the "@" symbol in email addresses. 
    - The **File Transfer Protocol**, which is still used today, allowed ARPANET users to send files to each other. 

## 1982: The ARPANET community grows
- As the ARPANET entered its second decade, it was still largely confined to the U.S. 
- Academic institutions depended on federal funding to join the network, so the number of nodes expanded slowly. 
- By 1982, the network only had about 100 nodes. 
    - This still was big enough for a vibrant online community 
- Long before Facebook and Twitter, ARPANET allowed computer scientists who had access to the network to stay in touch. 
- A **new bullentin board system called Usenet** was invented in 1980 and caught on quickly. 
    - Usenet was organized by topic, allowing users to swap programming tips, recipes, jokes, opinions about science fiction, and much more. 

## hosts.txt
- Computers need numeric addresses, but which human own which numeric address is hard for people to remember. 
- The ARPANET had no **distributed host name database**
- Originally a file named _HOSTS.TXT_ was manually maintained and made available via file sharing by Stanford Research Institute for the ARPANET membership, containing the **hostnames and address of hosts** as contributed for inclusion by member organizations. 
- **Each network node maintained its own map of the network nodes as needed and assigned them names that were memorable to the users of the system. 
- There was no method for ensuring that all references to a given node in a network were using the same name, nor there a way to read the hosts file of another computer to automatically obtain a copy. 
- The small size of the ARPANET kept the administrative overhead small to maintain an accurate host file. 
- Network nodes typically had one address and could have many names. 
- As local area TCP/IP computer networks gained popularity, however, the maintenance of hosts file names became a larger burden on system administrators as networks and network nodes were being added to the system with increasing frequency.
- The **Domain Name System (DNS)**, first described in 1983 and implemented in 1984, automated the publication process and provided instantaneous and dynamic hostname resolution in the rapidly growing network. 
- In modern operating systems, the hosts file remains an alternative name resolution mechanism, configurable often as part of facilities such as the Name Service Switch as either the primary method or as a fallback method. 

## 1984: ARPANET becomes the internet 
- Originally, the entire ARPANET was managed by the military 
- But network operators **realized that a centralized network would eventually become unmanageable** if they continued to grow. 
- They decided that the network should be reorganized as a decentralized **"network of networks."**
- Under this scheme, different networks would be controlled by different organizations, but all the **networks able to communicate using shared standards**, forming aa shared "internet."
- The military asked the computer scientists Robert Khan and Vint Cerf to develop new networking standards to make this possible. 
- The result was a set of standards known as **TCP/IP**
    - These **standards specified the basic format of data packets** transmitted across the internet. 
    - **On January 1, 1983, the ARPANET switched to using TCP/IP, marking the birth of the modern internet!**
    - The switch to TCP/IP didn't make much difference from a user perspective, since applications like email and Telnet worked about the same as they had before. 
    - But the new standard paved the way for much faster network growth by lowering the barrier to entry for new networks. 
- One of the first new networks to connect to the new internet was CSNET, which was funded by the National Science Foundation to link computer science departments across the country. 
- By the time the ARPANET was decommissioned in 1990, it was just one of many networks that comprised the internet. 
- "Today" (may be out of date now), the internet is made up of more than 40,000 different networks. 
- **These networks still communicate with each other using the TCP/IP** standards similar to those that Cerf and Kahn developed in the 1970s. 

## NSFNET: The first internet backbone
- During the 1980s, the National Science Network funded several super-computing centers around the United States. 
    - And in 1986 the agency created a TCP/IP-based network called NSFNET to link those super-computing centers together and allow researchers across the country to use them. 
    - The primary goal was to allow computer science researchers to log into the supercomputers and perform academic research. 
- But NSF decided not to limit NSFNET to that purpose, allowing the network to be used for a **wide variety of academic purposes**. 
- As a result, the NSFNET became the **internet's "backbone", the high-speed, long-distance network** that allowed different parts of the internet to communicate. 
- Schools that didn't have a direct connection to the NSFNET worked together to build regional networks that linked them to each other and to the nearest NSF node. 
- By 1992 there were 6,000 networks connected to NSFNET, with a third of them located overseas. 
- That meant that students and faculty at a growing number of universities had access to **email, Usenet, and event a recently-invented application called the World Wide Web!**
- And although the NSFNET was officially restricted to non-commercial use, for-profit companies were increasingly connecting to the network as well, setting the stage for the commercialization of the internet that followed. 

## The internet becomes a global network 
- In 1993, **the internet was still dominated by the United States**, but it was becoming a truly global network. 

## The privatization of the internet backbone
- In 1994, the Clinton Administration further facilitated the **privatized the internet backbone.**
- **Commercial firms that took over the job of carrying long-distance internet traffic**, allowing the government-funded NSFNET to be decommissioned . 
- Officials were careful to ensure that no single company controlled too much of the backbone, helping to create a **competitive market for internet connectivity that still exists today**. 
- By the turn of the century for of the largest long-distance network providers were UUNET, AT&T, Spring, and Level 3. 
- Each had its own nationwide (and global) network, and they competed with each other to provide long-distance connectivity to smaller networks. 
- UUNet became part of WorldCom in 1996, and became part of Verizon in 2006.
- Today, Verizon operates one of the world's largest internet backbones, in competition with AT&T, Spring, Level 3 and many other companies. 

## How the world gets online: fixed broadband penetration in 2012
- There are two primary ways people can long onto the internet: 
    - Through a **fixed broadband connection at home or in an office** and 
    - via a **wireless connection, often on a cell phone or tablet.**
- This data from the International Telecommunications Union shows how popular fixed internet access is around the world. 
- It shows internet access is widespread in the most parts of the world, but is still fairly scarce in much of sub-Saharan Africa and the Middle East. 
- Fixed internet access allows multiple devices in a customer's home to access the internet. 
- Fixed connections are also ideal for streaming-video services such as Netflix because they tend to have greater capacity than wireless networks. 

## How the world gets online: mobile broadband penetration in 2012
- In the developed world, people usually got fixed internet access first and obtained mobile internet devices later. 
- But some **developing countries are skipping the construction of fixed broadband networks altogether.** 
- This is a cost-effective because a single cell phone tower can provide service to hundreds of customers. 
- For example, 2.7 percent of Egyptians have fixed broadband service at home, but 10 times as many Egyptians have internet access using a cell phone. 
- The story is similar in Ghana, Uzbekistan, Indonesia, South Africa, and Nigeria. 
- **Mobile internet access can have profound implications for people in isolated areas.** 
- Farmers can use mobile phones to learn about recent market developments, increasing the amount they can get for their crops. 
- Some mobile phone operators also offer sophisticated payment capabilities, allowing people who don't have access to the conventional banking system to make electronic payments. 
- A few wealthy countries, including Japan, South Korea, and Sweden, that have more mobile internet subscriptions than people. 
- Some customers have two or more smartphones, tablets, or other connected mobile devices.

## World broadband speeds, 2014
- Internet access is a lot faster in some places than others. 
- According to Speedtest.net, a website that lets users test their own internet connections, the **fastest internet in the world is in Hong Kong**, with an average of almost 80 million bits per second (Mbps). 
- Other high-speed countries include Japan, South Korea, Sweden, Romania, the Netherlands, and Switzerland. 
- **The United States clocks in a number 30, with average speeds of 24 Mbps. 
- These figures are worth taking with a grain of salt because they're based on a self-selected sample. 

## Where does your data live?
- Big companies have centralized locations for data storage (maps can be found online).
- Smaller web companies store their servers in data centers managed by third parties, but the internet's largest companies have their own dedicated data centers with hundreds of thousands of servers in them. 
- These data centers are located around the world, **distributed** 
    - That has **two advantages**
    - First, locating data centers **close to users allows data to be delivered more quickly.**
    - Second, it helps provide **redundancy:** if the user data is kept in multiple locations, it will be **safe even in the event of a catastrophic failure** are one data center. 

##  Internet censorship around the world
- In most Western countries, the internet is a free-speech zone where ordinary people express themselves without fear of censorship. 
- But that's not true everywhere. 
- Cuba and several countries in Southeast Asia and the Middle East engage in pervasive censorship and are marked in purple. 

## And then COVID onlined everything... 
- COVID caused a rapid growth of online users worldwide. 
- Users that came online outpaced predictions. 