https://github.com/wzlwit/workshop/blob/main/Az%20Fundamentals/notes_mistake.md

# Part 1: Describe core Azure concepts
It is desirable to design Azure architecture based on the principles of a flexibility and elasticity in your cloud architecture. How do you achieve this?
- Automate scaling on-demand
- *(wrong)* Implement infrastructure coding and sharing. used to facilitate environmental automation.
- *(wrong)* Collect security data in Azure Sentinel.

What's the best way for Tailwind Traders to limit all outbound traffic from VMs to known hosts?
- Create application rules in Azure Firewall.

How can Tailwind Traders most easily implement a deny by default policy so that VMs can't connect to each other? 
- Create a network security group rule that prevents access from another VM on the same network.

Where can the legal team access information around how the Microsoft cloud helps them secure sensitive data and comply with applicable laws and regulations?
- Trust Center. 

Where can the IT department find reference blueprints that it can apply directly to its Azure subscriptions
- *(wrong)* Online Services Terms.
- Azure compliance documentation. 

What's the SLA for Azure Maps in terms of guaranteed uptime
- 99.9 percent

You want to send messages from the IoT device to the cloud and **vice versa**. Which IoT technology can send and receive messages
- IoT Hub
- *(wrong)* IoT Central.

Organizations hosting infrastructure in a ______________ do not need a data center
- Public cloud

Which group of data centers are connected by a fast network that is **geographically separated** in Azure?
- Region
- *(wrong)* Availability zone

Data center deployment is an example of CapEx?
- **TRUE**

You have an Azure web app and you need to manage your web app settings from your iPhone. Please select two Azure management tools
- Azure portal
- **Azure Cloud Shell**
- *(wrong)* Azure CLI. cannot be installed on iOS

Availability Zones are geographically independent?
- False

Availability Zone comes with multiple edge locations?
- False. separately from AZ

# Part 2: Describe core Azure services

Please select the **incorrect** statement about an Azure datacenter
- Azure employees can access the datacenter (incorrect)

regions connection:
- Data centers within a region are connected using a low-latency leased region network, but regions are connected via the Internet rather than a leased line.


Which of the following Azure regions is available to Japanese government agencies
- Azure Global
- *(wrong)* Azure Local/Japan. There is no such service
- *(wrong)* Azure Govenment. 

Users can leverage their data center to deploy Azure services?
- FALSE (should use **Azure Stack**)

Each region has at least three separate zones?
- True

You can merge two Azure subscriptions into one by creating a support request?
- False

__________ is an Azure service that detects and diagnoses web app anomalies.
- Azure Application Insights 

Data traffic between Azure services within the same Azure region is always free.
- Yes. if you're in the same region, Azure does not charge you for data transfers .

What is the correct Azure Storage data service to use if you want to store virtual machine data?
- Azure Blob Storage
- *(wrong)* Azure files

What are the correct features of Azure Resource Manager? Please select the three correct options.
- Resouce Group
- Tags
- Deployment of ARM templates
- *(wrong)* Activity logs

Which of the following Microsoft Azure services is available to all developers without needing machine learning expertise?
- Azure Cognitive Service (for all devlopers)
- *(wrong)* Azure Bot Service. (allows you to create and publish chatbots)

You are preparing to run an Azure PowerShell script from your Linux computer. What kind of preparation do you need? 
- Install PowerShell Core. (since 6.0, PowerShell Core can run PowerShell on MacOS and Linux)
- Install the Azure PowerShell Module. (Use the Azure PowerShell module to create and manage Azure resources with the PowerShell command line and scripts)
- *(wrong)* Install Azure PowerShell Core

You are considering using Azure Blueprints to streamline subscription compliance management. Choose two correct options for Azure Blueprints features.
- Azure Policy assignment
- Role-based access permission settings (RBAC)
- *(wrong)* Resource tag standardization

You are monitor the activities performed by users and want to store that data. Please select three solutions that will work for this.
- Azure monitor
- Azure Events Hubs
- Azure Storage
- *(wrong)* Azure logs
- exp: 
    - By default, activity logs are automatically saved for 90 days, but if you want to save logs over the medium to long term, you can save data in Azure Storage or Azure Events Hubs.  When you select the Event Hubs namespace, Azure Monitor creates an event hub in that namespace named insights-logs-operational-logs. For other log types, you can choose an existing event hub, or Azure Monitor can create an event hub for each log category. 

A Zone is same as an availability zone?
- False
    - Availability zone is deferent location from a zone in Azure. A zone are regional groups of Azure regions for billing. Data transfer charges are based on the zone.

In regards to moving Azure resources from one subscription to another, which of the following are correct statements?
- You can move some resources between subscriptions, but not all. (must support *move* option)
- Source and target resource groups are locked during the move.
- can move resources between subscriptions
- Transferring resources between subscriptions is free

"The benefit of using Azure virtual machines instead of traditional servers is: Improved remote access to the cloud."?
- False
    - Improving remote access to the cloud depends on the external environment and is not a characteristic of Azure virtual machines. It depends on the network inside the cloud and the performance of the leased line connection, the network performance of the on-premises environment, and so on.

There is no additional cost to use Azure globally across multiple regions.
- True. (cost depends on the resources used.)



# Part 3: Describe core solutions and management tools on Azure

Which service could help you manage the VMs that your developers and testers need to ensure that your new app works across various operating systems?
- Azure DevTest Labs
- *(wrong)* **Azure Test Labs**. Azure Test Labs is used to create automated tests, but not to manage VMs to test across various environments

Your company wants to use a serverless application to automate the data registration process. Which Azure service should you use?
- Azure Functions. 
- *(wrong)* Azure App Service

using multiple Azure virtual machines to ensure that the services running on the virtual machine do not stop in the event of a single data center failure. Proposed Solution: Deploy virtual machines in two or more regions. Is this the most appropriate solution
- No. 
- (need to use multiple **availability zones**)

Which deployment method should you choose to reduce downtime for the application you are deploying?
- Mutli-AZ deployment. **A**vailability **Z**one
- *(wrong)* multi-region deployment

