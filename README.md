# FRT Project: AimCure
## Project idea: 
The user from outside India will be redirected to the us server and the user from India can access the Indian server so that there is no lag when they are accessing the website.
## Project summary
I have designed a website using Bootstrap for the purpose of helping the underprivileged section of the society. Initially the site will help with the collection of the fund. Later on, the site can be developed to track people with different ailments and help them. Store the records for future reference. The site is hosted on two different servers(US & Asia) so that there is no lag when people from outside India access the website. The client will be redirected to his/her server according to the geography. This is done so that everyone in the world can help in any manner without getting frustrated by the buffer/loading time that they experience on any site. With increasing traffic, the site will be scaled up. This is a small step but there is a scope of improvement as and when I develop my cloud knowledge. There are two different flows in the website that can be tried out. 1) Home > Learn More > "Check the server (if in US, us server will be displayed otherwise Indian)" 2) Home > Services > Donate > Donate button > Redirected to Razorpay payment gateway
## On Azure Portal
1. I have created two resource groups namely "us" and "india". You can see the resource visualizer for the same below.
### India resource visualizer

2. In both resource group, I have created two virtual machines each.
3. Then I have configured the virtual machines and added the html documents in the server.
4. After configuration, I have created two application gateway in both resource group for load balancing.
5. Then I created a traffic manager profile in the us resource group and added two endpoints pointing to the two application gateway that I created earlier.
6. Using the DNS zone service, I created zone for my domain that I got from " dot tech " and added a CNAME record pointing to traffic manager.
