Chapter 12, *Serverless Computing on Kubernetes*

### **Understanding Serverless Computing**
Serverless computing allows developers to focus on writing code without worrying about infrastructure provisioning, scaling, or maintenance. The term "serverless" is a bit misleading because servers are still involved; however, their management is abstracted away from the user. The serverless model removes the need for capacity planning and infrastructure management, providing resources as needed and billing only for usage【6†source】.

### **Running Long-Running Services on Serverless Infrastructure**
Long-running services, the backbone of distributed systems, can benefit from a serverless model. Serverless Kubernetes services can run continuously and scale up or down based on demand. They maintain state, handle connections, and expose endpoints like HTTP or gRPC. These services are always running and are ideal for environments that handle fluctuating traffic【6†source】.

### **Running Functions as a Service (FaaS) on Serverless Infrastructure**
FaaS allows code to run in response to specific events. This model is useful for workloads that don't need constant uptime, as the system scales functions down to zero when they're idle. FaaS minimizes resource consumption by automatically scaling functions based on demand. It exposes a single endpoint and can trigger based on events such as HTTP requests or scheduled jobs.

### **Serverless Kubernetes in the Cloud**
Cloud providers like **Azure AKS**, **AWS EKS with Fargate**, and **Google Cloud Run** provide serverless solutions for Kubernetes:
- **Azure AKS**: Offers Azure Container Instances (ACI) to run serverless containers in an isolated environment.
- **AWS EKS and Fargate**: Fargate allows Kubernetes workloads to run in isolated, lightweight virtual machines without provisioning servers.
- **Google Cloud Run**: Based on Knative, Google Cloud Run offers serverless containers that scale down to zero.

### **Knative**
**Knative** provides a foundation for serverless workloads on Kubernetes. It supports both long-running services and functions. Key features include automatic scaling to zero, advanced routing (like blue-green and canary deployments), load balancing, and certificate management. Knative integrates with both HTTP and gRPC, and it is built around two primary components:
- **Knative Serving**: Manages versioned services and routes traffic based on various factors.
- **Knative Eventing**: Connects event producers to services and functions, enabling event-driven workloads.

### **Kubernetes Function-as-a-Service (FaaS) Frameworks**
Several FaaS frameworks are available for Kubernetes:
- **OpenFaaS**: A popular framework with extensive community support. OpenFaaS provides autoscaling and integrates with Prometheus for metrics.
- **Fission**: Focuses on speed, offering cold start times as low as 100 milliseconds. It uses executors like **PoolManager** and **NewDeploy** for function execution, supporting triggers like HTTP requests, message queues, and Kubernetes events.

### **Summary**
Serverless computing on Kubernetes simplifies infrastructure management, allowing teams to run both long-running services and event-driven functions efficiently. The key technologies like Knative and frameworks such as OpenFaaS and Fission provide flexibility in managing serverless workloads. These serverless solutions bring cost efficiency, reduced operational overhead, and dynamic scalability to Kubernetes environments.