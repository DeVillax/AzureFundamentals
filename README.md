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

Azure DevOps is Microsoftג€™s primary software development and deployment platform.
DevOps influences the application lifecycle throughout its plan, develop, deliver and operate phases.

Advisor is a personalized cloud consultant that helps you follow best practices to optimize your Azure deployments. It analyzes your resource configuration and usage telemetry and then recommends solutions that can help you improve the cost effectiveness, performance, high availability, and security of your Azure resources.

Azure Cognitive Services are APIs, SDKs, and services available to help developers build intelligent applications without having direct AI or data science skills or knowledge. Azure Cognitive Services enable developers to easily add cognitive features into their applications. The goal of Azure Cognitive Services is to help developers create applications that can see, hear, speak, understand, and even begin to reason. The catalog of services within Azure Cognitive Services can be categorized into five main pillars - Vision, Speech, Language, Web Search, and Decision.

Azure Application Insights detects and diagnoses anomalies in web apps.
Application Insights, a feature of Azure Monitor, is an extensible Application Performance Management (APM) service for developers and DevOps professionals.
Use it to monitor your live applications. It will automatically detect performance anomalies, and includes powerful analytics tools to help you diagnose issues and to understand what users actually do with your app.

SQL Server is a relational database service. Azure SQL Database is a managed SQL Server Database in Azure. The SQL Server is managed by Microsoft; you just have access to the database.

Azure SQL Synapse Analytics (previously called Data Warehouse) is a cloud-based Platform-as-a-Service (PaaS) offering from Microsoft. It is a large-scale, distributed, MPP (massively parallel processing) relational database technology in the same class of competitors as Amazon Redshift or Snowflake. Azure SQL
Synapse Analytics is an important component of the Modern Data Warehouse multi-platform architecture. Because Azure SQL Synapse Analytics is an MPP system with a shared-nothing architecture across distributions, it is meant for large-scale analytical workloads which can take advantage of parallelism.

You can process big data jobs in seconds with Azure Data Lake Analytics. You can process petabytes of data for diverse workload categories such as querying,
ETL, analytics, machine learning, machine translation, image processing and sentiment analysis by leveraging existing libraries written in .NET languages, R or
Python.

Apache Hadoop was the original open-source framework for distributed processing and analysis of big data sets on clusters. The Hadoop ecosystem includes related software and utilities, including Apache Hive, Apache HBase, Spark, Kafka, and many others.
Azure HDInsight is a fully managed, full-spectrum, open-source analytics service in the cloud for enterprises. The Apache Hadoop cluster type in Azure HDInsight allows you to use HDFS, YARN resource management, and a simple MapReduce programming model to process and analyze batch data in parallel.

Azure Monitor is used to monitor the health of Azure services.
Azure Monitor maximizes the availability and performance of your applications and services by delivering a comprehensive solution for collecting, analyzing, and acting on telemetry from your cloud and on-premises environments. It helps you understand how your applications are performing and proactively identifies issues affecting them and the resources they depend on.

You can browse available virtual machine images in the Azure Marketplace.
Azure Marketplace provides access and information on solutions and services available from Microsoft and their partners. Customers can discover, try, or buy cloud software solutions built on or for Azure. The catalog of 8,000+ listings provides Azure building blocks, such as Virtual Machines (VMs), APIs, Azure apps,
Solution Templates and managed applications, SaaS apps, containers, and consulting services.

Azure Advisor displays security recommendations.
Azure Advisor provides you with a consistent, consolidated view of recommendations for all your Azure resources. It integrates with Azure Security Center to bring you security recommendations. You can get security recommendations from the Security tab on the Advisor dashboard.
Security Center helps you prevent, detect, and respond to threats with increased visibility into and control over the security of your Azure resources. It periodically analyzes the security state of your Azure resources. When Security Center identifies potential security vulnerabilities, it creates recommendations. The recommendations guide you through the process of configuring the controls you need.

Azure Logic Apps is a cloud service that helps you schedule, automate, and orchestrate tasks, business processes, and workflows when you need to integrate apps, data, systems, and services across enterprises or organizations. Logic Apps simplifies how you design and build scalable solutions for app integration, data integration, system integration, enterprise application integration (EAI), and business-to-business (B2B) communication, whether in the cloud, on premises, or both.
For example, here are just a few workloads you can automate with logic apps:
✑ Process and route orders across on-premises systems and cloud services.
✑ Send email notifications with Office 365 when events happen in various systems, apps, and services.
✑ Move uploaded files from an SFTP or FTP server to Azure Storage.
✑ Monitor tweets for a specific subject, analyze the sentiment, and create alerts or tasks for items that need review.

