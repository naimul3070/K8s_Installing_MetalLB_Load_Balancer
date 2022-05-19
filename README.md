# K8s_Installing_MetalLB_Load_Balancer
## About Load Balancers
#### Load balancers can be used for exposing applications to the external network. Load balancer provides a single IP address to route incoming requests to your app. In order to successfully create Kubernetes services of type LoadBalancer, you need to have the load balancer (implementation) available for Kubernetes.

## Install MetalLB

    kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.10.2/manifests/namespace.yaml
    
    
## Create ConfigMap for MetalLB

#### Create a YAML file accordingly, and deploy it: kubectl apply -f metallb-configmap.yaml

    
    apiVersion: v1
    kind: ConfigMap
    metadata:
      namespace: metallb-system
      name: config
    data:
      config: |
        address-pools:
        - name: default
          protocol: layer2
          addresses:
          - <ip-address-range-start>-<ip-address-range-stop>
          
 ## You can assing single ip or can assign ar ipm range
