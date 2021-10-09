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