A content delivery network (CDN) is a distributed network of servers that can efficiently deliver web content to users. CDNs store cached content on edge servers in point-of-presence (POP) locations that are close to end users, to minimize latency.
Azure Content Delivery Network (CDN) offers developers a global solution for rapidly delivering high-bandwidth content to users by caching their content at strategically placed physical nodes across the world. Azure CDN can also accelerate dynamic content, which cannot be cached, by leveraging various network optimizations using CDN POPs. For example, route optimization to bypass Border Gateway Protocol (BGP).
The benefits of using Azure CDN to deliver web site assets include:
✑ Better performance and improved user experience for end users, especially when using applications in which multiple round-trips are required to load content.
✑ Large scaling to better handle instantaneous high loads, such as the start of a product launch event.
✑ Distribution of user requests and serving of content directly from edge servers so that less traffic is sent to the origin server.

IoT Hub (Internet of things Hub) provides data from millions of sensors.
IoT Hub is a managed service, hosted in the cloud, that acts as a central message hub for bi-directional communication between your IoT application and the devices it manages. You can use Azure IoT Hub to build IoT solutions with reliable and secure communications between millions of IoT devices and a cloud- hosted solution backend. You can connect virtually any device to IoT Hub.
There are two storage services IoT Hub can route messages to -- Azure Blob Storage and Azure Data Lake Storage Gen2 (ADLS Gen2) accounts. Azure Data
Lake Storage accounts are hierarchical namespace-enabled storage accounts built on top of blob storage. Both of these use blobs for their storage.
Data Lake: is typical storage for IoT Hub

The Azure portal offers three ways to create a VM:
✑ Using the graphical portal.
✑ Using the Azure Cloud Shell using Bash.
✑ Using the Azure Cloud Shell using PowerShell. 

Azure Advisor does not provide recommendations on how to improve the security of an Azure AD environment.

Azure Advisor does not provide recommendations on how to configure network settings on Azure virtual machines.

Azure virtual machines provide operation system virtualization.
Azure Virtual Machines (VM) is one of several types of on-demand, scalable computing resources that Azure offers. Typically, you choose a VM when you need more control over the computing environment than the other choices offer.

Azure Container Instances provide portable environments for virtualized applications.
Containers are becoming the preferred way to package, deploy, and manage cloud applications. Azure Container Instances offers the fastest and simplest way to run a container in Azure, without having to manage any virtual machines and without having to adopt a higher-level service.
Containers offer significant startup benefits over virtual machines (VMs). Azure Container Instances can start containers in Azure in seconds, without the need to provision and manage VMs.

Azure App Service is used to build, deploy and scale web apps.
Azure App Service is a platform-as-a-service (PaaS) offering that lets you create web and mobile apps for any platform or device and connect to data anywhere, in the cloud or on-premises. App Service includes the web and mobile capabilities that were previously delivered separately as Azure Websites and Azure Mobile Services.

Azure Security Center is a unified infrastructure security management system that strengthens the security posture of your data centers, and provides advanced threat protection across your hybrid workloads in the cloud - whether they're in Azure or not - as well as on premises.

The advanced monitoring capabilities in Security Center also let you track and manage compliance and governance over time. The overall compliance provides you with a measure of how much your subscriptions are compliant with policies associated with your workload.

DDoS is a type of attack that tries to exhaust application resources. The goal is to affect the applicationג€™s availability and its ability to handle legitimate requests.
DDoS attacks can be targeted at any endpoint that is publicly reachable through the internet.
Azure has two DDoS service offerings that provide protection from network attacks: DDoS Protection Basic and DDoS Protection Standard.
DDoS Basic protection is integrated into the Azure platform by default and at no extra cost.
You have the option of paying for DDoS Standard. It has several advantages over the basic service, including logging, alerting, and telemetry. DDoS Standard can generate reports that contain details of attempted attacks as required in this question.

To monitor threats by using sensors, you would use Azure Advanced Threat Protection (ATP).
Azure Advanced Threat Protection (ATP) is a cloud-based security solution that leverages your on-premises Active Directory signals to identify, detect, and investigate advanced threats, compromised identities, and malicious insider actions directed at your organization.
Sensors are software packages you install on your servers to upload information to Azure ATP.

To enforce MFA based on a condition, you would use Azure Active Directory Identity Protection.
Azure AD Identity Protection helps you manage the roll-out of Azure Multi-Factor Authentication (MFA) registration by configuring a Conditional Access policy to require MFA registration no matter what modern authentication app you are signing in to.

