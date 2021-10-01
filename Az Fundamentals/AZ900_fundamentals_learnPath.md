


[Application security groups](https://docs.microsoft.com/en-us/azure/virtual-network/application-security-groups)
- configure network security as a natural extension of an application's structure
- group virtual machines and define network security policies based on those groups
- (services for grouping virtual machines and managing access within a virtual network)

Azure Firewall
- a cloud-based managed network security service
- protects Azure Virtual Network resources. (not an user-built application)

Azure Information Protection (AIP)
- a cloud-based solution that helps organizations classify documents and emails
- by applying labels and can help to protect them


DDoS
- protection against DDoS attacks
- protects your website from a variety of **malicious** attacks 
- produces detailed **reports** on these attacks.

network security group
- filter network traffic to and from Azure resources in an Azure virtual network that has the network security group

Azure Application Insights
- a feature of Azure Monitor, an application performance management (APM) service.
- allows you to monitor running applications and automatically detect performance anomalies
- use built-in analytics tools to view what your users do on your app.

No access:
- Azure does not have permission to access the data

Tenancy
- defines how instances are distributed across physical hardware

End-to-end: describes a process that takes a system or service from beginning to end and delivers a complete functional solution, usually without needing to obtain anything from a third party
# Part 1: Describe core Azure concepts
## Introduction to Azure fundamentals
### why cheaper
- Lower your operating costs.
- Run your infrastructure more efficiently.
- Scale as your business needs change.

### why move to
In our ever-changing digital world, two trends emerge:
- Teams deliver new features to their users at record speeds.
- Users expect an increasingly rich and immersive experience with their devices and with software.

To power your services and deliver innovative and novel user experiences more quickly, the cloud provides on-demand access to:
- A nearly limitless pool of raw compute, storage, and networking components.
- Speech recognition and other cognitive services that help make your application stand out from the crowd.
- Analytics services that deliver telemetry data from your software and devices.

### Azure offer
**Be ready for the future**: Continuous innovation from Microsoft supports your development today and your product visions for tomorrow.
**Build on your terms**: You have choices. With a commitment to open source, and support for all languages and frameworks, you can build how you want and deploy where you want to.
**Operate hybrid seamlessly**: On-premises, in the cloud, and at the edge--we'll meet you where you are. Integrate and manage your environments with tools and services designed for a hybrid cloud solution.
**Trust your cloud**: Get security from the ground up, backed by a team of experts, and proactive compliance trusted by enterprises, governments, and startups.


### Azure work
https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/what-is-microsoft-azure
Fabric controller > orchestrator

### Azure portal
The Azure portal is a web-based, unified console that provides an alternative to command-line tools. With the Azure portal, you can manage your Azure subscription by using a graphical user interface. You can:
- Build, manage, and monitor everything from simple web apps to complex cloud deployments.
- Create custom dashboards for an organized view of resources.
- Configure accessibility options for an optimal experience.

Azure Cloud Shell
- can be used on iOS

Azure CLI
- cannot be installed on iOS

### [Azure Marketplace](https://azuremarketplace.microsoft.com/en-US/)
Azure Marketplace customers can find, try, purchase, and provision applications and services from hundreds of leading service providers. All solutions and services are certified to run on Azure

### [Azure services](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/tour-of-azure-services)

Resource groups:
- Resources with the same life cycle can be grouped together on the same resource group
- When you delete a resource group, all the resources on it are also deleted

#### Compute
Azure Service Fabric: Cluster management for VMs that run containerized services.Distributed systems platform that runs in Azure or on-premises.
Azure Batch: Managed service for parallel and high-performance computing applications.
Azure Container Instances: Containerized apps run on Azure without provisioning servers or VMs.

Azure Function
- an event-driven serverless computing platform
- can solve complex orchestration problems
- to develop serverless applications

#### Networking
Azure Virtual Network: Connects VMs to incoming virtual private network (VPN) connections
Azure Load Balancer: Balances inbound and outbound connections to applications or service endpoints.
Azure Application Gateway: Accesses Azure Virtual Networks through high-performance VPN gateways.
Azure DNS: Provides ultra-fast DNS responses and ultra-high domain availability.
Azure Content Delivery Network:Delivers high-bandwidth content to customers globally.
Azure DDoS Protection: Protects Azure-hosted applications from distributed denial of service (DDOS) attacks.
Azure Traffic Manager:Distributes network traffic across Azure regions worldwide.
Azure ExpressRoute:Connects to Azure over high-bandwidth dedicated secure connections.
Azure Network Watcher:Monitors and diagnoses network issues by using scenario-based analysis.
Azure Firewall:Implements high-security, high-availability firewall with unlimited scalability.
Azure Virtual WAN:Creates a unified wide area network (WAN) that connects local and remote sites.


#### Storage
Azure Blob storage:Storage service for very large objects, such as video files or bitmaps.
Azure File storage:File shares that can be accessed and managed like a file server.
Azure Queue storage:A data store for queuing and reliably delivering messages between applications.
Azure Table storage:Table storage is a service that stores non-relational structured data (also known as structured NoSQL data) in the cloud, providing a key/attribute store with a schemaless design.

characteristics:
- **Durable** and highly available with redundancy and replication.
- **Secure** through automatic encryption and role-based access control.
- **Scalable** with virtually unlimited storage.
- **Managed**, handling maintenance and any critical problems for you.
- **Accessible** from anywhere in the world over HTTP or HTTPS.

#### Mobile
developers can create mobile back-end services for iOS, Android, and Windows apps quickly and easily.
Features that used to take time and increase project risks, such as adding corporate sign-in and then connecting to on-premises resources such as SAP, Oracle, SQL Server, and SharePoint, are now simple to include.
other features include:
- Offline data synchronization.
- Connectivity to on-premises data.
- Broadcasting push notifications.
- Autoscaling to match business needs.

#### Databases
Azure Cosmos DB: Globally distributed database that supports NoSQL options.
Azure SQL Database: Fully managed relational database with auto-scale, integral intelligence, and robust security.
Azure Database for MySQL: Fully managed and scalable MySQL relational database with high availability and security.
Azure Database for PostgreSQL: Fully managed and scalable PostgreSQL relational database with high availability and security.
SQL Server on Azure Virtual Machines: Service that hosts enterprise SQL Server apps in the cloud.
Azure Synapse Analytics: Fully managed data warehouse with integral security at every level of scale at no extra cost.
Azure Database Migration Service: Service that migrates databases to the cloud with no application code changes.
Azure Cache for Redis: Fully managed service caches frequently used and static data to reduce data and application latency.
Azure Database for MariaDB: Fully managed and scalable MariaDB relational database with high availability and security.

#### Web
The following Azure services are focused on web hosting:  
Azure App Service: Quickly create powerful cloud web-based apps.
- fully managed platform and and platform service (PaaS), fast-building, deploying, and scaling service for web applications and API.
- does not provide a serverless environment
- when to use:
    - Web apps
    - API apps
    - WebJobs (run a progrom/script in the same context as w Web App; can be scheduled or run by a trigger)
    - Mobile apps (quickly build a back end for iOS and Android app)
        - Store mobile app data in a cloud-based SQL database.
        - Authenticate customers against common social providers, such as MSA, Google, Twitter, and Facebook.
        - Send push notifications.
        - Execute custom back-end logic in C# or Node.js.

- Benifits
    - Deployment and management are integrated into the platform.
    - Endpoints can be secured.
    - Sites can be scaled quickly to handle high traffic loads.
    - The built-in load balancing and traffic manager provide high availability. 

Azure Notification Hubs: Send push notifications to any platform from any back end.
Azure API Management: Publish APIs to developers, partners, and employees securely and at scale.
Azure Cognitive Search: Deploy this fully managed search as a service.
Web Apps feature of Azure App Service: Create and deploy mission-critical web apps at scale.
Azure SignalR Service: Add real-time web functionalities easily.


#### Internet of Things (IoT)
the internet allows any item that's online-capable to access valuable information. This ability for devices to garner and then relay information for data analysis is referred to as IoT.  
IoT Central: Fully managed global IoT software as a service (SaaS) solution that makes it easy to connect, monitor, and manage IoT assets at scale.
Azure IoT Hub: Messaging hub that provides secure communications between and monitoring of millions of IoT devices.
IoT Edge: Fully managed service that allows data analysis models to be pushed directly onto IoT devices, which allows them to react quickly to state changes without needing to consult cloud-based AI models.

#### Big data
Azure Synapse Analytics: Run analytics at a massive scale by using a cloud-based enterprise data warehouse that takes advantage of massively parallel processing to run complex queries quickly across petabytes of data.
Azure HDInsight: Process massive amounts of data with managed clusters of Hadoop clusters in the cloud.
Azure Databricks: Integrate this collaborative Apache Spark-based analytics service with other big data services in Azure.

#### AI
the core of which is machine learning. Machine learning is a data science technique that allows computers to use existing data to forecast future behaviors, outcomes, and trends. Using machine learning, computers learn without being explicitly programmed  
Azure Machine Learning Service: Cloud-based environment you can use to develop, train, test, deploy, manage, and track machine learning models. It can auto-generate a model and auto-tune it for you. It will let you start training on your local machine, and then scale out to the cloud.
Azure ML Studio: Collaborative visual workspace where you can build, test, and deploy machine learning solutions by using prebuilt machine learning algorithms and data-handling modules.

A closely related set of products are the cognitive services. You can use these prebuilt APIs in your applications to solve complex problems: 
Vision: Use image-processing algorithms to smartly identify, caption, index, and moderate your pictures and videos.
Speech: Convert spoken audio into text, use voice for verification, or add speaker recognition to your app.
Knowledge mapping: Map complex information and data to solve tasks such as intelligent recommendations and semantic search.
Bing Search: Add Bing Search APIs to your apps and harness the ability to comb billions of webpages, images, videos, and news with a single API call.
Natural Language processing: Allow your apps to process natural language with prebuilt scripts, evaluate sentiment, and learn how to recognize what users want.


#### DevOps
DevOps brings together people, processes, and technology by automating software delivery to provide continuous value to your users  
Azure DevOps: Use development collaboration tools such as high-performance pipelines, free private Git repositories, configurable Kanban boards, and extensive automated and cloud-based load testing. Formerly known as Visual Studio Team Services.
Azure DevTest Labs: Quickly create on-demand Windows and Linux environments to test or demo applications directly from deployment pipelines.


### Azure accounts
Azure free account includes:
- Free access to popular Azure products for 12 months.
- A credit to spend for the first 30 days.
- Access to more than 25 products that are always free.

The Azure free student account offer includes:
- Free access to certain Azure services for 12 months.
- A credit to use in the first 12 months.
- Free access to certain software developer tools.

## Discuss Azure fundamental concepts
### cloud models
Public cloud: Services are offered over the public internet and available to anyone who wants to purchase them. Cloud resources, such as servers and storage, are owned and operated by a third-party cloud service provider, and delivered over the internet.
- No capital expenditures to scale up.
- Applications can be quickly provisioned and deprovisioned.
- Organizations pay only for what they use.
Private cloud: A private cloud consists of computing resources used exclusively by users from one business or organization. A private cloud can be physically located at your organization's on-site (on-premises) datacenter, or it can be hosted by a third-party service provider.
- Hardware must be purchased for start-and maintenance.
- Organizations have complete control over resources and security.
- Organizations are responsible for hardware maintenance and updates.
Hybrid cloud: A hybrid cloud is a computing environment that combines a public cloud and a private cloud by allowing data and applications to be shared between them.
- Provides the most flexibility.
- Organizations determine where to run their applications.
- Organizations control security, compliance, or legal requirements.

### cloud computing advantages
*a consumption-based model*
- **High availability**: Depending on the service-level agreement (SLA) that you choose, your cloud-based apps can provide a continuous user experience with no apparent downtime, even when things go wrong.
- **Reliability** depends on the service level agreement you choose, but in the event of a problem, your cloud-based application will continue to provide the user experience without any obvious downtime
- **resiliency**. 
    - Continuing service in the event of a failure
    - Maintaining a DR (Disaster Recovery) configuration in other regions
- **Scalability**: Apps in the cloud can scale vertically and horizontally:
    - Scale vertically (up-down) to increase compute capacity by adding RAM or CPUs to a virtual machine.
    - Scaling horizontally (in-out) increases compute capacity by adding instances of resources, such as adding VMs to the configuration.
- **Elasticity**: You can configure cloud-based apps to take advantage of autoscaling, so your apps always have the resources they need.
    - cloud-based applications can be configured to always have the resources they need
    - the ability of services to automatically scale resources based on changing demand
    - ScalingSet helps automate the process of adding or removing virtual machines as demand increases or decreases
- **flexibility** to change resource allocation is an example of cloud flexibility.
- **Agility**: Deploy and configure cloud-based resources quickly as your app requirements change.
- **Geo-distribution**: You can deploy apps and data to regional datacenters around the globe, thereby ensuring that your customers always have the best performance in their region.
- **Disaster recovery**: By taking advantage of cloud-based backup services, data replication, and geo-distribution, you can deploy your apps with the confidence that comes from knowing that your data is safe in the event of disaster.

### CapEx VS OpEx
- Enterprise Agreement (EA) subscriptions and Azure Reserved Instances are CapEx solutions
- pay-as-you-go subscriptions are also available and are considered OpEx.
- Azure gives you the *flexibility* to choose.


### different cloud services:
[pros and cons](https://docs.microsoft.com/en-ca/learn/modules/fundamental-azure-concepts/categories-of-cloud-services)
- **IaaS**: provider will keep the hardware up-to-date, but operating system maintenance and network configuration is up to you
    - Virtual Machines. rapid deployment
- **PaaS**: providers manage the VMs and network; tenant deploys their applications into the managed hosting environment
    - Azure app services
    - Azure web apps. build applications on the Azure platform without deploying, configuring, and maintaining their own Azure virtual machines.
    - Azure Logic Apps. schedule, automate, and coordinate tasks, business processes, and workflows when you need to integrate apps, data, systems, and services across your enterprise or organization
    - Azure SQL
- **Saas**: provider manages all aspects; tenant only needs to provide their data to the application managed by the cloud provider
    - Office 365
- **DaaS**
    - Desktop as a Service (DaaS) is a virtual desktop, a cloud service that provides a desktop virtualization system deployed in a cloud environment.

## Describe core Azure architectural components
### organization
- Management groups: These groups help you manage access, policy, and compliance for multiple subscriptions. All subscriptions in a management group automatically inherit the conditions applied to the management group.
    - can build a flexible structure of management groups (can be nested)
    - apply policy to be inherited by sub mng groups, subscriptions, resource groups and resources
    - limits:
        - max 10,000 management groups in a single directory
        - a mng group can suport max 6 levels of depth (not including the root level)
        -  mng group and subscript only support 1 parent
        - all subscrtions and mng groups are in a single hierachy in each directory
- Subscriptions: A subscription groups together user accounts and the resources that have been created by those user accounts. For each subscription, there are limits or quotas on the amount of resources that you can create and use. Organizations can use subscriptions to manage costs and the resources that are created by users, teams, or projects.
    - Using Azure requires an Azure subscription
    - a logical unit of Azure services that links to an Azure account (Azure AD or in a directory that Azure AD trusts)
    - An account can have one subscription or multiple subscriptions that have different billing models and to which you apply different access-management policies
        - Billing Boundary
        - Access control boundary
    - to separate:
        - Envoironments
        - Organizational structures
        - Billing
        - Subscription Limits
            - Max ExpressRoute circuits per subscription: 10
            - 
- Resource groups: Resources are combined into resource groups, which act as a logical container into which Azure resources like web apps, databases, and storage accounts are deployed and managed.
- Resources: Resources are instances of services that you create, like virtual machines, storage, or SQL databases.

#### Geography
- any region of the world that contains at least one Azure region
- Regions define individual markets and maintain boundaries between data location and compliance

#### Region
- A group of data centers connected by a **high-speed** network
- geographically separated from each other
- Each region has at least **three** separate zones.

importants:
- Some services or VM features are only available in certain regions, such as specific VM sizes or storage types.
- There are also some global Azure services that don't require you to select a particular region, such as Azure Active Directory, Azure Traffic Manager, and Azure DNS.

special Azure regions
- US DoD Central, US Gov Virginia, US Gov Iowa and more: These regions are physical and logical network-isolated instances of Azure for U.S. government agencies and partners. These datacenters are operated by screened U.S. personnel and include additional compliance certifications.
- China East, China North, and more: These regions are available through a unique partnership between Microsoft and 21Vianet, whereby Microsoft doesn't directly maintain the datacenters.

region pairs
- Each Azure region is always paired with another region within the same geography
- advantages: reliable and data redundancy
    - f an extensive Azure outage occurs, one region out of every pair is prioritized to make sure at least one is restored as quickly as possible for applications hosted in that region pair.
    - Planned Azure updates are rolled out to paired regions one region at a time to minimize downtime and risk of application outage.
    - Data continues to reside within the same geography as its pair (except for Brazil South) for tax- and law-enforcement jurisdiction purposes.


#### [Availability zone (AZ)](https://docs.microsoft.com/en-us/azure/availability-zones/az-overview)
- (unique) physical locations within a unique physical region. Availability Zones within the region are geographically close and connected by a **leased line**
- Each zone consists of one or more data centers with **independent** power supplies, cooling means, and networks
- Availability zones are connected through high-speed, private fiber-optic networks.

Azure services that support availability zones fall into three categories:
- Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).
- Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).
- Non-regional services: Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages.


