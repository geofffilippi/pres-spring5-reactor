## Geoff Filippi

### Senior Architect

---

# [DISH Network](www.dish.com)

* Satellite Pay TV provider
* Sling TV
* Wireless
 * Spectrum
 * Narrow Band Internet of Things (NB-IoT) Network
 * 5G

---

Formerly:

# [Oildex](www.oildex.com)

A cloud service company for oil and gas

* 2 years

---

Formerly:

# [Time Warner Cable](www.timewarnercable.com)

* 12 years

---

## Experience

* Microservices
* Domain-Driven Design
* Event-Sourced Systems
* Security

---

## Experience

<i class="fa fa-phone"></i>

* Worked on streaming media (Voice over IP), 6 years
* 5 million phone customers

---

## Experience

<i class="fa fa-video-camera"></i>

* Worked on video and streaming video, 4 years

---

## Projects

[twctv.com](twctv.com)

* HTML5 Video streaming website
* HTML5 Video streaming Set-Top Box (STB) web application

---

## Oildex Projects

* Rewrite 10+-year-old apps
* Angular 1.4/Angular 2
* Scala/Play microservices

---
---

# We will cover

* Reactive
* Project Reactor
* Spring Framework 5
* Reactive Streams

---
---

# Reactive

---

# [Reactive Manifesto](https://www.reactivemanifesto.org)

* Responsive
* Resilient
* Elastic
* Message Driven

---

## Responsive

* Respond in a timely manner

---

## Resilient

* Stay responsive, even during failure
* Replication
* Isolation
* Delegation
* Contain failures
 * Circuit Breaker

---

## Elastic

* Responsive under varying workload
* Scales resources depending on load
* Cost effective

---

## Message Driven

* Rely on asynchronous message passing
* Loosely-coupled components
* Failures are also messages
* Uses message queues
* Backpressure
* Non-blocking communication

---
---

## Reactive Concepts

* Synchronous vs. Asynchronous
* Blocking vs. Non-Blocking

---

### Synchronous

* Client makes a request and waits for server to complete
* Server starts a thread per request
* Blocks the thread that it runs on
* Lots of concurrent requests use lots of threads
* Familiar Java APIs

---

### Asynchronous

* Client makes a request and does not wait for server to complete
* Server handles all requests on the same thread
* Does not block the thread that it runs on
* Run in an event loop in a single thread
* New Java APIs

---

### Blocking vs. Non-blocking

---

#### Blocking

* Related to synchronous
* Thread execution is postponed
* Caller waits for the resource to become available

---

#### Non-blocking

* Related to asynchronous
* Thread execution is not postponed
 * Inform the caller that resource is not immediately available
 * Allows the caller to do other work
* Notify the caller when results are ready

---

### Back Pressure

* Mechanism to prevent a message producer from overwhelming a consumer
* Consumer signals producer to pause
* Should propogate through responsive systems

---
---

## Async Java Features

---

## `Future`

* Java 7
* `.get()` Blocks
* No methods to combine
* No methods to handle errors

---

## [`CompletableFuture`](https://docs.oracle.com/javase/8/docs/api/java/util/concurrent/CompletableFuture.html)

* Java 8
* `CompletionStage<T>` interface
* Equivalent to JavaScript `Promise`
* Single Value
* Part of `java.util.concurrent`

---
---

## Project Reactor

---

## Project Reactor

* Reactive Core
* Typed Sequences
* Non-Blocking IO
* Efficient Message Passing
* Async
* Based on Reactive Streams

---

### Mono

* 0 or 1 async result
* Reactive equivalent of `CompletableFuture`

---

### Flux

* Stream of results
* Reactive equivalent of `Stream`

---
---

## Spring Framework 5

* Project Reactor
* WebFlux

---

## Spring Boot 2

* Spring 5
* `spring-boot-starter-webflux`

---

## WebFlux

* Netty
* No Servlet APIs

---

## Reactive Spring Data

* Cassandra
* MongoDB
* Couchbase
* Redis

---

## Reactive Spring Data

* No JPA
* JDBC is a fully-blocking API
* Asychronous Database Access API (ADBA)
 * Proposal
* Relational Databases are bottlenecks in reactive systems

---

## Spring Boot 2

* `spring-boot-starter-data-mongo-reactive`

---
---

# Reactive Streams

---

## Reactive Streams

* Java 9
* Standard for Asynchronous Stream Processing
 * `java.util.concurrent.Flow`
* Non-blocking back pressure

---

## Reactive Streams Java Specification

 * `Publisher`
 * `Subscriber`
 * `Subscription`
 * `Processor`

---

## Reactive Streams Implementations for Java

* RxJava
* Reactor
* Akka Streams
* Ratpack
* Vert.x

---

## Reactive Streams for Java

* 1.8
 * `org/reactivestreams`
