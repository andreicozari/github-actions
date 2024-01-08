# Welcome to Docker

This is a repo for new users getting started with Docker.

You can try it out using the following command.
```
docker run -d -p 8088:80 --name welcome-to-docker docker/welcome-to-docker
```
And open `http://localhost:8088` in your browser.

# Building

Maintainers should see [MAINTAINERS.md](MAINTAINERS.md).

Build and run:
```
docker build -t welcome-to-docker . 
docker run -d -p 8088:3000 --name welcome-to-docker welcome-to-docker
```
Open `http://localhost:8088` in your browser.


K8s:
kubectl apply -f welcome-to-k8s.yaml
kubectl get pods
kubectl logs pod-name
kubectl describe pod welcome-to-docker-6f468f6cc7-5xnq
kubectl scale deployment hi-k8s --replicas=0

kubectl apply -f .\first-k8s-service.yaml
kubectl get svc nodejs-service

http://10.107.95.178:80

kubectl delete service nodejs-service

see all service:
kubectl get svc

kubectl port-forward pod/nodeapp-deployment-8677777c6b-8j7jg 8080:80

Kubernetes is a popular container orchestration platform for deploying and managing containerized applications. When you deploy a containerized application to a Kubernetes cluster, it runs inside a Pod. By default, Pods are not exposed to the public internet. If you want to make the application running inside the Pod accessible from outside the Kubernetes cluster, you need to create a Service object.

However, there are scenarios where you might not want to expose your application to the external world using a Service for security reasons. For example, when you want to do some debugging or test the application locally. This is where "kubectl port-forward" comes into the picture.