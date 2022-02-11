# K8s Networking

## Container Primitves

* runC starts and manages the containers (cmp. https://en.wikipedia.org/wiki/Open_Container_Initiative)
* the containers facilitates linux primitives such as control groups and namespaces
* control groups (cgroups) control the access to resources (cmp. https://en.wikipedia.org/wiki/Cgroups)
* namespaces are individual slices of resources (cmp. https://en.wikipedia.org/wiki/Linux_namespaces)
* a process user and group id can be different inside and outside of a container

### Namespaces

* the information regarding the namespaces are stored in the /proc filesystem (cmp. https://man7.org/linux/man-pages/man7/namespaces.7.html)
* each process has a /proc/[pid]/ns/ subdirectory containing one entry for each namespace

```
sudo ls -l /proc/1/ns
```

https://github.com/joel113/Networking-and-Kubernetes/tree/master/chapter-3
