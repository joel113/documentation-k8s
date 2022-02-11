# K8s Networking

## K8s Essentials

### K8s CRI API

https://kubernetes.io/

https://github.com/kubernetes/cri-api

https://github.com/kubernetes/cri-api/blob/master/pkg/apis/runtime/v1alpha2/api.proto

https://github.com/containerd/containerd

### K8s CNI API

https://kubernetes.io/docs/concepts/extend-kubernetes/

https://kubernetes.io/docs/concepts/extend-kubernetes/compute-storage-net/network-plugins/#cni

https://www.cni.dev/

https://github.com/containernetworking

https://github.com/containernetworking/cni/blob/master/SPEC.md

https://github.com/aws/amazon-vpc-cni-k8s

## Container Primitves

* runC starts and manages the containers
* the containers facilitates linux primitives such as control groups and namespaces
* control groups (cgroups) control the access to resources
* namespaces are individual slices of resources
* a process user and group id can be different inside and outside of a container

https://en.wikipedia.org/wiki/Open_Container_Initiative
https://en.wikipedia.org/wiki/Cgroups
https://en.wikipedia.org/wiki/Linux_namespaces

### Namespaces

* the information regarding the namespaces are stored in the /proc filesystem 
* each process has a /proc/[pid]/ns/ subdirectory containing one entry for each namespace

```
sudo ls -l /proc/1/ns
```

https://github.com/joel113/Networking-and-Kubernetes/tree/master/chapter-3
https://man7.org/linux/man-pages/man7/namespaces.7.html

### IP

The ip command allows to setup a networking namespace and the virtual networking infrastructure to enable communication with and within the networking namespace.

https://man7.org/linux/man-pages/man8/ip.8.html

## Container Network Basics

### Network Modes

* None
* Bridge
* Host
* Macvlan
* Ipvlan
* Overlay
* Custom

https://docs.docker.com/network/

## Linux Networking Primitives

### Netfilter

https://www.netfilter.org/

### Conntrack

https://conntrack-tools.netfilter.org/
