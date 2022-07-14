# Summary of Chapter 2

- Quarkus is a kubernetes-native Java stack.
- Java is unable to see the amount of memory allocated to a container, could only see the memory of the entire physical machine.
- Resident Set Size (RSS) represents the amount of memory that a process is ccupying from RAM.
- Container density is a key characteristic of cloud deployments with Kubernetes
- Quarkus Apps are designed to run efficiently in containers and have built-in health checks and monitoring
- Containerization mechanisms: Docker, Jib and Source-to-Image (S2I)
- At Jib, dependencies are cached in a layer separate from the app, making subsequent container builds much faster.
