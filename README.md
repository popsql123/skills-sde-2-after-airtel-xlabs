# skills-sde-2-after-airtel-xlabs
i will add a revision summary of skills i have had till my airtel journey updating at the time of switch period for future reference 


# tech stack / Skills

## 0. DSA

 * **0.1 ArrayList, HashMap, HashSet, PriorityQueue, Stack, Queue -> LinkedList / ArrayDeque**
 * **0.2 Comparator and comparable interface**
 * **0.3 DSA Patterns templates**
 * **0.4 Important libraries**
   * Arrays, Collections -> to fill, sort, reverse, binarySearch
   * String and StringBuilder ->
        * String remains as it is -> single string fetching, searching a char, searching a pattern
        * String is divided -> convert to character array, split, subArray a string
        * String is transformed -> toUpperCase(), toLowerCase()
        * two strings compared -> equals(), equalsIgnoreCase(), .compare() -> chronological comparision
        * StringBuilder
             * reverse an array -> sb.reverse().toString()
             * add string to back -> append()
*  **0.5 Dsa notes notebooks DSA sheet from TakeUForward**

## 1. Java

* **1.1 Core java**

* **1.2 oops with java**

* **1.3 java collections framework**

  * 1.3.1 Iterable classes 
  * 1.3.2 Map classes
  * 1.3.3 java concurrent collections

* **1.4 java executor framework / multi-threading in java**

  * **1.4.1 runnable interface and thread class**

    * 1.4.1.1 Object.wait(), Object.notify(), Object.notifyAll()
    * 1.4.1.2 Thread.sleep(5000)
    * 1.4.1.3 run() method by runnable class
    * 1.4.1.4 Thread.currentThread.getName()

  * **1.4.2 callable interface**

    * 1.4.2.1 call() method by callable interface used for returning something after execution

  * 1.4.3 FutureTask as adapter between Thread and callable - get()

  * 1.4.4 CountDownLatch - countDown(), await()

  * 1.4.5 CircularBarrier - await()

  * 1.4.6 synchronized method and block

  * **1.4.7 synchronisation without locking**

    * 1.4.7.1 volatile
    * 1.4.7.2 immutable objects using final on class and fields
    * 1.4.7.3 AtomicBoolean, AtomicReference<Employee> for CAS operation access

  * 1.4.8 lock - Reenterant lock - to lock critical section for one thread ata a time access

* **1.5 java important utility libraries**

  * 1.5.1 Collections
  * 1.5.2 Arrays
  * 1.5.3 Math
  * 1.5.4 Objects - null checks to avoid null pointer
  * 1.5.5 Optional - avoid if else for null check

* 1.6 Exception handling

* 1.7 Generics

* 1.8 String, StringBuilder and StringBuffer

* 1.9 Streams api

* 1.10 lambda expressions

* 1.11 features in important versions of java - 8, 11, 17, 21, 25

---

## 2. Spring Webflux -> used for reactive programming paradigm in java

* 2.1 what is reactive programming?

* 2.2 what is event loop?

* 2.3 what is back pressure?

* 2.4 how does webflux provide backpressure support?

* **2.5 Four interfaces in webflux**

  * **2.5.1**

    ```java
    public interface Publisher<T> {
        void subscribe(Subscriber<? super T> s);
    }
    ```

  * **2.5.2**

    ```java
    public interface Subscriber<T> {
        void onSubscribe(Subscription s);
        void onNext(T t);
        void onError(Throwable t);
        void onComplete();
    }
    ```

  * **2.5.3**

    ```java
    public interface Subscription {
        void request(long n);
        void cancel();
    }
    ```

  * **2.5.4**

    ```java
    public interface Processor<T,R>
            extends Subscriber<T>, Publisher<R> {
    }
    ```

* **2.6 special publishers**

  * 2.6.1 Mono : can produce 0/1 results
  * 2.6.2 Flux : can produce 0...n results

* **2.7 some methods i remember**

  * 2.7.0 Mono.empty() / Flux.empty()  -> just like Optional.empty()
  * 2.7.1 just() -> Mono.just(1)
  * 2.7.2 flatmap() -> async and starts another thread consumes coming results and produce new result
  * 2.7.3 flatmapMany() -> mono to flux, this is also async and simplar to flatmap
  * 2.7.4 map() -> decorates/transforms comping result synchronously and returns the same but decorated or transformed result
  * 2.7.5 mono1.zipWith(mono2) zips two or three mono or flux to make tuple2<<>, <>> or triplet2<<>, <>, <>>

    * static method Mono.zip(mono1, mono2) can also be used



