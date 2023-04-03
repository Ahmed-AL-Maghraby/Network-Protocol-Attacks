
## What's The Telnet ?
Telnet is a protocol used for interactive communication between two devices over a network ( Remote Login )

| Name  | OSI Layer | Port | Attack  |
| ---   | ---       | ---  | ---     |
| Telnet | Application  | 23 TCP     |  - Password sniffing <br> - Brute force attacks <br> - MitM <br> - DOS   |

<BR>

## Several Common Attacks 

1. Password sniffing: Since TELNET sends all communication in plain text, an attacker can easily sniff network traffic and capture usernames and passwords.

2. Brute force attacks: Attackers can attempt to guess usernames and passwords by using automated tools to try a large number of possible combinations.

3. Man-in-the-middle (MitM) attacks: An attacker can intercept and modify TELNET traffic between a client and server, allowing them to steal data, inject malicious code, or hijack the session.

4. Denial-of-service (DoS) attacks: Attackers can flood a TELNET server with a large number of connection requests, overwhelming the server and causing it to crash or become unavailable.