A network security group works like a firewall. You can attach a network security group to a virtual network and/or individual subnets within the virtual network.
You can also attach a network security group to a network interface assigned to a virtual machine. You can use multiple network security groups within a virtual network to restrict traffic between resources such as virtual machines and subnets.
You can filter network traffic to and from Azure resources in an Azure virtual network with a network security group. A network security group contains security rules that allow or deny inbound network traffic to, or outbound network traffic from, several types of Azure resources.
In this question, we need to add a rule to the network security group to allow the connection to the virtual machine on port 80 (HTTP).

The just-in-time (JIT) virtual machine (VM) access feature in Azure Security Center allows you to lock down inbound traffic to your Azure Virtual Machines. This reduces exposure to attacks while providing easy access when you need to connect to a VM.

Azure Bastion helps protecting remote access to VMs

You can restrict traffic to multiple virtual networks with a single Azure firewall.
Azure Firewall is a managed, cloud-based network security service that protects your Azure Virtual Network resources. It's a fully stateful firewall as a service with built-in high availability and unrestricted cloud scalability.
You can centrally create, enforce, and log application and network connectivity policies across subscriptions and virtual networks. Azure Firewall uses a static public IP address for your virtual network resources allowing outside firewalls to identify traffic originating from your virtual network.

Azure Traffic Manager is a DNS-based load balancing solution. It is not used to ensure that a virtual machine named VM1 is accessible from the Internet over
HTTP.
To ensure that a virtual machine named VM1 is accessible from the Internet over HTTP, you need to modify a network security group or Azure Firewall.
In this question, we need to add a rule to a network security group or Azure Firewall to allow the connection to the virtual machine on port 80 (HTTP).

You would use the Azure Activity Log, not Access Control to view which user turned off a specific virtual machine during the last 14 days.
Activity logs are kept for 90 days. You can query for any range of dates, as long as the starting date isn't more than 90 days in the past.
In this question, we would create a filter to display shutdown operations on the virtual machine in the last 14 days.

An Azure Policy initiative definition is a collection of policy definitions.

You can add an ARM template to an Azure blueprint
You cannot assign an Azure blueprint to a resource group
You can use Azure Blueprints to grant permissions to a resource

An Azure resource can have multiple Delete locks
An azure resource inherits locks from its resource group
If an Azure resource has a Read-only lock, you can add a Delete lock to the resource

You can view a list of compliance certifications in the Trust Center to determine whether Azure meets your regional requirements.

Authorization to access Azure resources can be provided by other identity providers by using federation. A commonly used example of this is to federate your on- premises Active Directory environment with Azure AD and use this federation for authentication and authorization

As described above, third-party cloud services and on-premises Active Directory can be used to access Azure resources. This is known as ג€˜federationג€™.
Federation is a collection of domains that have established trust. The level of trust may vary, but typically includes authentication and almost always includes authorization. A typical federation might include a number of organizations that have established trust for shared access to a set of resources.

Azure Active Directory (Azure AD) is a centralized identity provider in the cloud. This is the primary built-in authentication and authorization service to provide secure access to Azure resources.

Azure Germany is available to eligible customers and partners globally who intend to do business in the EU/EFTA, including the United Kingdom.
Azure Germany offers a separate instance of Microsoft Azure services from within German datacenters. The datacenters are in two locations, Frankfurt/Main and
Magdeburg. This placement ensures that customer data remains in Germany and that the datacenters connect to each other through a private network. All customer data is exclusively stored in those datacenters. A designated German company--the German data trustee--controls access to customer data and the systems and infrastructure that hold customer data.

Azure Information Protection can encrypt documents and emails.
Azure Information Protection is a cloud-based solution that helps an organization to classify and optionally, protect its documents and emails by applying labels.
Labels can be applied automatically by administrators who define rules and conditions, manually by users, or a combination where users are given recommendations.
The protection technology uses Azure Rights Management (often abbreviated to Azure RMS). This technology is integrated with other Microsoft cloud services and applications, such as Office 365 and Azure Active Directory.
This protection technology uses encryption, identity, and authorization policies. Similarly to the labels that are applied, protection that is applied by using Rights
Management stays with the documents and emails, independently of the location ג€" inside or outside your organization, networks, file servers, and applications.

Compliance Manager in the Service Trust Portal is a workflow-based risk assessment tool that helps you track, assign, and verify your organization's regulatory compliance activities related to Microsoft Cloud services, such as Microsoft 365, Dynamics 365, and Azure.

Azure Information Protection is used to automatically add a watermark to Microsoft Word documents that contain credit card information.
You use Azure Information Protection labels to apply classification to documents and emails. When you do this, the classification is identifiable regardless of where the data is stored or with whom itג€™s shared. The labels can include visual markings such as a header, footer, or watermark.

 The Microsoft Privacy Statement explains what personal data Microsoft processes, how Microsoft processes the data, and the purpose of processing the data