What settings do you need to make to prevent accidental deletion and overwriting of Recource1's resources?
- Set a read-only lock on the resource.
- *(wrong)* Set delete and update locks on the resource.

You need to create an Azure support request.
- **Azure support ticket REST API**
- Azure portal
- *(wrong)* Knowledge Center. a collection of common questions and answers about Azure
- *(wrong)* Security & Compliance Center. provides operations related to security and regulatory compliance
- *(wrong)* support.microsoft.com. 

Your company needs to run 10 Windows Server 2016 and 20 Linux virtual machines on a regular basis and **remove** them after processing the task. Which Azure service should you use to minimize the administrative effort required to deploy and delete these virtual machines?
- Azure **DevTest** Labs
- *(wrong)* Azure virtual machine scale set. allow you to create and manage groups of virtual machines and distribute the load within the same group, which is used when building large-scale services

As an operations manager, you are in charge of managing each service in Azure. You need to find advice about maintenance-related events for Azure resources. Which service located on the Azure portal would you use?
- *(wrong)* Azure Advisor
- Help and support. You can find more information about maintenance in the help and support on the Azure portal. Planned maintenance information can be found on the Service Health page

Is the following true?"The cost of Azure services in private preview decreases as the service becomes publicly available."
- No

Which Azure service can be used to collect events from multiple resources into one repository?
- Azure Event Hub.
- *(wrong)* Azure Monitor.

From ______, you can track company regulatory standards and regulations such as ISO27001.
- Compliance Manager.

You can download the regulatory compliance report from the Azure Security Center.
- Yes. A new feature in Azure Security Center, the Regulatory Compliance Dashboard, is now available

Companies can extend their internal network by adding their physical servers to the public cloud
- **No**

Inbound data traffic from your on-premises network to Azure is always free when using Azure ExpressRoute connections
- Yes. 

On-demand flexibility is one of the benefits of using IaaS on the Azure cloud
- The advantage of the cloud is that you can quickly and flexibly build, delete, or expand infrastructure such as servers as needed

Infrastructure management flexibility is one of the benefits of using IaaS on the Azure cloud
- False
- Physical infrastructure management is often not possible on the part of the user. Therefore, infrastructure management is inflexible and requires very limited management options for the user

Your company is planning to purchase an Azure support plan. The main reason for this choice is to have access to a dedicated team from Azure to provide architectural support to the company and your new Azure environment creation.Which support plan should you choose to gain access to this?
- Professional Direct. 

What is the correct description of a benefit of on-demand cloud usage?
- Being able to flexibly configure resources at any time (configure and use the server whenever you need it)
- *(wrong)* Being able to maintain performance during load fluctuations. (scalable)

Your company wants to move their e-commerce site to Azure. Which is the correct option below for what the company should do/use during this initial planning stage
- Choosing services to use within Azure
- *(wrong)* Coordinate a meeting with Azure staff
- exp:
    - There is no initial cost, so there is no need to consider this, however, it is necessary to calculate the medium- to long-term resource usage fee. 
    - no need to apply or have a meeting with Azure in order to use Azure. It is always available. 
    - Since the EC site is a web application, it is not essential to make a VPN connection with the office. 

Global infrastructure deployment can be implemented immediately?
- True. Azure is deployed globally, allowing you to deploy infrastructure instantly to any region in any country. For example, a user living in Tokyo can select a region in the United States to deploy their infrastructure.

You want to subscribe to an Azure support plan so that you can get design reviews based on your specifications. Which support plan should you subscribe to? Please select the appropriate support plan.
- **Premier**. ( advisory services based on best practices)
- *(wrong)* Professional Direct. (general guidance)

You have built an application with an Azure virtual machine. This application delivers video content. Choose one of the best solutions to improve this delivery processing performance.
- Azure CDN (content delivery network)
- *(wrong)* Azure Cached for Redis (in-memory data store)

You are building a mechanism to save log files using BLOB storage. This data is rarely accessed. Choose the storage type that is most cost-effective?
- Archive
- *(wrong)* Cool. (infrequently, to be stored for at least 30 days)


# Part 4: Describe general security and network security features
You need to be aware of the latest Azure security standards to protect your data.Which of the following services should you use to ensure this?
- Trust Center
- *(wrong)* Azure compliance documentation


You are planning to extend your company's network to Azure to create a hybrid cloud configuration. In the on-premises environment, a VPN appliance that has the IP address of 136.168.103.1 is used and it is necessary to identify this on the Azure side. Which is the best solution for this situation?
- local network gateway. can be used to specify the IP address of the VPN device in the virtual network. This allows Azure to identify VPN appliances that use the IP address of 136.168.103.1.

A company has a VPN device that will be used on a Site-to-Site connection from an on-premise location to Azure. Which of the following would be used to represent the VPN device?
- Loca network gateway
- *(wrong)* Virtual network gateway.(which typically referes to your on-premises location. You give the site a name by which Azure can refer to it, then specify the IP address of the on-premises VPN device to which yo uwill create a connection)

You want to deploy multiple web servers and multiple database servers in Azure. As a security measure, you need to limit the connection to the database server to be only from the web server. Which solution should you use for this?
- Azure network security groups. 

Which of the following statements is correct
- Data stored in your Azure storage account will have at least **three copies in the primary region**.

Which service provides network traffic filtering for multiple Azure subscriptions and virtual networks?
- Azure Firewall

What are the security benefits of storing data in the Azure public cloud
- Users have full control over their data
- *(wrong)* Protection is automatically implemented without the need for user to implement their own data security measures.
- *exp* Users are required to take measures such as data encryption. 

Your company would use _________to automatically add watermarks to Microsoft Word documents that contain credit card information.
- Azure Information Protection

After you create a virtual machine, you need to change the _______ to allow the virtual machine to connect to TCP port 8080
- Network Security Group (NSG). By default, all inbound connections are not allowed on L4, so unless you have a network interface, you need to modify the rules of the network security group so that all inbound connections from port 80/8080 can reach the VM
- *(wrong)* virtual network gateway.
- *(wrong)* virtual network. 
- *(wrong)* Azure route table.

