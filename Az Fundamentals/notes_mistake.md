https://github.com/wzlwit/workshop/blob/main/Az%20Fundamentals/notes_mistake.md

# Part 1: Describe core Azure concepts
It is desirable to design Azure architecture based on the principles of a flexibility and elasticity in your cloud architecture. How do you achieve this?
- Automate scaling on-demand
- *(wrong)* Implement infrastructure coding and sharing. used to facilitate environmental automation.
- *(wrong)*Collect security data in Azure Sentinel.

What's the best way for Tailwind Traders to limit all outbound traffic from VMs to known hosts?
- Create application rules in Azure Firewall.

How can Tailwind Traders most easily implement a deny by default policy so that VMs can't connect to each other? 
- Create a network security group rule that prevents access from another VM on the same network.

Where can the legal team access information around how the Microsoft cloud helps them secure sensitive data and comply with applicable laws and regulations?
- Trust Center. 

Where can the IT department find reference blueprints that it can apply directly to its Azure subscriptions
- *(wrong)* Online Services Terms. The Online Services Terms is a legal agreement between Microsoft and the customer that details the obligations by both parties with respect to the processing and security of customer data and personal data. 
- Azure compliance documentation. The compliance documentation provides reference blueprints, or policy definitions, for common standards that you can apply to your Azure subscription. 

What's the SLA for Azure Maps in terms of guaranteed uptime
- 99.9 percent

You want to send messages from the IoT device to the cloud and vice versa. Which IoT technology can send and receive messages
- IoT Hub
- *(wrong)* IoT Central

Organizations hosting infrastructure in a ______________ do not need a data center
- Public cloud
- exp:
    - In the public cloud, the cloud vendor manages the data center, so users of the public cloud do not need a data center.
    - The private cloud requires a data center in order to host infrastructure.
    - A Hyper V host is a hypervisor that provides a virtualized environment.

Which group of data centers are connected by a fast network that is geographically separated in Azure?
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
- *(wrong)* Azure Govenment. Azure Government is a mission-critical cloud that delivers breakthrough innovations to US government customers and their partners. Only the US federal government, state governments, local governments, tribal governments, and their partners have access to this dedicated instance and operation are managed by selected US citizens.

Users can leverage their data center to deploy Azure services?
- FALSE (should use Azure Stack)

database:
- Azure Cosmos DB is a fully managed NoSQL database service for modern app development. Guaranteed single-digit millisecond response time and 99.999% availability. Azure Cosmos DB can store JSON documents.
- Azure SQL Data Warehouse is a fully managed cloud data warehouse. You can get query results in a short time across terabytes and petabytes of data.  
- Azure SQL Database is a fully managed, intelligent relational cloud database
- Azure Cache for Redis. A fast, fully managed in-memory data store. Not suitable for storing JSON documents

Each region has at least three separate zones?
- True

You can merge two Azure subscriptions into one by creating a support request?
- False
- You can't merge two subscriptions in Azure. It is incorrect because each subscription is a separate entity that cannot be merged. Alternatively, you can transfer ownership of a subscription to another account. In this case, you will need to manage two subscriptions with one account. 

__________ is an Azure service that detects and diagnoses web app anomalies.
- Azure Application Insights 

Data traffic between Azure services within the same Azure region is always free.
- Yes. if you're in the same region, Azure does not charge you for data transfers .

Azure Information Protection
- allows organizations to label content to detect, classify, and protect **documents** and **email**.
- This extends the labeling and classification capabilities provided by Microsoft 365.
- **can not** encrypt: 
    - records in Azure SQL Database
    - Azure storage account (to Encrypt stored data using the encryption service implemented in Azure services Encryption at Rest)
    - network traffic (To encrypt network traffic, you need to configure TLS.)


# Part 3: Describe core solutions and management tools on Azure
CLI
- You can use Bash from Cloud Shell by logging in to the Azure portal from your Android laptop. Then you can create a new virtual machine from Bash with CLI. Cloud Shell is a management machine for Azure, managed by Microsoft.
- Azure Cloud Shell gives you the flexibility to choose the best shell operation for your business.
- Both Bash and PowerShell are options for this.

Which service could help you manage the VMs that your developers and testers need to ensure that your new app works across various operating systems?
- Azure DevTest Labs
- *(wrong)* Azure Test Labs. Azure Test Labs is used to create automated tests, but not to manage VMs to test across various environments

