# Network Traffic Analysis Case Study: DNS and ICMP Incident

## Overview
This case study examines a network connectivity issue that prevented users from accessing the website www.yummyrecipesforme.com. The investigation focused on analyzing DNS and ICMP traffic using the tcpdump network protocol analyzer.

---

## Problem Description
Users reported that they were unable to access the website and encountered the error message "destination port unreachable." This indicated a potential issue with network communication or server availability.

---

## Investigation Process
To investigate the issue, network traffic was captured using tcpdump while attempting to access the website. The analysis focused on DNS queries and the responses received from the DNS server.

The captured traffic showed that the client system sent DNS queries using the UDP protocol to port 53 on the DNS server. Instead of receiving a valid DNS response, the system received ICMP error messages.

---

## Key Findings
- DNS queries were sent over UDP to port 53  
- The DNS server responded with ICMP error messages  
- The specific error message was "udp port 53 unreachable"  
- Multiple attempts to reach the DNS server resulted in the same error  
- No successful DNS resolution occurred  

These findings indicate that the DNS service was not available or accessible on the server.

---

## Analysis
The ICMP error message "port unreachable" indicates that the destination port (port 53) is not open or no service is listening on that port. Since DNS relies on UDP port 53, this failure prevents domain name resolution.

Without DNS resolution, the browser cannot obtain the IP address of the website, which results in the inability to establish an HTTPS connection.

---

## Root Cause
The most likely root cause of the issue is that the DNS server was not accepting connections on port 53. This could be due to:

- The DNS service being stopped or not running  
- A firewall blocking UDP traffic on port 53  
- Incorrect server configuration  

---

## Recommended Actions
To resolve the issue, the following steps are recommended:

- Verify that the DNS service is running on the server  
- Ensure that port 53 is open and listening for UDP traffic  
- Review firewall rules to confirm DNS traffic is not blocked  
- Test DNS resolution using alternative DNS servers  
- Restart the DNS service if necessary  

---

## Conclusion
The investigation determined that the failure to access the website was caused by an issue with DNS resolution. The DNS server was not responding to requests on port 53, leading to ICMP error messages and preventing users from reaching the website.

This case highlights the importance of monitoring network traffic and understanding protocol behavior when diagnosing connectivity issues.
