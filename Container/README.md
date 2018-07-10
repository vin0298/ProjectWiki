# Container
From Docker's explanation, [original web](https://www.docker.com/what-container#/virtual_machines)

A container image is a lightweight, stand-alone, executable package of a piece of software that includes everything needed to run it: code, runtime, system tools, system libraries, settings. Available for both Linux and Windows based apps, containerized software will always run the same, regardless of the environment. Containers isolate software from its surroundings, for example differences between development and staging environments and help reduce conflicts between teams running different software on the same infrastructure.
## Container is basically like a virtual machine. Instead of virtualizing the hardware, it virtualizes the operating system


![Compare](comparison.png)

Even simpler Container explaination ([YouTube](https://www.youtube.com/watch?v=IEGPzmxyIpo))<br>
Container in 1 Minute ([YouTube](https://www.youtube.com/watch?v=n-JwAM6XF88))<br>
Container in kubernetes ([Kubernetes](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/#why-containers))

# Linux Container
## What is Linux Container?

LXC (pronounced lex-see) is an operating system–level virtualization method for running multiple isolated Linux systems (containers) on a single control host. Linux containers, in short, contain applications in a way that keep them isolated from the host system that they run on. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package. And they are designed to make it easier to provide a consistent experience as developers and system administrators move code from development environments into production in a fast and replicable way.

In a way, containers behave like a virtual machine. To the outside world, they can look like their own complete system. But unlike a virtual machine, rather than creating a whole virtual operating system, containers don't need to replicate an entire operating system, only the individual components they need in order to operate. This gives a significant performance boost and reduces the size of the application. They also operate much faster, as unlike traditional virtualization the process is essentially running natively on its host, just with an additional layer of protection around it.

Containers have also sparked an interest in micro-service architecture, a design pattern for developing applications in which complex applications are broken down into smaller, compassable pieces which work together. Each component is developed separately, and the application is then simply the sum of its constituent components. Each piece, or service, can live inside of a container, and can be scaled independently of the rest of the application as the need arises.

## How to use Linux Container?

LXD is a next generation system container manager. It offers a user experience similar to virtual machines but using Linux containers instead. Its image based with pre-made images available for a wide number of Linux distributions and is built around a very powerful, yet pretty simple, REST API.

To get a better idea of what LXD is and what it does, you can [try it here](https://linuxcontainers.org/lxd/try-it/) Then if you want to run it locally, take a look at our [getting started guide](https://linuxcontainers.org/lxd/getting-started-cli/).

The core of LXD is a privileged daemon which exposes a REST API over a local Unix socket as well as over the network (if enabled). Clients, such as the command line tool provided with LXD itself then do everything through that REST API. It means that whether you're talking to your local host or a remote server, everything works the same way.
	





