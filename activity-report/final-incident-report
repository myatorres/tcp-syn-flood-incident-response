# Finalized Cybersecurity Incident Report

## Section 1: Identify the type of attack that may have caused this network interruption

The web server is likely experiencing a TCP SYN flood attack, which is a type of denial-of-service (DoS) attack. This attack prevents legitimate users from successfully establishing a connection with the server, resulting in connection timeout errors when attempting to access the company’s website. The captured network logs indicate that a single IP address is repeatedly sending TCP SYN packets at a consistent rate of one per second. Notably, no corresponding ACK packets are present, meaning that the connections initiated by these SYN requests are not being completed. As the server attempts to manage these numerous half-open connections, its resources become exhausted, ultimately blocking or delaying responses to legitimate connection attempts.

## Section 2: Explain how the attack is causing the website to malfunction

The TCP handshake, which is essential for establishing a reliable connection between a client and a server, consists of three steps. First, the client sends a SYN packet to the server to initiate the connection. The server responds with a SYN-ACK packet, acknowledging the client’s request and signaling readiness to establish the connection. Finally, the client completes the handshake by replying with an ACK packet, confirming that the connection has been successfully established. 

In the case of this attack, the malicious actor sends only the initial SYN packets but deliberately does not complete the handshake by sending the final ACK. Initially, the server responds with SYN-ACKs as expected, but as the volume of malicious SYN packets increases, the server's resources become tied up managing these incomplete connections. Eventually, the server is unable to respond to legitimate users attempting to access the website, causing connection timeouts and service outages. This disruption leads to downtime, negatively impacting the organization’s integrity, reputation, and ability to serve its customers through its web platform.

