# kubernetes-learning

Gist to have as a reference for Kubernetes Learning.

## Table of contents

1. [Useful Kubernetes Courses](#Useful-Kubernetes-Courses)
2. [Learning Resources](#Learning-Resources)
3. [K8s Community](#K8s-Community)
4. [Reference Links](#Reference-Links)
5. [Cluster administration with Kubeadm](#Cluster-administration-with-Kubeadm)
6. [Useful kubectl commands](#Useful-kubectl-commands)
7. [Troubleshooting with kubectl](#Troubleshooting-with-kubectl)
8. [Useful kubectl plugins](#Useful-kubectl-plugins)

## Useful Kubernetes Courses

* A Cloud Guru
  * [Cloud Native Certified Kubernetes Administrator (CKA)](https://learn.acloud.guru/course/certified-kubernetes-administrator)
  * [Certified Kubernetes Application Developer (CKAD)](https://learn.acloud.guru/course/d068441f-75b4-4fe8-a7a6-df9153f24a35)
  * [Kubernetes the Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way)
* O'Reilly
  * Certified Kubernetes Administrator (CKA)
* Udemy
  * Kubernetes Mastery: Hands-On Lessons From A Docker Captain

## Learning Resources

* [Play with k8s](https://labs.play-with-k8s.com/)
* [Kubernetes Readme](https://kubernetesreadme.com/)
* [killer.sh](https://killer.sh/)

## k8s Community

* https://github.com/kubernetes/community
* https://github.com/kubernetes/enhancements

## Reference Links

### Understanding Kubernetes API and Managing Kubernetes Objects in General

* Kubernetes API:
  * API Reference: https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/
  * Using API: https://kubernetes.io/docs/reference/using-api/
  * API Convention: https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api-conventions.md
  * https://kubernetes.io/docs/concepts/overview/kubernetes-api/
* Object Management
  * https://kubernetes.io/docs/concepts/overview/working-with-objects/object-management/
  * https://kubernetes.io/docs/concepts/overview/working-with-objects/kubernetes-objects/
  * https://blog.atomist.com/kubernetes-apply-replace-patch/

### Authentication and Authorization

* https://kubernetes.io/docs/concepts/security/controlling-access/
* https://kubernetes.io/docs/reference/access-authn-authz/authentication/
* https://kubernetes.io/docs/reference/access-authn-authz/authorization/
* https://kubernetes.io/docs/reference/access-authn-authz/admission-controllers/
* https://kubernetes.io/docs/reference/access-authn-authz/rbac/
* https://kubernetes.io/docs/reference/access-authn-authz/bootstrap-tokens/

### Accessing the Cluster

* https://kubernetes.io/docs/tasks/access-application-cluster/access-cluster/
* https://kubernetes.io/docs/tasks/administer-cluster/access-cluster-api/
  * Python Examples: https://github.com/kubernetes-client/python/tree/master/examples

### Cluster Management

* Kubectl
  * https://kubernetes.io/docs/reference/kubectl/overview/
  * https://kubectl.docs.kubernetes.io/
  * https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands
  * https://kubernetes.io/docs/reference/kubectl/cheatsheet/
  * https://kubernetes.io/docs/concepts/cluster-administration/
  * https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/
  * https://kubernetes.io/docs/concepts/configuration/organize-cluster-access-kubeconfig/

* Web UI Dashboard
  * https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/

### Networking

* Networking Overview: https://cloud.google.com/kubernetes-engine/docs/concepts/network-overview
* Cluster Networking: https://kubernetes.io/docs/concepts/cluster-administration/networking/
* Services
  * https://kubernetes.io/docs/concepts/services-networking/service/
  * https://cloud.google.com/kubernetes-engine/docs/concepts/service
* DNS
  * DNS for Services and Pods: https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/
  * Customizing DNG: https://kubernetes.io/docs/tasks/administer-cluster/dns-custom-nameservers/
  * Debugging DNS Resolution: https://kubernetes.io/docs/tasks/administer-cluster/dns-debugging-resolution/
* Network Policies
  * https://kubernetes.io/docs/concepts/services-networking/network-policies/
  * Declare Network Policies: https://kubernetes.io/docs/tasks/administer-cluster/declare-network-policy/
* Proxy: https://kubernetes.io/docs/tasks/extend-kubernetes/http-proxy-access-api/
* Port Forwarding: https://kubernetes.io/docs/tasks/access-application-cluster/port-forward-access-application-cluster/

### Logging

* https://kubernetes.io/docs/concepts/cluster-administration/logging/

### Monitoring

* https://kubernetes.io/docs/tasks/debug-application-cluster/resource-metrics-pipeline/
* https://kubernetes.io/docs/tasks/debug-application-cluster/resource-usage-monitoring/
* https://github.com/kubernetes-sigs/metrics-server
* https://kubernetes.io/docs/tasks/debug-application-cluster/monitor-node-health/

### Cluster Security

* https://kubernetes.io/blog/2018/07/18/11-ways-not-to-get-hacked/

### Container Security

* https://kubernetes.io/docs/tasks/configure-pod-container/security-context/
* https://kubesec.io/
* https://kubernetes.io/docs/concepts/containers/images/
* https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/
* https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/#add-imagepullsecrets-to-a-service-account

### Troubleshooting

#### Application Failure

* https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle/
* https://kubernetes.io/docs/tasks/debug-application-cluster/debug-application/
* https://kubernetes.io/docs/tasks/debug-application-cluster/debug-application-introspection/
* https://kubernetes.io/docs/tasks/debug-application-cluster/determine-reason-pod-failure/
* https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/

#### Control Plane Failure

* https://kubernetes.io/docs/tasks/debug-application-cluster/debug-cluster/#a-general-overview-of-cluster-failure-modes

#### Worker Node Failure

* https://kubernetes.io/docs/concepts/architecture/nodes/
* https://kubernetes.io/docs/tutorials/kubernetes-basics/explore/explore-intro/#nodes

#### Networking Failure

* https://kubernetes.io/docs/tasks/debug-application-cluster/debug-service/
* https://kubernetes.io/docs/tasks/access-application-cluster/port-forward-access-application-cluster/
* https://kubernetes.io/docs/tasks/debug-application-cluster/troubleshooting/
* https://kubernetes.io/docs/setup/independent/create-cluster-kubeadm/#pod-network

### High Availability Topologies

* https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/ha-topology/

## Cluster administration with Kubeadm

* https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/

### Install Kubernetes with Kubeadm

These steps show how to provision a k8s with containerd as container runtime using kubeadmin. The steps only were tested in Ubuntu 18.04.

Following steps should be run in all nodes (master and workers):

```text
# Create configuration file for containerd
cat <<EOF | sudo tee /etc/modules-load.d/containerd.conf
overlay
br_netfilter
EOF

# Load kernel modules
sudo modprobe overlay
sudo modprobe br_netfilter

# Set system configurations for Kubernetes networking
cat <<EOF | sudo tee /etc/sysctl.d/99-kubernetes-cri.conf
net.bridge.bridge-nf-call-iptables = 1
net.ipv4.ip_forward = 1
net.bridge.bridge-nf-call-ip6tables = 1
EOF

# Apply new networking settings
sudo sysctl --system

# Install containerd
sudo apt-get update && sudo apt-get install -y containerd

# Create default configuration file for containerd
sudo mkdir -p /etc/containerd

# Generate default containerd configuration and save to the newly created default file
sudo containerd config default | sudo tee /etc/containerd/config.toml

# Restart containerd to ensure new configuration file usage
sudo systemctl restart containerd

# Check the status of containerd service to verify it is running
sudo systemctl status containerd

# Disable swap -> https://github.com/kubernetes/kubernetes/issues/53533
sudo swapoff -a

# Disable swap on startup in /etc/fstab
sudo sed -i '/ swap / s/^\(.*\)$/#\1/g' /etc/fstab

# Install dependency packages
sudo apt-get update && sudo apt-get install -y apt-transport-https curl

# Download and add k8s GPG Key
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

# Add k8s repository to ubuntu repositories list
cat <<EOF | sudo tee /etc/apt/sources.list.d/kubernetes.list
deb https://apt.kubernetes.io/ kubernetes-xenial main
EOF

# Run apt-get update
sudo apt-get update

# Install K8s packages
sudo apt-get install -y kubelet=1.21.0-00 kubeadm=1.21.0-00 kubectl=1.21.0-00

# Turn off automatic updates
sudo apt-mark hold kubelet kubeadm kubectl
```

Following steps should be only run in master nodes:

```text
# Initialize the Kubernetes Cluster
sudo kubeadm init --pod-network-cidr 192.168.0.0/16 --kubernetes-version 1.21.0

# Set kubectl access
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config

`# Test access to cluster (Master node should be in "NotReady" status)
kubectl get nodes

# Install network add-on (In this case we are installing calico. But it could be flannel, weavenet, etc.)
kubectl apply -f https://docs.projectcalico.org/manifests/calico.yaml

# Test access to cluster again (Master node should be in "Ready" status)
kubectl get nodes

# Generate join command for the worker nodes
sudo kubeadm token create --ttl 2h --print-join-command

# Generate New Token
sudo kubeadm token generate

# List Available Tokens
sudo kubeadm token list
```

Following steps should be run in worker nodes:

```text
sudo kubeadm join 172.31.105.135:6443 --token yf1zxq.fu7zx2qmyat2rrx9 --discovery-token-ca-cert-hash sha256:9af9520166d86679f711dcbe3d6736b09cc0b6a7486ab8dc7f6eb30665ab350d
```

### Upgrade a cluster with Kubeadm

First of all, the master nodes should be upgraded and then the worker nodes.

Following commands should be run in the Master Node

```text
# Upgrade kubeadm
sudo apt-get update && sudo apt-get install -y --allow-change-held-packages kubeadm=1.21.1-00

# Make sure that kubeadm was upgraded properly
kubeadm version

# Drain the control plane
kubectl drain [master_node_name] --ignore-daemonsets

# Plan the upgrade
sudo kubeadm upgrade plan v1.21.1

# Upgrade the control plane components
sudo kubeadm upgrade apply v1.21.1

# Upgrade kubelet and kubectl on the control plane node
sudo apt-get update && sudo apt-get install -y --allow-change-held-packages kubelet=1.21.1-00 kubectl=1.21.1-00

# Restart kubelet
sudo systemctl daemon-reload
sudo systemctl restart kubelet

# Uncordon the control plane node
kubectl uncordon [master_node_name]

# Verify the control plane is working
kubectl get nodes
```

Following commands should be run in worker nodes

```text
# Drain the node
kubectl drain [worker_node_name] --ignore-daemonsets --force

# Upgrade kubeadm
sudo apt-get update && sudo apt-get install -y --allow-change-held-packages kubeadm=1.21.1-00

# Upgrade the kubelet configuration
sudo kubeadm upgrade node

# Upgrade kubelet and kubectl
sudo apt-get update && sudo apt-get install -y --allow-change-held-packages kubelet=1.21.1-00 kubectl=1.21.1-00

# Restart kubelet
sudo systemctl daemon-reload
sudo systemctl restart kubelet

# Uncordon the control plane node
kubectl uncordon [worker_node_name]

# Verify the control plane is working
kubectl get nodes
```

More Info:

* https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-certs/
* https://kubernetes.io/docs/setup/best-practices/certificates/
* https://kubernetes.io/docs/reference/command-line-tools-reference/kubelet-tls-bootstrapping/
* https://kubernetes.io/docs/tasks/administer-cluster/highly-available-master/
* https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/troubleshooting-kubeadm/
* https://kubernetes.io/docs/reference/setup-tools/kubeadm/kubeadm-reset/

## Useful kubectl commands

* Commands Reference: https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands

### Cluster management with kubectl

```text

# Get information of configured clusters in kubectl
kubectl config view

# Get only current configuration
kubectl config view --minify

# Switch Contex. If config file is not specified by default ~/.kube/config is used. config_file must be present in the same directory where kubectl command is run. Can not be used an absolute or relative path to the file.
kubectl config --kubeconfig=[config_file] use-context dev-frontend

# Get kubectl current context
kubectl config current-context

# Use KUBECONFIG env var to set up different config_files locations
export KUBECONFIG=$KUBECONFIG:$HOME/.kube/config:$HOME/.kube/config_test

# Skip TLS Verify. This must be use with catious because it skip the checking of the API Server Certificate
# https://stackoverflow.com/questions/46360361/invalid-x509-certificate-for-kubernetes-master
kubectl --insecure-skip-tls-verify get pods
```

### Manage TLS and Certificates

```text
# Managing TLS in the Cluster: https://kubernetes.io/docs/tasks/tls/managing-tls-in-a-cluster/
# Certificate Signing Requests: https://kubernetes.io/docs/reference/access-authn-authz/certificate-signing-requests/
# Bootstrapping TLS for Your kubelets: https://kubernetes.io/docs/reference/command-line-tools-reference/kubelet-tls-bootstrapping/
# How kubeadm Manages Certificates: https://kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-certs/

# Get/Describe Certificate Signing Requests
kubectl get csr
kubectl describe csr

# Approve a Certificate Signing Request
kubectl certificate approve [csr_name]

```

### Manage Service Accounts, Cluster Roles and Cluster Role Bindings

```text
# https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/

# List existing service accounts
kubectl get serviceaccounts

# Create a service account. This command automatically creates a secret for the service account
kubectl create serviceaccount [serviceaccount_name]

# Create a role binding for anonymous users (not recommended):
kubectl create clusterrolebinding cluster-system-anonymous --clusterrole=cluster-admin --user=system:anonymous
```

### Manage Pods

```text
# Configure Default CPU Requests and Limits: https://kubernetes.io/docs/tasks/administer-cluster/manage-resources/cpu-default-namespace/
# Configure Default Memory Requests and Limits: https://kubernetes.io/docs/tasks/administer-cluster/manage-resources/memory-default-namespace/
# Container Probes: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle/#container-probes
# Init Containers: https://kubernetes.io/docs/concepts/workloads/pods/init-containers/

# Run a pod
kubectl run nginx --image=nginx

# Run a pod and modify some fields in the pod spec and run "sleep infinity" command so the pod does not dies
kubectl run <pod_name> --image=<imagename> --namespace=<namespace> --overrides='{"spec":{"serviceAccountName":"<serviceaccountname>"}}' --command -- sleep infinity

# Get pods objects and order and filter the output
kubectl get pods <object_name> -o <output> --sort-by <JSONPath> --selector <selector>

# Get pod specific field output
kubectl get -o template pod/<pod-name> --template={{.status.phase}}

# Get pods objects with specific output organized by custom columns
kubectl get pod -o custom-columns=NAME:.metadata.name,NodeSelector:.spec.nodeSelector

# Get pods in default namespace with output format wide
kubectl get pods -o wide

# Get pods in default namespace with output format yaml
kubectl get pods -o yaml

# Get pods in an specific namespace using the default output format
kubectl get pods -n [specific_namespace]

# Get pods in all namespaces using the default output format
kubectl get pods --all-namespaces

# Show pod labels
kubectl get pods --show-labels

# Get pods filtering with its labels
kubectl get pods -l key1=value1,key2=value2
kubectl get pods -l key1!=value1

# Edit an existing pod configuration
kubectl edit pods [pod_name]

# Describe an specific pod to get more information
kubectl describe pods [pod_name]

# Open a shell/execute a specific command inside a pod. When pod has more than one container it defaults to the first defined container
kubectl exec -ti [pod_name] -- [command]

# Open a shell/execute a specific command inside a pod when pod has more than one container
kubectl exec -it [pod_name] -c [container_name] [command]

# Attach to a process that is already running inside an existing container
kubectl -n [namespace] attach [pod_name] -c [container_name] [options]

# Get logs from a pod
kubectl logs [pod-name]
kubectl logs [pod-name] -f # Follow logs

# Return snapshot logs from pod with multi containers
kubectl logs [pod-name] --all-containers=true

# Return snapshot logs from all containers in pods defined by label app=nginx
kubectl logs -lapp=nginx --all-containers=true

# Return snapshot of previous terminated ruby container logs from pod web-1
kubectl logs -p -c ruby web-1

# Begin streaming the logs of the ruby container in pod web-1
kubectl logs -f -c ruby web-1

# Begin streaming the logs from all containers in pods defined by label app=nginx
kubectl logs -f -lapp=nginx --all-containers=true

# Display only the most recent 20 lines of output in pod nginx
kubectl logs --tail=20 nginx

# Show all logs from pod nginx written in the last hour
kubectl logs --since=1h nginx

# Show logs from a kubelet with an expired serving certificate
kubectl logs --insecure-skip-tls-verify-backend nginx

# Return snapshot logs from first container of a job named hello
kubectl logs job/hello

# Return snapshot logs from container nginx-1 of a deployment named nginx
kubectl logs deployment/nginx -c nginx-1

# Add a label to a pod
kubectl label pod [pod_name] label-key=label-value

# Override the labels in a pod
kubectl label pod [pod_name] label-key=label-value --overwrite
```

### Manage DaemonSets

```text
# DaemonSets: https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/
```

### Manage Jobs and CronJobs

```text
# Jobs: https://kubernetes.io/docs/concepts/workloads/controllers/job/
# CronJobs: https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/
```

### Manage ReplicaSets

```text
# ReplicaSets: https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/

# Get existing ReplicaSets
kubectl get replicasets

```

### Manage StatefulSets

```text
# StatefulSets: https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/

# Get existing ReplicaSets
kubectl get statefulsets

# Describe existing StatefulSets
kubectl describe statefulsets
```

### Manage Deployments

```text
# Manage Deployments: https://kubernetes.io/docs/concepts/cluster-administration/manage-deployment/
# https://kubernetes.io/docs/concepts/workloads/controllers/deployment/
# https://kubernetes.io/docs/tutorials/kubernetes-basics/deploy-app/deploy-intro/
# https://kubernetes.io/docs/tutorials/kubernetes-basics/update/update-intro/

# Create a deployment
kubectl create deployment nginx --image=nginx

# Apply or Update a deployment.
kubectl apply -f [deployment_yaml_file]

# Replace an existing deployment.
kubectl replace -f [deployment_yaml_file]

# Get existing deployments
kubectl get deployments

# Create a deployment with a record (for rollbacks)
kubectl create -f [deployment_file] --record

# Check status of a rollout
kubectl rollout status deployments [deployment_name]

# Undo a rollout deployment
kubectl rollout undo deployments [deployment_name]

# Look at the rollout history 
kubectl rollout history [deployment_name] kubeserve

# Roll back to a certain revision
kubectl rollout undo deployment [deployment_name] --to-revision=2

# Pause the rollout in the middle of a rolling update (canary release)
kubectl rollout pause deployment [deployment_name]

# Resume the rollout after the rolling update looks good
kubectl rollout resume deployment [deployment_name]

# Scale a deployment
kubectl scale deployment/[deployment_name] --replicas=[number_replicas]
kubectl scale deploy [deployment_name] --replicas=[number_replicas] -n [namespace]

# Patch a deployment
kubectl patch deployment [deployment_name] -p '{"spec": {"minReadySeconds": 10}}'

# Modify image of deployment with a verbose level of six
kubectl set image deployments/[deployment_name] [some_label]=[image_name]:[image_tag] --v 6
kubectl set image deployments/kubeserve app=linuxacademycontent/kubeserve:v2 --v 6
```

### Manage Services, Networking and DNS

```text
# Configure Port Forwarding
# This commands have the same effect and forward a port in local machine where kubectl is running to a port inside the cluster where the pod is running.
kubectl port-forward [pod_name] 7000:6379
kubectl port-forward service/[service_name] 7000:6379

# Enable proxy server. After enabling the proxy, the k8s api can be accessed through the localhost like: http://localhost:8080
kubectl proxy --port=8080

# Creating a Service type of NodePort by exposing a port from cli
kubectl expose deployment [deployment_name] --port 80 --type NodePort

# View the list of services in the cluster
kubectl get services

# Describe services created in the cluster
kubectl describe services # default namespace
kubectl describe services -n [namespace_name]

# Edit created services in specific namespaces namespace.
kubectl edit services # default namespace
kubectl edit services -n [namespace_name]

# View the list of endpoints in your cluster that get created with a service:
kubectl get endpoints

# Look at the iptables rules for your services
sudo iptables-save | grep KUBE | grep [service_name]

# Set the annotation to route load balancer traffic local to the node. This makes the load balancer service pod unaware. So this means that only the traffic will be distributed accros nodes no matter if in one node there are more pods than in another node. By default this annotation is disabled so traffic is splitted in pod aware way but it adds more latency to the network packets and sometime this is not desired.
kubectl annotate service kubeserve2 externalTrafficPolicy=Local

```

### Manage Ingress

```text
# Ingress: https://kubernetes.io/docs/concepts/services-networking/ingress/

# View the list of services in the cluster
kubectl get ingress

# Describe services created in the cluster
kubectl describe ingress # default namespace
kubectl describe ingress -n [namespace_name]

# Edit created services in specific namespaces namespace.
kubectl edit ingress # default namespace
kubectl edit ingress -n [namespace_name]
```

### Manage ConfigMaps and Secrets

```text
# https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/
# https://kubernetes.io/docs/concepts/configuration/secret/

# Create a ConfigMap 
kubectl create configmap [configmap_name] --from-literal=key1=value1 --from-literal=key2=value2

# Create a ConfigMap from a file
kubectl create configmap demo-config --namespace=demo --from-file=config.yaml

# Get ConfigMaps
kubectl get configmaps

# Create a generic secret
kubectl create secret generic [secret_name] --from-literal=key1=supersecret --from-literal=key2=topsecret

# Create a generic secret from files
kubectl create secret generic [secret_name] --from-file=https.key --from-file=https.cert

# Create a docker-registry secret
kubectl create secret docker-registry acr --docker-server=[private-registry-url] --docker-username=[registry-access-username] --docker-password=[registry-access-password] --docker-email=[registry-user-email]

# Get Secrets
kubectl get secrets

```

### Manage Namespaces

```text
# Create a namespace
kubectl create namespace [namespace_name]

# Delete a namespace
kubectl delete namespace [namespace_name]
```

### Manage Events

```text
# https://kubernetes.io/docs/tasks/administer-cluster/configure-multiple-schedulers/#verifying-that-the-pods-were-scheduled-using-the-desired-schedulers

# Get Events in default namespace
kubectl get events

# Get Envents in an specific namespace
kubectl get events -n [namespace_name]

# Sort events by timestamp
kubectl get events --sort-by='{.lastTimestamp}' -n [namespace_name]

# Watch events in real time
kubectl get events -n [namespace_name] -w
```

### Manage Storage

```text
# Storage: https://kubernetes.io/docs/concepts/storage/
# Volumes: https://kubernetes.io/docs/concepts/storage/volumes/
# Persistent Volumes: https://kubernetes.io/docs/concepts/storage/persistent-volumes/
# Configure Persistent Volume Storage: https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/
# Storage Classes: https://kubernetes.io/docs/concepts/storage/storage-classes/

# Get existing Persistent Volumes, Persistent Volumes Claims or Storage Clasess
kubectl get pv
kubectl get pvc
kubectl get sc

# Delete a Persistent Volume, a Persistent Volume Claim or a Storage Class
kubectl delete pv [pv_name]
kubectl delete pvc [pvc_name]
kubectl delete sc [sc_name]

# Describe a Persistent Volume, a Persistent Volume Claim or a Storage Class
kubectl describe [pv_name]
kubectl describe pvc [pvc_name]
kubectl describe sc [sc_name]
```

### Manage Schedulling

```text
# Configuring Multiple Schedulers: https://kubernetes.io/docs/tasks/administer-cluster/configure-multiple-schedulers/
```

### Manage Nodes

```text
# Assigning Pod to a Node: https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/
# Pod and Node Affinity Rules: https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity
# Taints and Tolerations: https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/

# Get Node List
kubect get nodes -o wide

# Label a Node
kubectl label [node_name] label=value

# Add role label to a node
kubectl label node [node_name] node-role.kubernetes.io/worker=[label_value]
kubectl label node k8s-worker2 node-role.kubernetes.io/worker=worker

# Drain a Node
kubectl drain [node_name] --ignore-daemonsets

# Undrain Node
kubectl uncordon [node_name]

# Delete Node
kubectl delete node [node_name]

# Taint a node
kubectl taint node [node_name] key=value:NoSchedule

# Remove added taint
kubectl taint nodes [node_name] key:NoSchedule-

```

### Get Monitoring and Cluster Information

Before beign able to run the following commands the metric API should be installed. Check [this](#monitoring)

```text
# Get CPU and Memory utilization of the nodes in the cluster
kubectl top node

# Get the CPU and memory utilization of the pods in the cluster
kubectl top pods

# Get the CPU and memory of pods in all namespaces
kubectl top pods --all-namespaces

# Get the CPU and memory of pods in only one namespace
kubectl top pods -n [namespace_name]

# Get CPU and memory of an specific pod
kubectl top pods [pod_name]

# Get CPU and memory of the containers inside the pod
kubectl top pods [pod_name] --containers

# Get cpu and memory consumption of all the pods in a namespace filtering by a label selector and sorting by cpu consumption
kubectl -n [namespace_name] top pod --sort-by cpu --selector key=value

# Get cluster information
kubectl cluster-info
```

### Exporting kubernetes api resources/objects

```text
# Run a new deployment and get the output in yaml format with the --export flag
kubectl run newdemo --image=cloudnatived/demo:hello --port=8888 --labels app=newdemo
# Install neat kubectl plugin
kubectl krew install neat
# Use neat plugin to export a kubectl manifest removing automatically created fields by kubernetes api
kubectl get deployments newdemo -o yaml > deployment.yaml | kubectl neat
```

### Diffing Resoruces

```text
# Diff the resource to be deployed with the resource already deployed
kubectl diff -f deployment.yaml
```

## Troubleshooting with kubectl

### Namespace in Terminating state

When a namespace is in Terminating state following commands can be run to check what are the dangling resources that stops the namespace of beign deleted

```text
kubectl api-resources --verbs=list --namespaced -o name | xargs -n 1 kubectl get --show-kind --ignore-not-found -n <namespace-in-terminating-stage>
```

More info:

* https://www.ibm.com/docs/en/cloud-private/3.2.0?topic=console-namespace-is-stuck-in-terminating-state

### Patching dangling resources

```text
# Patching dangling resources to remove the finalizer so the object can be deleted
kubectl patch <resource-type> <resource-name> -p '{"metadata":{"finalizers":[]}}' --type=merge
```

Note: It is needed to use the patch command because the `kubectl edit` does not work.

## Useful kubectl plugins

[krew](https://krew.sigs.k8s.io/) is a kubectl plugin manager and these are some of the most useful plugins:

* [neat](https://github.com/itaysk/kubectl-neat)
  * To remove clutter from Kubernetes manifests to make them more readable.
* [ketall](https://github.com/corneliusweig/ketall)
  * To show really all kubernetes resources 

More Info:

* [Making Kubernetes Operations Easy with kubectl Plugins](https://martinheinz.dev/blog/58)