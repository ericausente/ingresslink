# ingresslink
Lab Repro 

The repo describes the BIG IP deployed for load balancing to the Kubernetes clusters and NGINX Ingress Controller handling ingress traffic. 

This is done via an IngressLink Solution where a Container Ingress Services (CIS) is enabled to notify BIG-IP when the set of - NGINX Ingress Controller pods has changed. This enables BIG‑IP to shift its corresponding load‑balancing policies to match.

The Ingress controller will bridge between the internal network, which connects the containerized app running within the Kubernetes cluster, and the external network outside the Kubernetes cluster, exposed as a NodePort Service and subsequently as pool members in F5.  Ingress controllers are used to configure and manage external interactions with Kubernetes pods that are labelled to a specific service. Ingress controllers is where the TLS termination, handling multiple domains and namespaces, and of course, load balancing traffic.

