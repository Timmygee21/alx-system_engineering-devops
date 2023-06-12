# 0x12. Web stack debugging #2  
![web](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/287/99littlebugsinthecode-holberton.jpg)  

Debugging usually takes a big chunk of a software engineer’s time. The art of debugging is tough and it takes years, even decades to master, and that is why seasoned software engineers are the best at it… experience. They have seen lots of broken code, buggy systems, weird edge cases and race conditions.  
![knowledge](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/9/45dffb0b1da8dc2ce47e340d7f88b05652c0f486.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230612%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230612T021824Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=fcba981ceda83acead7326b54450651551f979f8b51ad6267fba3f4657432454)  

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
* Debugging is pretty much about verifying assumptions, in a perfect world the software or system we are working on would be working perfectly, the server is in perfect shape and everybody is happy. But actually, it NEVER goes this way, things ALWAYS fail (it’s tremendous!).  
* Run software as another user
* Run Nginx as Nginx