create an Azure virtual machine using your Android laptop. Solution: Use the PowerApps portal
- No
- *(wrong)* Power Apps portal

Your company is planning to move from an on-premises environment to Azure. Azure will only use PaaS solutions. You need to deploy the required Azure environment for this. Solution: Take advantage of Azure App Service and have Microsoft SQL Server installed. 
- **Yes**
- You can use .NET, .NET Core, Node.js, Java, Python, PHP running inside a container or on Windows or Linux

Which solution should You use to assess whether your Azure environment meets security regulatory requirements?
- Azure Security Center
- *(wrong)* Azure Advisor

You have been asked to "clean up" the Azure resources that you are not currently using to avoid incurring extra costs. Which of the following services should you remove to achieve this?
- Public IP address
    
You want to configure a virtual machine to run a PowerShell script that creates an Azure resource. Solution: Configure a Linux virtual machine to run script from the Azure CLI tools. Will this solution meet the above requirements?
- Yes. Users can run PowerShell scripts on Linux operating systems that already have the Azure CLI tools installed.
- *(wrong)*

You're building a process in Azure to store over 30TB of data and perform data analysis with Microsoft Power BI. The amount of data is large, but the frequency of accessing individual data is low. Choose the two best solutions.
- Azure Data Lake
- Azure SQL Data Warehouse
- exp: 
    - Azure Data Lake is a storage repository suitable for holding large amounts of data. With 30TB of data stored, the data lake can scale up to terabytes and petabytes of data.
    - Azure SQL Data Warehouse is a data warehouse that can perform data analysis in cooperation with Azure Data Lake. You can import or export data directly from the Azure Data Lake Store (ADLS) to your Azure SQL Data Warehouse (SQL DW).  
    - Azure SQL Database. a fully managed, intelligent relational cloud database. It eliminates the complexity of configuring and managing high availability, tuning, backup, and other database tasks with a fully managed SQL database.

You are using Azure AD Connect to configure single sign-on (SSO). For this, you have enabled staging mode, but you need to check the synchronization result between ADs. What would you use to check this?
- Synchronization Service Manager. 

One of the benefits of using IaaS on the Azure cloud is that it will reduce costs compared to on-premises environments
- False
- The cost is often cheaper by using the cloud, but there is no guarantee that it will be cheaper. Extra costs may be incurred if you overuse various services for weight billing. In addition, having your own infrastructure may reduce costs in the medium to long term

One of the benefits of using IaaS on the Azure cloud is that you can leave security measures to the cloud vendor
- **False**. 
- You need to take security measures based on the application you have. The responsibility for managing the security of an application or service depends on the cloud service model. Built-in features and partner solutions that can be deployed to Azure subscriptions have features available on the Azure platform that cover these responsibilities. In this case, security is still a responsibility of the user.

You want to build a *serverless* application to perform simple application processing. Which is the best solution for this?
- Azure Functions
- *(wrong)* Azure App service.

You need to implement an application that leverages Azure to automatically send email notifications. Choose the two best solutions for this.
- Azure Functions. can be used to send email
- Azure Logic App.

You need to perform data processing utilizing Hadoop clusters in the cloud.Which solution is best for this?
- Azure HDInsight. 
- *(wrong)* Azure Databricks.

Who would utilize the standards-based approach when adding functionality to applications that are targeted by Azure AD?
- Azure Developer

move resources between regions
- You can move Azure resources to another Azure subscription or to another resource group in the same subscription. You can use the Azure portal, Azure PowerShell, Azure CLI, or REST API to move resources.
- You can also use Azure Resource Mover to move resources to another region. Leverage Azure Global Infrastructure capabilities to seamlessly move resources to the region that best suits your needs. You can streamline your planning process, accelerate your travel and protect your resources.

In order to get a security token, what does the application need to connect to/ use
- Azure Active Directory. Developers can get security tokens using Azure Active Directory
- *(wrong)* Azure Key Vault

You are building an application using a virtual machine in Azure. As a security requirement, it is necessary to monitor security threats. Which Azure service below do you need to choose?
- Azure Advanced Threat Protection
- *(wrong)* Azure Security Center

You have an Azure AD tenant in your Azure subscription. All administrators are required to enter a verification code to access the Azure portal. At that time, you need to allow your administrator to access the Azure portal only from your on-premises network.Choose the best solution for that.
- Azure AD Identity Protection sign-in risk policy
- *(wrong)* The multi-factor authentication service configuration. (MFA only allows you to configure trusted devices, not the login location such as on premise sites.)


# Part 5: Describe identity, governance, privacy, and compliance features

You are building an application using a virtual machine in Azure. As a security requirement, it is necessary to apply Azure Multi-Factor Authentication (MFA) based on certain conditions.Which Azure service should you choose
- Azure Active Directory ID Protection. Azure Active Directory ID Protection allows you to apply MFA conditionally. It is also used to detect risks such as anonymous IP address logins, unfamiliar sign-ins, and credential leaks.
- Explanation:
    - Azure Monitor is incorrect because it collects what is known as "application (code you wrote) monitoring data" . It does not have the ability to centrally manage events.  
    - Azure Security Center is an integrated infrastructure security management system  It's an advanced threat protection feature that protects your entire hybrid workload, both on the cloud and on-premises. can't use MFA.
    - Azure Threat Protection (ATP) is incorrect because it is used to monitor and analyze user activity and information across the network, such as permissions and group membership

There is an Azure virtual network named VNET-A in a resource group named MyResourceGroup. VNET-A  ___________ when you assign an Azure policy that says that MyResourceGroup is not allowed to create / update virtual networks.
- will **continue** to funciton normally
- Azure policies do not affect the pre-apply configuration. But MyResourceGroup does not allow you to create any more VNETs

There are regions that are not available to organizations that have business bases in the United States.
- true
- Organizations that do not have a business based in China will not be able to use the four regions of China. Global Azure is operated by Microsoft, but China is not available globally for political reasons. As a result, China Azure operates independently of Global Azure.

Azure Service Health:
- can set alerts for failures in Azure services
- can check the status of all services in the Azure Environment
- *(wrong)* can set preventive measures against failures. (cannot prevent failure)
- cannot apply for advice to Azure Support in ASH. (Apply for Azure support on the Azure support page)

