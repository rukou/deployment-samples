This configuration describes the following GKE setup:

* 3 Edge Layer pods
* loadbalancer in front
* global IP to support multi region deployments
* SSL certificates

### Instructions

Provision a global IP:

    gcloud compute addresses create rukou-ip --global

Create the certificate:

    kubectl apply -f certificate.yml

Create the deployment:

    kubectl apply -f deployment.yml

Create the service:

    kubectl apply -f service.yml

Create the ingress:
    
    kubectl apply -f ingress.yml
