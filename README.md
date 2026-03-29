# skills-sde-2-after-airtel-xlabs
i will add a revision summary of skills i have had till my airtel journey updating at the time of switch period for future reference 

tech stack :
0. DSA

1. Java
    1.1 Core java
    1.2 oops with java
    1.3 java collections framework
        1.3.1 iterator implementations
        1.3.2 hashmap
        1.3.3 java concurrent collections
    1.4 java executor framework / multi-threading in java
        1.4.1 runnable interface and thread class
            1.4.1.1 Object.wait(), Object.notify(), Object.notifyAll()
            1.4.1.2 Thread.sleep(5000)
            1.4.1.3 run() method by runnable class
            1.4.1.4 Thread.currentThread.getName()
        1.4.2 callable interface
            1.4.2.1 call() method by callable interface used for returning something after execution
        1.4.3 FutureTask as adapter between Thread and callable - get()
        1.4.4 CountDownLatch - countDown(), await()
        1.4.5 CircularBarrier - await()
        1.4.6 synchronized method and block
        1.4.7 synchronisation without locking
            1.4.7.1 volatile
            1.4.7.2 immutable objects using final on class and fields
            1.4.7.3 AtomicBoolean, AtomicReference<Employee> for CAS operation access
        1.4.8 lock - Reenterant lock - to lock critical section for one thread ata a time access
    1.5 java important utility libraries
        1.5.1 Collections
        1.5.2 Arrays
        1.5.3 Math
        1.5.4 Objects - null checks to avoid null pointer
        1.5.5 Optional - avoid if else for null check
    1.6 Exception handling 
    1.7 Generics 
    1.8 String, StringBuilder and StringBuffer
    1.9 Streams api
    1.10 lambda expressions
    1.11 features in important versions of java - 8, 21


2. Spring Webflux -> used for reactive programming paradigm in java
    2.1 what is reactive programming?
    2.2 what is event loop?
    2.3 what is back pressure?
    2.4 how does webflux provide backpressure support?
    2.5 Four interfaces in webflux
        2.5.1 public interface Publisher<T> {
                void subscribe(Subscriber<? super T> s);
            }   
        2.5.2 public interface Subscriber<T> {
                void onSubscribe(Subscription s);
                void onNext(T t);
                void onError(Throwable t);
             void onComplete();
            }
        2.5.3 public interface Subscription {
                void request(long n);
                void cancel();
            }
        2.5.4 public interface Processor<T,R>
                extends Subscriber<T>, Publisher<R> {
            }
    2.6 special publishers
        2.6.1 Mono : can produce 0/1 results 
        2.6.2 Flux : can produce 0...n results
    2.7 some methods i remember
        2.7.0 Mono.empty() / Flux.empty()  -> just like Optional.empty()
        2.7.1 just() -> Mono.just(1)
        2.7.2 flatmap() -> async and starts another thread consumes coming results and produce new result
        2.7.3 flatmapMany() -> mono to flux, this is also async and simplar to flatmap
        2.7.4 map() -> decorates/transforms comping result synchronously and returns the same but decorated or transformed result
        2.7.5 mono1.zipWith(mono2) zips two or three mono or flux to make tuple2<<>, <>> or triplet2<<>, <>, <>>
              -> static method Mono.zip(mono1, mono2) can also be used

3. Springboot

4. Apache Kafka

5. keycloak

6. ElasticSearch

7. Redhat OCP(Openshift Container platform) / amazon AWS

8. Aerospike

9. MongoDB

10. Sql




System Design

1. LLD

2. HLD