____________is used to store the secrets of your Azure Active Directory (Azure AD) user account.
- AzureKeyVault
- *(wrong)* Azure Active Directory (Azure AD) administrator account. (only for **administrative** work)

# Part 6: Describe Azure cost management and service level agreements

The cost of Azure services can be flexibly selected as either capital expenditure (CapEx) or operating expenditure (OpEx)?
- True

Using cloud is cost-effective because it provides managed traffic control
- False
- The fact that traffic control is provided in a managed manner does not affect cost reduction in response to fluctuations in demand. By using the cloud, you can use traffic distribution processing such as ELB and network traffic control such as Firewall. This does not specifically guarantee cost efficiency in response to fluctuations in demand

You can access the MSDN Support Forums by setting up a pay-as-you-go subscription.
- **TRUE**

minimum number of virtual machines
- 2. Based on the VM's SLA, deploying at least two VMs on two AZs guarantees 99.99% availability
- [SLA for Virtual Machines](https://www.azure.cn/en-us/support/sla/virtual-machines/)

Azure resources are available in all regions, not all regions are available to users
- there is an Availability Zone that is specially assigned to the US Government and has restricted general use.
- The special regions are: 1. US Government Virginia and US Gov Iowa 1.1. Physically and logically isolated Azure instances. For US government agencies and partners (run by selected US personnel). Includes other compliance certificates such as FedRAMP and DISA.

Azure services are available to all Azure users during ____
- **public preview**
- *(wrong)* Enterprise Agreement (EA) Subscription, private preview, development. All the three are only available to some users

Which of the following explanations about Azure usage costs is correct?
- Azure provides flexibility for capital expenditure (CapEx) and operating expenditure (OpEx).
- *(wrong)* If you create two Azure virtual machines of the same size, the monthly usage fee for each virtual machine will be exactly the same. (it also depends on the region where the virtual machine is located, as each  has a different cost)

If Microsoft plans to end support for Azure services that do not have a successor service, Microsoft will provide a notification at least _____________in advance
- **12** months

The Developer Support Plan allows you to contact a Microsoft support engineer by phone or email.
- False

The Basic Support Plan allows you to contact a Microsoft support engineer by phone or email.
- False

What is the maximum number of virtual machines that can be set in a virtual machine scale set?
- 1000

What is the "network" layer of network security?
- Subnet configuration
- *(wrong)*

correct statements below of the documentation provided by the Microsoft Service Trust Portal.
- Documentation that can be used to show Microsoft's compliance efforts
- **Penetration test results**. you can see the results of penetration testing by an independent third party. 
- **Security Evaluation**. 

Which of the following can Azure App Service Environment host? Please select two
- Docker container
- Functions
- *(wrong)* Database script
- *(wrong)* packaged code

Which **container** is used to collect logs and metrics from various Azure resources?
- Log Analytics Workspace
- *(wrong)* Azure Monitor Space. (no such service called by this name)

Select all the tools that can deploy resources according to the Azure Resource Manager model.
- Azure Portal
- **Powershell**
- CLI
- REST API
- **SDK**. (a collection of libraries built to make it easy to use Azure services in your language of choice)

What do you use to protect your Azure virtual network subnet?
- Network security group.
- *(wrong)* Azure Firewall. (portect VNets itself, not sbunets)

Which database service is specially designed to respond very fast to low latency data processing requests?
- Azure Cosmos DB
- *(wrong)* Azure Data Warehouse. a service that brings together tools for data warehousing and big data analysis.  

Which of the below corresponds to the minimum SLAs that an availability set has when **more than one** virtual machine is deployed in the same AZ.
- 99.95%

What is the maximum amount of Azure storage space that can be stored in one subscription?
- Almost unlimited


Which tools or services will find issues affecting the Azure global network? Please select all that apply.
- Azure Monitor
- **Resouce health blade for each virtual machines**
- Azure service health

You use RDP when accessing your Windows server. Also, you use SSH when accessing your Linux server. Select all recommendations to secure these protocols.
- Do not allow direct public internet access to the server through RDP and SSH ports.
- Set up access from the public internet using the Bastion server.
- *(wrong)* Enable RDP access using the Windows Services Control Panel Administrative Tools. (not a security recommendation in of itself.)

Which is considered part of the architectural **security layer**?
- Firewall configuration
- *(wrong)* Virtual network configuration
    
The availability of resources on demand is an example of scalability
- TRUE. (Being able to scale resources according to your needs is called scalability)

Achieving a flexible infrastructure configuration is an example of agility
- False. (Flexible configuration and resource allocation is called flexibility or elasticity.)

Making certain Azure services unavailable to certain users is possible with Azure policy
- False. (Azure policy evaluates the state of a resource for the entire account as it complies with the policy, rather than allowing only specific users to access the resource group.)

Azure Functions can be used for **continuously** running backend applications.
- False
    - Azure Functions is designed for short code that starts and ends quickly. You can use this to build simple applications that execute code serverlessly. Therefore, it is not well suited for continuously running backend batch applications.

What services do you need to use in order to take advantage of the Just-In-Time (JIT) Virtual Machine (VM) access feature?
- Azure Security Center
- *(wrong)* Azure NAT gateway. (With Azure Front Door, it's a feature that configures the routing of web applications)

correct description of the way to access the data stored in the archive access layer of your Azure storage account
- **Rehydrate** data from the archive layer (Rehydrate archived blobs hot or cool by changing the tier using the Set Blob Tier operation)
- Copy Blobs operation to make a new copy of the archived blobs. Specify a different blob name and hot or cool as the destination layer

You have created 5 virtual networks and 10 virtual machines and you want to control inbound traffic. What kind of settings do you need
- Azure Firewal
- *(wrong)* Network Security Group (NSG)

correct action to take if you want to increase your Azure subscription limit.
- make a new support request
    - request an increase in the limit by creating an Azure support request

You are mapping a network drive to Azure Storage from multiple computers running Windows 10. Choose the action you need to take to create a storage solution in Azure for the mapped drive.
- Azure Files. (can be attached/detached for sharing)
- *(wrong)* VM data disk. this adds additional capacity on only VM, and is not for a shared storage solution.

You have set up four virtual machines and are implementing traffic control with a public load balancer. What do you need to configure in order to transfer all Remote Desktop Protocol (RDP) connections to only one virtual machine?
- Inbound NAT rules. (use a load balancer to create inbound NAT rules to port traffic from a particular port on a particular front-end IP address to a another port on another backend instance in your virtual network)

Which file type do you need to use to copy files into your storage account using the Azure Import / Export service?
- CSV file. (The Azure Import / Export service can securely import large amounts of data into Azure Blob Storage and Azure Files by sending disk drives to your Azure datacenter.  )
- *(wrong)* JSON File.

our company has a public DNS zone for example.com. You also have an Azure AD tenant example2.com in your Azure environment. What type of DNS record do you need to create if you add example.com as a custom domain name to Azure AD?
- TXT. (TXT DNS record type)

You are planning to migrate your server from your on-premises environment to Azure. The DB server must be configured on a separate network segment to ensure data security. Which Azure solution should you choose to achieve this?
- Divide the **virtual network** for the DB server and another virtual network for all other servers.
- *(subnet)*. (resources are in the same VNet, which will fail)

Which billing accounts are supported by the Azure portal? Please select all applicable items.
- Microsoft online Service Program
- Ms Customer Agreement
- Ms Enterprise Contract
- Ms Partner Agreement
- *(wrong)* Paid subscription account.

You need a private connection between your Azure datacenter and your on-premises infrastructure. Which solution would you like to use?
- Azure ExpressRoute. (on-premise)
- *(wrong)* Virtual network gateway

You plan to store shared documents in blob storage. Since this data is stored over the medium to long term, it is necessary to be able to respond in the event of a disaster while keeping costs down as much as possible. Choose the appropriate storage redundancy type.
- Geo Redundancy. (high availability)
- *(wrong)* Local Redundancy. (not recommended for high availablity)

What is the **incorrect** option in regards to the range of guidance topics provided by Azure Advisor?
- Redundancy

correct statement about Azure **public review**.
- It can be used for a lower price than general availability.
- *(wrong)* they are used from a dedicated portal

Users are encouraged to use regions that are geographically close to each other. Why are they encouraged this?
- To ensure lower latency. (user are closer to the datacenters)

Azure Cost Management and Billing can help you with cost optimization
- False. (Azure Advisor provides advice on cost optimization)

To build a hybrid cloud configuration, you need a private cloud.
- False?. (You can also build a hybrid cloud configuration by using multiple public clouds)
- should be true. Multe-cloud is not hybrid

You can use Azure Cost Management to get information about the expected costs of a resources in Azure.
- False

When you implement efficient permission management by dividing users into groups and setting permissions, you would set groups with Azure management group.
- True. (Management groups enable efficient privilege management by dividing users into groups and setting permissions.)

Your company has decided to use a free Azure account to verify if Azure resources are suitable for their needs. With this free account you can test all services for up to 3 months.
- False. (limited to 30 days.)

Three months after you set up your Azure free account, you'll still have free access to a subset of Azure services.
- True. (a subset = a part of)

A Media company is considering using Microsoft Azure. They are currently using Microsoft Active Directory and so they need to work with Azure AD. For this, they can use the “Inter-Consumer (B2C)” feature of Azure AD to manage their customers.
- True. (Azure Active Directory B2C provides a business-to-consumer (B2C) identity as a service. Customers can use their favorite social, enterprise, or local account IDs for single sign-on access to applications and APIs.)

In order to use the Azure AD service, you need to implement a domain controller in your Azure virtual machine.
- False. Azure Active Directory is provided as a managed service and does not require any environment setup such as installation on the user side)

Your company has objects stored in Azure Blob Storage. What action do you need to take before accessing these objects?
- Rehydrate the objects. (Objects stored in BLOB storage are in the archive tier)
- *(wrong)* change the type of the objects. (should set tier)

You are developing a web application using Azure. This application needs to collect events from multiple sources and process them on the application. Which service can you use to meet this requirement?
- Azure Event Grid. (event-based architecture)
- *(wrong)* Azure Iot Hub

Which of the following services is used to store virtual hard disk files for virtual machines?
- Azure Backup

Azure Active Directory Premium P1 also includes advanced identity protection and Privileged Identity Management features?
- False. (p2 includes the both)

ufficient redundancy is required to access services on the virtual machines, ensuring access even if one **data center** goes down. To achieve this, you should use a scale set to deploy a set of virtual machines in a single Availability Zone.
- True

Redundancy is required to ensure access to services on virtual machines, even in the event that one AZ goes down. For this, you should use a scale set to deploy a set of virtual machines in multiple Availability Zones.
- True

Redundancy is required so that access to your services on your virtual machines is ensured, even in the event that one region goes down. For this, you should deploy a set of virtual machines in two or more Availability Zones.
- False. (should deploy the set of virtual machines in two or more regions with the appropriate traffic configuration)

You want to develop a web application hosted on a virtual machine. This application needs to store petabytes of data and requires complex queries across the data. Which service should you use?
- Azure Synapse. (Azure Synapse is an enterprise analytics service that speeds the time to retrieve analytics across data warehouses and big data systems.)
- *(wrong)* Azure Cosmos DB. (unable to execute SQL)

You are deploying 4 virtual machines on Azure. These virtual machines host your web application. To improve the application's availability, you should configure scale sets for the virtual machines.
- True. (You can increase the availability of your application by adding virtual machines to the virtual machine scale set.)

You can manage devices using Azure AD (Active Directory) features
- True. (Azure Active Directory manages how cloud or on-premises devices access your company's data. Register your device ID and provide a centralized place to manage it.)

You can use Microsoft Active Directory to set permissions, by dividing users into groups and setting permissions.
- False
    - Azure Active Directory (Azure AD) enables identity management and security with single sign-on and multi-factor authentication. However, it is not possible to divide users into groups and grant permissions.
    - To divide users into groups and set permissions on a per-group basis, it is recommended that you take advantage of managed group or Azure role-based access management controls.

With ____, developers can deploy code and pay for its **run time** only, without worring about the provisioning, configuration and management of the underlying infrastructure.
- Serverless Computing
- *(wrong)* Iaas. (OS and run-time to manage)
- *(Saas)*. (Cannot deploy code)

A subscription can have only one license?
- True

Company plans to use a custom SaaS application and wants to minmize costs. The company should be able to maintain and secure all data onsite legally
- Hybrid Model

It's customer's responsibility to retain the data
- True

Company wants to host data disks on Azure. The data disks must be available to other on-premises machines using network sharing via Server Message Block protocal. Data must be secure both in-transit and at rest.
- **File Storage**

Which Azure resource can be classified as Software-as-a-Service
- Azure Internet-of-Things (IoT) Center
- *(wrong)* API Management

Which feature of Azure Monitor allows you to visually analyze telemetry data by integrating with Visual Studio
- Application Insights
- *(wrong)* Metrics

Which services should you use to analyze large volumes of streaming data being collected from Internet of Things (IoT) devices?
- HDsight

A company is considering using Linux-based Azure Container Instances (ACIs) to deploy a simple application. The application runs as a stateful application. The service should provide storage to retrieve and persist state.
- Azure Files
- *(wrong)* Azure Blob
- *(wrong)* Azure Disk

Which feature of Azure Monitor sends an email to an administrator when a virtual machine is about to exceed its usage quto for the month?
- Service Health
- *(wrong)* Alerts

All Azure free accounts expire after a specific period?
- True

one MS account can only creat **one** free Azure account

A company is planning to build a solution for an automobile manufacturing company. The solution should permit vehicles to send on-board diagonostic sensory and vehicle telemetry data on the cloud for **analysis**. The solution should indentify individual vehicles from the data that is sent.
- IoT Central
- *(wrong)* IoT hub

A subscription can have only one license?
- False. (a license can be assigned to each user account)

The responsiblity for accounts is transfered to the cloud  provider?
- False.

To what should an application connect to retrieve security tokens?
- Azure Active Directory
- *(wrong)* Azure Key Vault

Which regulation addresses data protection and privacy for all individuals in the European Union (EU)?
- General Data Protection Regulation (GDPR)

A company is going to start collecting data about your azure infrastructure with Azure Monitor. which type of data collection is required to enable diagnostics
- Event logs

what are conditional access:
- restricted by location
- compliant devices

Which US regualtion addresses protecting unclassified information created by the government and stored in non-gvoernmental systems?
- National Institute of Standards & technology (NIST) 800-171

A company can extend it's storage resources by implementing hybrid model for it's internal network
- True

Only guest users of the company can access resources in public cloud
- False. (Actuall, anyone can access only if permitted)

What are the characteristics of public cloud hosting? (two)
- Metered Pricing
- **Self-Service Management**

Is Authentication the process of granting access to perform an action?
- No
- (Authorizatioin will allow to perform a certain action)

Can you use Azure Blueprints to deploy resource groups to newer subscriptions?
- Yes

Can you use Azure Blueprints to deploy Role assignments to newer subscriptions?
- Yes

Are the SLA for Azure Virtual Machines the same irrespective of whether they are deployed across Availability Sets or Availability Zones?
- NO

Would the use of Spot Virtual Machines help to reduce the costs?
- NO

A development team is planning on creating a General Purpose-V2 storage account. They want to store files and ensure that each is accessible via a unique URL. Which of the following is the right service within Azure Storage Accounts that can be used for this purpose?
- Blob
- *(wrong)* File

Can you decide which paired region is used by the underlying Azure storage service?
- No

forms of verification that are possible with Azure AD Multi-Factor Authentication?
- SMS
- Voice call
- Microsoft Authentication App
- *(wrong)* Email
- *(wrong)* Photo Identification.
- bio metrics

Azure Support plan with a) 24/7 access to technical support by email and phone; b) Save on monthly costs
- **Standard Plan**
- *(wrong)* Professional Direct Plan

