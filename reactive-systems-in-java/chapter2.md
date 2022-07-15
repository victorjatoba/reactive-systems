# Summary of Chapter 2

- Quarkus is a kubernetes-native Java stack.
- Java is unable to see the amount of memory allocated to a container, could only see the memory of the entire physical machine.
- Resident Set Size (RSS) represents the amount of memory that a process is ocupying from RAM.
- Container density is a key characteristic of cloud deployments with Kubernetes
- Quarkus Apps are designed to run efficiently in containers and have built-in health checks and monitoring
- Containerization mechanisms: Docker, Jib and Source-to-Image (S2I)
- At Jib, dependencies are cached in a layer separate from the app, making subsequent container builds much faster.

## Kubernetes
- To create pods, we need a deployment
  - Indicate which containers need to run in the pod
  - indicate the number of instances of the pod
  - What you need
    1. A container image accessible to your k8s cluster
    2. A YAML file

### To build and deploy Quarkus Apps

- docker installed
- To expose the Docker daemon from minikube to the local terminal environment: `eval $(minikube -p minikube docker-env)`
- `mvn verify -D quarkus.kubernetes.deploy=true`

### Service

- Is a channel of communication delegating to a set of pods
- This service delegates the port 8080 on pods with matching labels (app.kubernetes.io/name and app.kubernetes.io/version)
- How to know the service URL: `minikube service code-with-quarkus --url`

### Check Pod's memory

- `kubectl top pods`

## Go Native

- GraalVM generates native application from Java code
- GraalVM puts static initialization in build process
