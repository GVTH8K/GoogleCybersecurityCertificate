Cybersecurity Incident Report: 
Network Traffic Analysis

| **Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log**                                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| The traffic logs suggest that the DNS server is down or unreachable.                                                                                                                                                           |
| This is evident in the traffic logs, where it can be seen that attempts to ping the server resulted in ICMP echo reply messages stating that UDP port 53 is unreachable.                                                       |
| UDP port 53 is commonly used for DNS protocol traffic; therefore, it is highly likely that the DNS server is not responsive.                                                                                                   |
|                                                                                                                                                                                                                                |

| **Part 2: Explain your analysis of the data and provide one solution to implement**                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| The reported incident occurred today at 1:23 p.m. Around this time, customers contacted the IT department, stating that they received an error stating “destination port unreachable” when attempting to access the website.   |
| The issue is currently being investigated by the network security team in order to bring the service back up as soon as possible.                                                                                              |
| During our investigation into this issue, we conducted packet sniffing tests using tcpdump and Wireshark. In the resulting log file, we found that DNS port 53 was unreachable.                                                |
| The next step will be to identify whether the DNS server is down or traffic being sent to port 53 is being blocked by the firewall.                                                                                            |
| The DNS server may also be down due to a successful Denial of Service attack or some misconfiguration on the server itself.                                                                                                    |
|                                                                                                                                                                                                                                |
