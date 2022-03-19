# What is a server?

A server is a computer connected to the internet with an application expecting to receive data from other computers and return something to them.

## Common keywords

* Client: the end-user computer 
* DNS: Domain Name Service
* NAT: Network address translation
* AWS: Amazon Web Services, the Amazon cloud service 
* AWS S3: An AWS storage plan
* Azure: Microsoft cloud service
* Blob: A type of flexible cloud storage  plz
* Latency: The time that the information takes to go back and forth
* Handshake: the exchange of basic information between the computer at each end, like a first time greeting
* DRM: Digital rights management
* DevOps: A occupation in with the person does development and IT operations at the same time
* Cloud computing: Using someone else computer to do server work

## What does a server do?

A server's main job is to handle the output from multiple machines. As it is a form of centralization of data management, something that optimizes workflows and lessens the burden on the player machines and creates the possibility for the machine to dedicate more resources to the game, or even lowering the requirements for the title, is the main inspiration for cloud gaming services.

## Servers in today's context
As maintaining a physical server include costs in the electrical bill, planned obsolescence, hardware degradation, and maintenance costs in general, the vast majority of the companies decided to use someone else computers to do the work, as such, cloud computing was born.

### What exactly is cloud computing?
Cloud computing is a way to borrow someone else computer with a fancy name and business plan involved. 
This category of server displays many advantages over traditional on-premises hosting, with the main benefit of the cloud being the scalability of the solution, with the possibility to reduce and expand the number of servers, or even the resources allocated to them.

#### Wow, the cloud looks like a great idea! What can go wrong? 
Every part in the pipeline can go wrong, from the server development to the end-user experience, when the server is not on the premise, the developers dos not have 100% control of the computer, some cloud plans offer a set of functionality or an entire virtual machine, with it being possible to occur problems in the integration between services, virtual machine set-up process, or even the communication between the cloud servers and the on-premise servers that the company can keep to maintain control over due to special circumstances.

#### On-premises does not seem like a bad idea
On-premises servers have downsides and advantages like cloud, and the easiest drawback to notice is the lack of dynamic allocation of resources that can cause the service to slow down and hinder the end-user experience. The resource allocation problem is the easiest to occur, happening when an unexpected number of requests occurs without planning, with the result being the server increasing the response time or even going down. 
An example of this type of issue is when MMOs launches and the servers stay down during the launch week.

## Testing servers

To test servers, it is necessary to understand the context of the server in the target application, and why it was used. 

### Use cases for servers in games

The majority of games use servers as a means to facilitate multiplayer features, and in some cases, even to prevent damages to the product and increase ways to generate revenue.
* Matchmaking server for competitive games
* Authentification for Digital Rights Management(DRM) reasons
* Crossplay
* Synchronization of progress between platforms
* Microtransactions and premium currencies
* Ways of offering transactions outside a closed ecosystem, like the Apple Vs Fortnite legal dispute

### Server related issue in games
Every application will have issues, and as such, every game that depends on a server to do anything will face problems, at some point, with the most common ones being listed below:
* Data disparity
* Requests time out
* Strong interpolation 
* Rollbacks

### How to force server issues
As we know the common types of server issues, it is possible to force them by using only the application the client provided, with the most common method being the stress test.

#### Stress test
The stress test is usually done by letting the player base test the game in a Closed Beta Test(CBT) to ensure that the servers can support a large number of players, but it can be done by testers using the application and exploiting actions that send a large number of data packages to the game servers

#### Data disparity
In this instance, the test can occur when the servers do not respond well to the incoming data, like during a maintenance or an instability, with the requests not being processed well and the data that the player can access, differing from the server-side, with the most common one being currency not updating for the player but it being deducted in the server when a purchase happens.

#### Strong interpolation
This issue does not need to be tested isolated or forced to occur, it is a fruit of server-side problems or even network ones, the tester needs to only pay attention to see if the data sent goes back in an approximated form, and if the approximation occurred in a way that hinders the player experience.

#### Rollbacks
Like the Interpolation, it is better to observe when the issue occurs naturally or when the servers are under special circumstances like stress or problems. When the problems happen, the data that the application sent to the server, does not affect the server-side, making the changes revert to before the actions like it never happened, it is the best outcome possible for a data disparity, but still a problem on its own.
