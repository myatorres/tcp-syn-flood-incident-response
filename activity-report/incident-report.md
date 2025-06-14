# Cybersecurity Incident Report

## Section 1: Identify the type of attack that may have caused this network interruption

One potential explanation for the website's connection timeout error message is:
> The web server is likely experiencing a TCP flood attack, which is a denial-of-service (DoS) attack. This attack prevents users from successfully establishing a connection with the server, resulting in connection timeout errors when trying to access the website.

The logs show that:
> A single IP address is sending repeated TCP SYN packets every second. There are no responding ACK packets meaning the connections are not being completed. Thus the server becomes overwhelmed by the amount of requests being sent, eventually preventing legitimate connections.

This event could be:
> A TCP SYN flood attack (DoS).

---

## Section 2: Explain how the attack is causing the website to malfunction

When website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol:

1. The client sends a SYN packet to the server to initiate the connection.
2. The server responds with a SYN-ACK packet to acknowledge the request.
3. The client responds with an ACK packet to confirm the connection, completing the handshake.

---

Explain what happens when a malicious actor sends a large number of SYN packets all at once:
> The malicious actor sends only the first part of the handshake—the SYN request—but never completes the process by sending the final ACK. The server responds with SYN-ACKs initially, but as the volume of requests increases, its resources become exhausted.

Explain what the logs indicate and how that affects the server:
> The logs reveal a surge of SYN packets from a single IP address, sent at a rate of one per second. The server eventually stops responding to both the malicious traffic and legitimate connection attempts. As a result, legitimate users experience connection timeouts, and the server becomes effectively unreachable. This disruption leads to service downtime, negatively impacting the organization’s integrity and reputation, as customers are unable to access critical services through the company’s website.
