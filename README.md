# AzureFundamentals
Study guide of the Azure Fundamentals certification (AZ-900)

An Azure AD tenant can have multiple subscriptions but an Azure subscription can only be associated with one Azure AD tenant.

If your subscription expires, you lose access to all the other resources associated with the subscription. However, the Azure AD directory remains in Azure. You can associate and manage the directory using a different Azure subscription.

An Azure subscription is a container for Azure resources. It is also a boundary for permissions to resources and for billing. You are charged monthly for all resources in a subscription. A single Azure tenant (Azure Active Directory) can contain multiple Azure subscriptions.

A resource group is a container that holds related resources for an Azure solution. The resource group can include all the resources for the solution, or only those resources that you want to manage as a group.

To enable each department administrator to manage the Azure resources used by that department, you will need to create a separate subscription per department. You can then assign each department administrator as an administrator for the subscription to enable them to manage all resources in that subscription

You can use the same account to manage multiple subscriptions. You can create an additional subscription for your account in the Azure portal. You may want an additional subscription to avoid hitting subscription limits, to create separate environments for security, or to isolate data for compliance reasons.

You cannot merge two subscriptions into a single subscription. However, you can move some Azure resources from one subscription to another. You can also transfer ownership of a subscription and change the billing type for a subscription.

A company can have multiple subscriptions and store resources in the different subscriptions. However, a resource instance can exist in only one subscription.

You can move a VM and its associated resources to a different subscription by using the Azure portal.
Moving between subscriptions can be handy if you originally created a VM in a personal subscription and now want to move it to your company's subscription to continue your work. You do not need to start the VM in order to move it and it should continue to run during the move.

To implement a solution that enables the client computers on your on-premises network to communicate to the Azure virtual machines, you need to configure a
VPN (Virtual Private Network) to connect the on-premises network to the Azure virtual network.
The Azure VPN device is known as a Virtual Network Gateway. The virtual network gateway needs to be located in a dedicated subnet in the Azure virtual network. This dedicated subnet is known as a gateway subnet and must be named ג€˜GatewaySubnetג€™.
Note: a virtual network (answer D) is also required. However, as we already have virtual machines deployed in a Azure, we can assume that the virtual network is already in place.

any Azure resource have quote limits. The purpose of the quota limits is to help you control your Azure costs. However, it is common to require an increase to the default quota.
You can request a quota limit increase by opening a support request. In the support request, select ג€˜Service and subscription limits (quotas)ג€™ for the Issue type, select your subscription and the service you want to increase the quota for. For this question, you would select ג€˜SQL Database Managed Instanceג€™ as the quote type.

You need an Azure Active Directory account to manage a subscription, not a Microsoft account.
An account is created in the Azure Active Directory when you create the subscription. Further accounts can be created in the Azure Active Directory to manage the subscription.

Not all Azure regions support availability zones.

Availability zones can be used with many Azure services, not just VMs.

Availability Zones are unique physical locations within a single Azure region.

Azure containers are the backbone of the virtual disks platform for Azure IaaS. Both Azure OS and data disks are implemented as virtual disks where data is durably persisted in the Azure Storage platform and then delivered to the virtual machines for maximum performance. Azure Disks are persisted in Hyper-V VHD format and stored as a page blob in Azure Storage.

Networks in Azure are known as virtual networks. A virtual network can have multiple IP address spaces and multiple subnets. Azure automatically routes traffic between different subnets within a virtual network.
The question states that FinServer must be on a separate network segment. The only way to separate FinServer from the other servers in networking terms is to place the server in a different virtual network to the other servers.

Azure Files is Microsoft's easy-to-use cloud file system. Azure file shares can be seamlessly used in Windows and Windows Server.
To use an Azure file share with Windows, you must either mount it, which means assigning it a drive letter or mount point path, or access it via its UNC path.
Unlike other SMB shares you may have interacted with, such as those hosted on a Windows Server, Linux Samba server, or NAS device, Azure file shares do not currently support Kerberos authentication with your Active Directory (AD) or Azure Active Directory (AAD) identity, although this is a feature we are working on.
Instead, you must access your Azure file share with the storage account key for the storage account containing your Azure file share. A storage account key is an administrator key for a storage account, including administrator permissions to all files and folders within the file share you're accessing, and for all file shares and other storage resources (blobs, queues, tables, etc) contained within your storage account.

Azure Cosmos DB is Microsoft's globally distributed, multi-model database service. With a click of a button, Cosmos DB enables you to elastically and independently scale throughput and storage across any number of Azure regions worldwide.
Azure Cosmos DB is a great way to store unstructured and JSON data. Combined with Azure Functions, Cosmos DB makes storing data quick and easy with much less code than required for storing data in a relational database.

