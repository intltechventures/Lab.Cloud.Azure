Lab.Cloud.Azure
====
Microsoft Azure Resources


### References
* https://azure.microsoft.com/en-us/status/
* Azure products available by region
  * https://azure.microsoft.com/en-us/global-infrastructure/services/

### Pricing Information
* https://azure.microsoft.com/en-us/pricing/calculator/
* https://azure.microsoft.com/en-us/offers/pay-as-you-go/

  
### Documentation
* https://docs.microsoft.com/en-us/azure/
* https://azure.microsoft.com/en-us/campaigns/developer-guide/
* https://docs.microsoft.com/en-us/azure/
* Hybrid Connectivity Gateway
  * https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-gateway-install
  * https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-gateway-install#gateway-cloud-service
* https://github.com/MicrosoftDocs/azure-docs

  
### News
* https://azure.microsoft.com/en-us/blog/
  * https://azure.microsoft.com/en-us/blog/archives/
* http://www.azpodcast.com/


### Storage
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/managed-disks-overview
  * https://docs.microsoft.com/en-us/azure/virtual-machines/linux/premium-storage
  * https://docs.microsoft.com/en-us/azure/virtual-machines/linux/disks-standard-ssd
  * https://docs.microsoft.com/en-us/azure/virtual-machines/linux/disks-ultra-ssd


### Sizes for Linux virtual machines in Azure
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/sizes
  * https://docs.microsoft.com/en-us/azure/virtual-machines/linux/managed-disks-overview
  * https://docs.microsoft.com/en-us/azure/virtual-machines/linux/sizes-general
  * https://docs.microsoft.com/en-us/azure/virtual-machines/linux/sizes-compute
  * https://docs.microsoft.com/en-us/azure/virtual-machines/linux/sizes-memory
  * https://docs.microsoft.com/en-us/azure/virtual-machines/linux/sizes-hpc



### Low Priority VMs
* https://azure.microsoft.com/en-us/updates/public-preview-low-priority-vms-on-vm-scale-sets/
* https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-use-low-priority
  * "The amount of available unutilized capacity can vary based on size, region, time of day, and more. When deploying low-priority VMs on scale sets, Azure will allocate the VMs if there is capacity available, but there is no SLA for these VMs. A low-priority scale set is deployed in a single fault domain and offers no high availability guarantees."
* https://azure.microsoft.com/en-us/blog/low-priority-scale-sets/
  * "Low-priority VMs are available through VM scale sets with up to an 80 percent discount."
  * "Low-priority VMs enable you to take advantage of our unutilized capacity. The amount of available unutilized capacity can vary based on size, region, time of day, and more. When deploying Low-priority VMs in VM scale sets, Azure will allocate the VMs if there is capacity available, but there are no SLA guarantees. At any point in time when Azure needs the capacity back, we will evict low-priority VMs"
  * "viction Policy: When provisioning low-priority VMs, you can set the eviction policy. The two evictions policies that are supported are stop-deallocate on eviction and deleted on eviction. Stop-deallocate on eviction allows users to maintain the disks associated with these VMs. Users can try to restart the low priority in the scale set but remember, there are no allocation guarantees. The delete on eviction policy deletes the VM and all disks associated to the VM. "
* https://blogs.msdn.microsoft.com/uk_faculty_connection/2017/11/07/microsoft-azure-low-priority-virtual-machines-take-advantage-of-surplus-capacity-in-azure/
  * "In general, batch processing workloads are a good fit, as jobs are broken into many parallel tasks or there are many jobs that are scaled out and distributed across many VMs."
    * "Development and testing: In particular, if large-scale solutions are being developed, significant savings can be realized. All types of testing can benefit, but large-scale load testing and regression testing are great uses."
    * "Supplementing on-demand capacity: Low-priority VMs can be used to supplement regular dedicated VMs - when available, jobs can scale and therefore complete quicker for lower cost; when not available, the baseline of dedicated VMs remains available."
    * "Flexible job execution time: If there is flexibility in the time jobs have to complete, then potential drops in capacity can be tolerated; however, with the addition of low-priority VMs jobs frequently run faster and for a lower cost."
* https://docs.microsoft.com/en-us/azure/batch/batch-low-pri-vms



### Cloud Services
* https://docs.microsoft.com/en-us/azure/cloud-services/
  * https://docs.microsoft.com/en-us/azure/cloud-services/cloud-services-choose-me
* Training Vidoes 
  * https://azure.microsoft.com/en-us/resources/videos/index/?services=cloud-services
* .NET
  * https://docs.microsoft.com/en-us/azure/cloud-services/cloud-services-dotnet-get-started
* REST APIs
  * https://docs.microsoft.com/en-us/rest/api/compute/cloudservices/
  

