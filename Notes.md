## K8s Architecture
### Nodes (Minions)
 - Is a machine _(physical or virtual)_ on which K8s is installed.
 - Nodes are mainly worker machines where conainers will be running.
 - Master node is the one which manages other nodes and **responsible for actual orchestration** of containers in worker nodes.
 - Master Vs Worker nodes:
   - Master has KubeAPI server , worker nodes have kubelet agent **which is resposible to interact with master node about healthcheck etc.
   - All info gathered in stored in etcd store **present on Master node**
   - Other components like controller, scheduler etc can only be on master node.
  - Worker node
      - Has (1) Kubelet and (2) Container runtime
     
   
### Cluster
 - Set of Nodes grouped Together.

### API Server
 - Front face of K8s.
 - All users, management devices, CLIs talk to API Server to interact with K8s Cluster.
   
### Etcd 
 - Distributed, Reliable Key value store.
 - Stores all data required to manage cluster.
 - If more than one nodes or master in cluster, etcd stores all this info on **all the nodes**
 - Implements locks wothin the cluster to ensure no conflicts b/w masters.
 - etcdctl is the CLI tool to interact with etcd
 - [TO DO]: Leader Election in K8s and etcd too , etcd election time
 - [TO DO]: Hands on etcdctl

### Scheduler
 - Responsible for distributing work or containers across multiple nodes.
 - Looks for newly created containers and assigns them to nodes.

### Controllers
 - Is the brain behind Orchestration.
 - Notices and Responds if nodes,containers, endpoints goes down.
 - Takes decision whether to bring up a new container if prev container goes down.
 - 

### Container Runtime
 - Underlying S/w used to run containers
 - Like Podman, Docker etc

### Kubelet
 - Agent that runs on **each node**
 - Resposible for ensuring the containers are running on nodes as expected. 

## Kubectl tool
Tool required to deploy and manage applications on K8s cluster.
 - `kubeclt cluster-info`
 - `kubectl run <image-name>`

## Ingress
 - Ingress is part of Kubernetes networking and can be understood in two parts - 1) Ingress Controller 2) Ingress rules
 - Ingress is an API object that provides external access to the services within K8s Cluster.
 - Ingress provides the routing rules to http and https traffic to various services based on hostname and path.
   This way it allows us to expose multiple services to the external world using single IP address and Port.
 - Ingress resources are used to configure the rules for how traffic should be flowing to respective backend services.

 - Ingress Controllers are not present in Kubernetes by default.
 - Ingress Controllers can be HAProxy, NGINX, TRAEFIK


## Sample Ingress Yaml

## Pros of using Ingress

## Cons of having Ingress

## Which Scenarios should one go for Ingress
 - **_Web Application Hosting_**:
   * Ingress is commonly used for hosting web applications with multiple services, such as frontend and backend services, behind a single public IP address.
 - **_API Gateway_**: It can serve as an API gateway, routing requests to different backend APIs based on paths or hostnames.
 - **_TLS Termination_**: When you need to terminate TLS encryption for external traffic before reaching your services.
> Note: Above three are copied ones, need to provide more information here soon.

## Commonly asked questions

## Challenges with Ingress

## Diagrams/Pictures for reference

## Comments/Notes
