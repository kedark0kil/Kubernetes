# Kubernetes
Documentation and steps that I followed for kubernetes

This document contains all the documentation and links that will helped me to understand the concepts of the Kubernetes. All the course that I followd are from the Kodekloud also I'll add other google/YouTube links that'll help. 

**# First starting with the basic concepts of the DevOps**
> Pre-requisite you'll need to have some basic knowledge of the Linux system, DevOps tools, networking basics, source control management such as Git, Database, security, YAML and JSON conecpts.
> For these details you can follow the [kodekloud course](- https://kodekloud.com/courses/devops-pre-requisite-course/) that will take you through the basics.
> I'll start working with the kubernetes basics as the other things you might be aware of, if you need help understanding those you can checkout the course mentioned above.
> Will follow the official documentation for the [Kubernetes](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/). 

  **Networking**
  
  
  Kubernetes have different components that are listed here - https://kubernetes.io/docs/concepts/overview/components/. One of the base component is "etcd" that is used for storing consistent and highly-available key value used as Kubernetes' backing store for all cluster data. We also need to have setup the backup plan for those data. More information about the etcd - https://etcd.io/docs/
    
https://www.infracloud.io/kubernetes-school/basics-of-kubernetes/what-is-kubernetes/
Reconsiliation: The process of managing the replicas as required state and the current state, creating the replicas as needed can be called as reconsiliation.
kube-scheduler: It will ask API-server to create a pod and once we get the pod, will look into all the worker nodes to check on which node it can be scheduled according to the resources.
API-server: API server creates the pod which requested.
etcd: Cosistent key-value pair storage.