## 3. Springboot

## 4. Apache Kafka

## 5. keycloak

## 6. ElasticSearch

## 7. Redhat OCP(Openshift Container platform) / amazon AWS

## 8. Aerospike

## 9. MongoDB

## 10. Sql


# System Design

## 1. LLD

## 2. HLD

--------------------
----
----
----
----
----

# 🚀 SDE-2 Skills Inventory (Post Airtel XLabs)

Revision summary of skills acquired during my Airtel journey.
Maintained as a **switch-prep checklist + revision sheet**.

---

# 📚 Table of Contents

* [DSA](#-dsa)
* [Java](#-java)
* [Spring WebFlux](#-spring-webflux)
* [Spring Boot](#-spring-boot)
* [Kafka](#-apache-kafka)
* [Security](#-keycloak)
* [Datastores](#-datastores)
* [Cloud / Platform](#-cloud--platform)
* [System Design](#-system-design)

---

# 🧠 DSA

* Arrays
* Strings
* Sliding Window
* Two Pointer
* Stack / Queue
* Trees
* Graphs
* Heap
* Recursion / Backtracking
* Dynamic Programming

---

# ☕ Java

## Core

* Core Java
* OOPS with Java
* Exception Handling
* Generics
* Streams API
* Lambda Expressions
* Java 8 features
* Java 21 features

---

## Java Collections Framework

* Iterator implementations
* HashMap
* Concurrent Collections

---

## Multithreading / Executor Framework

### Runnable & Thread

* Object.wait()
* Object.notify()
* Object.notifyAll()
* Thread.sleep()
* run() method
* Thread.currentThread().getName()

### Callable

* call() method (returns value)

### FutureTask

* Adapter between Thread & Callable
* get()

### Synchronization Utilities

* CountDownLatch → countDown(), await()
* CyclicBarrier → await()

### Synchronization

* synchronized method
* synchronized block

### Lock-free Synchronization

* volatile
* immutable objects (final)
* AtomicBoolean
* AtomicReference
* CAS operations

### Locks

* ReentrantLock
* Critical section locking

---

## Utility Libraries

* Collections
* Arrays
* Math
* Objects (null safety)
* Optional

---

## Strings

* String
* StringBuilder
* StringBuffer

---

# ⚡ Spring WebFlux (Reactive Programming)

## Concepts

* Reactive Programming
* Event Loop
* Backpressure
* Non-blocking IO
* Async processing

---

## Reactive Streams Interfaces

### Publisher

```java
public interface Publisher<T> {
    void subscribe(Subscriber<? super T> s);
}
```

### Subscriber

```java
public interface Subscriber<T> {
    void onSubscribe(Subscription s);
    void onNext(T t);
    void onError(Throwable t);
    void onComplete();
}
```

### Subscription

```java
public interface Subscription {
    void request(long n);
    void cancel();
}
```

### Processor

```java
public interface Processor<T,R>
        extends Subscriber<T>, Publisher<R> {
}
```

---

## Special Publishers

* Mono → 0..1 result
* Flux → 0..N result

---

## Common Operators

### Creation

* Mono.empty()
* Flux.empty()
* Mono.just()
* Flux.just()

### Transform

* map() → synchronous transform
* flatMap() → async transform
* flatMapMany() → Mono → Flux

### Combining

* zipWith()
* Mono.zip()
* Flux.zip()

---

# 🌱 Spring Boot

* REST APIs
* Auto configuration
* Dependency injection
* Profiles
* Configuration properties
* Actuator

---

# 📨 Apache Kafka

* Producer
* Consumer
* Consumer Groups
* Offsets
* Partitions
* Kafka Streams
* Retry / DLQ

---

# 🔐 Keycloak

* OAuth2
* OpenID Connect
* JWT
* Role based access
* Client credentials
* Token validation

---

# 🗄 Datastores

## NoSQL

* MongoDB
* Aerospike
* ElasticSearch

## SQL

* Joins
* Indexes
* Query optimization
* Transactions

---

# ☁️ Cloud / Platform

* AWS
* RedHat OpenShift (OCP)
* Containers
* Deployment configs
* Scaling

---

# 🏗 System Design

## LLD

* SOLID principles
* Design patterns
* Interface driven design
* Thread safe design

## HLD

* Microservices
* Event driven architecture
* Caching
* Load balancing
* Circuit breaker
* API Gateway
* Distributed systems

---

# 🎯 Target Role

**Backend Engineer / SDE-2 / SDE-3**
Java • Spring • WebFlux • Distributed Systems • High Scale


