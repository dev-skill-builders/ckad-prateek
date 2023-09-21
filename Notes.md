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
