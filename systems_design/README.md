# [Grokking Modern System Design Interview for Engineers & Managers](https://www.educative.io/courses/grokking-modern-system-design-interview-for-engineers-managers)

## Takeaway - [Grokking Modern System Design Interview for Engineers \& Managers](#grokking-modern-system-design-interview-for-engineers--managers)
- [Grokking Modern System Design Interview for Engineers \& Managers](#grokking-modern-system-design-interview-for-engineers--managers)
  - [Takeaway - Grokking Modern System Design Interview for Engineers \& Managers](#takeaway---grokking-modern-system-design-interview-for-engineers--managers)
  - [Overview](#overview)
  - [Introduction](#introduction)
    - [**What is system design?**](#what-is-system-design)
    - [**Modern System Design Using Building Blocks**](#modern-system-design-using-building-blocks)
    - [**What will this course offer?**](#what-will-this-course-offer)
  - [Abstractions](#abstractions)
    - [**Abstractions: Why are they Important?**](#abstractions-why-are-they-important)
      - [**Database Abstractions**](#database-abstractions)
      - [**Abstractions In Distributed Systems**](#abstractions-in-distributed-systems)
    - [**Network Abstractions: Remote Procedure Calls (RPC)**](#network-abstractions-remote-procedure-calls-rpc)

## Overview

Distributed systems are the standard to deploy applications and services.  Mobile and cloud computing combined with expanded internet access make system design a core skill for the modern developer.

This course provides a bottom-up approach to design scalable systems.  First, we learn about the building blocks of modern systems, with each component being a completely scalable application itself.  You'll then explore the RESHADED framework for architecting web-scale applications by determining requirements, constraints, and assumptions before diving into a step-by-step design process.  Finally, you'll design several popular services by using these modular building blocks in unique combinations

## Introduction

### **What is system design?**

- System design is the process of defining components and their integrations, APIs, and data models to build large-scale systems that meet a specified set of functional and non-functional requirements.
- System design uses the concepts of computer networking, parallel computing, and distributed systems to build scalable, reliable, and efficient systems.
- ![Intro to system design](./images/intro-system-design.png)
- System design aims to build systems that are reliable, effective, and maintainable, among other characteristics
  - **Reliable systems** handle faults, failures, and errors
  - **Effective systems** meet all user needs and business requirements
  - **Maintainable systems** are flexible and easy to scale up or down.  The ability to add new features also comes under the umbrella of maintainability

### **Modern System Design Using Building Blocks**

We have separated out commonly-used design elements, such as **load balancers**, as the basic building blocks for high-level system design.  This serves two purposes.  First, it allows us to discuss all the building blocks in detail and discuss their interesting mini-design problems.  Second, when we tackle a design problem, we can concentrate on problem-specific aspects, mention the building block we'll use, and how we'll use it.  This helps us remove duplicate discussions of commonly-occurring design elements.
We have identified **16 building blocks** that are crucial to designing modern systems

### **What will this course offer?**

1.  **A fresh look at system design:** Many system design courses provide a formula to attack a specific problem. This might seem attractive in a high-stress situation like an interview, but it might encourage memorizing a design solution instead of actually understanding the problem and devising an appropriate solution. If system design were that formulaic, then we probably wouldn’t need people for system designing. System design is as much an art as it is a science, and attacking a design problem from the first principles gives a fresh feel to it.
2.  **Going deep and broad**: We tackle some traditional problems, but with added in-depth discussions on them. We give proper rationale for why we use some components despite their tradeoffs. For example, we explain why we use a particular **database**, a **caching system**, or a **load balancing** technique in a design.
  We address some new design problems as well that touch upon not only **scalability** but also **availability**, **maintainability**, **consistency**, and **fault-tolerance**. Collectively, traditional and new problems cover all aspects of modern system design activity. Our hope is that this course prepares learners to effectively tackle any new design problem they encounter.
  Real systems are complex and, often, we might need to make appropriate assumptions to properly scope a problem. We cover problems in more detail to properly grasp the real-world systems.
3. **Iterative process:** Systems, in reality, improve over iterations. We often start with something simple, but when bottlenecks arise in one or more of the system’s parts, a new design becomes necessary. In some design problems, we make one design, identify bottlenecks, and improve on it. Working under time constraints might not permit iterations on the design. However, we still recommend two iterations—first, where we do our best to come up with a design (that takes about 80 percent of our time), and a second iteration for improvements. Another choice is to change things as we figure out new insights. Inevitably, we discover new details as we spend more time working with a problem.
4. **Interactive learning:** We provide ample opportunities to get experience with system design. Some design problems guide learners through many steps to design a system. We also have a few examples where the learner designs the full system end-to-end without any guided steps. We reinforce the important concepts by testing learners with questions and quizzes.

## Abstractions

### **Abstractions: Why are they Important?**

**Abstraction** is the art of obfuscating details that we don't need.  It allows us to look at the bigger picture.  Looking at the bigger picture is vital because it hides the inner complexities, thus giving us a broader understanding of our set goals and staying focused on them

In the context of computer science, we all use computers for our work, but we don’t start making hardware from scratch and developing an operating system. We use that for the purpose at hand rather than digging into building the system.

The developers use a lot of libraries to develop the big systems. If they start building the libraries, they won’t finish their work. Libraries give us an easy interface to use functions and hide the inside detail of how they are implemented. A good abstraction allows us to reuse it in multiple projects with similar needs.

#### **Database Abstractions**

**Transactions** is a database abstraction that hides many problematic outcomes when concurrent users are reading, writing, or mutating the data and gives a simple interface of commit, in case of success, or abort, in case of failure.  Either way, the data moves from one consistent state to a new consistent state.  The transactions enables end users to not be bogged down by the subtle corner-cases of concurrent data mutation, but instead focus on the business logic.

#### **Abstractions In Distributed Systems**

Abstractions in distributed systems help engineers simplify their work and relieve them of the burden of dealing with the underlying complexity of the distributed systems.

The abstraction of distributed systems has grown in popularity as many big companies like Amazon AWS, Google Cloud, and Microsoft Azure provide distributed services. Every service offers different levels of agreement. The details behind implementing these distributed services are hidden from the users, thereby allowing the developers to focus on the application rather than going into the depth of the distributed systems that are often very complex.

Today’s applications can’t remain responsive/functional if they’re based on a single node because of an exponentially growing number of users. Abstractions in distributed systems help engineers shift to distributed systems quickly to scale their applications.

### **Network Abstractions: Remote Procedure Calls (RPC)**

**Remote Procedure Calls (RPCs)** provide an abstraction of a local procedure call to the developers by hiding the complexities of packing and sending function arguments to the remote server, receiving the return values, and managing any network retries