* 1.9
 * [`java.util.concurrent.Flow`](https://docs.oracle.com/javase/9/docs/api/java/util/concurrent/Flow.html)

---
---

## Demo

* [Spring Initializr](https://start.spring.io)
* [Josh Long - FluxFlix Service](https://github.com/joshlong/flux-flix-service)
 * [Application](https://github.com/joshlong/flux-flix-service/blob/master/java/ffs-service/src/main/java/com/example/FfsServiceApplication.java)

---

# Questions?

--

# References

## Spring

* [Spring Boot 2](http://www.baeldung.com/new-spring-boot-2)
* [Spring Framework 5](https://content.pivotal.io/blog/reacting-to-spring-framework-5-0)
* [Spring WebFlux](https://docs.spring.io/spring/docs/current/spring-framework-reference/web-reactive.html#spring-webflux)
* [Project Reactor](https://projectreactor.io)
* [Reactor by Example](https://www.infoq.com/articles/reactor-by-example)
* [WebFlux framework](https://docs.spring.io/spring/docs/5.0.0.BUILD-SNAPSHOT/spring-framework-reference/html/web-reactive.html)
* [Flux](https://projectreactor.io/docs/core/release/api/reactor/core/publisher/Flux.htm://projectreactor.io/docs/core/release/api/reactor/core/publisher/Flux.html)
* [Mono](https://projectreactor.io/docs/core/release/api/reactor/core/publisher/Mono.html)
* [Notes on Reactive Programming Part I: The Reactive Landscape](https://spring.io/blog/2016/06/07/notes-on-reactive-programming-part-i-the-reactive-landscape)
* [Notes on Reactive Programming Part II: Writing Some Code](https://spring.io/blog/2016/06/13/notes-on-reactive-programming-part-ii-writing-some-code)
* [Reactor 3 Reference Guide](http://projectreactor.io/docs/core/release/reference/)
* [Spring Initializr](https://start.spring.io)
* [SampleWebFluxApplication](https://github.com/spring-projects/spring-boot/blob/master/spring-boot-samples/spring-boot-sample-webflux/src/main/java/sample/webflux/SampleWebFluxApplication.java)
* [SampleConsumer](https://github.com/reactor/reactor-kafka/blob/master/reactor-kafka-samples/src/main/java/reactor/kafka/samples/SampleConsumer.java)
* [Reactor Kafka Reference Guide](https://repo.spring.io/milestone/io/projectreactor/kafka/reactor-kafka-docs/1.0.0.M1/reactor-kafka-docs-1.0.0.M1.zip!/docs/index.html)
* [Reactor by Example](https://www.infoq.com/articles/reactor-by-example/#)
* [Spring Webflux](https://docs.spring.io/spring/docs/current/spring-framework-reference/web-reactive.html#spring-webflux)
* [Reacting to Spring Framework 5.0](https://content.pivotal.io/blog/reacting-to-spring-framework-5-0)
* [What's new in Spring Boot 2](http://www.baeldung.com/new-spring-boot-2)
* [Going reactive with Spring Data](https://spring.io/blog/2016/11/28/going-reactive-with-spring-data)
* [Spring Messaging with RabbitMQ](https://spring.io/guides/gs/messaging-rabbitmq/)
* [Reactive Streams With Spring Data and MongoDB](https://dzone.com/articles/reactive-streams-with-spring-data-and-mongodb)
* [https://github.com/joshlong/flux-flix-service](https://github.com/joshlong/flux-flix-service)
* [Reactive Spring 5 and Application Design Impact](https://dzone.com/articles/reactive-spring-5-and-application-design-impact)

## Reactive

* [Reactive Streams](https://dzone.com/articles/what-are-reactive-streams-in-java)
* [Java 9 Reactive Streams](http://www.baeldung.com/java-9-reactive-streams)
* [Advanced Reactive Java](https://akarnokd.blogspot.co.uk/2016/03/operator-fusion-part-1.html)
* [Fetch first element which matches criteria](https://stackoverflow.com/questions/22940416/fetch-first-element-which-matches-criteria)
* [Reactive Streams](https://github.com/reactive-streams/reactive-streams-jvm/blob/v1.0.2/README.md)
* [The Reactive Manifesto](https://www.reactivemanifesto.org)
* [Advanced Reactive Java - Operator-fusion (Part 1)](https://akarnokd.blogspot.co.uk/2016/03/operator-fusion-part-1.html)
* [What Are Reactive Streams in Java?](https://dzone.com/articles/what-are-reactive-streams-in-java)
* [Understanding Reactive types](https://spring.io/blog/2016/04/19/understanding-reactive-types)
* [Intro To Reactor Core](http://www.baeldung.com/reactor-core)
* [What Are Reactive Streams in Java?](https://dzone.com/articles/what-are-reactive-streams-in-java)

## Integrations

* [MongoDB Reactive Streams Java Driver](https://mongodb.github.io/mongo-java-driver-reactivestreams/)
* [Project Kafka Reference Guide](http://projectreactor.io/docs/kafka/milestone/reference/docs/index.html#_kafka_streams_api)
* [Kafka 1.0 Documentation](https://kafka.apache.org/documentation/#streamsapi)
* [Reactive Kafka](https://github.com/akka/reactive-kafka)
* [RabbitMQ](https://www.rabbitmq.com/management-cli.html)
* [RabbitMQ Node Tutorial](https://github.com/rabbitmq/rabbitmq-tutorials/blob/master/javascript-nodejs/src/receive.js)
* [Reactor RabbitMQ Reference Guide](http://projectreactor.io/docs/rabbitmq/snapshot/reference/)
* [Design Principles behind Akka Streams](https://doc.akka.io/docs/akka/2.5.13/general/stream/stream-design.html)
* [Doing Reactive Programming with Spring 5](https://stackify.com/reactive-spring-5/)

---

- [X] This talk will start with an introduction to reactive programming.
- [X] We will introduce the Reactive Manifesto and 
- [X] explain Non-blocking IO. 
- [X] We will look at some of the new reactive programming features in Java like 
- [X] CompletableFuture and 
- [X] Reactive Streams. 
- [X] Project Reactor, 
- [X] Spring 5 and 
- [X] Spring Boot 2 are helping to make these new features accessible to Java developers. 
- [X] We will also introduce the concept of backpressure to control the flow of data.

- [X] You will learn how to create a Non-blocking application using Spring Boot 2. 
- [X] We will use start.spring.io to create a new Reactive application. 
- [X] Will will compare the Flux and Mono types and discuss when to use each.

