Write your answers to a Markdown file, and add it to the same git project.

• Q1: Define what is a Microservices architecture and how does it differ from a Monolithic application.
I can define microservice architecture as a architecture style in which the application is splitted in the small independent services. This services should follow the next criteria: 
- microservices should be functionally complete, which means they should implement all requested feature and only them
- microservices should be resilient by meaning that if one microservice fails, other microservices should not be impacted(graceful degradation)
- microservices should be easily scale up or dowm independently
- microservices communicate between each other using interfaces 
- microservices should also be able to be deployed independently
The key difference between Monolithic and Microservice architecture is that monolithic application runs as a single entity where each component of the application is coupled and highly depends on another one, while in microservices the main criteria is decoupling. 

• Q2: Compare Microservices and Monolithic architectures by listing their respective pros and cons.
Monolithic pros + : 
- simple development 
- easy testing 
- easy deployment 
Monolothic cons - :
- not flexible, which means that it is hard to adapt new technology
- becomes hard to manage for complex applications (even difficult to understand)
- difficult to scale, the whole system needs to be redeployed
- even one bug can affect whole system

Microservices pros +
- graceful degradation 
- deployed independently 
- easy to manage by different teams
- agile development
- stop cascading failtures
Microservices cons - : 
- higher chance of failing(because of network connection)
- eventual consistency 
- operational complexity


• Q3: In a Micoservices architecture, explain how should the application be split and why.
In a Microservices architecture, an application is divided into small, independently services, each aligned with specific business capabilities.
Services are granular, owning their unique business logic and data models, which ensures that they can be developed, deployed, and scaled independently. Each service typically has its own database to maintain loose coupling and avoid inter-service dependencies. Communication between services is often handled asynchronously, using lightweight mechanisms to enhance performance and resilience. This approach is important in modern technology world because it promotes scalability and enables continuous delivery and deployment, which refers to agile practices.


• Q4: Briefly explain the CAP theorem and its relevance to distributed systems and Microservices.
The CAP theorem stands for the fact that in computer architecture any distrubuted system can provide only two of three CAP guarantees(consistency, availability, partition tolerance). 

• Q5: What consequences on the architecture ?
The main consequence of the microservice architecture is for sure it's complexity and sometimes hard management due to the distributed system. It can introduce challenges in maintaining data consistency and transaction management across services. However, the main pros is the independence. The microservice architecture enhances scalability and resilience, as services can be scaled independently, and failures in one service have minimal impact on others. 


• Q6: Provide an example of how microservices can enhance scalability in
a cloud environment.
The example we talk about on the class is the usage of cloud space by Amazon on the Christmas time. The usage of containers allows to get a scalable amount of storage in the cloud and get resources that are on demand(resources are elastic).

• Q7: What is statelessness and why is it important in microservices archi-
tecture ?
In the Microservice architecture the stateless means that microservices do not maintain any previous interactions or store user session data. That means that the microservice receives the request, operates on it and then sends back the respond, without saving any state information. With using stateless any service instance can handle any request. It is important because it is a key feature for adapting resilience, scability and load balancing in the microservice architecture.

• Q8: What purposes does an API Gateway serve ?
An API Gateway in a microservices architecture acts as a single entry point for all client requests, directing them to the appropriate microservices. The main purpose of it is that it simplifies client interactions by providing a centralized handling of API communication between client and service. The gateway also handles concerns such as authorization, authentication,rate limiting and enhancing security. Additionally, the API Gateway can handle load balancing, ensuring even distribution of incoming requests to maintain optimal service performance.