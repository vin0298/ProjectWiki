# Kubernetes

Please read the concept about [containers](https://github.com/vin0298/ProjectWiki/tree/master/Container) first<br>
From Kubernetes's explanation, [original web](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/#why-containers)<br>
Step-by-step tutorial on setting up an app to kubernetes, [Minikube](https://kubernetes.io/docs/tutorials/hello-minikube/)

Kubernetes is a portable, extensible open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation.

## Kubernetes provides a container-centric management environment. It orchestrates computing, networking, and storage infrastructure on behalf of user workloads.

## Why use kubernetes
1. Users expect applications to be available 24/7, and developers expect to deploy new versions of those applications several times a day. 
2. Containerization helps package software to serve these goals, enabling applications to be released and updated in an easy and fast way without downtime. 
3. Kubernetes helps you make sure those containerized applications run where and when you want, and helps them find the resources and tools they need to work. 
4. Kubernetes is a production-ready, open source platform designed with Google's accumulated experience in container orchestration, combined with best-of-breed ideas from the community.

## Kubernetes clusters
Kubernetes coordinates a highly available **cluster of computers** that are connected to work as a single unit.<br>
Kubernetes **automates the distribution and scheduling** of application containers across a cluster in a more efficient way

A Kubernetes cluster consists of two types of resources:
1. The **Master** coordinates the cluster, responsible for managing the cluster.
2. **Nodes** are the workers that run applications, a VM or a physical computer in a Kubernetes cluster. Also have tools for handling container operations, such as Docker or rkt. The nodes communicate with the master using the Kubernetes API.

![1](https://d33wubrfki0l68.cloudfront.net/99d9808dcbf2880a996ed50d308a186b5900cec9/40b94/docs/tutorials/kubernetes-basics/public/images/module_01_cluster.svg)

## Kubernetes Deployments
To deploy your application to your Kubernetes cluster, you need create a **Kubernetes Deployment configuration**

 Kubernetes Deployment Controller continuously monitors all deployed application instances. It provides a **self-healing mechanism** to address machine failure or maintenance.
 
 ![1](https://d33wubrfki0l68.cloudfront.net/152c845f25df8e69dd24dd7b0836a289747e258a/4a1d2/docs/tutorials/kubernetes-basics/public/images/module_02_first_app.svg)

## Kubernetes Pods
When you created a Deployment, Kubernetes created a Pod to host your application instance. A Pod is a Kubernetes abstraction that represents a group of one or more application containers (such as Docker or rkt), and some shared resources for those containers. Those resources include:

- Shared storage, as Volumes
- Networking, as a unique cluster IP address
- Information about how to run each container, such as the container image version or specific ports to use

**Pods are the atomic unit on the Kubernetes platform**

Pods can contain different application containers which are relatively tightly coupled.<br>
Each Pod is tied to the Node where it is scheduled, and remains there until termination (according to restart policy) or deletion. In case of a Node failure, identical Pods are scheduled on other available Nodes in the cluster.

![1](https://d33wubrfki0l68.cloudfront.net/fe03f68d8ede9815184852ca2a4fd30325e5d15a/98064/docs/tutorials/kubernetes-basics/public/images/module_03_pods.svg)

## Nodes
A Pod always runs on a Node.<br>
A Node is a worker machine in Kubernetes and may be either a virtual or a physical machine.<br>
Each Node is managed by the Master.<br>
A Node can have multiple pods.

Every Kubernetes Node runs at least:
1. Kubelet, a process responsible for communication between the Kubernetes Master and the Node; it manages the Pods and the containers running on a machine.
2. A container runtime (like Docker, rkt).

![1](https://d33wubrfki0l68.cloudfront.net/5cb72d407cbe2755e581b6de757e0d81760d5b86/a9df9/docs/tutorials/kubernetes-basics/public/images/module_03_nodes.svg)
