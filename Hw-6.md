
# Homework 6

### 1 – What is the difference between manual testing and automated testing ?
* Manual testing is a software testing process in which test cases are run manually without the use of an automated tool. All test cases and reports are also created manually.
* Automated testing is a method of software testing that uses specialized software tools to control the execution of tests and then compares actual test results with predicted results.
* While manual tests may not always be accurate due to the human factor, Automated testing is more reliable, as it is performed by tools and/or scripts.
* Manual testing is time-consuming because developers write everything, but automated tests are faster than manual testing.
* Manual tests are efficient if they are to run once or twice, while automated tests allow the same test plan to be executed over and over.
* While investment is required for human resources in manual testing, in atomated testing, investment is required for testing tools.
### 2 – What does Assert class ?
The assertion class of JUnit, the open source framework for writing and running unit tests in Java, contains many different helper methods that support declaring conditions in tests.So, Assert is a class that provides a set of assertion methods that useful in determining Pass or Fail status of a test case and only failed assertions are recorded.Some methods it includes are: ssertEquals, assertTrue, assertFalse, assertNotNull, assertNotSame.
### 3 - How can be tested 'private' methods ?
We shouldn’t test private methods directly, but only their effects on the public methods that call them.We shouldn't make our private methods public just for testing. This can cause other problems later on.But in some cases we can test private methods.We can test private methods indirectly by testing the package-level, protected, and public methods that call them.We can use nested test class inside our production class under test.Or we can use reflect Api that included methods that allowed client code to circumvent access protection mechanism of the Java virtual machine.
### 4 – What is Monolithic Architecture ?
Monolithic architecture is the development and presentation of all parts of the application under one roof. So all components are under one roof.The Monolithic application describes a single-tiered software application in which different components combined into a single program from a single platform.Components are business layer,database layer, model layer.
There are some disadvantages of monolithic architecture:
* All components must be developed with the same framework, the same programming language.
* Because of their interdependence, a change made for one component may affect the other component.
* For a change on a component, the entire project must be deployed and restarted.
And here are the some advantages of monolithic architecture:
* Easy to manage and develop for small teams.
* CI/CD and Test processes almost do not require DevOPS.
### 5 - What are the best practices to write a Unit Test Case ?
* *Unit Tests Should Be Maintainable and Readable:* Unit testing should be maintainable and readable. As the project changes, unit tests also need to be changed and debugged. 
* *Well Naming Convension:* The readable and clear naming of unit tests is good for code readability.
* *Trustworthy:* Unit tests need to be trustworthy.
* *Focus on Single Use-Case at A Time:* Unit tests should only focus on one situation at a time.
* *Aim for 100% Code Coverage*
* *Should Be Isolated:* Unit test needs to be completely isolated from any other unit or dependencies.
* *Unit Tests Should Be Automated:* Unit tests should be run in an automated process.
### 6 - Why does JUnit only report the first failure in a single test ?
Reporting multiple failures on a single test is often a sign that the test is doing too much compared to what a unit test should do and it is too big a unit test.While it's okay to report multiple bugs for functional,acceptance tests, if it is a unit test, then it is too big a unit test. JUnit is designed to work best with a number of small tests. It executes each test within a separate instance of the test class. It reports failure on each test.
### 7 - What are the benefits and drawbacks of Microservices ?
The benefits of Microservices are:
* Since microservices are applications that are independent of each other and focused on a single job, it is possible to develop each service with a different programming language.
* When a new developer joins the team, instead of learning the whole structure of the application, it is enough to learn the structure of the service the developer will work with, so the developer adapts in a short time.
* Each service can be changed independently of each other, easy testing and build can be done.
* Architecture does not need to be set up from scratch, as the product evolves, the architecture evolves.
And disadvantages of Microservice are as follows:
* Since the services can run on different platforms and environments, management and monitoring costs will arise.
* Multiple databases and transactions can be difficult to manage. And it can also be difficult to debug.
* Since different services that become independent from each other will use the same objects, an inevitable code duplication will occur.
### 8 - What is the role of actuator in spring boot ?
Spring Boot Actuator is a sub-project of the Spring Boot Framework. Spring Boot Actuator automatically activates production-ready features like health check, disk usage, heap dump of applications and offers a structure that allows interacting with different HTTP endpoints.We can enable or disable these endpoints provided by the spring boot actuator.There are three main features of Spring Boot Actuator:Endpoints,Metrics and Audit.
Some of important and widely used actuator endpoints are: /env,/health,/auditevents,/beans,/trace,/dump,/metrics.
### 9 - What are the challenges that one has to face while using Microservices ?
* *Data Consistency:* Some challenges arise from the distributed approach to managing data.Duplicate data can be found, which can lead to data integrity and consistency issues.The SAGA design pattern can use for this challenge.
* *Monitoring:* When an error arises in the application, finding the root cause can be challenging.Monitoring can be done using open-source tools like Amazon CloudWatch,Kubernetes,VisualVM, jProfiler, YourToolKit.
* *Testing:* Testing is much more complex in a microservices environment owing to the different services, their integration and interdependencies.This issue can be solved with unit testing by mocking microservices.
* *Security:* Since data is distributed in a microservices, maintaining the confidentiality and integrity of user data is difficult.An API Gateway can solve these challenge. 
* *Debugging issues:* Debugging a Microservice architecture is both time consuming and expensive. This architecture is also difficult to debug backwards.
* *Technical Debt:* Since we can develop microservices with different software languages and we don't have to design them in the first place, it may cause technical debts later on.
* *Data Staleness:* The database should be always updated to give recent data. The API will fetch data from the recent and updated database. 
### 10 - How independent microservices communicate with each other?
The communication protocol can be divided into two categories; synchronous communication and asynchronous communication.
RestTemplate, WebClient, FeignClient can be used for synchronous communication between two microservices.
In asynchronous Communication the client does not wait for a response, instead, it just sends the message to the message broker.An example of asynchronous communication is kafka, rabbitmq.
### 11 - What do you mean by Domain driven design ?
Domain Driven Design is an approach that helps us to solve and manage the complexity in our project and also allows us to make our project sustainable.Domain driven design has some principles like Ubiquitous Language, Bounded context,Aggreagate / Aggreagete Root, Entity object and Value object.With DDD, we can efficiently break up large projects and manage our teams successfully and thanks to this approach, we can write clean, testable code.
### 12 – What is container in Microservices ?
* A container is a technology solution to the problem of keeping software running reliably when moving software from one server environment to another server environment and containers are highly suitable for a microservices architecture, in which applications are broken into small, self-sufficient components, which can be deployed and scaled individually. 
* Containers allow applications to be more rapidly deployed, patched, or scaled.
* Containers take up very little space.
* Thanks to containers, we can update each microservice without maintenance interruption.
* Containers are also highly portable and easy to use in continuous integration (CI) and continuous delivery (CD) pipelines.
### 13 - What are the main components of Microservices architecture ?
Microservice is a collection of services that have a single responsibility, do a single job and are divided into modules that carry out the responsibilities of the job.The microservice is highly maintainable,testable,loosely coupled and independently deployable.There are 8 core components of Microsoft Architecture.These are Clients, Identity Providers,API Gateway, Messaging Formats,Databases, Static Content, Management,Service Discovery.
### 14 - How does a Microservice architecture work?
Microservice architecture is an approach that has mechanisms in a modular structure, each of which is a small service and has little dependency on other services, while developing a single application.
1. *Clients:* Clients send requests to places they want to access and receive response.
2. *Api Gateway:* The API gateway is the entry point for clients. Instead of calling services directly, clients call the API gateway.
3. *Microservices:* Each service runs on its own server. These services contain jobs for a single party.hus, there are no restrictions on technology and language.Different software languages can be used in each service.For example, the user service should only have jobs belonging to the user.T In addition, the Services may be divided into smaller services.
4. *Database of each service:* Each service has its own database.And these databases can also be divided into smaller databases.
