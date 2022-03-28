# Tech Radar

## Table of Contents

1. [Container Tools](#Container-Tools)
2. [Kubernetes Tools](#Kubernetes-Tools)
3. [Security Tools](#Security-Tools)
4. [CI-CD](#CI-CD)
5. [GitOps Tools](#GitOps-Tools)
6. [Plataform as a Service](#Plataform-as-a-Service)
7. [Infraestructure as a Service](#Infraestructure-as-a-Service)
8. [Infraestructure as a Code](#Infraestructure-as-a-Code)
9. [Infrastructure as Software](#Infrastructure-as-Software)
10. [Certificates and Key Management](#Certificates-and-Key-Management)
11. [IAM](#IAM)
12. [Load Balancers, Proxies, Service Meshes and Service Discovery](#Load-Balancers-Proxies-Service-Meshes-and-Service-Discovery)
13. [Monitoring](#Monitoring)
14. [Logging and Tracing](#Logging-and-Tracing)
15. [Data visualization](#Data-visualization)
16. [Distribute Storage Systems](#Distribute-Storage-Systems)
17. [Databases and Cache](#Databases-and-Cache)
18. [Content Management System](#Content-Management-System)
19. [Messaging and Queuing Systems](#Messaging-and-Queuing-Systems)
20. [Testing Tools](#Testing-Tools)
21. [Interesting Links](#Interesting-Links)

## Container Tools

### Container Runtimes

#### CRI Container Runtimes

* [cri-o](https://cri-o.io/)
* [containerd](https://containerd.io/)

#### OCI Container Runtimes

* [runc](https://github.com/opencontainers/runc)
* [crun](https://github.com/containers/crun)
* [gVisor](https://gvisor.dev/docs/)

### Container Engines

* [docker](https://www.docker.com/)
* [podman](https://podman.io/)
* [rkt](https://coreos.com/rkt/)
* [lxd/lxc](https://linuxcontainers.org/)
* [frakti](https://kubernetes.github.io/frakti/deploy.html)

### Virtual Machines containers-like Runtimes

* [katacontainers](https://katacontainers.io/)

### Build Image Tools

* [buildah](https://buildah.io/)
* [kaniko](https://github.com/GoogleContainerTools/kaniko)
* [buildkit-cli-for-kubectl](https://github.com/vmware-tanzu/buildkit-cli-for-kubectl)
* [img](https://github.com/genuinetools/img)

### Images and Registries Interaction Tools

* [crane](https://github.com/google/go-containerregistry/tree/main/cmd/crane)
* [skopeo](https://github.com/containers/skopeo)
* [umoci](https://github.com/openSUSE/umoci)
* [dive](https://github.com/wagoodman/dive)

### Image Build and Post Build Scan

* [Microscanner](https://github.com/aquasecurity/microscanner): Scan during build of images
* [Trivy](https://github.com/aquasecurity/trivy#os-packages): Post build scans
* [snyk containers](https://snyk.io/product/container-vulnerability-management/)
* [Clair](https://github.com/quay/clair)
* [Aqua Security](https://www.aquasec.com/)
* [kube-hunter](https://github.com/aquasecurity/kube-hunter)
* StackRox
* Twistlock
* Sysdig Secure

### Container Runtime Scanners

* [Sysdig Falco](https://sysdig.com/opensource/falco/)
* NeuVector

### Container Images Signing

* Notary

### Dockerfile Linting

* [hadolint](https://github.com/hadolint/hadolint)

### Container Monitoring/Statistics

* [cAdvisor](https://github.com/google/cadvisor)

### Containers Orchestrators

* [Kubernetes](https://kubernetes.io/)
* [k3s](https://k3s.io/): Lightweight Kubernetes
* [Docker Swarm](https://docs.docker.com/engine/swarm/)
* [Marathon](https://mesosphere.github.io/marathon/)
* [Nomad](https://www.nomadproject.io/)

## Kubernetes Tools

### Package Managers

* [kustomize](https://github.com/kubernetes-sigs/kustomize)
* [Helm](https://helm.sh/)

### Observability

* [kube-state-metrics](https://github.com/kubernetes/kube-state-metrics)
* [metrics-server](https://github.com/kubernetes-sigs/metrics-server)
* [node-problem-detector](https://github.com/kubernetes/node-problem-detector)
* [k8s dashboard](https://github.com/kubernetes/dashboard)
* [kube-web-view](https://codeberg.org/hjacobs/kube-web-view)
* [octant](https://octant.dev/)
* [weave scope](https://github.com/weaveworks/scope)
* [kube-ops-view](https://codeberg.org/hjacobs/kube-ops-view)

### Cluster Management

* [kops](https://github.com/kubernetes/kops)
* [kubespray](https://github.com/kubernetes-sigs/kubespray)
* [kubeadm](https://github.com/kubernetes/kubeadm)
* [kubicorn](http://kubicorn.io/)

### Kubernetes Managers

* RedHat OpenShift
* Rancher
* Digital Ocean Kubernetes
* EKS (AWS)

### Kubernetes Manifests Validation Tools

* [kubeval](https://github.com/instrumenta/kubeval)

### Backup Tools

* [Velero](https://velero.io/)

### Kubernetes Network Policies and Plugins

* [WeaveNet](https://www.weave.works/oss/net/)
* [flannel](https://github.com/coreos/flannel)
* [Calico](https://www.projectcalico.org/)
* [Cilium](https://cilium.io/)
* [kube-router](https://github.com/cloudnativelabs/kube-router)

### Kubernetes Operations

* [operators whitepaper](https://github.com/cncf/tag-app-delivery/blob/eece8f7307f2970f46f100f51932db106db46968/operator-wg/whitepaper/Operator-WhitePaper_v1-0.md)
* [operator-framework](https://operatorframework.io/)
* [ansible operators](https://learn.openshift.com/ansibleop/ansible-operator-overview/): Deploying containers into Kubernetes
* [kubebuilder](https://github.com/kubernetes-sigs/kubebuilder): Kubebuilder is a framework for building Kubernetes APIs using custom resource definitions (CRDs)
* [shell-operator](https://github.com/flant/shell-operator): Tool for running event-driven scripts in a Kubernetes cluster
* [kudo](https://kudo.dev/)
* [charmed operator framework](https://juju.is/)
* [metacontroller](https://metacontroller.github.io/metacontroller/intro.html)
* [kubediff](https://github.com/weaveworks/kubediff)

### Machine Learning Kubernetes Tools

* [kubeflow](https://www.kubeflow.org/)

### DNS Tools

* [external-dns](https://github.com/kubernetes-sigs/external-dns)

### Schedulling Tools

* [descheduler](https://github.com/kubernetes-sigs/descheduler)

### Ingress Controllers

* [aws-load-balancer-controller](https://kubernetes-sigs.github.io/aws-load-balancer-controller/latest/)
* [Traefik](https://doc.traefik.io/traefik/providers/kubernetes-ingress/)
* [Nginx](https://kubernetes.github.io/ingress-nginx/)
* [Ambassador](https://www.getambassador.io/docs/edge-stack/latest/topics/running/ingress-controller/)
* [Gloo](https://docs.solo.io/gloo-edge/1.6.19/guides/integrations/ingress/)
* [Contour](https://projectcontour.io/)
* [Kong](https://konghq.com/solutions/kubernetes-ingress/)

### Auditing, Security and Certificates

* [Cert Manager](https://cert-manager.io/docs/installation/kubernetes/)
* [popeye](https://github.com/derailed/popeye)
* [kube-bench](https://github.com/aquasecurity/kube-bench)
* [k8Guard](https://k8guard.github.io/)
* [copper](https://github.com/cloud66-oss/copper)

### Autoscaling

* [cluster-autoscaler](https://github.com/kubernetes/autoscaler)
* [karpenter](https://github.com/aws/karpenter)
* [keda](https://keda.sh/)
* [cluster-proportional-autoscaler](https://github.com/kubernetes-sigs/cluster-proportional-autoscaler)
* [aws-node-termination-handler](https://github.com/aws/aws-node-termination-handler)
* [kube-downscaler](https://codeberg.org/hjacobs/kube-downscaler): Scale down Kubernetes deployments after work hours

### Functions as a Service Tools

* [Knative](https://knative.dev/)
* [OpenFaaS](https://www.openfaas.com/)

### Local Development

* [Skaffold](https://skaffold.dev/)
* [Draft](https://github.com/Azure/draft)
* [Teleprecense](https://www.telepresence.io/)
* [Bridge to K8s](https://docs.microsoft.com/en-us/visualstudio/bridge/bridge-to-kubernetes-vs-code)
* [squash](https://github.com/solo-io/squash): Code debugging tool

### Cluster Administration Tools

* [kube-janitor](https://codeberg.org/hjacobs/kube-janitor): Clean up (delete) Kubernetes resources after a configured TTL (time to live)
* [kube-shell](https://github.com/cloudnativelabs/kube-shell): An integrated shell for working with the Kubernetes CLI
* [kubespy](https://github.com/pulumi/kubespy): Tool for observing Kubernetes resources in real time
* [kube-ps1](https://github.com/jonmosco/kube-ps1): PS1 prompt to see the namespace and the current kubetcl context
* [kubetail](https://github.com/johanhaleby/kubetail): Easily tail pod logs
* [stern](https://github.com/wercker/stern): Easily tail pod logs
* [kubens](https://github.com/ahmetb/kubectx): Change kubernetes default namespace
* [kubectx](https://github.com/ahmetb/kubectx): Change kubectl contexts
* [krew](https://krew.sigs.k8s.io/): Kubectl plugin manager
* [clic](https://github.com/databricks/click): Command Line Interactive Controller for Kubernetes
* [kubed-sh](https://kubed.sh/): Lets you execute a program in a Kubernetes cluster without having to create a container image or learn new concepts
* [k2tf](https://github.com/sl1pm4t/k2tf): Kubernetes to Terraform converter

### Debugging Tools

* [crictl](https://github.com/kubernetes-sigs/cri-tools)

## Security Tools

### Secrets Management

* [sealed-secrets](https://github.com/bitnami-labs/sealed-secrets)
* [sops](https://github.com/mozilla/sops)
* [vault](https://www.vaultproject.io/)

### Source Code Scan

* [synk](https://snyk.io/)
* [aquasec](https://www.aquasec.com/)

### Static Code Analysis

* [sonarqube](https://www.sonarqube.org/)

## CI-CD

* [Spinnaker](https://spinnaker.io/)
* [Jenkins](https://www.jenkins.io/)
* [Jenkins X](https://jenkins-x.io/)
* [Tekton](https://tekton.dev/)
* [Travis CI](https://www.travis-ci.com/)
* [GiLab CI](https://docs.gitlab.com/ee/ci/)
* [Github Actions](https://docs.github.com/en/actions)
* [Bamboo](https://www.atlassian.com/software/bamboo)
* [Circle CI](https://circleci.com/)
* [Team City](https://www.jetbrains.com/teamcity/)
* [Drone](https://www.drone.io/)
* [Harness](https://harness.io/)
* [Codefresh](https://codefresh.io/)

## GitOps Tools

* [Argo CD](https://github.com/argoproj/argo-cd)
  * [Argo Rollouts](https://github.com/argoproj/argo-rollouts)
  * [Argo Events](https://github.com/argoproj/argo-events)
* [Flux](https://fluxcd.io/)
  * https://www.weave.works/oss/flux/
* [GitKube](https://gitkube.sh/)
* [Flagger](https://flagger.app/)

## Plataform as a Service

* Digital Ocean
* Heroku
* [Dokku](http://dokku.viewdocs.io/dokku/)
* Linode
* Cloud Foundry
* Pivotal

## Infraestructure as a Service

* CloudFoundry
* Digital Ocean
* OpenStack
* AWS
* Azure
* GCE

## Infraestructure as a Code

* [Terraform](https://www.terraform.io/)
* [Vagrant](https://www.vagrantup.com/)
* [Packer](https://www.packer.io/)
* [Ansible](https://www.ansible.com/)
* [Ansible Tower](https://www.ansible.com/products/tower)
* [AWX](https://github.com/ansible/awx)
* [Puppet](https://puppet.com/)
* [Chef](https://www.chef.io/)
* [Salt](https://saltproject.io/)

## Infrastructure as Software

* [Pulumi](https://www.pulumi.com/)
* [Amazon CDK](https://aws.amazon.com/cdk/)
* [cdk8s](https://cdk8s.io/)
* [terraform-cdk](https://github.com/hashicorp/terraform-cdk)

## Certificates and Key Management

* [Vault](https://www.vaultproject.io/)
* DIY encryption
* [Spiffe](https://spiffe.io/)
* [cfssl](https://github.com/cloudflare/cfssl)
* [step tools](https://smallstep.com/)
  * [step-ca](https://github.com/smallstep/certificates)
  * [step-cli](https://github.com/smallstep/cli)
* [ssh-key-authority](https://github.com/operasoftware/ssh-key-authority)
* [Syspass](http://syspass.org/en)

## IAM

* [Keycloak](https://www.keycloak.org/)
* [dex](https://dexidp.io/)
* Free IPA
* WsO2 IAM

## Load Balancers, Proxies, Service Meshes and Service Discovery

### Load Balancers and Proxies

* [Envoy Proxy](https://www.envoyproxy.io/)
* [HAProxy](http://www.haproxy.org/)
* [Nginx](https://www.nginx.com/)
* [Traefik](https://traefik.io/)

### Service Discovery and DNS Tools

* [Consul](https://www.consul.io/)
* [Apache Zookeeper](https://zookeeper.apache.org/)
* [CoreDNS](https://coredns.io/)
* [nip.io](https://nip.io/)

### Service Meshes

[smi-spec](https://smi-spec.io/)

* [Istio](https://istio.io/)
* [Linkerd](https://linkerd.io/)
* [Consul Connect](https://www.consul.io/docs/connect)
* [Nginx Service Mesh](https://www.nginx.com/products/nginx-service-mesh/)

## Monitoring

* [Prometheus](https://prometheus.io/)
* [Cortex](https://cortexmetrics.io/)
* [Thanos](https://thanos.io/)
* [cAdvisor](https://github.com/google/cadvisor)
* Sysdig
* Loggly
* New Relic
* [Datadog](https://www.datadoghq.com/)
* App Dynamics

## Logging and Tracing

* [Zipkin](https://zipkin.io/)
* [Jaeger](https://www.jaegertracing.io/)
* [OpenTracing](https://opentracing.io/)
* [ELK](https://www.elastic.co/what-is/elk-stack)
* [Fluentd](https://www.fluentd.org/)
* [Logplex](https://devcenter.heroku.com/articles/logplex)
* [Splunk](https://www.splunk.com/)
* [Scribe](https://github.com/outr/scribe)

## Data visualization

* [Kibana](https://www.elastic.co/kibana/)
* [Grafana](https://grafana.com/)
* [Graylog](https://www.graylog.org/)

## Distribute Storage Systems

* [Rook](https://rook.io/)
* [Gluster](https://www.gluster.org/)
* [Ceph](https://ceph.io/en/discover/technology/)
* [OpenEBS](https://openebs.io/)

## Databases and Cache

* NoSQL (Key-Value)
  * Etcd
  * MongoDB
  * CockroachDB
  * Elasticsearch
  * Apache Cassandra
  * CoudchDB
  * etcd
  * RocksDB
  * Memcached
  * Redis
* SQL
  * Mysql
  * Postgres
  * Yugabyte
  * Apache ignite
  * NuoDB
  * CreateDB

## Content Management System

* WordPress
* Drupal
* BonitaSoft

## Messaging and Queuing Systems

* RabbitMQ
* Apache Kafka
* Beanstalkd

## Testing Tools

### HTTP Load and Stress Testing

* Siege: Siege is an open source regression test and benchmark utility: https://www.joedog.org/siege-home/
* Apache Bench
* Apache JMeter

### Chaos Engineering

* [Chaos Monkey](https://netflix.github.io/chaosmonkey/)
* [chaoskube](https://github.com/linki/chaoskube)
* [kube-monkey](https://github.com/asobti/kube-monkey)
* [PowerfulSeal](https://github.com/powerfulseal/powerfulseal)

## Interesting Links

* [Netflix OSS](https://netflix.github.io/)
* [Netflix Tech Blog](https://netflixtechblog.com/)
* [Airbnb Engineering](https://medium.com/airbnb-engineering)
* [Pinterest Engineering](https://medium.com/@Pinterest_Engineering)
* [CDF Presentations](https://github.com/cdfoundation/presentations)
* [Twelve Factor](https://12factor.net/)
* [Open Containers](https://www.opencontainers.org/)
* [Open Containers - Runtime Spec](https://github.com/opencontainers/runtime-spec)
* [CNCF Landscape](https://landscape.cncf.io/)