#### Azure datacenter
- perform third-party security audits to ensure security
- Azure employees **cannot** access the datacenter. 
- MS employee are not informed of the location of the data center

#### Azure Stack
- an “on-premises version of Azure service”
- allows you to build an environment based on the same technology and management infrastructure as Microsoft Azure

#### [Edge zone](https://azure.microsoft.com/en-us/blog/microsoft-partners-with-the-industry-to-unlock-new-5g-scenarios-with-azure-edge-zones/)
- the edge location is set up separately from the AZ
- Microsoft deploys Edge Zone services at edge locations, allowing Azure services to connect directly to 5G networks within mobile operator data centers

### resource,Resource Group ARM
[benefits of using Resource Manager](https://docs.microsoft.com/en-ca/learn/modules/azure-architecture-fundamentals/resources-resource-manager)


Azure Marketplace: an online store that hosts applications that are certified and optimized to run in Azure.



# Part 2: Describe core Azure services
## compute services
**Azure Virtual Machines**
- Total control over the operating system (OS).
- The ability to run custom software.
- To use custom hosting configurations.
- when to use:
    - During testing and development
    - When running applications in the cloud
    - When extending your datacenter to the cloud
    - During disaster recovery

**Azure Virtual machine scale sets**
- deploy and manage a set of identical VMs
- easier to build large-scale services targeting big compute, big data, and containerized workloads
- easy to maintain route request
- more VM instances can be added or removed.
- The process can be manual, automated, or a combination of both.

**Azure Batch**: enables large-scale parallel and high-performance computing (HPC) batch jobs with the ability to scale to tens, hundreds, or thousands of VMs. When you're ready to run a job, Batch does the following:
- Starts a pool of compute VMs for you.
- Installs applications and staging data.
- Runs jobs with as many tasks as you have.
- Identifies failures.
- Requeues work.
- Scales down the pool as work completes.

**Azure Container** & **Azure Kubernetes Service**
- to deploy and manage containers (lightweight, virtualized application environment)
- multiple container in one host
**[microservice] (https://docs.microsoft.com/en-ca/learn/modules/azure-compute-fundamentals/azure-container-services)**
**Azure App Service**
**Azure Functions** (serverless computing)
    - Abstraction of servers
    - Event-driven scale
        - Timers, for example, if a function needs to run every day at 10:00 AM UTC.
        - HTTP, for example, API and webhook scenarios.
        - Queues, for example, with order processing.
        - And much more.
    - micro-billing
    - you write code to complete each step
**Azure Logic Apps** (serverless computing)
    - designed in a web-based designer
    - can execute logic triggered by Azure services without writing any code.
    - you use a GUI to define the actions and how they relate to one another.
**Azure Virtual Desktop**
- simplified management
- performance management. gives you options to load balance users on your VM host pools. Host pools are collections of VMs with the same configuration assigned to multiple users.
- Multi-session Win10 Deployment

## networking services

Communicate between Azure resources
- virtual networks
- Sevice endpoints

Communicate with on-premises resources
- **Point-to-site virtual private networks**. The typical approach to a virtual private network (VPN) connection is from a computer outside your organization, back into your corporate network. In this case, the client computer initiates an encrypted VPN connection to connect that computer to the Azure virtual network.
- **Site-to-site virtual private networks**. A site-to-site VPN links your on-premises VPN device or gateway to the Azure VPN gateway in a virtual network. In effect, the devices in Azure can appear as being on the local network. The connection is encrypted and works over the internet.
- **Azure ExpressRoute**. For environments where you need greater bandwidth and even higher levels of security. ExpressRoute provides dedicated private connectivity to Azure that doesn't travel over the internet




## storage services
## database and analytics services


Azure Cognitive Services
- incorporate mechanisms such as image identification into your applications from APIs without any machine learning expertise.

Azure Databricks
- a fast, easy-to-use Apache Spark-based big data analytics service designed for data engineering


Azure Machine Learning
- a development platform for coding machine learning
- to build a predictive analytics model that uses past user behavior data

Azure Synapse Analytics
- an Azure analytics service that combines data integration, big data analytics and an enterprise data warehouse (EDW)
- possible to build a data warehouse that can be used for BI and machine learning by integrating data collection, exploration, preparation, and management.
- significantly reducing the time it takes to develop your project with an integrated experience that supports the development of **end-to-end** analytics solutions
- cannot be used for a predictive analytics model



# Part 3: Describe core solutions and management tools on Azure
## best Az IoT service for your apllications
## best AI service for your needs
## best Az serveless technology for your business scenario
## best tools to help organizations build better solutions
## best tools for managing and configuring Az environment
Azure Advisor: available for **free** and provides
- solutions to improve cost-effectiveness, performance, high availability, reliability, and security
- cannot file a cap relaxation request for resource limit
- access the Advisor using the Azure portal, the Azure command line interface (CLI), or the Advisor API. 
- configure alerts to automatically notify you of new recommendations
- doesn't provide a way to improve the security of your Azure Active Directory (Azure AD) environment. Azure Active Directory has a function called Identity Protection, which allows you to obtain analysis information on the security structure of your organization. It helps you identify potential attacks and understand the effectiveness of your policies.

## best monitoring service for visibility, insight and outage mitigation

# Part 4: Describe general security and network security features
## Protect agains security threats on Azure
## Secure network connectivity on Azure

# Part 5: Describe identity, governance, privacy, and compliance features
## Secure access to your applications by using Azure identity services
## Build a cloud governance strategy on Azure
## Examine privacy, compliance, and data protection standards on Azure

# Part 6: Describe Azure cost management and service level agreements

MSDN
- MSDN Platforms is a comprehensive, cost-effective set of resources for setting up development and test environments.
- This will be accessible as a benefit of a pay-as-you-go subscription

## Plan and manage your Azure costs
## Choose the right Azure services by examining SLAs and service lifecycle















