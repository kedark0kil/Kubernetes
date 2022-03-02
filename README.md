**# Kubernetes
Documentation and steps that I followed for kubernetes**

This document contains all the documentation and links that will helped me to understand the concepts of the Kubernetes. All the course that I followd are from the Kodekloud also I'll add other google/YouTube links that'll help. 

**First starting with the basic concepts of the DevOps**
> - Pre-requisite you'll need to have some basic knowledge of the Linux system, DevOps tools, networking basics, source control management such as Git, Database, security, YAML and JSON conecpts.
> - For these details you can follow the [kodekloud course](- https://kodekloud.com/courses/devops-pre-requisite-course/) that will take you through the basics.
> - I'll start working with the kubernetes basics as the other things you might be aware of, if you need help understanding those you can checkout the course mentioned above.
> - Will follow the official documentation for the [Kubernetes](https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/). 

**Networking**
> Kubernetes have different components that are listed here - https://kubernetes.io/docs/concepts/overview/components/. One of the base component is "etcd" that is used for storing consistent and highly-available key value used as Kubernetes' backing store for all cluster data. We also need to have setup the backup plan for those data. More information about the etcd - https://etcd.io/docs/
  
 **Kubernetes Components**
> https://www.infracloud.io/kubernetes-school/basics-of-kubernetes/what-is-kubernetes/
> - Reconsiliation: The process of managing the replicas as required state and the current state, creating the replicas as needed can be called as reconsiliation.
> - kube-scheduler: It will ask API-server to create a pod and once we get the pod, will look into all the worker nodes to check on which node it can be scheduled according to the resources.
> - API-server: API server creates the pod which requested.
> - etcd: Cosistent key-value pair storage.
> The components that are responsible for scheduling the pod are **kubelet and kubeproxy**. Kubelet is the service that communicate with the container on worker node and schedule the container.
> The container engine that is running on the worker node can be docker, CRIO, etc.
> Kubernetes cluster consist of all the above components and to communicate with the kubenetes cluster we need to talk to the API server, kubeconfig is the file which have all the details that can help to communicate to the Kubernetes API server, like authentication method, endpoint on which it is running, etc.
> The life cycle for the kubernetes cluster - API server act as a entry point for the cluster then it will talk to the etcd(key-value pair storage). It'll get the pod created from the API server and kube-scheduler help to schedule the container on the worker node according to resources. And the component which manages the replicas of the container as per the configuration file. The kubeproxy and kubelet are the services that actually help in running the container on the nodes.
> One of the most important component is configuration file of the kubernetes.  

**Pod,Container and Node**
> **Conatiner** - the smallest part on the cluster which runs the application by using the config file.
> **Pod** - the container runs inside the pod and maintain the container replicas.
> **Node** - the node has the pods running with different instances.
> Pod have 1 to 1 relationship with the containers, If you want to scale up you create a new pod and to scale down you delete the existing pod. You do not add additional container to the existing pod for scaling the application. But this scenario changes when there's helper container which supports the application to process data, then that container can be inside the same pod. As when the application is termincated the helper will also get termincated. These two containers in the same pod and can communicate using localhost as they are in the same network.