A company is planning on hosting a set of Azure virtual machines. One set is going to be hosted in the Central US location and the other set in the East US location. Would the cost for hosting the Azure virtual machine be the same , assuming the instance size and other aspects the same when it comes to the virtual machines?
- No. (The cost for resources differs from region to region.)

 want a managed service that can orchestrate the deployment and management of the containers
 - Azure Kubernets
 - *(wrong)* Azure container services.

Which of the following service is a high-level application platform that has built-in communication and security features for internet-connected devices?
- Azure Sphere
- *(Azure IoT Central)*

A company is planning on using an Azure service which is currently in public preview. Is an SLA provided for services that are in public preview?
- NO

A company needs to create around 50 customized Virtual Machines. Out of these 20 are Windows based Virtual machines and 30 are Ubuntu Machines. Which of the following would help reduce the administrative effort required to **deploy** the machines?
- Azure Scale sets. (one set for win, another set for Ubuntu)
- *(wrong)* Azure Load Balancer. (can be used for Scale Sets, but it is only used to divert traffice)

Which of the following is true when it comes to SaaS?
- You are responsible for configuring the solution
- *(wrong)* You are responsible for scalability of the solution

An IT administrator for a company has been given a powershell script. This powershell script will be used to create several Virtual Machines in Azure. You have to provide a machine to the IT administrator for running the powershell script. You decide to provide a Linux machine which has the Azure CLI tools installed. Would this solution fit the requirement?
- NO. (We can execute Powershell scripts on Linux only when *Powershell Core and Azure CLI* is installed)
- https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/deploy/azure-cli?view=azure-devops https://docs.microsoft.com/en-us/azure/virtual-machines/linux/run-command

