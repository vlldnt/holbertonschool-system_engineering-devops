## Secured and monitored web infrastructure


### **Adding firewalls, SSL certificate and 3 monitoring clients**
    
- **3 firewalls** have been added to filter incoming requests:
    - One at the client side (Chrome firewall) to prevent unauthorized external trafic
    - One in front of each backend server (2) to isolate servers from unexpected requests

- A **SSL certificate** to secure communication beteen client and infrastrcuture by encrypting data in transit, handled by the load-balancer

- **3 monitoring client** to colect data from the load balancer, server #1 and #2 and report data to Sumo Logic

### Firewalls 
Allow, limit, and block network traffic based on preconfigured rules in the hardware or software, analyzing data packets that request entry to the network. In addition to limiting access to computers and networks, a firewall is also useful for allowing remote access to a private network through secure authentication certificates and logins

### Why is the traffic served over HTTPS ?
To **encrypt data in transit** ensuring privacy and protection, **authentificate** the client to the server


### What monitoring is used for ?
To **colect data** from the ***load balancer, server #1 and #2*** and report data to Sumo Logic. Data could be traffic patterns or ressource usage.
<br>It can **detect failures** or anomalies. It provides a **view of the infrastructure** for debugging and performance optimisation

### How the monitoring tool is collecting data
Monitoring tools collect data using agents, log forwarding, APIs, or exporters
<br>For example, the SumoLogic watches logs, parses them, and sends data to the platform for realtime analysis and alerts

### What to do if you want to monitor your web server QPS ?
Measuring Queries Per Second involves monitoring the number of requests processed by a server over a specific period:
- Select the Time Frame: Decide the period over which you want to measure the requests (e.g., one minute)
- Count the Requests: Track the total number of requests received in that time frame
- Calculate QPS: Divide the total number of requests by the number of seconds
```python
600 requests / 60 seconds = 10 QPS (Queries Per Second)
```
---
### Why terminating SSL at the load balancer level is an issue ?
**Unencrypted traffic** between the load balancer and web servers is an acceptable risk only in a secure internal network, but it is not recommended in a shared environment

### Why having only one MySQL server capable of accepting writes is an issue ?
If the primary MySQL server fails, no new data can be written to the database, the application can still read data, but any attempt to write data will fail which could be a problem

### Why having servers with all the same components (database, web server and application server) might be a problem ?
If the server is hosting all the components and fails, everything fails the entire application will be down.
