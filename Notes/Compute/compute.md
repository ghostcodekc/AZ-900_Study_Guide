## **Table of Contents**
- [**Table of Contents**](#table-of-contents)
- [**Introduction**](#introduction)
- [**Helpful Links**](#helpful-links)
- [**IaaS Compute Services**](#iaas-compute-services)
  - [**Virtual Machines**](#virtual-machines)
  - [**Scale Sets**](#scale-sets)
- [**PaaS Compute Services**](#paas-compute-services)
  - [**App Services**](#app-services)
  - [**Azure Container Instances**](#azure-container-instances)
  - [**Azure Kubernetes Service**](#azure-kubernetes-service)
  - [**Windows Virtual Desktop**](#windows-virtual-desktop)
- [Serverless](#serverless)
  - [**Azure Functions**](#azure-functions)

## **Introduction**

- Virtual Machines - Most common referenced service in the cloud.
- Scale Sets - Super user case of using VM's.
- App Services - Versitile multi-purpose services.
- Azure Container Instances - Containers.
- Azure Kubernetes Services - Azures offering 
- Windows Virtual Desktop - VDI
- Azure Functions - Cloud FaaS

---

## **Helpful Links**

- [Azure Compute Hands-On Labs](https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/)

---

## **IaaS Compute Services**
- Infrastructure-as-a-service
  
### **Virtual Machines**

[Azure Reference Documentation](https://docs.microsoft.com/learn/modules/intro-to-azure-compute/3-virtual-machines)

- You manage everything except the hardware. This includes networking components.
- Pricing for VMs are calculated hourly.
- A virtual machines is your machine exclusively. 
- You don't buy, own, or control any hardware. Azure does this.
- Virtual machines are an IaaS offering, where you are responsible for the entire machine.
- Azure virtual machines take advantage of Azure tools.
- Pricing goes up as resources go up, and you pay by the hour.

### **Scale Sets**
[Azure Reference Documentation](https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/overview)
- A group of identical load balanced VMs.
  - Identical is key. 
  - You provide a single VM as a baseline for your scale set. 
  - You can create VM's from that instantly.
- Allows to scale up and down based on resource utilization.
- You can schedule the scaling if you know the load of your application.
- Using a scale set allows your Azure infrastructure to work with a load balancer effectively.
- If one VM fails or stops the others in the scale set will keep working.
- You can run up to 1000 VMs in a single scale set. 
- There is no extra cost for using Azure Scale Sets. You only pay for the VM, storage, and networking resources you use.

---

## **PaaS Compute Services**
### **App Services**
[Azure App Services Documentation](https://docs.microsoft.com/learn/modules/intro-to-azure-compute/5-appservice)

- Fully managed platform.
  - Servers, network, storage is all managed by Azure. 
- App services is an easy way to host and manage your web application.
- Web Apps are used to host websites and web apps.
- Web Apps for Containers can host your existing container images.
- API apps can host your data backend services.
- An app service is always created within an App Service Plan.
  - App service plan pricing tier determines the location, features, cost, and compute resources associated with your app.
- App Services come in 3 main categories:
  1. Web Apps
      - Runs on both Windows and Linux
      - Supports a wide variety of languages such as .NET, Java, Node.js, PHP, Python, and Ruby.
      - Azure integration for easier deployment.
      - App Services support load balancing. 
  2. Web Apps for Containers
      - Lets you run and deploy containerized applications in Azure.
      - All dependencies are shipped inside the container.
      - You can deploy anywhere with a consistent experience.
      - Allow software to run reliably between environments.
  3. API Apps
     - Efficient way to connect and expose any data backend you have.
       - API = Application programming interface.
     - No GUI
     - Connect other applications programmatically.

### **Azure Container Instances**
[Azure Container Instance Documentation](https://docs.microsoft.com/en-us/azure/container-instances/container-instances-overview)

- Azure Container Instances allow you to run Docker containers on-demand in a managed, serverless Azure environment. 
- Can be used for any scenario that can operate in isolated containers, without orchestration. 
- Allows you to run event-driven applications, quickly deploy from your container development pipelines, and run data processing and build jobs.
- Azure Container Instances offers the fastest and simplest way to run a container in Azure, without having to manage any virtual machines and without having to adopt a higher-level service.
- Priced on a per-second basis. 

### **Azure Kubernetes Service**
[Azure Kubernetes Service Documentation](https://docs.microsoft.com/en-us/azure/aks/intro-kubernetes)

- Azure Kubernetes Service (AKS) simplifies deploying a managed Kubernetes cluster in Azure by offloading the operational overhead to Azure.
- Kubernetes abbreviation: K8s
- Kubernetes is an open-source container orchestration system for automating application development, scaling, and management.
  - Open Source: Public code base.
  - Orchestration: Keeps track of lots of parts of a system to make sure containers are configured correctly to work together.
  - Automatic application deployment: K8s will deploy more images of containers when needed.
  - Automatic Scaling: K8s monitors the application load to determine when to scale the number of containers used.
- K8s allows you to replicate container architectures.
- Standard Azure services are included. 
  - You get identity and access management (IAM), Elastic provisioning (scaling up and down), integration with VSCode, and much more.
- Using Azure Kubernetes Service you get global reach.
  - You can use K8s with supported Azure regions and on-premises installations using Azure Stack.
- Container images are stored in Azure Container Registry (ACR)
  - Keeps track of current valid container images.
  - Manages files and artifacts for containers.
  - Feeds container images to Azure Container Instances (ACI) and Azure Container Service (AKS)
  - You can use Azure identity and security to ensure that the container images are safe.

### **Windows Virtual Desktop**
[Windows Virtual Desktop Documentation](https://docs.microsoft.com/en-us/azure/virtual-desktop/overview)

- Azure Virtual Desktop is a desktop and app virtualization service that runs on the cloud.
- You can use any VM and size you want.
- Once deployed you can access it from any device with internet and a modern browser.
- Completely virtualized version of Windows meaning it runs 100% in the cloud.
- You can reuse Windows 10 licenses.
- Multiple users can use the same VM instance.
- You can use Azure Storage to secure your data.
- Windows Virtual Desktop integrates with existing Azure security features and user authentication services.
  - This includes MFA, role based access control, Azure policies, and more.
  
## Serverless
### **Azure Functions**
[Azure Functions Documentation](https://docs.microsoft.com/en-us/azure/azure-functions/)

- Smallest compute service on Azure
- A single function of compute.
- Called or invoked via a standard web address (URL)
- Runs once and stops.
- Functions still run on a VM.
  - No maintenance
  - No processes
  - Nothing VM related.
  - No access to Operating System or resources.
- Only runs when needed. 
- It can save money.
  - If there is no traffic there is no resource usage.
- Functions are resilient.
  - If your function fails, it doesn't affect other function instances.
- 