The first thing you create in Azure is a subscription. You can think of an Azure subscription as an ג€˜Azure accountג€™. You get billed per subscription.
A subscription is an agreement with Microsoft to use one or more Microsoft cloud platforms or services, for which charges accrue based on either a per-user license fee or on cloud-based resource consumption.
Microsoft's Software as a Service (SaaS)-based cloud offerings (Office 365, Intune/EMS, and Dynamics 365) charge per-user license fees.
Microsoft's Platform as a Service (PaaS) and Infrastructure as a Service (IaaS) cloud offerings (Azure) charge based on cloud resource consumption.
You can also use a trial subscription, but the subscription expires after a specific amount of time or consumption charges. You can convert a trial subscription to a paid subscription.
Organizations can have multiple subscriptions for Microsoft's cloud offerings.

Azure resources deployed to a single resource group can be located in different regions. The resource group only contains metadata about the resources it contains.
When creating a resource group, you need to provide a location for that resource group. You may be wondering, "Why does a resource group need a location?
And, if the resources can have different locations than the resource group, why does the resource group location matter at all?" The resource group stores metadata about the resources. When you specify a location for the resource group, you're specifying where that metadata is stored. For compliance reasons, you may need to ensure that your data is stored in a particular region.

Tags for Resources are not inherited by default from their Resource Group

Azure storage offers different access tiers: hot, cool and archive.
The archive access tier has the lowest storage cost. But it has higher data retrieval costs compared to the hot and cool tiers. Data in the archive tier can take several hours to retrieve.
While a blob is in archive storage, the blob data is offline and can't be read, overwritten, or modified. To read or download a blob in archive, you must first rehydrate it to an online tier.
Example usage scenarios for the archive access tier include:
✑ Long-term backup, secondary backup, and archival datasets
✑ Original (raw) data that must be preserved, even after it has been processed into final usable form.
✑ Compliance and archival data that needs to be stored for a long time and is hardly ever accessed.

You need a minimum of two virtual machines with each one located in a different availability zone.
Availability Zones is a high-availability offering that protects your applications and data from datacenter failures. Availability Zones are unique physical locations within an Azure region. Each zone is made up of one or more datacenters equipped with independent power, cooling, and networking. To ensure resiliency, thereג€™s a minimum of three separate zones in all enabled regions. The physical separation of Availability Zones within a region protects applications and data from datacenter failures. Zone-redundant services replicate your applications and data across Availability Zones to protect from single-points-of-failure. With Availability
Zones, Azure offers industry best 99.99% VM uptime SLA.

Azure Monitor collects events from resources and transfers them to Azure Event Hubs which processes them for any other SIEM. Azure Event Hubs is a streaming platform and event ingestion service. It can transform and store data using any real-time analytics provider or batching/storage adapters. Use Event Hubs to stream Azure Monitor data to partner SIEM and monitoring tools

Availability Zones is a high-availability offering that protects your applications and data from datacenter failures. Availability Zones are unique physical locations within an Azure region.

There are different replication options available with a storage account. The ג€˜minimumג€™ replication option is Locally Redundant Storage (LRS). With LRS, data is replicated synchronously three times within the primary region.

Data is not backed up automatically to another Azure Data Center although it can be depending on the replication option configured for the account. Locally
Redundant Storage (LRS) is the default which maintains three copies of the data in the data center.
Geo-redundant storage (GRS) has cross-regional replication to protect against regional outages. Data is replicated synchronously three times in the primary region, then replicated asynchronously to the secondary region.

The current storage limit is 2 PB for US and Europe, and 500 TB for all other regions (including the UK) with no limit on the number of files.

North America has several Azure regions, including West US, Central US, South Central US, East Us, and Canada East. 

A region is a set of datacenters deployed within a latency-defined perimeter and connected through a dedicated regional low-latency network.

Outbound data transfer is charged at the normal rate and inbound data transfer is free.

Azure virtual machine scale sets let you create and manage a group of load balanced VMs. The number of VM instances can automatically increase or decrease in response to demand or a defined schedule. Scale sets provide high availability to your applications, and allow you to centrally manage, configure, and update many VMs.
Virtual machines in a scale set can be deployed across multiple update domains and fault domains to maximize availability and resilience to outages due to data center outages, and planned or unplanned maintenance events.

Azure Service Health provides a personalized view of the health of the Azure services and regions you're using. This is the best place to look for service impacting communications about outages, planned maintenance activities, and other health advisories because the authenticated Service Health experience knows which services and resources you currently use.

You can use Azure Resource Manager templates to automate the creation of the Azure resources. Deploying resource through templates is known as
ג€˜Infrastructure as codeג€™.
To implement infrastructure as code for your Azure solutions, use Azure Resource Manager templates. The template is a JavaScript Object Notation (JSON) file that defines the infrastructure and configuration for your project. The template uses declarative syntax, which lets you state what you intend to deploy without having to write the sequence of programming commands to create it. In the template, you specify the resources to deploy and the properties for those resources.

