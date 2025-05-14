## Scale up

### Adding one server and one load balancer and split components

![scaleup](https://github.com/vlldnt/holbertonschool-system_engineering-devops/blob/main/web_infrastructure_design/images/3-scale___up.png?raw=true)

### Adding Cluster load Balancer
One load balancer added in a cluster ensures high availability by eliminating the load balancer as a single point of failure, allowing seamless failover between nodes. It can also improve reliability and potentially boost performance through active-active traffic distribution

### Split Components into Separate Servers
Splitting components onto separate servers improves performance, scalability, and security by allowing each service to use resources efficiently and operate independently. It also simplifies maintenance and enables specialized configurations tailored to each server’s role