### Azure Command Line Interface (CLI)
* https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest
* https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest
* https://docs.microsoft.com/en-us/cli/azure/release-notes-azure-cli?view=azure-cli-latest
* https://docs.microsoft.com/en-us/cli/azure/reference-index?view=azure-cli-latest


  
### Azure Cloud Shell 
* https://shell.azure.com
* https://docs.microsoft.com/en-us/azure/cloud-shell/overview
  * https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart
  * https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart-powershell
* https://docs.microsoft.com/en-us/azure/cloud-shell/features#tools


### PowerShellGallery
* [Azure Resource Manager Module](https://www.powershellgallery.com/packages/AzureRM/)


  
### Azure Container Registry (ACR)
* https://azure.microsoft.com/en-us/services/container-registry/
  * "Azure Container Registry allows you to store images for all types of container deployments including DC/OS, Docker Swarm, Kubernetes, and Azure services such as App Service, Batch, Service Fabric, and others. Your DevOps team can manage the configuration of apps isolated from the configuration of the hosting environment."
  * "You don’t have to learn new APIs or commands. Because Azure Container Registry is compatible with the open-source Docker Registry v2, you can use the same open-source Docker CLI tools you already know and the skills you have to efficiently interact with the registry."
* https://docs.microsoft.com/en-us/azure/container-registry/
* https://azure.microsoft.com/en-us/pricing/details/container-registry/
  * "Azure Container Registry provides storage of private Docker container images, enabling fast, scalable retrieval, and network-close deployment of container workloads on Azure. Additional capabilities include geo-replication, image signing with Docker Content Trust, Helm Chart Repositories and Task base compute for building, testing, patching container workloads."
* Github Resources
  * https://github.com/Azure/acr
    * https://github.com/Azure/acr/tree/master/docs
	  * https://github.com/Azure/acr/blob/master/docs/acr-roadmap.md

	
  
### Azure Resource Manager (ARM)
* https://docs.microsoft.com/en-us/azure/azure-resource-manager/
* https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview


### Azure Marketplace, Containers
* https://azuremarketplace.microsoft.com/en-us/marketplace/apps/category/containers?page=1
  * [Docker EE for Azure (Standard/Advanced)](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/docker.dockerdatacenter?tab=Overview)
  * [Docker on Ubuntu Server])(https://azuremarketplace.microsoft.com/en-us/marketplace/apps/CanonicalandMSOpenTech.DockerOnUbuntuServer1404LTS?tab=Overview)



### Azure Kubernetes Service (AKS)
* https://docs.microsoft.com/en-us/azure/aks/
* https://azure.microsoft.com/en-us/services/kubernetes-service/
* https://azure.microsoft.com/en-us/updates/?product=kubernetes-service
  * 2018
    * 2018-12-26 
	  * https://azure.microsoft.com/en-us/updates/azure-kubernetes-service-december-update/
	  * AKS Adoption of Moby as container runtime
	  * "With the exception of GPU-based VMs, all new AKS nodes are now provisioned with Moby as the container runtime, including new nodes in existing clusters added via the scale or upgrade commands."
	 * 2018-12-11
	   * https://azure.microsoft.com/en-us/updates/azure-monitor-for-containers-is-now-available/
	     * Azure Monitor for containers is now generally available
		 * "possible to get all the monitoring telemetry in a centralized location in Azure without having to sign into containers or rely on other tools. "
		 * "With live logs, you get a real time, live stream of your container logs directly in your Azure portal to help you interactively troubleshoot issues. "
* https://github.com/Azure/AKS
   https://github.com/Azure/AKS/blob/master/previews.md
* https://github.com/Azure/aks-engine/
  * https://github.com/Azure/aks-engine/blob/master/docs/README.md
  * https://github.com/Azure/aks-engine/blob/master/docs/tutorials/README.md
  * https://github.com/Azure/aks-engine/blob/master/docs/topics/README.md
  
  
  
  
### Application Insights
* Azure Monitor for Containers 
  * https://docs.microsoft.com/en-us/azure/azure-monitor/insights/container-insights-overview
  * Container Monitoring solution in Log Analytics
    * https://docs.microsoft.com/en-us/azure/azure-monitor/insights/containers
	  * "This article describes how to set up and use the Container Monitoring solution in Log Analytics, which helps you view and manage your ```Docker``` and Windows container hosts in a single location"
  
 
### Azure Templates
* https://azure.microsoft.com/en-us/resources/templates/
  * https://azure.microsoft.com/en-us/resources/templates/?term=docker&pageNumber=1 
    * https://azure.microsoft.com/en-us/resources/templates/docker-kibana-elasticsearch/
	* https://azure.microsoft.com/en-us/resources/templates/docker-swarm-cluster/
	* https://azure.microsoft.com/en-us/resources/templates/docker-rancher/
	* https://azure.microsoft.com/en-us/resources/templates/docker-neo4j/
	* https://azure.microsoft.com/en-us/resources/templates/docker-parse/
	* https://azure.microsoft.com/en-us/resources/templates/docker-wordpress-mysql/
	* https://azure.microsoft.com/en-us/resources/templates/docker-simple-on-ubuntu/
	* https://azure.microsoft.com/en-us/resources/templates/301-jenkins-aks-zero-downtime-deployment/
	* https://azure.microsoft.com/en-us/resources/templates/jenkins-cicd-container/

  
### Azure Container Services (Retires on 2020-01-31)
* [Azure Container Service Will Retire on January 31, 2020](https://azure.microsoft.com/en-us/updates/azure-container-service-will-retire-on-january-31-2020/)


### Azure Container Instances
* https://docs.microsoft.com/en-us/azure/container-instances/
  * "Certain features of Azure Container Instances are in preview, and some limitations apply." 
  "Azure Container Instances offers the fastest and simplest way to run a container in Azure, without having to provision any virtual machines and without having to adopt a higher-level service."
  * https://docs.microsoft.com/en-us/azure/container-instances/container-instances-quickstart
  * https://docs.microsoft.com/en-us/azure/container-instances/container-instances-quickstart-portal
  * https://docs.microsoft.com/en-us/azure/container-instances/container-instances-quickstart-powershell
  * https://docs.microsoft.com/en-us/learn/paths/administer-containers-in-azure/
	* Docker:
	  * https://docs.microsoft.com/en-us/learn/modules/run-docker-with-azure-container-instances/
  * https://docs.microsoft.com/en-us/dotnet/api/overview/azure/containerinstance?view=azure-dotnet
  * https://docs.microsoft.com/en-us/rest/api/container-instances/listcapabilities/listcapabilities
    * Example: ```GET https://management.azure.com/subscriptions/{subscriptionId}/providers/Microsoft.ContainerInstance/locations/{location}/capabilities?api-version=2018-10-01```
  * https://github.com/Azure/acs-engine
    * Azure Container Service Engine - provision and deploy container orchestrators on Azure: Kubernetes, DC/OS, and Docker Swarm. 
	* ```"This codebase has been deprecated in favor of aks-engine, the natural evolution from acs-engine"```
  * https://github.com/Azure/aks-engine
    * AKS-Engine: Units of Kubernetes on Azure! 
	* "AKS-Engine provides convenient tooling to quickly bootstrap Kubernetes clusters on Azure. By leveraging ARM (Azure Resource Manager), AKS-Engine helps you create, destroy and maintain clusters provisioned with basic IaaS resources in Azure. AKS-Engine is also the library used by AKS for performing these operations to provide managed service implementations."
	* https://github.com/Azure/aks-engine/blob/master/docs/README.md
  * Kubernetes Yaml File:
	* https://github.com/Microsoft/OMS-docker/tree/master/Kubernetes
    * https://github.com/Microsoft/OMS-docker/tree/master/Kubernetes/windows
  * Docker Monitoring Agent for OMI Server
    * https://github.com/microsoft/docker-provider/tree/ci_feature_prod
	* https://azure.microsoft.com/en-us/updates/ciagent12182018/
* Docker.com Resources
  * https://hub.docker.com/editions/enterprise/docker-ee-azure?tab=description
  * https://docs.docker.com/v17.09/docker-for-azure/
	* https://docs.docker.com/v17.09/docker-for-azure/faqs/
  * https://hub.docker.com/editions/enterprise/docker-ee-azure?tab=description
  * https://docs.docker.com/v17.09/docker-for-azure/faqs/
	* "Docker for Azure should work with all supported Azure Marketplace regions."
	* "All regions can be found here: Microsoft Azure Regions. An excerpt of the above regions to use when you create your service principal are:"
	  * "usgovvirginia"
	  * "usgoviowa"
  * [Microsoft Azure Channel, How to run an app inside a container image with Docker | Azure Tips and Tricks](https://www.youtube.com/watch?v=lpr2tO-FCEw)
* Visual Studio 2017 Support for Docker
  * [Using Visual Studio Tools for Docker (Visual Studio on Windows)](https://docs.microsoft.com/en-us/dotnet/standard/containerized-lifecycle-architecture/design-develop-containerized-apps/visual-studio-tools-for-docker?toc=/visualstudio/docker/toc.json&bc=/visualstudio/docker/breadcrumb/toc.json&view=vs-2017)
    * "The Visual Studio Tools for Docker development workflow is similar to the workflow when using Visual Studio Code and Docker CLI. In fact, it's based on the same Docker CLI, but it's easier to get started, simplifies the process, and provides greater productivity for the build, run, and compose tasks. Execute and debug your containers via simple actions like F5 and Ctrl+F5. With the optional container orchestration support, in addition to being able to run and debug a single container, you can run and debug a group of containers (a whole solution) at the same time."
	* "There are two levels of Docker support you can add to a project. In .NET Core web app projects, you can just add a Dockerfile file to the project by enabling Docker support. The next level is container orchestration support, which adds a Dockerfile to the project (if it doesn't already exist) and a docker-compose.yml file at the solution level. Container orchestration support, via Docker Compose, is added by default in Visual Studio 2017 versions 15.7 or earlier. Container orchestration support is an opt-in feature in Visual Studio 2017 versions 15.8 or later, in which case Docker Compose and Service Fabric are supported."
  * [Debugging apps in a local Docker container](https://docs.microsoft.com/en-us/visualstudio/docker/vs-azure-tools-docker-edit-and-refresh?view=vs-2017)
  
  
  
### Virtual Machines
* https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes
* https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/
  * https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/overview

  
### Azure Batch
* https://docs.microsoft.com/en-us/azure/batch/
  * https://docs.microsoft.com/en-us/azure/batch/batch-technical-overview

 
### Azure Application Service Environments (ASE)
* https://docs.microsoft.com/en-us/azure/app-service/environment/intro
  * "The Azure App Service Environment is an Azure App Service feature that provides a fully isolated and dedicated environment for securely running App Service apps at high scale."
  * "ASEs are isolated to running only a single customer's applications and are always deployed into a virtual network."
  * "Customers have fine-grained control over inbound and outbound application network traffic."
  * "Applications can establish high-speed secure connections over VPNs to on-premises corporate resources."
  * https://docs.microsoft.com/en-us/azure/app-service/environment/create-ilb-ase
	* "Azure App Service Environment is a deployment of Azure App Service into a subnet in an Azure virtual network (VNet). There are two ways to deploy an App Service Environment (ASE):"
	  * "With a VIP on an external IP address, often called an External ASE."
      * "With a VIP on an internal IP address, often called an ILB ASE because the internal endpoint is an internal load balancer (ILB)."
  * [Configuring a Web Application Firewall (WAF) for App Service Environment](https://docs.microsoft.com/en-us/azure/app-service/environment/app-service-app-service-environment-web-application-firewall)
 * https://docs.microsoft.com/en-us/azure/app-service/environment/network-info
   * "There are two versions of App Service Environment: ASEv1 and ASEv2. For information on ASEv1, see Introduction to App Service Environment v1. ASEv1 can be deployed in a classic or Resource Manager VNet. ASEv2 can only be deployed into a Resource Manager VNet."
   * "The size of the subnet used to host an ASE cannot be altered after the ASE is deployed."
   * "When you scale up or down, new roles of the appropriate size are added and then your workloads are migrated from the current size to the target size. Only after your apps are migrated are the original VMs removed. This means that if you had an ASE with 100 ASP instances ```there would be a period where you need double the number of VMs.``` It is for this reason that we recommend the use of a '/24' to accommodate any changes you might require. "
* [Security and Horsepower with App Service: The New Isolated Offering](https://channel9.msdn.com/Shows/Azure-Friday/Security-and-Horsepower-with-App-Service-The-New-Isolated-Offering?term=app%20service%20environment)
* https://docs.microsoft.com/en-us/azure/app-service/environment/app-service-app-service-environment-layered-security
* Gitub Resources
  * https://github.com/hansenms/iac/tree/master/ase-devops
    * "The pattern in this template deployment illustrates how to combine ASE with CI/CD using VSTS or TFS. It uses the ase template to establish an App Service Environment with a Web App. It also uses the ase-agent template to deploy a VSTS/TFS agent in the Virtual Network and connect this agent with a VSTS or TFS instance. Finally, a jump-box is also deploy in this case to allow access to the Virtual Network for testing purposes."
  * https://github.com/hansenms/iac 
  

  
### Azure Stack (for on-prem deployments)
* https://azure.microsoft.com/en-us/overview/azure-stack/
  * https://azure.microsoft.com/en-us/resources/videos/microsoft-azure-stack-azure-services-on-premises/

  
### Interesting Azure News Articles
====
* 2019
  * [2019-01-15 Azure Monitor logs in Grafana - now in public preview](https://azure.microsoft.com/en-us/blog/azure-monitor-logs-in-grafana-now-in-public-preview/)
    * https://docs.microsoft.com/en-us/azure/azure-monitor/platform/grafana-plugin
	* https://grafana.com/
	* https://grafana.com/plugins/grafana-azure-monitor-datasource
* 2018 
  * [2018-07-16 What’s new in Azure Monitor—container health ](https://azure.microsoft.com/en-us/updates/updatecontainerhealth71518/)
	* "We released a public preview of the Azure Monitor container health monitoring capability "
* https://azure.microsoft.com/en-us/blog/new-lower-azure-pricing/
* https://azure.microsoft.com/en-us/blog/announcing-general-availability-of-vm-storage-and-network-azure-cli-2-0/