An IT administrator for a company has been given a powershell script. This powershell script will be used to create several Virtual Machines in Azure. You have to provide a machine to the IT administrator for running the powershell script. You decide to provide a ChromeOS based machine and use Azure Cloud Shell Would this solution fit the requirement?
- Yes. (From the Azure Portal, if you use Azure Cloud Shell, you can run both Bash and powershell based scripts)

you can install Powershell on MacOS and then run the powershell scripts For more information on installing powershell on MacOS. (https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-macos?view=powershell-6)

A company has a set of resources deployed to Azure. They want to make use of the Azure Advisor tool. Would the Azure Advisor tool alone be able to give recommendations on how to improve the security of the Azure AD environment?
- No.
    - Azure Advisor integrates with Azure Security Center to give security recommendations
    - Azure Security can give you recommendations on how to secure your resources in Azure

A company is planning on hosting solutions on the Azure Cloud. They need to implement MFA for identities hosted in Azure. Is it necessary to deploy a federation solution or sync on-premise identities to the cloud?
- NO. 

A company wants to host their applications on Azure using serverless components. They don’t want to manage the underlying infrastructure for the application. Which of the following could be used to implement a workflow that could be run on a serverless infrastructure?
- Azure Logic Apps. (host app)
- *(wrong)* Azure Fucntion App. (host functions)

