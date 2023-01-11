# TutrIt Weekly 220110

## [Apache Tomcat: Low: Apache Tomcat JsonErrorReportValve injection (CVE-2022-45143)](https://www.rapid7.com/db/vulnerabilities/apache-tomcat-cve-2022-45143/)
Description  
The JsonErrorReportValve in Apache Tomcat 8.5.83, 9.0.40 to 9.0.68 and 10.1.0-M1 to 10.1.1 did not escape the type, 
message or description values. In some circumstances these are constructed from user provided data and it was therefore 
possible for users to supply values that invalidated or manipulated the JSON output.

Solution(s)  
apache-tomcat-upgrade-10_1_2 apache-tomcat-upgrade-8_5_84 apache-tomcat-upgrade-9_0_69  
![tag](https://img.shields.io/badge/Vulnerability-1min-blueviolet.svg?labelColor=red)

## [Kubernetes, Your Next Java App Server • Burr Sutter • GOTO 2022](https://www.youtube.com/watch?v=pwxAZWqt4I8)
n the Java ecosystem, we have historically been enamored by the concept of the “Application Server",
the runtime engine that not only gave us portable APIs (e.g. JMS, JAX-RS, JSF, EJB) but also gave us critical runtime
infrastructure for things like farm deployments, configuration, load-balancing, fail-over, distributed management and monitoring.

In this session, Burr Sutter will demonstrate how Kubernetes and OpenShift give you the critical runtime infrastructure you need for JVM-based applications.

This is whether they are Java EE, Spring, MicroProfile, Vert.x, Kotlin, etc. because in a cloud-native world,
your APIs can be whatever best fit your project’s requirements.  
[![](http://img.youtube.com/vi/pwxAZWqt4I8/0.jpg)](http://www.youtube.com/watch?v=pwxAZWqt4I8)  
![tag](https://img.shields.io/badge/video-44min-blueviolet.svg)

## [From ThreadLocal to ScopedValue Tutorial](https://www.youtube.com/watch?v=fjvGzBFmyhM)
The video explains drawbacks of using TreadLocal variables and the way it is now fixed with ScopedValue variables. You
will understand how ScopedValue are working and how it could be used.  
[![](http://img.youtube.com/vi/fjvGzBFmyhM/0.jpg)](http://www.youtube.com/watch?v=fjvGzBFmyhM)  
![tag](https://img.shields.io/badge/JDK-20-blue.svg) ![tag](https://img.shields.io/badge/video-18min-blueviolet.svg)  

## [Secure Coding Guidelines for Java SE](https://www.youtube.com/watch?v=4iEiKa1JmBU)
The video gives examples of insecure practices that may lead to security vulnerabilities and also discuss 
how to avoid them by applying the guidelines. It covers recent updates, including expanded guidance on topics such as deserialization, 
exception and error handling, and others.  
[![](http://img.youtube.com/vi/4iEiKa1JmBU/0.jpg)](http://www.youtube.com/watch?v=4iEiKa1JmBU)  
![tag](https://img.shields.io/badge/video-32min-blueviolet.svg)

## [Ktor 2.2.2 has been released](https://ktor.io/changelog/2.2/)
The Apache Maven team is pleased to announce the release of the Apache Maven 3.8.7. Release notes under the link.    
![tag](https://img.shields.io/badge/article-1min-blueviolet.svg)

## [Maven 3.8.7 has been released](https://maven.apache.org/docs/3.8.7/release-notes.html)
The Apache Maven team is pleased to announce the release of the Apache Maven 3.8.7. Release notes under the link.    
![tag](https://img.shields.io/badge/article-1min-blueviolet.svg)

## [Efficient JSON serialization with Jackson and Java](https://blogs.oracle.com/javamagazine/post/java-json-serialization-jackson)
Ben Evans is a Java Champion and Senior Principal Software Engineer at Red Hat. He has written five books on programming, 
including Optimizing Java (O'Reilly) and The Well-Grounded Java Developer (Manning).  
In the article he reveals modern serialization problems and shares best practices to work with JSON.  
![tag](https://img.shields.io/badge/article-16min-blueviolet.svg)

## [Hidden gems in Java 19, Part 1: The not-so-hidden JEPs](https://blogs.oracle.com/javamagazine/post/java-19-gems-jeps)
The article demonstrates use of the latest Java 19 updates made in the scope of [Panama](https://openjdk.org/projects/panama/), 
[Amber](https://openjdk.org/projects/amber/) and [Loom](https://wiki.openjdk.org/display/loom) projects,
as well as porting the JDK to the Linux/RISC-V instruction set:
1. Virtual threads
2. Structured concurrency
3. Record patterns
4. Pattern matching for switch
5. Foreign Function and Memory API
6. Vector API
7. Linux/RISC-V port  

![tag](https://img.shields.io/badge/article-18min-blueviolet.svg)

## [Nothing is better than the Optional type. Really. Nothing is better.](https://blogs.oracle.com/javamagazine/post/optional-class-null-pointer-drawbacks)
Best practices on using Optional class from Michael Ernst, professor of computer science and engineering at the University of Washington in Seattle, Washington.
The misunderstanding of using the real problem Optional built to solve just creates new problems, clutters code and adds leads to space, time, and coding overhead. 
The article gives an idea which is a better way for null checking and how use Optional without causing new troubles.  
![tag](https://img.shields.io/badge/JDK-8-blue.svg) ![tag](https://img.shields.io/badge/artilce-10min-blueviolet.svg)

## [Colossal Sparse Memory Segments](https://https://minborgsjavapot.blogspot.com/2023/01/java-20-colossal-sparse-memory-segments.html)
Did you know you can allocate memory segments that are larger than the physical size of your machine’s RAM and indeed larger 
than the size of your entire file system? Read this article and learn how to make use of mapped memory segments that may 
or may not be “sparse” and how to allocate 64 terabytes of sparse data on a laptop.  
![tag](https://img.shields.io/badge/JDK-20-blue.svg) ![tag](https://img.shields.io/badge/article-5min-blueviolet.svg)  

## [Time for pudding... and another Panama update](https://mail.openjdk.org/pipermail/panama-dev/2022-December/018182.html)
With [JEP 434: Foreign Function & Memory API (Second Preview)](https://openjdk.org/jeps/434) an API has been introduced which allows Java programs interoperate 
with code and data outside of the Java runtime. By efficiently invoking foreign functions (i.e., code outside the JVM), 
and by safely accessing foreign memory (i.e., memory not managed by the JVM), the API enables Java programs to call native 
libraries and process native data without the brittleness and danger of JNI.  
This work has been done in the scope of [Panama project](https://openjdk.org/projects/panama/).  
The mail will give you the latest updates on Panama project and future development direction regarding feedbacks gathered.  
![tag](https://img.shields.io/badge/JDK-20-blue.svg) ![tag](https://img.shields.io/badge/mail-5min-blueviolet.svg)  

