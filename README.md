# Java21-feature
i decided to talk to you about the feature of JAVA 21 that is finally release on 19-sep- 2023 in this short but comperhensive gide .

i hope it will be interesting and effective for you .

with out wasting time , lets get first feature .
1. virtual treads 
The virtual threads are JVM-managed lightweight threads that will help in writing high-throughput concurrent applications (throughput means how many units of information a system can process in a given amount of time) . In Java 21, virtual threads are ready for production use.

With the introduction of virtual threads, it becomes possible to execute millions of virtual threads using only a few operating system threads. The most advantageous aspect is that there is no need to modify existing Java code. All that is required is instructing our application framework to utilize virtual threads in place of platform threads.

To create a virtual thread, using the Java APIs, we can use the Thread or Executors.


Please note that virtual threads are not faster than platform threads. They should be used to scale the number of concurrent tasks that spend much of their time waiting. For example, server applications that handle many client requests and perform blocking I/O operations. For resource/processing-intensive tasks, continue using the traditional platform threads, as virtual threads will not provide any advantage.

Also, beware that more threads mean more dependent system resources, and these resources may not scale in proportion. To prevent resource exhaustion and ensure optimal system utilization, we must run tests by limiting the number of concurrent threads using mechanisms such as Semaphore.