A company wants to try out some services which are being offered by Azure in Public Preview. Should the company deploy resources which are part of Public Preview in their production environment?
- NO. (there is no SLA or guarantee)

Which of the following is a feature of the Azure SQL Datawarehouse architecture?
- Scalability
- *(wrong)* High Availability

A company is planning on using Azure Storage Accounts. They have the following requirement: 1)Storage of 2 TB of data;2)Storage of a million files Would using Azure Storage fulfill these requirements?
- Yes. (a blob max 200TB, and no limit for number of blobs)

The company needs to know if the underlying infrastructure in Azure hosting the Virtual Machine has any issues? Where could they view such issues?
- The Virtual Machine Blade
- *(wrong)* Azure Advisor

Would the Azure Advisor tool give recommendations on how to configure Virtual Network settings?
- No

want to have a comprehensive solution for collecting, analyzing, and acting on telemetry from your cloud.
- Azure monitor
    - Azure Monitor maximizes the availability and performance of your applications and services by delivering a comprehensive solution for collecting, analyzing, and acting on telemetry from your cloud and on-premises environments
- *(wrong)* Azure Event hubs
    - a big data streaming platform and event ingestion service

A company has a virtual machine defined as demovm. This Virtual Machine was created with the standard settings. An application is installed on demovm. It now needs to be ensured that the application can be accessed over the Internet via HTTP using prioritized security rules and port ranges You make modifications to the Azure firewall Would this solution fit the requirement?
- No. (Azure Firewall we can only add normal security rules but we CANNOT "prioritize" the security rules)
- (correct way) "prioritized security rules" can only be added through a "network security group"

the support plan Ensure that for high severity cases, there is a response within 10 minutes A recommendation is made to purchase the Professional Direct Support plan Would this recommendation fulfil the requirement?
- no. (professional direct is within 1 hour)

to transfer billing ownership of the subscriptions between your company's accounts Does your administrator need to contact Microsoft for this activity ?
- no. (go to your subscription, there will be a Transfer subscription option)

A company needs to deploy several virtual machines. Each of these virtual machines will have **the same set of permissions**. To minimize the administrative overhead, in which would you deploy the Azure Virtual Machines
- Azure Resource Groups

A company needs the list of planned maintenance events that can affect the availability of an Azure subscription. Which of the following would help them achieve this requirement?
- Help + Support
- *(wrong)* Security Center

A company needs the list of planned maintenance events that can affect the availability of an Azure subscription. Which of the following would help them achieve this requirement?
- Help + Support. (re-direct to 'Service Health')

Provide an option to contact Microsoft support engineers by phone or email A recommendation is made to purchase the Standard Support plan
- Yes. (24x7 access to Support Engineers via email and phone)

A company has 100 machines in their on-premise environment. They want to **extend** their infrastructure without too much extra capital or operational expenditure. Which of the following could they opt to carry out for this requirement?
- migrate all to the public cloud

 You need to ensure that traffic can flow into the Virtual Machine on port 8080. Which of the following must you modify to make this work?
- Network Security Group (always). (inbound: destination port rage - 8080)
- *(wrong)* Network Interface Card

A company wants to host a set of tables in Azure. They want absolutely zero administration of the underlying infrastructure and low latency access to data. You recommend using the CosmosDB service? Would this suit the requirement
- Azure Sql database
- Azure Cosmos DB
    - fully managed service with low latency access to data
    - has a table API to work with Table-like data

Used to analyze data on End user devices
- IoT Edge
- *(wrong)* IoT central

A company wants to implement an IoT solution using the service available in Azure. Which of the following would meet the below requirement? “Helps provide a powerful data exploration and telemetry tools to help you refine operational analysis”
- Azure Time Series Insights (IoT deployments)
    - an end-to-end PaaS
    - to ingest, process, store and query highly contexualized, time-series-optimized IoT-scale data.
    - is ideal for ad-hoc data exploration and operational analysis
- *(wrong)* IoT central

protect their resources against DDoS attacks and also get real time attack **metrics**
- DDoS Portection Standard

A company is planning on deploying an Azure Windows Server 2016 virtual machine. Could a VPN be used to encrypt all traffic from the virtual machine itself to a host on the Internet?
- Yes. (You can install roles such as the Remote Access Server for VPN to ensure traffic is encrypted when it flows out of the server)

want to reduce the costs for resources hosted in Azure They decide to remove the network interfaces from Azure AD Would this fulfil the requirement
- No. (network interface is free)

want to *create and update* the resources as a group, rather than handling them individually, within the Azure subscription.Which of the following could be used for this requirement
- Azure Resource Manager
- *(wrong)* Azure Resource groups.

Ensure that the Virtual Machine Administrator team can only deploy virtual machines and their dependent resources.
- azure RBAS (role for virtual machine access)
- *(wrong)* Azure Polices

Is it possible for the Azure Advisor tool to give a list of Azure virtual machines that are currently not enabled by Azure Backup?
- **Yes**.

advantages of using a hybrid cloud model?
- **better control**
- More Flexibility
- *(wrong)* Less Maintenance

Is there a default spending limit when it comes to the spending limit for the Azure free account?
- **YES**

They then decide to use the File service to store the user data. Is this the ideal service for storage of user related data
- **NO**. (Files is used when you want have files that can be accessed via the SMB 3.0 and HTTPS protocol)

