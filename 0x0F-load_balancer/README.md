# 0x0F. Load balance

![load balancer](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/275/qfdked8.png)

Ever wonder how Facebook, Linkedin, Twitter and other web giants are handling such huge amounts of traffic? They don’t have just one server, but tens of thousands of them. In order to achieve this, web traffic needs to be distributed to these servers, and that is the role of a load-balancer
![load balancer](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/9/6cefdd14b2f8c36789cba132bd5a10d42d88a177.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230429%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230429T074845Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=00f6a11889a3d509e5ee65fb9abe06fabf3dd4196a0bbb4b0f6c6e4070e4bd86)

On a high level, there are two types of load balancers, which implements different types of scheduling algorithms and routing mechanisms
- Software load balancer: Software load balancers generally implements a combination of one or more scheduling algorithms

The following are the three different basic algorithms used by load balancers. Most modern load balancers use combination of these algorithms to reach high performance and to set a trade off between various parameters
- Weighted Scheduling Algorithm
![weighted load balancer](https://static.thegeekstuff.com/wp-content/uploads/2016/01/1-weighted-scheduling-load-balancer.png)
- Round Robin Scheduling
![Round RObin Scheduling](https://static.thegeekstuff.com/wp-content/uploads/2016/01/2-round-robin-load-balancer.png)
- Least Connection First Scheduling

- Hardware load balancer: Load balancing hardwares are often referred as specialized routers or switches which are deployed in between the servers and the client. It can also be a dedicated system in between the the client and the server to balance the load

The hardware load balancers are implemented on Layer4 (Transport layer) and Layer7 (Application layer) of OSI model so prominent among these hardwares are L4-L7 routers
![load balancer](https://static.thegeekstuff.com/wp-content/uploads/2016/01/3-osi-layer-load-balancer.png)

The diagram below depicts a Layer7 load balancer
![layer 7 load balancer](https://static.thegeekstuff.com/wp-content/uploads/2016/01/4-layer7-load-balancer.png)

# When is this algorithm mostly used?
This is used when there is a considerable difference between the capabilities and specification of the servers present in the farm or cluster

This algorithm stands out to be efficient in managing the load without swarming the low capability servers the most and efficiently utilizing the available server resource at any instant of time
