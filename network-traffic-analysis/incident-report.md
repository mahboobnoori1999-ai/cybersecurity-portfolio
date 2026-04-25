# Cybersecurity Incident Report: Network Traffic Analysis

## Activity Overview
This project analyzes DNS and ICMP traffic using tcpdump to identify network issues and determine the root cause of a cybersecurity incident.

---

## Part 1: Summary of the Problem

### Question:
Provide a summary of the problem found in the DNS and ICMP traffic log.

### Answer:
The network protocol analysis shows that DNS queries were sent using the UDP protocol to resolve the domain www.yummyrecipesforme.com. However, these requests failed because the system received ICMP error messages stating "udp port 53 unreachable."

Port 53 is used for DNS services, which translate domain names into IP addresses. The presence of ICMP error messages indicates that the DNS server could not process the request.

This suggests that the DNS service was unavailable, possibly due to a misconfiguration, the service being down, or a firewall blocking access to port 53.

---

## Part 2: Analysis and Cause of the Incident

### Question:
Explain your analysis of the data and provide at least one cause of the incident.

### Answer:

Time incident occurred:  
The incident occurred at approximately 13:24 (1:24 PM) based on the tcpdump log timestamps.

How the issue was discovered:  
The IT team became aware of the issue when users reported they could not access the website and received a "destination port unreachable" error.

Investigation actions taken:  
The cybersecurity analyst used tcpdump to capture and analyze network traffic. During this process, UDP packets were observed being sent to the DNS server, followed by ICMP error responses.

Key findings:  
- DNS queries were sent using UDP on port 53  
- The DNS server responded with ICMP error messages  
- The error message was: "udp port 53 unreachable"  
- Multiple attempts resulted in the same error  
- This confirmed that the DNS service was not accessible  

Likely cause of the incident:  
The most likely cause is that port 53 on the DNS server is closed, blocked, or the DNS service is not running, preventing DNS queries from being processed.

---

## Key Takeaways

- DNS relies on UDP port 53  
- ICMP errors help identify network issues  
- "Port unreachable" indicates a service failure or blockage  
- Network analysis tools like tcpdump are essential for troubleshooting
