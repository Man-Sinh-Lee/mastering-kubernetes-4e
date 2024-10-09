Chapter 1, "Understanding Kubernetes Architecture" from *Mastering Kubernetes, Fourth Edition*:

### **What is Kubernetes?**
Kubernetes is an open-source platform designed for automating deployment, scaling, and management of containerized applications. Its core functionalities include scheduling containerized workloads across infrastructure, handling application health, replicating instances, and scaling resources. Kubernetes is highly extensible and integrates seamlessly with cloud providers, but it's not a Platform as a Service (PaaS).

### **What Kubernetes is not**
Kubernetes does not provide:
- A predefined application framework
- Built-in databases or message queues
- Click-to-deploy services
- A CI/CD pipeline
- A built-in function as a service (FaaS) solution

### **Understanding Container Orchestration**
Kubernetes orchestrates containers across physical or virtual machines, efficiently allocating resources and replacing failed containers. It supports various infrastructures:
- **Physical Machines**: Real hardware with compute and storage resources.
- **Virtual Machines**: Virtual environments hosted on physical machines.
- **Containers**: Lightweight environments, encapsulating applications, offering portability and consistency across different environments.
- **Cattle vs. Pets**: In large systems, Kubernetes treats nodes as "cattle" (interchangeable units) rather than "pets" (unique, irreplaceable servers), allowing for scalable management.

### **Kubernetes Concepts**
- **Node**: A host (physical or virtual) that runs containers managed by Kubernetes.
- **Cluster**: A group of nodes running applications.
- **Control Plane**: The central management system (API server, scheduler, controller manager) that orchestrates workloads and maintains the global state.
- **Pod**: The smallest deployable unit containing one or more containers.
- **Labels & Selectors**: Mechanisms for organizing resources and selecting them based on certain attributes.
- **Service**: A way to expose an application running on a set of Pods as a network service.
- **Volume**: A way for containers in Pods to share data.
- **Replication Controller/Replica Set**: Tools that ensure a specific number of replicas of Pods are running.
- **StatefulSet**: Manages stateful applications, ensuring that Pods are created in a specific order.
- **Namespace**: Provides scope for names, allowing multiple virtual clusters within a physical cluster.

### **Distributed Systems Design Patterns**
- **Sidecar Pattern**: A helper container that runs alongside the primary application container.
- **Ambassador Pattern**: Manages interactions between services, acting as a proxy.
- **Adapter Pattern**: Adapts external systems to the Kubernetes environment.
- **Level-triggered Infrastructure and Reconciliation**: Kubernetes constantly observes the desired state and takes actions to reconcile any discrepancies.

### **Kubernetes APIs**
The Kubernetes API is organized into multiple categories based on resource types, enabling efficient management of workloads and infrastructure. 

### **Kubernetes Components**
- **Control Plane Components**:
  - **API Server**: Handles communication and provides the interface to the cluster.
  - **etcd**: The key-value store for cluster data.
  - **Kube Controller Manager**: Manages controllers (replication, node management, etc.).
  - **Cloud Controller Manager**: Handles cloud-specific integration.
  - **Kube Scheduler**: Assigns Pods to nodes.
- **Node Components**:
  - **Kubelet**: Ensures that containers in Pods are running.
  - **Kube Proxy**: Handles networking for services.
  - **DNS**: Cluster DNS for service discovery.

### **Kubernetes Container Runtimes**
- **Container Runtime Interface (CRI)**: Kubernetes abstracts the container runtime, allowing it to support various runtimes.
- **Docker, containerd, CRI-O**: Common runtimes for running containers.
- **Lightweight VMs**: Options for container runtimes that provide a higher level of isolation.

These concepts form the foundation for understanding Kubernetes’ design and operation.