Your company wants to use a serverless application to automate the data registration process. Which Azure service should you use?
- Azure Functions. an event-driven serverless computing platform that can solve complex orchestration problems. You can use this to develop serverless applications.
- *(wrong)* Azure App Service

using multiple Azure virtual machines to ensure that the services running on the virtual machine do not stop in the event of a single data center failure. Proposed Solution: Deploy virtual machines in two or more regions. Is this the most appropriate solution
- No. 
- A single region is made up of multiple availability zones. Therefore, to prevent a single data center failure, you only need to use multiple **availability zones** and do not need to have a multi-region configuration. In addition, multi-region support is not optimal in terms of architectural configuration because it is difficult to link virtual machines across regions.

Which deployment method should you choose to reduce downtime for the application you are deploying?
- Mutli-AZ deployment. **A**vailability **Z**one
- *(wrong)* multi-region deployment
- Administrators can lock subscriptions, resource groups, or resources to prevent accidental deletion or modification of critical resources
    - Delete locks allow legitimate users to read and modify resources, but cannot delete them
    - Read-only locks allow legitimate users to read resources, but cannot update or delete resources

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
- Azure DevTest Labs
- *(wrong)* Azure virtual machine scale set. allow you to create and manage groups of virtual machines and distribute the load within the same group, which is used when building large-scale services


As an operations manager, you are in charge of managing each service in Azure. You need to find advice about maintenance-related events for Azure resources. Which service located on the Azure portal would you use?
- *(wrong)* Azure Advisor
- Help and support. You can find more information about maintenance in the help and support on the Azure portal. Planned maintenance information can be found on the Service Health page

Is the following true?"The cost of Azure services in private preview decreases as the service becomes publicly available."
- No

private preview
- this feature is always free.
- Private previews are usually the first release of a product and are to help customers try out the service, provide feedback, verify if the service is actually needed, and shape the future of the product.
- In general, the number of customers invited to private previews is limited, and these customers are expected to spend time with the product to provide feedback.
- When the service becomes publicly available, it will be in full production mode. Fully supported by SLAs, customer support, and run on production workloads. Since the service is now running normally, you will be charged for it.

Which Azure service can be used to collect events from multiple resources into one repository?
- Azure Event Hub. Azure Event Hubs is a big data streaming platform and event capture service. It can receive and process millions of events per second. By using Azure Event Hubs, you can import events from multiple resources into a centralized repository.
- *(wrong)* Azure Monitor.

From ______, you can track company regulatory standards and regulations such as ISO27001.
- Compliance Manager. allows you to track, assign, and validate regulatory compliance activities for organizations related to Microsoft cloud services.

You can download the regulatory compliance report from the Azure Security Center.
- Yes. A new feature in Azure Security Center, the Regulatory Compliance Dashboard, is now available. This compliance dashboard continuously monitors your Azure and hybrid environment against specific compliance requirements. It can also provide security assessments and recommendations as needed. 

Companies can extend their internal network by adding their physical servers to the public cloud
- **No**

Inbound data traffic from your on-premises network to Azure is always free when using Azure ExpressRoute connections
- Yes. Azure Express Route is used to transfer data from your on-premises datacenter to Azure Public Cloud. When you use Express Route to transfer data from your on-premises datacenter to the Azure public cloud, you are not charged for inbound data transfer.

On-demand flexibility is one of the benefits of using IaaS on the Azure cloud
- The advantage of the cloud is that you can quickly and flexibly build, delete, or expand infrastructure such as servers as needed

Infrastructure management flexibility is one of the benefits of using IaaS on the Azure cloud
- False
- Physical infrastructure management is often not possible on the part of the user. Therefore, infrastructure management is inflexible and requires very limited management options for the user

Your company is planning to purchase an Azure support plan. The main reason for this choice is to have access to a dedicated team from Azure to provide architectural support to the company and your new Azure environment creation.Which support plan should you choose to gain access to this?
- Professional Direct. 
- Only Professional Direct (ProDirect) Advisory support provides architectural support for Azure environments. This plan provides access to Azure support guidance based on publicly available best practice documentation for Microsoft Azure and information from the Azure forums. ProDirect advisors support users based on their access to Microsoft-related documentation, Microsoft Azure support engineers, and Microsoft Azure product groups.

