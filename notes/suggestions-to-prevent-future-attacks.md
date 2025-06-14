## As part of the activity we had an option to give suggestions to secure the network against future attacks.

To prevent similar TCP SYN flood (DoS) attacks and improve the resilience of the company’s web server, the following mitigations are recommended:

- **Implement SYN cookies:** Enable SYN cookies on the web server. This technique ensures the server doesn’t allocate resources for half-open connections, making it harder for attackers to exhaust connection slots.
- **Deploy a Web Application Firewall (WAF):** A WAF can help detect and block malicious traffic patterns, including SYN flood attacks, before they reach the web server.
- **Rate limiting / throttling:** Configure rate-limiting rules at the firewall or load balancer level to detect and slow down traffic that matches suspicious SYN patterns.
- **Intrusion Detection and Prevention Systems (IDS/IPS):** Use IDS/IPS to detect anomalous SYN traffic and automatically block or drop malicious packets.
- **Geo-blocking or IP reputation filtering:** If attacks originate from certain regions or known bad IPs, you can block or challenge those requests.
- **Increase server capacity with load balancers:** Distribute traffic across multiple servers so no single machine is overwhelmed by connection requests.
- **Monitor and log traffic patterns:** Continuously monitor network traffic using tools like Wireshark, Zeek, or commercial solutions to identify and respond to unusual spikes early.

Applying a combination of these strategies can significantly reduce the risk and impact of future DoS attacks on the organization’s infrastructure.
