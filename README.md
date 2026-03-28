https://github.com/260925578/assignment-1-FortunateAneliswaMajozi.git

Purpose
Deploy a lightweight Kubernetes cluster (k3s) on AWS, document the deployment, demonstrate evidence, and reflect on the work. This develops technical, problem-solving, documentation, and professional skills.

student number: 260925578
name(s): Fortunate Aneliswa
surname: Majozi
            
## System requirements
| Requirement | Master |
| :--- | :--- |
| **Instance type** | t3.large|
| **CPU** | vCPUs(2)|
| **Disk** | 50Gb |
| **RAM** |7.6Gi |
| **OS** | Ubuntu 22.04 LTS |
ARCHITECTURE EXPLANATION
# What is K3s?
K3s is designed for resource-constrained situations. K3s is a lightweight, fully compliant Kubernetes distribution. It is simple to install, run and manage because it bundles all necessary Kubernetes components into a single binary.
K3s is employed due to the following reasons
•	It uses less memory and CPU than complete Kubernetes.
•	is easy to customize and quick to install.
•	is perfect for development environments, IoT, and edge computing.
•	simplifies Kubernetes while preserving its essential features

Because of this, K3s is appropriate for cloud deployments (such as AWS EC2) and edge situations where speed and efficiency are crucial.

KEY COMPONENTS
The control plane is the brain of the Kubernetes cluster. In K3s, it is simplified and runs as a single service. IT is responsible for handling pods.
Agent nodes are where application workloads run. They  receive instructions from the control plane and run pods.
The container runtime is responsible for running containers.
The CNI provides networking between pods and services inside the cluster. K3s uses flannel, which enables pod-to-pod communication and IP address allocation for pods. 
Ingress and load balancing manage external access to applications. They route external traffic to the correct services and enable exposure of the application to the internet. 
Storage in k3s uses supports persistent volumes and persistent volume claims, which allows applications to store data reliably even if containers restart.

## Instances

![Instance](screenshots/aneliswa-instances.png)

## Nodes

![Nodes](screenshots/aneliswa-nodes-master1.png)

![Nodes](screenshots/aneliswa-nodes-master2.png)

![Nodes](screenshots/aneliswa-nodesmaster3.png)

# PODS

![Pods](screenshots/aneliswa-pods-master1.png)

![Pods](screenshots/aneliswa-pods-master2.png)

![Pods](screenshots/aneliswa-pods-master3.png)

# Deployment

![Deployment](screenshots/aneliswa_agent_deployment.PNG)

## TECHNICAL REFLECTION
# What did i learn?
This project provided comprehensive, hands-on experience in deploying a Kubernetes cluster using K3s on Amazon Web Services (AWS) EC2 instances, bridging the gap between theoretical knowledge and practical application.
Throughout this process, I learned how to configure cloud infrastructure from the ground up, including the provisioning of virtual machines, managing Virtual Private Cloud (VPC) settings, and implementing robust networking rules. 
Understanding how cluster nodes communicate using private IP addresses and the critical role of security groups in acting as a virtual firewall was particularly important for ensuring a secure and functional deployment.

# Challenges i faced and how i solved them
One of the main challenges encountered was persistent node connectivity issues, specifically when attempting to join additional master nodes to the initial control plane.
Errors such as “connection refused” and token mismatches frequently disrupted the setup, highlighting the importance of meticulous configuration and the necessity of thorough cleanup after previous installation attempts.
These issues were resolved by systematically resetting the nodes to a clean state, carefully verifying the accuracy of the cluster join tokens, and meticulously configuring AWS security groups to allow traffic on the essential port 6443, which is used for the Kubernetes API server. This troubleshooting process reinforced the value of methodical debugging in distributed systems.

# How k3s relates to production kubernetes/5G cloud-native concept
K3s relates closely to production Kubernetes environments, particularly in emerging fields such as edge computing and 5G cloud-native architectures. 
It provides a simplified yet remarkably powerful platform for running containerized workloads, which is essential for modern distributed systems. 
In the context of 5G networks, lightweight Kubernetes distributions like K3s are increasingly used to deploy network functions and services closer to end-users, significantly reducing latency and improving overall application performance.

# How virtualization and containerization enable scalable services
Virtualization and containerization play a foundational role in enabling these scalable services. 
Virtual machines provide isolated, secure environments for running entire clusters, while containers allow applications to be packaged with their exact dependencies, ensuring consistency across development and production environments. 
This powerful combination ensures portability, seamless scalability, and efficient resource utilization across diverse cloud environments. 
Overall, this project significantly enhanced my understanding of cloud-native technologies, Kubernetes architecture, and the real-world challenges involved in deploying and managing resilient distributed systems.
 
