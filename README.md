#中文:
这是一个Java线程池的demo代码, 主要是用来展示和验证Java线程池 ThreadPoolExecutor中 RejectedExecutionHandler拒绝一个新提交的任务所需要的前提条件(如下两个条件满足一个即可成立):

1. 当线程池已处于关闭状态(SHUTDOWN)
2. 当线程池中所有线程都处于运行状态, 并且线程池内的阻塞队列也满了.


#English:
This is a Java thread-pool-related demo, mainly to demonstrate under what condition the RejectedExecutionHandler in a ThreadPoolExecutor will reject the newly-added tasks. According to JDK, either of the two conditions below will cause the rejection to happen:

1. When the thread pool has already been in SHUTDOWN state. 
2. when the Executor uses finite bounds for both maximum threads and work queue capacity, and is saturated.
