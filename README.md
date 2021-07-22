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