# Part 4: Describe general security and network security features

Trust Center
- The Trust Center implements Microsoft's principles for maintaining data integrity in the cloud and Microsoft implements security, privacy, compliance, and transparency in all Microsoft cloud products and services. it is a web page that contains information and details about how Microsoft supports security, privacy, compliance, and transparency in all Microsoft cloud products and services, and is not relevant here.
-  The Trust Center is an important part of the Microsoft Trusted Cloud Initiative, providing support and resources to the legal and compliance community

You need to be aware of the latest Azure security standards to protect your data.Which of the following services should you use to ensure this?
- Trust Center
- *(wrong)* Azure compliance documentation


Azure Security Center offers free and paid services
- The free tier only provides security policies, ongoing security assessments, and practical security features that help protect your Azure resources
-  Paid services extend the free tier functionality and add:
    - **threat protection**. It uses built-in behavioral analytics and machine learning to identify attacks and zero-day exploits, and uses access and application control to reduce exposure to network attacks and malware.
    - **virtual machine vulnerability scan**.

You are planning to extend your company's network to Azure to create a hybrid cloud configuration. In the on-premises environment, a VPN appliance that has the IP address of 136.168.103.1 is used and it is necessary to identify this on the Azure side. Which is the best solution for this situation?
- local network gateway. can be used to specify the IP address of the VPN device in the virtual network. This allows Azure to identify VPN appliances that use the IP address of 136.168.103.1.

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
- *(wrong)* Protection is automatically implemented without the need for user to implement their own data security measures.
- *exp* Users are required to take measures such as data encryption. 

Your company would use _________to automatically add watermarks to Microsoft Word documents that contain credit card information.
- Azure Information Protection

After you create a virtual machine, you need to change the _______ to allow the virtual machine to connect to TCP port 8080
- Network Security Group (NSG). By default, all inbound connections are not allowed on L4, so unless you have a network interface, you need to modify the rules of the network security group so that all inbound connections from port 80/8080 can reach the VM
- *(wrong)* virtual network gateway. a VPN device in the Azure virtual network that is used to set up a site-to-site VPN connection between the Azure virtual network and the local network, or a VNet-to-VNet VPN connection
- *(wrong)* virtual network. nothing more than a private isolated network in Azure, because it is used to enable Azure resources such as virtual machines to communicate securely with other Azure resources, the Internet, and resources in your on-premises network
- *(wrong)* Azure route table. only contains a set of rules (routes) that specify how packets are routed in the virtual network

create an Azure virtual machine using your Android laptop. Solution: Use the PowerApps portal
- No
- *(wrong)* Power Apps portal to create external websites that allow users outside your organization to sign in with different identities, create and view data in Microsoft Dataverse, and browse content anonymously. This is not the mechanism to use when creating a virtual machine

Your company is planning to move from an on-premises environment to Azure. Azure will only use PaaS solutions. You need to deploy the required Azure environment for this. Solution: Take advantage of Azure App Service and have Microsoft SQL Server installed. 
- **Yes**
- You can use .NET, .NET Core, Node.js, Java, Python, PHP running inside a container or on Windows or Linux

Which solution should You use to assess whether your Azure environment meets security regulatory requirements?
- Azure Security Center
- *(wrong)* Azure Advisor


You have been asked to "clean up" the Azure resources that you are not currently using to avoid incurring extra costs. Which of the following services should you remove to achieve this?
- Public IP address
    - Static public IP addresses in the ARM deployment model and reserved IP addresses in the ASM deployment model begin billing the from the second hour after the IP address has been created, taking into account the time needed to properly allocate the IP address.  Billing for this ends when you delete the IP address resource.
    - For all other public IP addresses, billing begins when the associated resource is started and ends when the associated resource is deleted or stopped and then deallocated. Therefore, it is possible to stop billing by deleting unused public IP addresses.  
- exp
    - There is no charge for private IP, whether static or dynamic.
    - Azure Virtual Network is **free**. You can create up to **50** virtual networks in all regions with each subscription.  
    - he network interface is free to use.

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
- Synchronization Service Manager. is used to configure the more advanced aspects of the synchronization engine and to verify the operational aspects of the service. This allows you to check the synchronization execution details and status.