They then decide to use the Table service to store the user data. Is this the ideal service for storage of user related data?
- **YES**

to ensure that the services on the virtual machines are still accessible even if a single data center goes down. They decide to deploy the set of virtual machines to two or more regions
- **Yes**

Is it possible to manage *external partners* using the "Business-to-Customer (B2C)" feature of Azure AD
- No. (Using the "Business-to-Business (B2B)" feature of Azure AD you can manage your guest users and external partners)

Which of the following category does Azure Kubernetes come under
- **IaaS**

A company needs to deploy a server named “evotechserver” to the Azure cloud. The company’s policy states that the server needs to be deployed on a separate network segment. Which of the following could be used to deploy the server to ensure that it’s meet the company policy?
- A separate virtual network
- *(wrong)* A separate account for the server

Provide a service that could help **store** objects that could be accessed from anywhere around the world via HTTP Which of the following would be best suited for this requirement?
- Azure Storage Accounts
- *(Azure Application Gateway)

Provide capabilities to perform Big Data analytics over data stored on Azure Blob storage Which of the following would be best suited for this requirement?
- Azure Data Lake Storage ()

to get alerts whenever the CPU of the virtual machines goes beyond a certain threshold
- Azure Monitor. (can create alerts in Azure Monitor based on the virtual machine metrics)

Does the Cosmos DB service provide the ability to create different types of data stores such as Mongo DB and Cassandra?
- **YES** (Cosmos DB is a multi-model database)

if there is any way to have a reduction in costs for running the virtual machines in Azure
- Advisor. (at Azure Advisor, it can actually give you a purchase recommendation on how you can reduce costs)

availability metrics you would get from customers to understand the acceptability SLA for an application
- Mean time to recover (MTTR)
- Mean time between failures (MTBF)
- *(wrong)* Mean time to success (MTTS)
- *(wrong)* Mean time to failure (MTTF)

Every Region has multiple Datacenters.
- True

You have been tasked with ensuring that virtual machines continue to run if a datacenter fails. Bob Ross, your co-worker, suggests that you create virtual machine scale sets. Does this meet the requirement?
- **YES** (you can use Availability Zones to automatically distribute VM instances in a scale set within a single datacenter or across multiple datacenters.)

allow more resources on demand to stop the application from running in a degraded state when reports are generated
- Elasticity. (allows applications to consume more resources on demand, then release those resources when resource demand is lessened)

Which of the following Azure features is most likely to deliver the most immediate savings when it comes to reducing Azure costs?
- Using Azure Reserved Instances for most of your virtual machines. (the most, >40%)
- *(wrong)* shutdown VMs overnight and on weekends.

What service does Azure provide as an optional upgrade to protect against DDoS attacks?
- Azure DDoS Protection Standard. (upgrade from basic)
- *(wrong)* Advanced Threat Protection

What makes a system highly available?
- A system specifically designed to be resilient, with no single point of failures
- *(wrong)* Must have a minimum of two VMs

Which tool within Azure helps you to track your compliance with various international standards and government laws?
- Complance Manager. (exact tool)
- *(wrong)* Service Trust Portal

One of the benefits of the cloud is agility. What does that mean in the context of the cloud?
- The ability to respond to and drive **market change quickly**
- *(wrong)* The ability of a system to grow it's capacity easily when it reaches full capacity

What is the concept of being able to get your applications and data running in another environment quickly?
- Business Continuity / Disaster Recovery (BC/DR)
- *(wrong)* Reproducible deployments

What does it mean if a service is in Public Preview mode?
- Anyone can use the service but it must not be for production use
- *(wrong)*Anyone can use the service for any reason

What is the Azure SLA for two or more Virtual Machines in an Availability Set?
- 99.95%
- *(wrong)* 99.99%. (scale set has lower SLA)

all features part of Azure AD?
- Custome banned password list
- Smart lockout
- **Device Management**
- Single sing-on
- *(wrong)* Log Alert Rule

What is the benefit of using a command line tool like Powershell or CLI as opposed to the Azure portal?
- **Automation**
- *(wrong)* Quicker to deploy VMs

What would be a good reason to have multiple Azure subscriptions?
- There is one person/credit card paying for resources, but many people who have accounts in Azure, and you need to separate out resources between clients so that there is absolutely no chance of resources being exposed between them.

What types of files can a Content Delivery Network speed up the delivery of?
- **JavaScript files**
- PDFS
- Images
- Videos

Which of the following elements is considered part of the "perimeter" layer of security?
- Use a firewall
- ~~Locks on the data center doors~~

Approximately how many regions does Azure have around the world?
- 60+ (There are 60+ Azure regions currently, in 10+ geographies)

Which tool within Azure is comprised of : Azure Status, Service Health and Resource Health?
- Azure Service Health
- ~~Azure Monitor~~

If you have an Azure free account, with a $200 credit for the first month, what happens when you reach the $200 limit?
- All services are stopped and you must decide whether you want to convert to a paid account or not.
- ~~You cannot create any more resources until you add more credits to the account.~~

How many hours are available free when using the Azure B1S General Purpose Virtual Machines under a Azure free account in the first 12 months?
- **750**

What is the core problem that you need to solve in order to have a high-availability application?
- **You need to avoid single points of ilure**

How many minutes per month downtime is 99.99% availability?
- **4** (4/m)

What operating systems does an Azure Virtual Machine support?
- **Windows and Linux**
- ~~Windows, Linux and macOS~~

Which style of computing is easiest when migrating an existing hosted application from your own data center into the cloud?
- **IaaS**
- ~~Serverless~~

rue or false: Azure PowerShell scripts and Command Line Interface (CLI) scripts are entirely compatible with each other?
- NO. (PowerShell is it's own language, different than CLI)

Which of the following resources are not considered Compute resources?
- Load Balancer. (A load balancer is a networking product, and does not execute your code.)
- ~~Function Apps~~

If you wanted to deploy a virtual machine to China, you would just choose the China region from the drop down.
- False. (Some regions of the world require special contracts with the local provider such as Germany and China.)