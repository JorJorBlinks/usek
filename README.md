# useK(ubernetes) - kubernetes starter, guides, and cheatsheets



## Overview



### Why kubernetes?



If you're coming from a KVM or XEN background (or even Vmware) then you will have very little trouble picking up kubernetes.  While developers who have used Cloud Foundry prefer the ease of deployment, Ops Engineers have largely embraced Kubernetes for its ease of management and rich ecosystem.  As a benefit of K8's ubiquitousness (over 96% of code-houses use it today!), there are many online resources to get you started (videos, diy guides, etc.).



### Scope



This repo aims to provide a directory of my ever-evolving toolset favorites, and implementation notes.  I will populate yaml files into the related services, and architectural diagrams/guides as time permits.



## Deployment methods



### Local deployment methods



Kind:

•Requires Docker to run.

•declarative automation via YAML file cluster configuration

•Good for testing Kubernetes features and creating multi-node clusters.

Minikube:

•Hypervisor required (KVM, VirtualBox, etc.) to run a single-node Kubernetes cluster.

•Friendly UX standing up and running a local Kubernetes cluster

•Great for local development and testing of applications.

K3s:

•A lightweight Kubernetes distribution designed for edge and IoT deployments.

•Requires minimal resources and can run on small machines.

•Can be installed with a few commands.

•SQLite for the backend datastore

K8s:

•Massive ecosystem

•Large-scale production deployments, complex applications, and environments with high availability requirements

•Native and extensible pod/container management for rapid elasticity and savings

•etcd for the backend datastore

K9:

•K9s provides an advanced terminal-based UI that simplifies navigation and resource management of Kubernetes.

•Great for seasoned sysadmins who ran their libvirt from the cli (or someone who hacked their esxi cli)



### Datacenter deployment optimizations (Generally using K8)

•Virtualized

•Baremetal

•Hardware Load Balancer APIs and considerations



### Cloud based Methods (Generally using K8)

•AWS

•GCE

•Azure

•IBMCloud

•OracleCloud

•Digitalocean

•AlibabaCloud



# Docker hacks



##Images and binaries

•Git-LFS -- ATTN: move to v3.6.1 (see CVE-2024-53263)

•AWS S3 integrations

•Dropbox integrations



