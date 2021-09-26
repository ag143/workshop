# Part 1: Describe core Azure concepts

- Collect security data in Azure Sentinel. Azure Sentinel is Microsoft's cloud-based SIEM. A SIEM aggregates security data from many different sources to provide additional capabilities for threat detection and responding to threats. 

What's the best way for Tailwind Traders to limit all outbound traffic from VMs to known hosts?
- Create application rules in Azure Firewall. Azure Firewall enables you to limit outbound HTTP/S traffic to a specified list of fully qualified domain names (FQDNs). 

How can Tailwind Traders most easily implement a deny by default policy so that VMs can't connect to each other? 
- Create a network security group rule that prevents access from another VM on the same network.

Where can the legal team access information around how the Microsoft cloud helps them secure sensitive data and comply with applicable laws and regulations?
- Trust Center. The Trust Center is a great resource for people in your organization who might play a role in security, privacy, and compliance. 

Where can the IT department find reference blueprints that it can apply directly to its Azure subscriptions
- *wrong* Online Services Terms. The Online Services Terms is a legal agreement between Microsoft and the customer that details the obligations by both parties with respect to the processing and security of customer data and personal data. 
- Azure compliance documentation. The compliance documentation provides reference blueprints, or policy definitions, for common standards that you can apply to your Azure subscription. 

What's the SLA for Azure Maps in terms of guaranteed uptime
- 99.9 percent

You want to send messages from the IoT device to the cloud and vice versa. Which IoT technology can send and receive messages
- IoT Hub
- *wrong* IoT Central



# Part 2: Describe core Azure services

services:
- IaaS
    - Virtual Machines
- PaaS
    - Azure web apps. build applications on the Azure platform without deploying, configuring, and maintaining their own Azure virtual machines.  
    - Azure Logic Apps. schedule, automate, and coordinate tasks, business processes, and workflows when you need to integrate apps, data, systems, and services across your enterprise or organization
    - Azure SQL
- Saas

Which of the following Azure regions is available to Japanese government agencies
- Azure Global
- *wrong* Azure Local/Japan. There is no such service
- *wrong* Azure Govenment. Azure Government is a mission-critical cloud that delivers breakthrough innovations to US government customers and their partners. Only the US federal government, state governments, local governments, tribal governments, and their partners have access to this dedicated instance and operation are managed by selected US citizens.

database:
- Azure Cosmos DB is a fully managed NoSQL database service for modern app development. Guaranteed single-digit millisecond response time and 99.999% availability. Azure Cosmos DB can store JSON documents.
- Azure SQL Data Warehouse is a fully managed cloud data warehouse. You can get query results in a short time across terabytes and petabytes of data.  
- Azure SQL Database is a fully managed, intelligent relational cloud database
- Azure Cache for Redis. A fast, fully managed in-memory data store. Not suitable for storing JSON documents

characteristics of the cloud
- Reliability depends on the service level agreement you choose, but in the event of a problem, your cloud-based application will continue to provide the user experience without any obvious downtime
- **Scalability** means that applications in the cloud can be scaled/increased in two distinct ways - in-out and up-down
- **Elasticity** means that cloud-based applications can be configured to always have the resources they need
- **Agility** is cloud-based resources that can be quickly deployed and configured as application requirements change
- *optional* The **flexibility** to change resource allocation is an example of cloud flexibility.
- *otpional* **resiliency**. 
    - Continuing service in the event of a failure
    - Maintaining a DR (Disaster Recovery) configuration in other regions

Availability zones are unique physical locations within your Azure region. Each zone consists of **one or more data centers** with independent power supplies, cooling means, and networks. Therefore, it does not necessarily consist of a single data center

Each region has at least three separate zones.
- True
- https://docs.microsoft.com/en-us/azure/availability-zones/az-overview

Azure Advisor is available for **free** and provides:
- a way to improve the security of your Azure resources
- solutions that help you improve cost-effectiveness, performance, reliability, and security, and you cannot file a cap relaxation request for resource limit
- You can access the Advisor using the Azure portal, the Azure command line interface (CLI), or the Advisor API. 
- Alternatively, configure alerts to automatically notify you of new recommendations
- doesn't provide a way to improve the security of your Azure Active Directory (Azure AD) environment. Azure Active Directory has a function called Identity Protection, which allows you to obtain analysis information on the security structure of your organization. It helps you identify potential attacks and understand the effectiveness of your policies.




# Part 3: Describe core solutions and management tools on Azure

Which service could help you manage the VMs that your developers and testers need to ensure that your new app works across various operating systems?
- Azure DevTest Labs
- *wrong* Azure Test Labs. Azure Test Labs is used to create automated tests, but not to manage VMs to test across various environments