Azure Functions provides the platform for serverless code.
Azure Functions is a serverless compute service that lets you run event-triggered code without having to explicitly provision or manage infrastructure.

Azure Databricks is a big analysis service for machine learning.
Azure Databricks is an Apache Spark-based analytics platform. The platform consists of several components including ג€˜MLibג€™. Mlib is a Machine Learning library consisting of common learning algorithms and utilities, including classification, regression, clustering, collaborative filtering, dimensionality reduction, as well as underlying optimization primitives.

Azure Application Insights detects and diagnoses anomalies in web apps.
Application Insights, a feature of Azure Monitor, is an extensible Application Performance Management (APM) service for developers and DevOps professionals.
Use it to monitor your live applications. It will automatically detect performance anomalies, and includes powerful analytics tools to help you diagnose issues and to understand what users actually do with your app.

Azure App Service hosts web apps.
Azure App Service is an HTTP-based service for hosting web applications, REST APIs, and mobile back ends. You can develop in your favorite language, be it
.NET, .NET Core, Java, Ruby, Node.js, PHP, or Python. Applications run and scale with ease on both Windows and Linux-based environments.


DevTest Labs creates labs consisting of pre-configured bases or Azure Resource Manager templates.
By using DevTest Labs, you can test the latest versions of your applications by doing the following tasks:
✑ Quickly provision Windows and Linux environments by using reusable templates and artifacts.
✑ Easily integrate your deployment pipeline with DevTest Labs to provision on-demand environments.
✑ Scale up your load testing by provisioning multiple test agents and create pre-provisioned environments for training and demos.

 For Windows the Azure CLI is installed via an MSI, which gives you access to the CLI through the Windows Command Prompt (CMD) or PowerShell.
 
Azure Cloud Shell is a browser-based shell experience to manage and develop Azure resources.
Cloud Shell offers a browser-accessible, pre-configured shell experience for managing Azure resources without the overhead of installing, versioning, and maintaining a machine yourself.
Being browser-based, Azure Cloud Shell can be run on a browser from a tablet that runs the Android operating system.

PowerApps lets you quickly build business applications with little or no code. It is not used to create Azure virtual machines. Therefore, this solution does not meet the goal.
PowerApps Portals allow organizations to create websites which can be shared with users external to their organization either anonymously or through the login provider of their choice like LinkedIn, Microsoft Account, other commercial login providers.

The Azure portal is a web-based, unified console that provides an alternative to command-line tools. With the Azure portal, you can manage your Azure subscription using a graphical user interface. You can build, manage, and monitor everything from simple web apps to complex cloud deployments. Create custom dashboards for an organized view of resources. Configure accessibility options for an optimal experience.
Being web-based, the Azure portal can be run on a browser from a tablet that runs the Android operating system.

Azure Monitor maximizes the availability and performance of your applications and services by delivering a comprehensive solution for collecting, analyzing, and acting on telemetry from your cloud and on-premises environments. Azure Monitor uses Target Resource, which is the scope and signals available for alerting. A target can be any Azure resource. Example targets: a virtual machine, a storage account, a virtual machine scale set, a Log Analytics workspace, or an Application Insights resource.

Azure Repos is a set of version control tools that you can use to manage your code.

In the Azure virtual machines page in the Azure portal, there is a named Maintenance Status. This column will display service issues that could affect your virtual machine. A service failure is rare but host server maintenance that could affect your virtual machines is more common.
Azure periodically updates its platform to improve the reliability, performance, and security of the host infrastructure for virtual machines. The purpose of these updates ranges from patching software components in the hosting environment to upgrading networking components or decommissioning hardware.

With the Azure Cloud Shell, you can run PowerShell cmdlets and scripts in a Web browser. You log in to the Azure Portal and select the Azure Cloud Shell option.
This will open a PowerShell session in the Web browser. The Azure Cloud Shell has the necessary Azure PowerShell module installed.

Azure Service Health consists of three components: Azure Status, Azure Service Heath and Azure Resource Health.
Azure service health provides a personalized view of the health of the Azure services and regions you're using. This is the best place to look for service impacting communications about outages, planned maintenance activities, and other health advisories because the authenticated Azure Service Health experience knows which services and resources you currently use.
To view the health of all other services available in Azure, you would use the Azure Status component of Azure Service Health. Azure status informs you of service outages in Azure on the Azure Status page. The page is a global view of the health of all Azure services across all Azure regions.

The best way to use Service Health is to set up Service Health alerts to notify you via your preferred communication channels when service issues, planned maintenance, or other changes may affect the Azure services and regions you use.
You can use Resource Health to view the health of a virtual machine. However, you cannot use Resource Health to prevent a service failure affecting the virtual machine.
Azure resource health provides information about the health of your individual cloud resources such as a specific virtual machine instance.

