Cybersecurity Incident Report

| **Section 1: Identify the type of attack that may have caused this network interruption**                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| A potential cause for the website’s connection timeout error is a denial-of-service attack.                                                                   |
| The logs show that the web server stopped responding after it was overloaded with SYN packet requests.                                                        |
| Because of this, the event was likely caused by an attack known as SYN flooding.                                                                              |
|                                                                                                                                                               |

| **Section 2: Explain how the attack is causing the website to malfunction**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| When establishing a connection with the web server, the connection is established through a three-way handshake that occurs when using the TCP protocol.      |
| The handshake consists of three steps, starting with a SYN packet being sent from the source to the destination to request a connection.                      |
| Next, the destination replies with a SYN-ACK packet to accept the connection, and the destination will reserve resources for the source to connect.           |
| Finally, an ACK packet is sent from the source to the destination, acknowledging the permission to connect.                                                   |
| During a SYN flood attack, a malicious actor sends a large number of SYN packets all at once.                                                                 |
| This overwhelms the server’s available resources reserved for new connections.                                                                                |
| Since there are no longer any available resources on the server, legitimate TCP connection requests will fail.                                                |
| The logs indicate that the web server was overwhelmed and is unable to process any new SYN requests from visitors.                                            |
| Because of this, the server is unable to establish any new connections, and visitors to the website will receive a connection timeout error.                  |
|                                                                                                                                                               |
