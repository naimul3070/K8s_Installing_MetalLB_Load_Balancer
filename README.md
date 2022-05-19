# K8s_Installing_MetalLB_Load_Balancer
## About Load Balancers
#### Load balancers can be used for exposing applications to the external network. Load balancer provides a single IP address to route incoming requests to your app. In order to successfully create Kubernetes services of type LoadBalancer, you need to have the load balancer (implementation) available for Kubernetes.

## Install MetalLB

  kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.10.2/manifests/namespace.yaml
