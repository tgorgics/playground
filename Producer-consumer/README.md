# Producer-consumer

This is a simple solution for the producer-consumer problem: https://en.wikipedia.org/wiki/Producer%E2%80%93consumer_problem

This solution uses BlockingQueue to prevent deadlocks, but this way the threads are not aware of each other so the weakness of this solution is that when the producer finishes producing the consumer still tries to consume in an endless loop. 

ProducerConsumer2.java contains the same solution, only difference is that is uses ExecutorService instead of raw Threads.

ProducerConsumer3.java contains the "old-school" solution, so it uses a non-blocking buffer. Therefore the wait-notify pattern is being used.
