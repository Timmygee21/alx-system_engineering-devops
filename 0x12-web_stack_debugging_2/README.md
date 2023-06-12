# 0x12. Web stack debugging #2  
![web](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/287/99littlebugsinthecode-holberton.jpg)  

Debugging usually takes a big chunk of a software engineer’s time. The art of debugging is tough and it takes years, even decades to master, and that is why seasoned software engineers are the best at it… experience. They have seen lots of broken code, buggy systems, weird edge cases and race conditions.  

# Test and verify your assumptions  
The idea is to ask a set of questions until you find the issue. For example, if you installed a web server and it isn’t serving a page when browsing the IP, here are some questions you can ask yourself to start debugging:  

* Is the web server started? - You can check using the service manager, also double check by checking process list.  
* On what port should it listen? - Check your web server configuration  
* Is it actually listening on this port? - netstat -lpdn - run as root or sudo so that you can see the process for each listening port  
* It is listening on the correct server IP? - netstat is also your friend here  
* Is there a firewall enabled?  
* Have you looked at logs? - usually in /var/log and tail -f is your friend  
* Can I connect to the HTTP port from the location I am browsing from? - curl is your friend  

There is a good chance that at this point you will already have found part of the issue.

- Get a quick overview of the machine state  

Debugging is pretty much about verifying assumptions, in a perfect world the software or system we are working on would be working perfectly, the server is in perfect shape and everybody is happy. But actually, it NEVER goes this way, things ALWAYS fail (it’s tremendous!).  

* Run software as another user
* Run Nginx as Nginx
