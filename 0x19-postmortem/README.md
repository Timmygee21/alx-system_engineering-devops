# 0x19. Postmortem

* What is a postmortem?  
A postmortem is a tool widely used in the tech industry. After any outage, the team(s) in charge of the system will write a summary that has 2 main goals:  

- To provide the rest of the company’s employees easy access to information detailing the cause of the outage. Often outages can have a huge impact on a company, so managers and executives have to understand what happened and how it will impact their work.  
- And to ensure that the root cause(s) of the outage has been discovered and that measures are taken to make sure it will be fixed.  

![posmortem](https://twitter.com/devopsreact/status/834887829486399488)

# Being on-call
- (of a person) able to be contacted in order to provide a professional service if necessary, but not formally on duty.  

“our technicians are on call around the clock”  

synonyms: on duty, on standby, available  
 
“Dr. Merton is on call this evening”  

Users and consumers expect their favorite websites and services to be constantly accessible. Have you ever seen Facebook, Amazon, LinkedIn, Ebay down? Probably not. Any downtime means users frustration and potentially millions of dollars in loss. That’s true for the big players but also for any company where its online presence is crucial, which is the case for a lot of businesses.  

This does not happen magically. Software engineers are building reliable systems that are supposed to be up and running 100% of the time, but sometimes things go sideways and the issue needs to be fixed as soon as possible. To achieve quick resolution time, companies are putting in place monitoring systems to detect any anomaly and alert the employee who is on-call. This sometimes happens during working hours, but also at 3am or at night.  

# Setup  
* To be on call you need at least 4 components:

- A service or website you want to monitor  
- A monitoring tool  
- An oncall management system  
- A software engineer (that’s you)  

![setup](https://s3.amazonaws.com/alx-intranet.hbtn.io/uploads/medias/2020/9/35d138aa05cb69a538bd539ce2304eda50f74215.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIARDDGGGOUSBVO6H7D%2F20230605%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230605T110100Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=2108d6cc74a9021d7b32c05e168166d38bc372e92ae1975c701e5bd8e6b06b6b)

* A service or website you want to monitor  
You can monitor thousands of things:  

Is my website returning HTTP 200?  
Is my website loading in less than 500ms?  
Is my webserver daemon up?  
Is there more than 50% free disk space on my server?  

# A monitoring tool  
You need to configure one or multiple monitoring tool(s) to your on-call system, they are the ones that will actually detect any anomaly and report it to the on-call platform. Check out the Monitoring concept page for recommandations.  