Your company wants to use a serverless application to automate the data registration process. Which Azure service should you use?
- Azure Functions. an event-driven serverless computing platform that can solve complex orchestration problems. You can use this to develop serverless applications.
- *wrong* Azure App Service

using multiple Azure virtual machines to ensure that the services running on the virtual machine do not stop in the event of a single data center failure. Proposed Solution: Deploy virtual machines in two or more regions. Is this the most appropriate solution
- No. 
- A single region is made up of multiple availability zones. Therefore, to prevent a single data center failure, you only need to use multiple **availability zones** and do not need to have a multi-region configuration. In addition, multi-region support is not optimal in terms of architectural configuration because it is difficult to link virtual machines across regions.

Which deployment method should you choose to reduce downtime for the application you are deploying?
- Mutli-AZ deployment. **A**vailability **Z**one
- *wrong* multi-region deployment
- Administrators can lock subscriptions, resource groups, or resources to prevent accidental deletion or modification of critical resources
    - Delete locks allow legitimate users to read and modify resources, but cannot delete them
    - Read-only locks allow legitimate users to read resources, but cannot update or delete resources

What settings do you need to make to prevent accidental deletion and overwriting of Recource1's resources?
- Set a read-only lock on the resource.
- *wrong* Set delete and update locks on the resource.

You need to create an Azure support request.
- **Azure support ticket REST API**
- Azure portal
- *wrong* Knowledge Center. a collection of common questions and answers about Azure
- *wrong* Security & Compliance Center. provides operations related to security and regulatory compliance
- *wrong* support.microsoft.com. 

Your company needs to run 10 Windows Server 2016 and 20 Linux virtual machines on a regular basis and **remove** them after processing the task. Which Azure service should you use to minimize the administrative effort required to deploy and delete these virtual machines?
- Azure DevTest Labs
- *wrong* Azure virtual machine scale set. allow you to create and manage groups of virtual machines and distribute the load within the same group, which is used when building large-scale services



# Part 4: Describe general security and network security features

Azure Security Center offers free and paid services
- The free tier only provides security policies, ongoing security assessments, and practical security features that help protect your Azure resources
-  Paid services extend the free tier functionality and add:
    - **threat protection**. It uses built-in behavioral analytics and machine learning to identify attacks and zero-day exploits, and uses access and application control to reduce exposure to network attacks and malware.
    - **virtual machine vulnerability scan**.

You are planning to extend your company's network to Azure to create a hybrid cloud configuration. In the on-premises environment, a VPN appliance that has the IP address of 136.168.103.1 is used and it is necessary to identify this on the Azure side. Which is the best solution for this situation?
- local network gateway. can be used to specify the IP address of the VPN device in the virtual network. This allows Azure to identify VPN appliances that use the IP address of 136.168.103.1.
- explanation:
    - the routing table is the routing route information recorded in the router itself. It is the table to be referred to when performing the routing process but it does not identify the IP address of the VPN appliance.
    - Application gateways are used to load balance traffic to various web applications. It does not identify the IP address of the VPN appliance
    - The network interface allows Azure VMs to communicate with Internet, Azure, and on-premises resources. It does not identify the IP address of the VPN appliance.

You want to deploy multiple web servers and multiple database servers in Azure. As a security measure, you need to limit the connection to the database server to be only from the web server. Which solution should you use for this?
- Azure network security groups. to filter network traffic to and from Azure resources in your Azure virtual network. Network security groups contain security rules that allow or deny inbound or outbound network traffic to many types of Azure resources. You can specify the source, destination, port, and protocol for each rule. 
- explanation:
    - Azure Service Bus is a fully managed enterprise integration message broker with message queues and publish / subscribe topics
    - Route filtering is a way to take advantage of a subset of the services supported through Microsoft peering

Which of the following statements is correct
- Data stored in your Azure storage account will have at least **three copies in the primary region**.
- explanation:
    - The Azure storage account copies the data into three times within the primary region and keeps them synchronous
    - It is also asynchronously copied to the secondary region. 
    - An Azure storage account contains all Azure Storage data objects (blobs, files, queues, tables, and disks).

Which service provides network traffic filtering for multiple Azure subscriptions and virtual networks?
- Azure Firewall
- explanation:
    - Application security groups are services for grouping virtual machines and managing access within a virtual network
    - A network security group is a service that manages access within a virtual network. Azure does not have permission to access the data

What are the security benefits of storing data in the Azure public cloud
- Users have full control over their data
- *wrong* Protection is automatically implemented without the need for user to implement their own data security measures.
- *exp* Users are required to take measures such as data encryption. 

Your company would use _________to automatically add watermarks to Microsoft Word documents that contain credit card information.
- Azure Information Protection

