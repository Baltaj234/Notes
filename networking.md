# Introduction to IP and Networking Protocols

# Overview of modern Networks

Modern networks are designed to transfer information between devices using various methods like Ethernet, wireless and DSL.

Networks can be visualized as a series of highways or roads, where IP acts as the truck carrying data across the network.

# Encapsulation and Decapsulation

Encapsulation is the process of nesting data within multiple layers of protocls for transmission.

Decapsulation is the reverse process, where data is unpacked layer by layer upon arrival. 

# Internet Protocol

Internet Protocol (IP) is the primary protocol for data transmission across networks.

Two key transport protocols are usually used in IP packets:
- TCP (Transmission control protocol)
- UDP (User Datagram Protocol)

# transmission control protocol

TCP is a connection oriented protocol meaning it establishes a formal connection before data transfer and formally closed it afterwards.

Key features include:

Reliable Delivery - Uses acknowledgments to confirm data receipt

Flow Control - The receiver can request the sender to speed up or slow down data transmission.

Error Recovery - Detects and corrects errors during transmission.


# User Datagram Protocol

UDP is a connectionless protocol. Meaning it does not establish a formal connection before sending any data.

Key features include:

Unreliable Delivery - No acknowledgments are sent, so there is no guarantee that data will arrive intact.

No error recovery - lost or corrupted bits are not transmitted again.

no flow control - The sender transmits data at its own pace without any feedback from the receiver.

low overhead - Faster and more efficient than TCP due to the lack of connection setup and acknowledgment processes.

# Multiplexing

Multiplexing allows multiple types of data to be transmitted at the same time across a network using TCP or UDP.

Each type of traffic is assigned a unique port number to ensure it reaches the correct application on the receiving device.