One of the benefits of using IaaS on the Azure cloud is that it will reduce costs compared to on-premises environments
- False
- The cost is often cheaper by using the cloud, but there is no guarantee that it will be cheaper. Extra costs may be incurred if you overuse various services for weight billing. In addition, having your own infrastructure may reduce costs in the medium to long term

One of the benefits of using IaaS on the Azure cloud is that you can leave security measures to the cloud vendor
- **False**. 
- You need to take security measures based on the application you have. The responsibility for managing the security of an application or service depends on the cloud service model. Built-in features and partner solutions that can be deployed to Azure subscriptions have features available on the Azure platform that cover these responsibilities. In this case, security is still a responsibility of the user.

You want to build a serve rless application to perform simple application processing. Which is the best solution for this?
- Azure Functions.an event-driven serverless computing platform that can solve complex orchestration problems. You can use this to develop serverless applications.
- *(wrong)* Azure App service.

You need to implement an application that leverages Azure to automatically send email notifications. Choose the two best solutions for this.
- Azure Functions. event driven, serverless, can be used to send email
- Azure Logic App.

You need to perform data processing utilizing Hadoop clusters in the cloud.Which solution is best for this?
- Azure HDInsight. Azure HDInsight processes large amounts of data in managed **Hadoop** clusters on the cloud
- *(wrong)* Azure Databricks. integrates this collaborative Apache Spark-based analytics service with other big data services in Azure.  

Who would utilize the standards-based approach when adding functionality to applications that are targeted by Azure AD?
- Azure Developer

move resources between regions
- You can move Azure resources to another Azure subscription or to another resource group in the same subscription. You can use the Azure portal, Azure PowerShell, Azure CLI, or REST API to move resources.
- You can also use Azure Resource Mover to move resources to another region. Leverage Azure Global Infrastructure capabilities to seamlessly move resources to the region that best suits your needs. You can streamline your planning process, accelerate your travel and protect your resources.

In order to get a security token, what does the application need to connect to/ use
- Azure Active Directory. Developers can get security tokens using Azure Active Directory
- *(wrong)* Azure Key Vault



# Part 5: Describe identity, governance, privacy, and compliance features

You are building an application using a virtual machine in Azure. As a security requirement, it is necessary to apply Azure Multi-Factor Authentication (MFA) based on certain conditions.Which Azure service should you choose
- Azure Active Directory ID Protection. Azure Active Directory ID Protection allows you to apply MFA conditionally. It is also used to detect risks such as anonymous IP address logins, unfamiliar sign-ins, and credential leaks.
- Explanation:
    - Azure Monitor is incorrect because it collects what is known as "application monitoring data" (data about the performance and functionality of the code you write, regardless of platform). zure Monitor collects monitoring metrics from a variety of on-premises and Azure sources. It does not have the ability to centrally manage events.  
    - Azure Security Center is an integrated infrastructure security management system that enhances the security structure of the data center. It's an advanced threat protection feature that protects your entire hybrid workload, both on the cloud and on-premises. With this option, you can't use MFA.
    - Azure Security Center is a support service that helps you prevent, detect, and respond to threats by visualizing and controlling the security of your Azure resources. The Security Center continually views new resources deployed throughout your workload, evaluates whether they are configured according to security best practices, and flags them otherwise. It also provides a prioritized list of recommendations for the corrections needed to protect your machine. It provides integrated security monitoring and policy management across subscriptions and assesses whether your Azure environment meets regulatory requirements
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

Compliance Manager
- a workflow-based risk assessment tool listed on Microsoft's Microsoft Service Trust Porta
- allows you to track, assign, and validate regulatory compliance activities for organizations related to Microsoft Professional Services such as Microsoft Office 365, Microsoft Dynamics 365, and Microsoft Azure, as well as Microsoft Cloud Services.

There are regions that are not available to organizations that have business bases in the United States.
- true
- Organizations that do not have a business based in China will not be able to use the four regions of China. Global Azure is operated by Microsoft, but China is not available globally for political reasons. As a result, China Azure operates independently of Global Azure.

Azure Service Health:
- can set alerts for failures in Azure services
- can check the status of all services in the Azure Environment
- *(wrong)* can set preventive measures against failures. (cannot prevent failure)
- cannot apply for advice to Azure Support in ASH. (Apply for Azure support on the Azure support page)

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