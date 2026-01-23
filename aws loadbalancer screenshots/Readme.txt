                                                                           AWS Load Balancer Web Server Project

## Objective  
To create multiple EC2 instances, configure them as web servers, and use an AWS Load Balancer to distribute traffic among them.

## Tools & Services Used  
- Amazon EC2  
- Application Load Balancer  
- Target Group  
- Apache Web Server  
- AWS Management Console  

## Architecture  
User → Load Balancer → Target Group → 3 EC2 Web Servers

## Project Description  
Three EC2 instances were launched in AWS. Apache web server was installed on all instances.

- Instance 1 displays the default Apache web page.  
- Instance 2 displays a custom page f1.html file with the message “This is Server 2” 
- Instance 3 displays a custom page f2.html file with the message “This is Server 3”.

All three instances were added to a target group. An Application Load Balancer was created and linked to this target group.

When the load balancer DNS name is accessed in a browser and refreshed multiple times, different server pages appear, proving that traffic is distributed among the servers.

## Steps Followed  

1. Created three EC2 instances.  
2. Installed Apache web server on all instances.  
3. Modified the default web page on Instance 2 and Instance 3.  
4. Created a target group and registered all three instances.  
5. Created an Application Load Balancer.  
6. Attached the target group to the load balancer.  
7. Accessed the load balancer DNS name in a browser.  

## Output Screenshots  

Screenshots included in the screenshots folder:
- Running EC2 instances  
- Target group health status  
- Load balancer details  
- Browser output showing different server pages  

## Result  
The load balancer successfully distributed incoming requests among the three EC2 web servers. Different pages were displayed on refresh, proving proper load balancing and high availability.

## Conclusion  
This project demonstrates how multiple servers can be combined using a load balancer to improve availability, reliability, and performance of a web application.
