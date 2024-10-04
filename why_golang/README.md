Why golang?

1. Concurrency: Multiple users can use the application made with golang simultaneously without any interruption.
Ex: Youtube, Instagram.
two ways to achieve concurrency - multithreading and multiprocessing
In java threads are handled by kernel so they become kernel threads but in golang they are always user threads and this is achieved by go scheduler in go runtime so no context switching happens.
The kernel level threads are not only heavy in nature but they consume a lot of memory and cpu as well. So java takes much more time than golang.
2. Popular choice for cloud native applications.
3. Performance - way faster than python, java.
4. scalability - very good at scalability as k8s also scales the app very efficiently.
5. Garbage collection - Don't have to worry about garbage collection or leakage of memory.
7. Simple syntax 
8. Cross-platform compatibility - Same binary can be executed on windows, Linux, mac.
9. Easy to deploy - (self contained binary - no additional runtime is required as java runtime)

Self Contained Binaries

The Go compiler, which is a component of the Go installation, takes your source code and creates a binary executable file with all the required libraries and dependencies when you compile a Go program. The destination system does not need to have the Go installation or any other dependencies in order for this binary file to run because it is self-contained.

Because to this, it is simple to distribute and run Go applications across several platforms without worrying about the target system's Go version or any other requirements.

Better than Java ?

Golang is better than Java in few scenarios only. It is better to evaluate your use-case before choosing any option.

The advantages of using golang is well described in the above section(Why Golang?). However, Java on the other hand is a very mature programming language in its own ways.

    Java has a strong type system, which can help catch errors at compile time.

    Strong enterprise frameworks

    Large community compared to Golang.

So, it is not completely correct to say Golang is better than Java or Java is better than Golang.
Why DevOps Applications are written in Golang ?

It is a known fact that popular devops applications such as Kubernetes, Docker and many are written in Golang. But why ?

As Go was created with concurrency in mind, writing concurrent and parallel programs is made simpler. Applications for DevOps, which frequently need to handle numerous containers or processes at once, should pay special attention to this. This is one of the primary reasons why Golang is a popular choice in DevOps community.

 
