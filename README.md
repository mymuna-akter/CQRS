# Implementation of CQRS Pattern in a ASP.NET Web Application
## Introduction
CQRS means Command Query Responsibility Segregation. It is not an entire architecture. CQRS is just a small pattern. The main idea behind CQS is: “A method should either change state of an object, or return a result, but not both". In other words, asking the question should not change the answer.
Implementing CQRS in any application can maximize its performance, scalability and security.
## Problem 
 In traditional architecture, the same data model is used to query and update a database. That's simple and works well for basic CRUD operations. In more complex applications, however, this approach can become unwieldy. For example, on the read side, the application may perform many different queries, returning data transfer objects (DTOs) with different shapes. Object mapping can become complicated. On the write side, the model may implement complex validation and business logic. As a result, you can end up with an overly complex model that does too much.

 Read and write workloads are often asymmetrical, with very different performance and scale requirements.

 ## Solution
 My version in CQRS, I have used two different services for read and write, using Read service to read data, and Write service to update data. Separate database are used for Read and Write database  and  both database has kept in sync using a message broker,RabbitMQ.
 Also used two types of database in a different different way.
 
 

> Full Project Link
[Implementing CQRS in ASP.Net Core](https://github.com/mahedee/Articles/blob/master/Code/CQRS_ASPDOTNET_CORE.zip)