After you create a virtual machine, you need to change the _______ to allow the virtual machine to connect to TCP port 8080
- Network Security Group (NSG). By default, all inbound connections are not allowed on L4, so unless you have a network interface, you need to modify the rules of the network security group so that all inbound connections from port 80/8080 can reach the VM
- *wrong* virtual network gateway. a VPN device in the Azure virtual network that is used to set up a site-to-site VPN connection between the Azure virtual network and the local network, or a VNet-to-VNet VPN connection
- *wrong* virtual network. nothing more than a private isolated network in Azure, because it is used to enable Azure resources such as virtual machines to communicate securely with other Azure resources, the Internet, and resources in your on-premises network
- *wrong* Azure route table. only contains a set of rules (routes) that specify how packets are routed in the virtual network

create an Azure virtual machine using your Android laptop. Solution: Use the PowerApps portal
- No
- *wrong* Power Apps portal to create external websites that allow users outside your organization to sign in with different identities, create and view data in Microsoft Dataverse, and browse content anonymously. This is not the mechanism to use when creating a virtual machine

Your company is planning to move from an on-premises environment to Azure. Azure will only use PaaS solutions. You need to deploy the required Azure environment for this. Solution: Take advantage of Azure App Service and have Microsoft SQL Server installed. 
- **Yes**
- Azure App Service is a fully managed platform and platform service (PaaS) for building, deploying, and scaling web apps. Azure App Service allows you to quickly build, deploy, and scale web apps and APIs.
You can use .NET, .NET Core, Node.js, Java, Python, PHP running inside a container or on Windows or Linux



# Part 5: Describe identity, governance, privacy, and compliance features

You are building an application using a virtual machine in Azure. As a security requirement, it is necessary to apply Azure Multi-Factor Authentication (MFA) based on certain conditions.Which Azure service should you choose
- Azure Active Directory ID Protection. Azure Active Directory ID Protection allows you to apply MFA conditionally. It is also used to detect risks such as anonymous IP address logins, unfamiliar sign-ins, and credential leaks.
- Explanation:
    - Azure Monitor is incorrect because it collects what is known as "application monitoring data" (data about the performance and functionality of the code you write, regardless of platform).
    - Azure Security Center is an integrated infrastructure security management system that enhances the security structure of the data center. It's an advanced threat protection feature that protects your entire hybrid workload, both on the cloud and on-premises. With this option, you can't use MFA
    - Azure Threat Protection (ATP) is incorrect because it is used to monitor and analyze user activity and information across the network, such as permissions and group membership

There is an Azure virtual network named VNET-A in a resource group named MyResourceGroup. VNET-A  ___________ when you assign an Azure policy that says that MyResourceGroup is not allowed to create / update virtual networks.
- will **continue** to funciton normally
- Azure policies do not affect the pre-apply configuration. Therefore, VNET-A works fine because it was already created before the Azure policy was created. However, MyResourceGroup does not allow you to create any more VNETs

AD and ATP
- Azure AD Identity Protection requires users who sign from the Internet with an anonymous IP address to change their password and "self-heal". Identity Protection is a tool that allows organizations to perform three main tasks:
    - Automate identity-based risk detection and action.
    - Investigate risk using portal data.
    - Export risk detection data to third-party utilities for further analysis.  
- Azure AD Connect Health. used to monitor identity governance or identity infrastructure for on-premises resources or servers. You can use the Azure AD Connect Health portal to view alerts, performance monitoring, usage analysis, and other information.
- Azure AD privileged ID management. used to provide just-in-time access, prevent malicious activity, and provide a fully integrated review of "privileged roles" in real time. It also helps you manage privileged administrator roles across Azure resources and Azure AD
- Azure Advanced Threat Protection (ATP). used to detect threats from on-premises resources. It is incorrect because the questions is not regarding internal sources.


# Part 6: Describe Azure cost management and service level agreements

minimum number of virtual machines
- 2. Based on the VM's SLA, deploying at least two VMs on two AZs guarantees 99.99% availability
- [SLA for Virtual Machines](https://www.azure.cn/en-us/support/sla/virtual-machines/)

Azure resources are available in all regions, not all regions are available to users
- there is an Availability Zone that is specially assigned to the US Government and has restricted general use.
- The special regions are: 1. US Government Virginia and US Gov Iowa 1.1. Physically and logically isolated Azure instances. For US government agencies and partners (run by selected US personnel). Includes other compliance certificates such as FedRAMP and DISA.

Azure services are available to all Azure users during ____
- **public preview**
- *wrong* Enterprise Agreement (EA) Subscription, private preview, development. All the three are only available to some users

Which of the following explanations about Azure usage costs is correct?
- Azure provides flexibility for capital expenditure (CapEx) and operating expenditure (OpEx).
- *wrong* If you create two Azure virtual machines of the same size, the monthly usage fee for each virtual machine will be exactly the same. (it also depends on the region where the virtual machine is located, as each  has a different cost)