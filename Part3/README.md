# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to a repository to complete the task. Remember to also submit your answers to Blackboard

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency and paralellism is running overlapping processes. The difference is that parallelism requires the processes to run on seperate CPU's.
 
 ### Why have machines become increasingly multicore in the past decade?
 > Because other factors in computer optimisation has reached, or are close to, their theoretical limit. Adding cores is a method which is basically unaffecded by limits such as clock-speed.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > It usually improves performance. By excecuting a program out-of-order, one can significantly improve speeds in multicore systems. However, one does not need multiple CPU's.
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > They are sertainly difficult and annoying...
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Processes exist in their own adress-space (OS-managed). Threads are managed within the same adress-space as their parents (OS managed). Green threads are of the same concept as threads, but not OS managed, so probably not truly concurrent. Coroutines appear to me to be not OS managed, and direct subroutines for non-preemptive multitasking. i understand this to be a sort of non-overhead form of priority queue. 
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > From what i could gather online, they all seem to create threads. (unsertain as to whether this is unspesific)
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > GIL will make sure that only one thread is "followed" at a time, thus making pyton slower for large calculations. 
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > one might use Cyton which is a subset of python which allows you to release til GIL around spesific code.
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > it sets the maximum number of CPU's that can work simultaniously.
