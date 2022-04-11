## The What and the Why: Containers

*A container is a standard unit of software that packages up code and all its dependencies and enables applications to run quickly and reliably from one computing environment to another*. Over the years, containerization has become an industry standard. But what value do they provide? Why do we need them? **Let's talk**. 

## Why do we need containers?
**1. Recreating runtime environments:** 

![dev_env_1.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1630135994331/XDL_stIvE.jpeg)
Imagine that a team of developers is working on a large project. It may comprise of many applications running together to form a single application. If a new developer joins the team, **the whole development environment needs to be recreated** on their system to get things working. It consumes a lot of time and energy and is inefficient.

**2. Dependency Conflicts:** 

![dependency_conflict.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1630136101035/ItcoUPFaD.jpeg)
Imagine two java applications running on the same server. Both applications are running Java version 8. Upgrading one application to Java version 11 **may introduce breaking changes to the other application** as some features may not be compatible with version 11. The two applications can no longer run on the same server. Introducing this change has created a dependency conflict.

**3. Scaling Up: **

![scaling_1.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1630136153389/El_WxSY_Y.jpeg)
When traffic increases, **applications scale up by creating replicas**. Runtime environments need to be set up on these new servers before the application can run. Recreating the entire runtime environment for each application with all its dependencies consumes a lot of resources.

**4. Fault Isolation: **

Failure of one application may bring down the server. Even the applications that are running without any errors. Since applications share the environment, a fault in any part may lead to a complete failure.

## How containers work?

Now that we've seen why we need containers, let's learn about how they work.

![container_1.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1630136365997/Qrmj9Pd3_.jpeg)

As evident from the name, one can think of a container as a "box" that contains an application and everything it needs to carry out its operations. Each application inside the "box" is capable of performing all of its functions on its own. The contents of the "box" are not affected by any changes made outside it. Similarly, any changes made to the contents of the "box" don't affect anything outside the "box".

*Containers encapsulate an application as a single executable package of software that bundles application code with all of the related configuration files, libraries, and dependencies required by it.*


![docker.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1630136447442/IKk3VOkVe.png)

**Containerized applications are isolated and do not need a copy of an operating system.** Instead, **a container runtime engine (like Docker)** runs on the host system which allows the containers to **share the operating system.** The ability to share an operating system makes containers a more efficient alternative to using virtual machines which can also be used to create isolated environments. Sharing an operating system allows running multiple containers on the same hardware.

## What are the advantages of using containers?

We talked about the need for containers previously. Now let's see how containers are a solution to those problems.

**1. Recreating runtime environments:**

Containers contain everything an application needs to run, including the runtime environment. So simply installing a container runtime engine and running the container on the new machine is all that's needed now.

**2. Solve dependency conflicts:** 


![dependency_conflict_2.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1630137570206/1qVfWpsDr.jpeg)

Containers provide isolated an environment for applications to run. **So any changes made outside that environment do not affect the application.** The java 8 application can run on a java 8 runtime in its container and the java 11 application can run on a java 11 runtime without affecting each other.

**3. Scaling up: **


![scaling_2.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1630136981188/HzBm6nxOc.jpeg)

Scaling up is now as simple as **running another instance of the same container.** Traffic can then be distributed among these containers using a load balancer.

**4. Fault isolation: **

Failure of an application is **limited only to its container** and will have no effect outside that container. This way we can identify where the fault lies and take remedial action.

**5. Speed: **

Containers are "lightweight" since they only contain what's needed for the containerized application to run and share the host machine's operating system. It's not only efficient in terms of resource consumption but is also **very fast as there is no need to boot up an operating system, unlike in virtualization.**

**6. Portability: **

Containers create an executable package of software that can run on any machine as long as it runs a container runtime, making the application portable.

The popularity of containerization has led to the emergence of a few container runtime engines. Some of the popular ones are :

-  [Docker](https://www.docker.com/) 
-  [containerd](https://containerd.io/) 
-  [CRI-O](https://cri-o.io/) 

That brings us to the end of this blog. I tried my best to include all the things that I found helpful when learning about containerization myself. If it helped please leave a Like. Any feedback is more than welcome.

Image Credits: 

- Cover image: Photo by <a href="https://unsplash.com/@carrier_lost?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Ian Taylor</a> on <a href="https://unsplash.com/s/photos/containers?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>

- Docker: Docker

  



