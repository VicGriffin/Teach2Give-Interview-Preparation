# Summary on system design primer blog
•	System design is a step by step process of defining a particular software’s architecture, modules, components etc. 

**Need for System Design**

1. **Understanding Requirements**: The first step in software development involves gathering both functional and non-functional requirements from business owners. Non-functional requirements include aspects like scalability, high availability, and consistency.

2. **Architectural Planning**: Based on these requirements, system design helps in deciding the architecture of the application. This includes choosing between SQL or NoSQL databases depending on data storage needs and planning for scalability to handle increased traffic.

3. **Efficiency and Performance**: Proper system design ensures that applications are efficient and can handle user demands. For instance, companies like Google and Facebook use multiple servers worldwide to deliver resources from the nearest server to users, enhancing application performance.

## Essential Design Methods in System Design
 **Architectural Design:** Describes the infrastructure, model, view, components, and interaction.  
**ERD Diagram:** The entity-relationship diagram(ERD) is mainly used in designing the application's database structure.one can define multiple database schemas, add entities in each schema, and add multiple attributes for each entity.  
**UML Diagram:** The unified modeling language(UML) is used to prepare modeling software systems. It contains different diagrams like activity diagrams, class diagrams, sequence diagrams.  
**Class Diagrams:** The class diagrams are used to represent the classes which contain the class's attributes, methods, and relationships between multiple classes.  
**Sequence Diagrams:** It represents the interaction between the various components of the system and is used to model the behavior of the system.
## System design concepts
1.	Performance and scalability of the application 
1.	Latency and throughput greatly affect the efficiency of the system
1.	Consistency patterns and availability patterns while designing the system architecture

## Concepts in system design

**Content delivery network(CDN):**This is a server network used to deliver different contents like images and various data. It delivers the resource faster, decreases latency and improves the applications performance.  
**Domain Name System(DNS):** This allows users to access the website and its resources through the domain name, mapping the unique domain name with an ip address.  
**Caching:** This is a mechanism to serve resources faster which works between the web application and the source of the data.  
**Proxies (proxy server):** They are used for caching. Works between the client of the application and the internet where when the client request for resources from the internet, the application requests the proxy server and the proxy server gets the resources and sends them back to the application.

## Components of system design
1.	**Micro services and services discovery** – This enables service to works independently and accomplish specific tasks because the micro services break down complex application into smaller services.
1.	**Database systems (RDBMS & NoSQL)** 
    -   RDBMS(Relational database management system) – used when one needs to store structured data for the software or application. 
        -	Different characteristics are:-
	stores the data in the table format
1.	communication protocols – these are the rules used in communicating or exchange between two systems. This includes 
    -	HTTP/HTTPS (hypertext transfer protocol): HTTPS is a secure version of HTTP. They are used in web-based communication
    -   TCP/IP (transmission control protocol): The TCP protocol is used to communicate over the internet.
    -   UDP (user datagram protocol): It is mainly used for live streaming, video calls, etc., in which data loss can be tolerable.
    -   WebSockets: The web sockets are used for bi-directional duplex communication. It builds the connection between two web applications.

### How to approach System Design Interview step by step guide
1.	**Requirement clarification** – know the function and non-function requirement.
1.	**Estimation of resources** – decide on the resources you should use to build the application
1.	**System interface definition** – this step involves designing the system interface.
1.	**Defining data model** – this step involves selecting a database for the application.
1.	**High-level design** – this step involves deciding on how you will connect the components of the systems with each other.
1.	**Detailed design** - After creating the basic design of the application, you need to improve the system design. This is achieved by analyzing the system to fulfill the non-functional requirements.  
    - How to use caching to improve the performance of the application?
    - How do we scale the application via load balancing?
    - Should you use the CDN for caching, or are cookies enough?
    - How would you handle the failure of the application?
    - Should you distribute the data across multiple databases?
    - How will you replicate the database?
1.	Identifying and solving bottlenecks – the step involves identifying the bottlenecks in your system design and confer solutions to resolve with the interviewer.
### Sample sytem design interview question and solutions
1. How would you design a URL Shortening service similar to TinyURL?  
The URL shortening service allows users to shorten the long URLs. So users can use the short URL instead of the long URL, and the fun fact is that the short URL works the same as the long URL.
**Requirements clarification:**  

    •	When you give a long URL as an input, it should return the shortened URL.  
    •	When you click the shortened URL, it should redirect to the original URL.  
    •	Consider 500 requests per second, and make scalable accordingly.  
    •	Delete the expired URLs.  
    •	Track the number of clicks on the URL.  
**Approach:**  

You can discuss the below stuff.  
•	How you will use the REST API to communicate with the server.  
•	How will you handle the 500 requests every second via load balancing?  
•	You can discuss using the relational database, as it doesn’t require horizontal scaling.  
•	You can discuss how you will prepare a table for relational database to map long URLs with short URLs.  
•	The critical point is how to shorten the long URL by providing a unique id to each shortened URL.  

1.**How would you design a Web Crawler?**  
The Web crawlers allow to extract the information from different web pages.  
**Approach:**  
You can discuss how you open multiple web pages in the web browser. Also, it is important to know how many browser windows you will open simultaneously to crawl multiple web pages. Let’s say if you allow us to open 1000 browser windows together, the device may run out of memory.
You can also discuss changing the web pages and domains dynamically.  
1. **How would you design Facebook and Instagram?**  
Here, you are required to build a social media application.  
**Requirements:**  
    •	User signup/sign-in  
    •	Allowing users to publish posts and short videos  
    •	Followers and following features  
    •	Direct messaging  
    •	Showing the latest posts from their followers       
    •	Showing trending posts in the feed  
**Approach:**  
•	Talk about how you will handle the relationship between users in the database.  
•	Talk about how you will implement the chat features. You may talk about integrating third-party chatting applications.  
•	Furthermore, you can discuss how you will implement the authentication.  
•	Discuss algorithms to show trending or latest posts.  
•	Talk about handling user’s data in the database, as users will publish multiple posts.  
•	Discuss database replication to handle failures.  
•	Discuss data caching and load balancing.  
1. **How would you design the API rate limit?**  
The API rate limiter allows one to make a particular number of API requests in a specified time. If the API request increases, it blocks the request for some time.  
**Approach:**  
•	Talk about rate-limit matrics. How many maximum requests do you want to allow per second?  
•	Talk about how you will handle multiple requests simultaneously.  
•	Talk about how you can keep count of requests. You may use the IP address received in the request header.  

### Resources for further learning
Refer the following – 
1.	[The system design interview roadmap](https://www.designgurus.io/path/system-design-interview-playbook)
2.	[System Design Interview Survival Guide (2024): Preparation Strategies and Practical Tips](https://levelup.gitconnected.com/system-design-interview-survival-guide-2023-preparation-strategies-and-practical-tips-ba9314e6b9e3)
3.	[The Complete Guide to Ace the System Design Interview](https://www.designgurus.io/blog/complete-guide-sys-design)
4.	[Ace Your System Design Interview with 7 Must-Read Papers in 2024](https://www.designgurus.io/blog/sys-design-papers) 
