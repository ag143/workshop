
Azure Information Protection (AIP)
- a cloud-based solution that helps organizations classify documents and emails
- by applying labels and can help to protect them

Azure Application Insights
- an application performance management (APM) service, a service for sending telemetry information from application source code to Azure
- a feature of Azure Monitor and uses Azure Monitor under the hood, 
- allows you to monitor running applications and automatically detect performance anomalies
- use built-in analytics tools to view what your users do on your app.

No access:
- Azure does not have permission to access the data

Tenancy
- defines how instances are distributed across physical hardware

End-to-end: describes a process that takes a system or service from beginning to end and delivers a complete functional solution, usually without needing to obtain anything from a third party

Azure support request:
- Azure portal
- Azure support ticket REST API

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

#### Azure storage account and copies
- Data in your Azure Storage account is always replicated three times in the primary region.
- The Azure storage account copies the data into three times within the primary region and keeps them synchronous.
- It is also asynchronously copied to the secondary region.
- An Azure storage account contains all Azure Storage data objects (blobs, files, queues, tables, and disks).



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
- globally distributed, multi-model database service
- supports schema-less data, build highly responsive and "Always On" applications 
- Azure Cosmos DB stores data in atom-record-sequence (ARS) format. The
- The data is abstracted and projected as an API, include SQL, MongoDB, Cassandra, Tables, and Gremlin

Azure SQL Database: Fully managed relational database with auto-scale, integral intelligence, and robust security.
- enables you to process both relational data and non-relational structures, such as graphs, JSON, spatial, and XML.
- Azure Database Migration Service can be used to migrate on-premise sql server to cloud

Azure Database for MySQL: Fully managed and scalable MySQL relational database with high availability and security.
- 99.99%
- Built-in high availability with no additional cost.
- Predictable performance and inclusive, pay-as-you-go pricing.
Azure Database for PostgreSQL: Fully managed and scalable PostgreSQL relational database with high availability and security.
- single server. 3 pricing tiers: Basics, General Purpose, Memory Optimized
- hyper scale. 
    - horizontally scales queries across multiple machines by using sharding
    - can serve worklods exceeding 100GB data
    - supports multi-tenant applications, real-time operational analytics, and high throughput transactional workloads

Azure SQL Managed Instance
- PaaS, 99.99%
- provides several options that might not be available to Azure SQL Database (Azure SQL Database only uses the default SQL_Latin1_General_CP1_CI_AS server collation)
- easy to migrate using the Azure Database Migration Service (DMS) or native backup and restore
- [ Features comparison: Azure SQL Database and Azure SQL Managed Instance](https://docs.microsoft.com/en-us/azure/azure-sql/database/features-comparison)

SQL Server on Azure Virtual Machines: Service that hosts enterprise SQL Server apps in the cloud.
Azure Database Migration Service: Service that migrates databases to the cloud with no application code changes.
Azure Cache for Redis: Fully managed service caches frequently used and static data to reduce data and application latency.
Azure Database for MariaDB: Fully managed and scalable MariaDB relational database with high availability and security.

#### Web
The following Azure services are focused on web hosting:  
Azure App Service: Quickly create powerful cloud web-based apps.
- fully managed **platform** and and platform service (**PaaS**), fast-building, deploying, and scaling service (web app) for web applications and API.
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

IoT hub: 
- a central message hub for *bi-directional* communication between your IoT application and the devices it manages
- supports multiple messaging patterns: 
    - device-to-cloud telemetry
    - file upload from devices
    - and request-reply methods to control your devices from the cloud
- After an IoT hub receives messages from a device, it can route that message to other Azure services.
- a cloud-to-device perspective, IoT Hub allows for *command and control*
    - either manual or automated remote control of connected devices
    - can instruct the device to open valves, set target temperatures, restart stuck devices, and so on

IoT Central: 
- Fully managed global IoT software as a service (SaaS) solution that makes it easy to connect, monitor, and manage IoT assets at scale.
- builds on top of IoT Hub by adding a dashboard to connect, monitor, and manage your IoT devices.
- UI helps to monitor, aggregate, alert and push notifications and firmware updates.
- provides starter templates for different business types.
- use of device templates to construct the dashboards, alerts, and so on. Device developers still need to create code to run on the devices, and that code must match the device template specification.

Azure Sphere (hardware)
- Azure Sphere micro-controller unit (MCU).  responsible for processing the operating system and signals from attached sensors.
- customized Linux operating system (OS).  handles communication with the security service and can run the vendor's software
- Azure Sphere Security Services, also known as AS3

IoT Edge: Fully managed service that allows data analysis models to be pushed directly onto IoT devices, which allows them to react quickly to state changes without needing to consult cloud-based AI models.

#### Big data (and analytics)
Azure Synapse Analytics: Fully managed data warehouse with integral security at every level of scale at no extra cost.  Run analytics at a massive scale by using a cloud-based enterprise data warehouse that takes advantage of massively parallel processing to run complex queries quickly across petabytes of data.
- query data on your terms by using either serverless or provisioned resources at scale
- unified experience to ingest, prepare, manage, and serve data for immediate business intelligence and machine learning needs

- an Azure analytics service that combines data integration, big data analytics and an enterprise data warehouse (EDW)
- possible to build a data warehouse that can be used for BI and machine learning by integrating data collection, exploration, preparation, and management.
- significantly reducing the time it takes to develop your project with an integrated experience that supports the development of **end-to-end** analytics solutions
- cannot be used for a predictive analytics model

Azure HDInsight: Process massive amounts of data with managed clusters of Hadoop clusters in the cloud.
- open-source analytics service
- run open-source frameworks and create cluster as Apache (Spark, Hadoop, Kafa, HBase, Storm), and Machine learning services
- supports a broad range of scenarios such as ETL, data warehousing, machine learning, and IoT.

Azure Databricks: Integrate this collaborative Apache Spark-based analytics service with other big data services in Azure.
- a fast, easy-to-use Apache Spark-based big data analytics service designed for data engineering
- Python, Scala, R, Java, and SQL
- data science frameworks and libraries: TensorFlow, PyTorch, and scikit-learn.

Azure Data Lake Analytics. 
- an on-demand analytics job service that simplifies big data
- write queries to transform your data and extract valuable insights without taking care of hardwares
- pay for your job when it's running 


#### AI
- deep learning, which is modeled on the neural network of the human mind, enabling it to discover, learn, and grow through experience
- machine learning, a data science technique that uses existing data to train a model, test it, and then apply the model to new data to forecast future behaviors, outcomes, and trends.

the core of which is machine learning. Machine learning is a data science technique that allows computers to use existing data to forecast future behaviors, outcomes, and trends. Using machine learning, computers learn without being explicitly programmed  

**Azure Machine Learning Service**: Cloud-based environment you can use to develop, train, test, deploy, manage, and track machine learning models. It can auto-generate a model and auto-tune it for you. It will let you start training on your local machine, and then scale out to the cloud.
- a development platform for coding machine learning
- to build a predictive analytics model that uses past user behavior data
You can:
- Create a process that defines how to obtain data, how to handle missing or bad data, how to split the data into either a training set or test set, and deliver the data to the training process.
- Train and evaluate predictive models by using tools and programming languages familiar to data scientists.
- Create pipelines that define where and when to run the compute-intensive experiments that are required to score the algorithms based on the training and test data.
- Deploy the best-performing algorithm as an API to an endpoint so it can be consumed in real time by other applications.


Azure ML Studio: Collaborative visual workspace where you can build, test, and deploy machine learning solutions by using prebuilt machine learning algorithms and data-handling modules.

A closely related set of products are the **Azure Cognitive** services. You can use these prebuilt APIs in your applications to solve complex problems: 
- incorporate mechanisms such as image identification into your applications from APIs without any machine learning expertise.
- **Vision**: Use image-processing algorithms to smartly identify, caption, index, and moderate your pictures and videos.
- **Speech**: Convert spoken audio into text, use voice for verification, or add speaker recognition to your app.
Natural Language processing(**language**): Allow your apps to process natural language with prebuilt scripts, evaluate sentiment, and learn how to recognize what users want.
- Knowledge mapping (**decision**):
    -Map complex information and data to solve tasks such as intelligent recommendations and semantic search.
    - Add personalized *recommendations* for each user that automatically improve each time they're used, moderate content to monitor and remove offensive or risky content, and detect abnormalities in your time series data.
    - can use Personalizer to predict their behavior and provide relevant experiences as it identifies usage patterns
    - less expense and effort than Azure Machine Learning
- Bing Search: Add Bing Search APIs to your apps and harness the ability to comb billions of webpages, images, videos, and news with a single API call.

**Azure Bot Services**.  and Bot Framework are platforms for creating virtual agents that understand and reply to questions just like a human

#### DevOps
DevOps brings together people, processes, and technology by automating software delivery to provide continuous value to your users  
**Azure DevOps**: Use development collaboration tools such as high-performance pipelines, free private Git repositories, configurable Kanban boards, and extensive automated and cloud-based load testing. Formerly known as Visual Studio Team Services.
- Azure Repos
- Azure Boards
- Azure Pipelines. CI/CD pipeline automation tool
- Azure Artifacts. a repository for hosting artifacts, such as compiled source code, which can be fed into testing or deployment pipeline steps.
- Azure Test Plans. is an automated test tool that can be used in a CI/CD pipeline
**Github and github actions**
- less permission granularity than DevOps
**Azure DevTest Labs**: Quickly create on-demand Windows and Linux environments to test or demo applications directly from deployment pipelines.
- provides an automated means of managing the process of building, setting up, and tearing down virtual machines (VMs) that contain builds of your software projects.
- developers and testers can perform tests across a variety of environments and builds. And this capability isn't limited to VMs
- Anything you can deploy in Azure via an ARM template can be provisioned through DevTest Labs.
- Provisioning pre-created lab environments with their required configurations and tools already installed is a huge time saver

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
        - Azure SQL Managed Instance
- **Saas**: provider manages all aspects; tenant only needs to provide their data to the application managed by the cloud provider
    - IoT central
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
- multi-region support is not optimal in terms of architectural configuration because it is difficult to link virtual machines across regions

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
- Availability zones are connected through *high-speed, private fiber-optic* networks.
- to prevent a single data center failure, you only need to use multiple availability zones and do not need to have a multi-region configuration
- By default, Azure Availability Zones are used to replicate applications and data only within the Azure region. (not differe region)

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
Resource Manager is a management service that provides a way to organize and secure your cloud resources.access Resource Manager from the Azure portal, Azure Cloud Shell, Azure PowerShell, and the Azure CLI



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

attention:
- By default, all inbound connections are not allowed on L4, so unless you have a *network interface*, you need to modify the rules of the **network security group** so that all inbound connections from port 80/8080 can reach the VM. 

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
Azure virtual networks enable Azure resources, such as VMs, web apps, and databases, to communicate with each other, with users on the internet, and with your on-premises client computers. You can think of an Azure network as a set of resources that links other Azure resources.
- a private isolated network in Azure

key networking capabilities:
- Isolation and segmentation. Virtual Network allows you to create multiple isolated virtual networks. When you set up a virtual network, you define a private IP address space by using either public or private IP address ranges. You can divide that IP address space into subnets and allocate part of the defined address space to each named subnet
- Internet communications.A VM in Azure can connect to the internet by default. You can enable incoming connections from the internet by defining a public IP address or a public load balancer. For VM management, you can connect via the Azure CLI, Remote Desktop Protocol, or Secure Shell.
- Communicate between Azure resources
    - virtual networks
    - Service endpoints
- Communicate with on-premises resources
    - **Point-to-site virtual private networks**. The typical approach to a virtual private network (VPN) connection is from a computer outside your organization, back into your corporate network. In this case, the client computer initiates an encrypted VPN connection to connect that computer to the Azure virtual network.
    - **Site-to-site virtual private networks**. A site-to-site VPN links your on-premises VPN device or gateway to the Azure VPN gateway in a virtual network. In effect, the devices in Azure can appear as being on the local network. The connection is encrypted and works over the internet.
    - **Azure ExpressRoute**. For environments where you need greater bandwidth and even higher levels of security. ExpressRoute provides dedicated private connectivity to Azure that doesn't travel over the internet
- Route network traffic. Azure routes traffic between subnets on any connected virtual networks, on-premises networks, and the internet. You also can control routing and override those settings, as follows:
    - **Route tables**. define rules about how traffic should be directed. control how packets are routed between subnets. Azure automatically creates a route table for each subnet within an Azure virtual network and adds system default routes to the table. You can add custom route tables to modify traffic between virtual networks
    - **Border Gateway Protocol** Border Gateway Protocol (BGP) works with Azure VPN gateways or ExpressRoute to propagate on-premises BGP routes to Azure virtual networks.
- Filter network traffic. filter traffic between subnets by using the following approaches:
    - **Network security groups** A network security group is an Azure resource that can contain multiple inbound and outbound security rules. You can define these rules to allow or block traffic, based on factors such as source and destination IP address, port, and protocol. You create the network security group separately, Then you associate it with the virtual network
    - **Network virtual appliances** A network virtual appliance is a specialized VM that can be compared to a hardened network appliance. A network virtual appliance carries out a particular network function, such as running a firewall or performing wide area network (WAN) optimization.

- Connect virtual networks
    - virtual network *peering*, which links virtual networks and enables resources in each vNet to communicate
    - the vNets can be in separate regions, which allows to create a global interconnected network through Azure
    - user-defined Routing (UDR). a significant update to Azure’s Virtual Networks; allows allows network admins to control the routing tables between subnets within a VNet, as well as between VNets, allowing for greater control over network traffic flow.
    - https://docs.microsoft.com/en-ca/learn/modules/azure-networking-fundamentals/azure-virtual-network-fundamentals

Routing talbe: 
- the routing table is the routing route information recorded in the router itself. it only contains a set of rules (routes) that specify how packets are routed in the virtual network
- It is the table to be referred to when performing the routing process but it does not identify the IP address of the VPN appliance.

[Azure Virtual Network settings](https://docs.microsoft.com/en-ca/learn/modules/azure-networking-fundamentals/azure-virtual-network-settings)

### [VPN gateways](https://docs.microsoft.com/en-ca/learn/modules/azure-networking-fundamentals/azure-vpn-gateway-fundamentals)
deployed in Azure Virtual Network instances and enable the following connectivity:
- Connect on-premises datacenters to virtual networks through a site-to-site connection.
- Connect individual devices to virtual networks through a point-to-site connection.
- Connect virtual networks to other virtual networks through a network-to-network connection.

You can deploy only one VPN gateway in each virtual network, but you can use one gateway to connect to multiple locations, which includes other virtual networks or on-premises datacenters.

VPN type:
- Policy-based VPN gateways
- Route-based VPNs

#### Azure virtual network gateway
a VPN device in the Azure virtual network that is used to set up a site-to-site VPN connection between the Azure virtual network and the local network, or a VNet-to-VNet VPN connection.


#### Policy-based VPN gateways

specify statically the IP address of packets that should be encrypted through each tunnel, and
- Support for IKEv1 only
- Use of static routing, where combinations of address prefixes from both networks control how traffic is encrypted and decrypted through the VPN tunnel. The source and destination of the tunneled networks are declared in the policy and don't need to be declared in routing tables.
- Policy-based VPNs must be used in specific scenarios that require them, such as for compatibility with legacy on-premises VPN devices.

#### Route-based VPNs
IPSec tunnels are modeled as a **network interface** (allows Azure VMs to communicate with Internet, Azure, and on-premises resources. It does not identify the IP address of the VPN appliance.) or virtual tunnel interface. IP routing (either static routes or dynamic routing protocols) decides which one of these tunnel interfaces to use when sending each packet. Route-based VPNs are the preferred connection method for on-premises devices. They're more resilient to topology changes such as the creation of new subnets.

when to use:
- Connections between virtual networks
- Point-to-site connections
- Multisite connections
- Coexistence with an Azure ExpressRoute gateway

Key features
- Supports IKEv2
- Uses any-to-any (wildcard) traffic selectors
- Can use dynamic routing protocols, where routing/forwarding tables direct traffic to different IPSec tunnels

High-availability scenarios:
- Active/standby
- Active/active

### [Azure ExpressRoute](https://docs.microsoft.com/en-ca/learn/modules/azure-networking-fundamentals/express-route-fundamentals)
ExpressRoute connections don't go over the public Internet, it is a private connection from your on-premises infrastructure to your Azure infrastructure

focus on two different layers of the Open Systems Interconnection (OSI) model
- Layer 2 (L2): Data Link Layer
- Layer 3 (L3): Network  Layer

Features and benefits
- Layer 3 connectivity
- connect to MS cloud service across all regions in the geopolitical region
- Global connectivity to Microsoft services across all regions with the ExpressRoute premium add-on.
- Dynamic routing between your network and Microsoft via BGP.
- Built-in redundancy in every peering location for higher reliability.
- Connection uptime SLA.
- QoS support for Skype for Business.

ExpressRoute enables direct access to the following services in all regions:
- Microsoft Office 365
- Microsoft Dynamics 365
- Azure compute services, such as Azure Virtual Machines
- Azure cloud services, such as Azure Cosmos DB and Azure Storage

## storage services
### Disk Storage
provides disks for Azure virtual machines. Applications and other services can access and use these disks as needed. Disk Storage allows data to be persistently stored and accessed from an attached virtual hard disk.

### Blob Storage
ideal for:
- Serving images or documents directly to a browser.
- Storing files for distributed access.
- Streaming video and audio.
- Storing data for backup and restore, disaster recovery, and archiving.
- Storing data for analysis by an on-premises or Azure-hosted service.
- Storing up to 8 TB of data for virtual machines.

### Azure Files
use for:
- Many on-premises applications use file shares.
- Store configuration files on a file share and access them from multiple VMs
- Write data to a file share, and process or analyze the data later.

 can access the files from anywhere in the world, by using a URL that points to the file. You can also use Shared Access Signature (SAS) tokens to allow access to a private asset for a specific amount of time.

### Access tiers
 - Hot access tier
 - Cool access tier
 - Archive access tier
 
 considerations: 
- Only the hot and cool access tiers can be set at the account level. The archive access tier isn't available at the account level.
- Hot, cool, and archive tiers can be set at the blob level, during upload or after upload.
- Data in the cool access tier can tolerate slightly lower availability, but still requires high durability, retrieval latency, and throughput- characteristics similar to hot data. For cool data, a slightly lower availability service-level agreement (SLA) and higher access costs compared to hot data are acceptable trade-offs for lower storage costs.
- Archive storage stores data offline and offers the lowest storage costs, but also the highest costs to rehydrate and access data.

## database and analytics services

# Part 3: Describe core solutions and management tools on Azure
## best Az IoT service for your apllications
## best AI service for your needs
## best Az serveless technology for your business scenario
## best tools to help organizations build better solutions
## best tools for managing and configuring Az environment

### Azure Protal

### Azure mobile app
provides iOS and Android access to your Azure resources
- Monitor the health and status of your Azure resources.
- Check for alerts, quickly diagnose and fix issues, and restart a web app or virtual machine (VM).
- Run the Azure CLI or Azure PowerShell commands to manage your Azure resources.

### Azure PowerShell
- windows
- can execute commands called cmdlets (pronounced command-lets). 
- Azure PowerShell is available for Windows, Linux, and Mac, and you can access it in a web browser via Azure Cloud Shell.
- to orchestrate:
    - The routine setup, teardown, and maintenance of a single resource or multiple connected resources.
    - The deployment of an entire infrastructure, which might contain dozens or hundreds of resources, from imperative code.

### The Azure CLI
- almost identical to Azure PowerShell
- Both run on Windows, Linux, and Mac, and can be accessed in a web browser via Cloud Shell.

### ARM templates
- describe the resources you want to use in a declarative JSON format
- he entire ARM template is verified before any code is executed to ensure that the resources will be created and connected correctly

**Infrastructure coding** is used to facilitate environmental automation

## best monitoring service for visibility, insight and outage mitigation
### Azure Advisor
available for **free** and provides:
- solutions to improve cost-effectiveness, performance, high availability, reliability, and security. designed to help you save time on cloud optimization
    - Operational Excellence:  achieve process and workflow efficiency, resource manageability, and deployment best practices.
- cannot file a cap relaxation request for resource limit
- access the Advisor using the Azure portal, the Azure command line interface (CLI), or the Advisor API. 
- configure alerts to automatically notify you of new recommendations
- doesn't provide a way to improve the security of your Azure Active Directory (Azure AD) environment. Azure Active Directory has a function called Identity Protection, which allows you to obtain analysis information on the security structure of your organization. It helps you identify potential attacks and understand the effectiveness of your policies.

### Azure Monitor
a platform for collecting, analyzing, visualizing, and potentially taking action based on the metric and logging data from your entire *Azure* and *on-premises* environment.
-Scenarios:
    - measure custom events alongside other usage metrics
    - set up alerts for outages or when autoscaling is about to deploy new instances

### Azure Service Health
provides a personalized view of the health of the Azure services, regions, and resources you rely on; displays both major and smaller, localized issues that affect you:
- **Service issues** are problems in Azure, such as outages, that affect you right now. You can drill down to the affected services, regions, updates from your engineering teams, and find ways to share and track the latest information.
- **Planned maintenance events** can affect your availability. You can drill down to the affected services, regions, and details to show how an event will affect you and what you need to do. Most of these events occur without any impact to you and aren't shown here. In the rare case that a reboot is required, Service Health allows you to choose when to perform the maintenance to minimize the downtime.
- **Health advisories** are issues that require you to act to avoid service interruption, including service retirements and breaking changes. Health advisories are announced far in advance to allow you to plan.
- scenario:
    - You can view the current status of the Azure services you rely on, upcoming planned outages, and services that will be sunset. 
    - You can set up alerts that help you stay on top of incidents and upcoming downtime without having to visit the dashboard regularly.

# Part 4: Describe general security and network security features
## Protect agains security threats on Azure
### Azure Security Center
a monitoring service that provides visibility of your security posture across all of your services, both on *Azure* and *on-premises*

Security Center can:
- Monitor security settings across on-premises and cloud workloads.
- Automatically apply required security settings to new resources as they come online.
- Provide security recommendations that are based on your current configurations, resources, and networks.
- Continuously monitor your resources and perform automatic security assessments to identify potential vulnerabilities before those vulnerabilities can be exploited.
- Use machine learning to detect and block malware from being installed on your virtual machines (VMs) and other resources. You can also use **adaptive application controls** to define rules that list allowed applications to ensure that only applications you allow can run.
- Detect and analyze potential inbound attacks and investigate threats and any post-breach activity that might have occurred.
- Provide just-in-time access control for network ports. Doing so reduces your attack surface by ensuring that the network only allows traffic that you require at the time that you need it to.


**security posture**: cybersecurity policies and controls, as well as how well you can predict, prevent, and respond to security threats.
**secure score**: a measurement of an organization's security posture; based on security controls, or groups of related security recommendations. Your score is based on the percentage of security controls that you satisfy. helps:
- Report on the current state of your organization's security posture.
- Improve your security posture by providing discoverability, visibility, guidance, and control.
- Compare with benchmarks and establish key performance indicators (KPIs).

#### Protect agains threats:
Security Center includes advanced cloud defense capabilities for VMs, network security, and file integrity
- **Just-in-time VM access** Tailwind Traders will configure just-in-time access to VMs. This access blocks traffic by default to specific network ports of VMs, but allows traffic for a specified time when an admin requests and approves it.
- **Adaptive application controls** Tailwind Traders can control which applications are allowed to run on its VMs. In the background, Security Center uses machine learning to look at the processes running on a VM. It creates exception rules for each resource group that holds the VMs and provides recommendations. This process provides alerts that inform the company about unauthorized applications that are running on its VMs.
- **Adaptive network hardening** Security Center can monitor the internet traffic patterns of the VMs, and compare those patterns with the company's current network security group (NSG) settings. From there, Security Center can make recommendations about whether the NSGs should be locked down further and provide remediation steps.
- **File integrity monitoring** Tailwind Traders can also configure the monitoring of changes to important files on both Windows and Linux, registry settings, applications, and other aspects that might indicate a security attack.

#### respond to security alerts
from Security Center, the company can dismiss false alerts, investigate them further, remediate alerts manually, or use an automated response with a *workflow automation*:
- uses Azure Logic Apps and Security Center connectors
- The logic app can be triggered by a threat detection alert or by a Security Center recommendation, filtered by name or by severity
- then configure the logic app to run an action, such as sending an email, or posting a message to a Microsoft Teams channel.

### Azure Sentinel
- dedicated Security Information And Event Management (SIEM):
- aggregates security data from many different sources (as long as those sources support an open-standard logging format). 
- It also provides capabilities for threat detection and response.

Azure Sentinel is Microsoft's cloud-based SIEM system and enables:
- **Collect cloud data** at scale Collect data across all users, devices, applications, and infrastructure, both on-premises and from multiple clouds.
- **Detect previously undetected threats**  Minimize false positives by using Microsoft's comprehensive analytics and threat intelligence.
- **Investigate threats with artificial intelligence** Examine suspicious activities at scale, tapping into years of cybersecurity experience from Microsoft.
- **Respond to incidents rapidly** Use built-in orchestration and automation of common tasks.

Azure Sentinel supports a number of data sources, handled by built-in connectors or industry-standard log formats and APIs.
- **Connect Microsoft solutions** Connectors provide real-time integration for services like Microsoft Threat Protection solutions, Microsoft 365 sources (including Office 365), Azure Active Directory, and Windows Defender Firewall.
- **Connect other services and solutions** Connectors are available for common non-Microsoft services and solutions, including AWS CloudTrail, Citrix Analytics (Security), Sophos XG Firewall, VMware Carbon Black Cloud, and Okta SSO.
- **Connect industry-standard data sources** Azure Sentinel supports data from other sources that use the Common Event Format (CEF) messaging standard, Syslog, or REST API.

Detect threats
- Built in analytics. use templates designed by Microsoft's team of security experts and analysts based on known threats, common attack vectors, and escalation chains for suspicious activit
- Custom analytics. rules that you create to search for specific criteria within your environment.

[Azure Monitor Workbooks](https://docs.microsoft.com/en-us/azure/azure-monitor/visualize/workbooks-overview) to automate responses to threats. one example with steps:
- When the alert is triggered, open a ticket in the IT ticketing system.
- Send a message to the security operations channel in Microsoft Teams or Slack to make sure the security analysts are aware of the incident.
- Send all of the information in the alert to the senior network admin and to the security admin. The email message includes two user option buttons: **Block** or **Ignore**.

### Azure Key Vault
- Manage secrets
- Manage encryption keys
- Manage SSL/TLS certificates
- Store secrets backed by hardware security modules (HSMs)

### Azure Dedicated Host
A dedicated host is mapped to a physical server in an Azure datacenter. A host group is a collection of dedicated hosts. Benifits:
- Gives you visibility into, and control over, the server infrastructure that's running your Azure VMs.
- Helps address compliance requirements by deploying your workloads on an isolated server.
- Lets you choose the number of processors, server capabilities, VM series, and VM sizes within the same host.

For high availability, you can provision multiple hosts in a host group, and deploy your VMs across this group. VMs on dedicated hosts can also take advantage of *maintenance control*. This feature enables you to control when regular maintenance updates occur, within a 35-day rolling window.


## Secure network connectivity on Azure

[layers of defense in depth](https://docs.microsoft.com/en-ca/learn/modules/secure-network-connectivity-azure/2-what-is-defense-in-depth):
- The physical security layer is the first line of defense to protect computing hardware in the datacenter.
- The identity and access layer controls access to infrastructure and change control.
- The perimeter layer uses distributed denial of service (DDoS) protection to filter large-scale attacks before they can cause a denial of service for users.
- The network layer limits communication between resources through segmentation and access controls.
- The compute layer secures access to virtual machines.
- The application layer helps ensure that applications are secure and free of security vulnerabilities.
- The data layer controls access to business and customer data that you need to protect.

Security posture: your organization's ability to protect from and respond to security threats
- Confidentiality. *principle of list privilege*
- integrity
    Prevent unauthorized changes to information:
    - At rest: when it's stored
    - In transit: when it's being transferred from one place to another, including from a local computer to the cloud.
    A common approach used in data transmission is for the sender to create a unique fingerprint of the data by using a one-way hashing algorithm
- Availability. DDos

*Azure Firewall and Azure DDoS Protection can help control what traffic can come from outside sources*

### Azure Firewall
a managed, cloud-based network security service that helps protect resources in your Azure virtual networks; a stateful firewall, analyzes the complete context of a network connection, not just an individual packet of network traffic.
- Built-in high availability.
- Unrestricted cloud scalability.
- Inbound and outbound filtering rules. 
    - create application rules in Az firewall to limit all outbound traffic from VMs to known host
- Inbound Destination Network Address Translation (DNAT) support.
- Azure Monitor logging.

With Azure Firewall, you can configure:
- Application rules that define fully qualified domain names (FQDNs) that can be accessed from a subnet.
- Network rules that define source address, protocol, destination port, and destination address.
- Network Address Translation (NAT) rules that define destination IP addresses and ports to translate inbound requests.

Azure Firewall provides:
- Inbound protection for non-HTTP/S protocols (for example, RDP, SSH, and FTP).
- Outbound network-level protection for all ports and protocols.
- Application-level protection for outbound HTTP/S.

*Azure Application Gateway* also provides a firewall that's called the web application firewall (WAF). WAF provides centralized, inbound protection for your web applications against common exploits and vulnerabilities.
- used to **load balance** traffic to various web applications.
- It does not identify the IP address of the VPN appliance

*Azure Front Door* and *Azure Content Delivery Network* also provide WAF services.

### DDoS protection
Always-on traffic monitoring and real-time mitigation of common network-level attacks provide the same defenses that Microsoft's online services use.The Azure global network is used to distribute and mitigate attack traffic across Azure regions.
- protection against DDoS attacks
- protects your website from a variety of **malicious** attacks 
- produces detailed **reports** on these attacks.

service tiers:
- **basic**. enabled for free as part of your Azure subscription.
- **standard**
    - Protection policies are tuned through dedicated traffic monitoring and machine learning algorithms.
    - Policies are applied to public IP addresses, which are associated with resources deployed in virtual networks such as Azure Load Balancer and Application Gateway.

The Standard service tier can help prevent:
- Volumetric attacks
- protocal attacks
- Resource-layer (application-layer) attacks (only with web application firewall)

### network security group
- filter network traffic to and from Azure **resources** in an Azure virtual network that has the network security group.
- NSGs like an internal firewall. An NSG can contain multiple inbound and outbound security rules that enable you to filter traffic to and from resources by source and destination IP address, port, and protocol
- provide distributed network-layer traffic filtering to limit traffic to resources within virtual networks in each subscription

[Exercise - Configure network access to a VM by using a network security group](https://docs.microsoft.com/en-ca/learn/modules/secure-network-connectivity-azure/6-configure-access-network-security-group)

### combine services
- Network security groups and Azure Firewall


[Application security groups](https://docs.microsoft.com/en-us/azure/virtual-network/application-security-groups)
- configure network security as a natural extension of an application's structure
- group virtual machines and define network security policies based on those groups
- (services for grouping virtual machines and managing access within a virtual network)


# Part 5: Describe identity, governance, privacy, and compliance features
## Secure access to your applications by using Azure identity services

**Authentication** is the process of establishing the identity of a person or service that wants to access a resource
**authorization** is the process of establishing what level of access an authenticated person or service has. It specifies what data they're allowed to access and what they can do with it

### Azure Active Directory
-  With Azure AD, you control the identity accounts, but Microsoft ensures that the service is available globally
-  When you connect Active Directory with Azure AD, Microsoft can help protect you by detecting suspicious sign-in attempts at no extra cost.

who uses Azure AD
- IT administrators
- App developers
- Users
- Online service subscriblers

tenant
- A tenant is a representation of an organization
- A tenant is typically separated from other tenants and has its own identity.
- Each Microsoft 365, Office 365, Azure, and Dynamics CRM Online tenant is automatically an Azure AD tenant.

services Azure AD provide:
- Authentication
- Single Sing-on (SSO)
- Application management. You can manage your cloud and on-premises apps by using Azure AD. Features like Application Proxy, SaaS apps, the My Apps portal (also called the access panel), and single sign-on provide a better user experience.
- Device management. Along with accounts for individual people, Azure AD supports the registration of devices. Registration enables devices to be managed through tools like **Microsoft Intune**. It also allows for **device-based Conditional Access** policies to restrict access attempts to only those coming from known devices, regardless of the requesting user account.

Azure AD Connect
- a way to connect your existing Active Directory installation with Azure AD
- synchronizes user identities **between** on-premises Active Directory and Azure AD.

### Multifactor authentication
provides additional security for your identities by requiring two or more elements to fully authenticate.
- Something the user knows. This might be an email address and password.
- Something the user has. This might be a code that's sent to the user's mobile phone.
- Something the user is. This is typically some sort of biometric property, such as a fingerprint or face scan that's used on many mobile devices.

the services that provice Azure AD Multi-Factor Authentication:
- Azure Active Directory.
    - Azure Active Directory free edition enables Azure AD Multi-Factor Authentication for administrators with the global admin level of access, via the Microsoft Authenticator app, phone call, or SMS code. You can also enforce Azure AD Multi-Factor Authentication for all users via the Microsoft Authenticator app only, by enabling security defaults in your Azure AD tenant.
    - Azure Active Directory Premium (P1 or P2 licenses) allows for comprehensive and granular configuration of Azure AD Multi-Factor Authentication through Conditional Access policies (explained shortly).
- Mutifactor authentication for office 365
    - A subset of Azure AD Multi-Factor Authentication capabilities is part of your Office 365 subscription.


### Conditional Access
access to resources based on identity *signals*. These signals include who the user is, where the user is, and what device the user is requesting access from. it helps:
- Empower users to be productive wherever and whenever.
- Protect the organization's assets.

when to use Conditional Access
- Require multifactor authentication to access an application.
- Require access to services only through approved client applications.
- Require users to access your application only from managed devices.
- Block access from untrusted sources, such as access from unknown or unexpected locations.

To use Conditional Access, you need an Azure AD Premium P1 or P2 license. If you have a Microsoft 365 Business Premium license, you also have access to Conditional Access features.

## Build a cloud governance strategy on Azure
Governance is most beneficial when you have:
- Multiple engineering teams working in Azure.
- Multiple subscriptions to manage.
- Regulatory requirements that must be enforced.
- Standards that must be followed for all cloud resources.

Role-based Access Control (RBAC)
- Azure RBAC doesn't enforce access permissions at the application or data level. Application security must be handled by your application.
- You can apply Azure RBAC to an individual person or to a group. You can also apply Azure RBAC to other special identity types, such as service principals and managed identities

resource lock:
- prevents resources from being accidentally deleted or changed.
- levels of locking
    - **Delete**, *CanNotDelete*. read and modify.
    - **ReadOnly**. only read

Tags, is useful for:
- Resource management
- Cost management and optimization
- Operations management. (how critical there availability is; formulate SLA)
- Security level
- Governance and regulatory compliance. 
    - specifiy compliance
    - resouces for different department
- Workload optimization and automation.
    - tag a resource with its associated workload or application name and use software such as Azure DevOps to perform automated tasks on those resources.

Azure Policy. a service in Azure that enables you to create, assign, and manage policies that control or audit your resources
- enables you to define both individual policies and groups of related policies, known as **initiatives**
- evaluates your resources and highlights resources that aren't compliant with the policies you've created
- prevent noncompliant resources from being created
- Azure Policy comes with a number of built-in policy and initiative definitions
- In some cases, Azure Policy can automatically remediate noncompliant resources and configurations to ensure the integrity of the state of the resources
- Azure policies do not affect the pre-apply configuration, but will not allow create any more sources of the type that vilate the policy 

Implementing a policy in Azure Policy involves these three steps:
1. Create a policy definition.
1. Assign the definition to resources.
1. Review the evaluation results.

Policy assignment
- is a policy definition that takes place within a specific scope
- inherited by all child resources within that scope
- can exclude a subscope from the policy assignment if there are specific child resources you need to be exempt from the policy assignment.

Policy evaluation happens about once per hour. If you make changes to your policy definition and create a policy assignment, that policy is evaluated over your resources within the hour.

policy initiatives

example policy definitions:
- Allowed virtual machine SKUs
- Allowed locations
- MFA should be enabled on accounts with write permissions on your subscription
- CORS should not allow every resource to access your web applications (Cross-origin resource sharing)
- System updates should be installed on your machines

### Azure Blueprints
- enables you to define the set of standard Azure resources that your organization requires
- ie. you can define a blueprint that specifies that a certain resource lock must exist. Azure Blueprints can automatically replace the resource lock if that lock is removed.

Azure Blueprints orchestrates the deployment of various resource templates and other artifacts, such as:
- Role assignments
- Policy assignments
- Azure Resource Manager templates
- Resource groups

implement by 3 steps:
1. Create an Azure blueprint.
1. Assign the blueprint.
1. Track the blueprint assignments.

blueprint artifacts - Each component in the blueprint definition is known as an artifact.

### Cloud Adoption Framework
- provides you with proven guidance to help with your cloud adoption journey
- helps you create and implement the business and technology strategies needed to succeed in the cloud

includes these stages:
1. Define your strategy.
    1. Define and document your motivations
    1. Document business outcomes
    1. evaluate financial considerations
    1. understand technical considerations
1. Make a plan.
    1. digital estate
    1. initial organizational alignemnt (right peope, technical and cloud governance)
    1. skill readiness plan
    1. cloud adoption plan
1. Ready your organization.
    1. Azure setup guide
    1. azure landing zone (cloud infrastructure as well as governance, accounting, and security capabilities.)
    1. expand the landing zone
    1. best practices
1. Adopt the cloud.
    - migrate
        1. migrate your first workload
        1. migrationscenarios
        1. best practices
        1. prcess improvements
    - innovate
        1. Business value consensus
        1. azure innovation guide
        1. best practices
        1. feedback loops
1. Govern and manage your cloud environments.
    - govern
        1. Methodology
        1. benchmark: Use the governance benchmark tool to assess your current state and future state to establish a vision for applying the framework
        1. initial governance foundation
        1. Improve the initial governance foundation
    - manage
        1. establis a management baseline
        1. define business commitments
        1. expand the management baseline
        1. advanced operations and design priciples

### create a subscription governance strategy
Billing
- one billing report per subscription
- organize subscriptions by department or by project
- Resource Tags can also help

Access control
- A subscription is a deployment boundary for Azure resources. 
- Every subscription is associated with an Azure Active Directory tenant. Each tenant provides administrators the ability to set granular access through defined roles by using Azure role-based access control.
- need separate subscriptions for development and for production environments?

Subscription limits
- Azure ExpressRoute circuits per subscription is 10

## Examine privacy, compliance, and data protection standards on Azure
compliance categories:
- global
- US government
- industry
- regional

closer look at some:
- Criminal Justice Information Service
    - Any US state or local agency that wants to access the FBI's CJIS database
    - Azure is the only major cloud provider that comply
- Cloud Security Alliance STAR Certification. Azure, Intune, and Microsoft Power BI have obtained Cloud Security Alliance (CSA) STAR Certification
    - Conforms to the applicable requirements of ISO/IEC 27001. ( International Organization of Standards/International Electrotechnical Commission)
    - Has addressed issues critical to cloud security as outlined in the CCM. (Clod Controls Matrix)
    - Has been assessed against the STAR Capability Maturity Model for the management of activities in CCM control areas.
- European Union Model Clauses. around transfers of personal data outside of the EU
- Health Insurance Portability and Accountability Act. US federal law that regulates patient Protected Health Information (PHI).
- Multi-Tier Cloud Security Singapore.  rigorous assessments conducted by the Multi-Tier Cloud Security (MTCS) Certification Body, for IaaS, Paas, and Saas
- Service Organization Controls 1, 2, and 3
- National Institute of Standards and Technology Cybersecurity Framework
- United Kingdom Government G-Cloud

#### Azure compliance documentation
 provides you with detailed documentation about legal and regulatory standards and compliance on Azure, across:
- Global
- US government
- Financial services
- Health
- Media and manufacturing
- Regional


### microsoft Privacy statement

data access:
- Azure, all the data used in applications is completely controlled by the user
- Azure themselves do not have the authority to access the data.
- Users are required to take measures such as data encryption


### Online Services Terms
a legal agreement between Microsoft and the customer

### Data Protection Addendum (DPA)
urther defines the data processing and security terms for online services, including:
- Compliance with laws.
- Disclosure of processed data.
- Data Security, which includes security practices and policies, data encryption, data access, customer responsibilities, and compliance with auditing.
- Data transfer, retention, and deletion.

access DPA:
1. goto [Licensing Terms and Documentation](https://www.microsoft.com/licensing/docs)
1. in the search bar, enter DPA
1. locate the link to the DPA in your preferred language

### Trust Center
- In-depth information about security, privacy, compliance offerings, policies, features, and practices across Microsoft cloud products.
- Additional resources for each topic.
- Links to the security, privacy, and compliance blogs and upcoming events.
- is a great resource for people in your organization who might play a role in security, privacy, and compliance
- don't require Azure subscription

access [Trust Center](https://www.microsoft.com/en-ca/trust-center?rtc=1)

### Azure Government
a separate instance of the Microsoft Azure service. It addresses the security and compliance needs of US federal agencies, state and local governments, and their solution providers. Azure Government offers physical isolation from non-US government deployments and provides screened US personnel.

zure Government customers, such as the US federal, state, and local government or their partners, are subject to validation of eligibility. Azure Government services handle data that is subject to certain government regulations and requirements:
- Federal Risk and Authorization Management Program (FedRAMP)
- National Institute of Standards and Technology (NIST) 800.171 Defense Industrial Base (DIB)
- International Traffic in Arms Regulations (ITAR)
- Internal Revenue Service (IRS) 1075
- Department of Defense (DoD) L4
- Criminal Justice Information Service (CJIS)

### Azure China 21Vianet
physically separated instance of cloud services located in China. Azure China 21Vianet is independently operated and transacted by Shanghai Blue Cloud Technology Co., Ltd. ("21Vianet"), a wholly owned subsidiary of Beijing 21Vianet Broadband Data Center Co., Ltd.

Azure agreements and contracts in China, where applicable, are signed between customers and 21Vianet.

# Part 6: Describe Azure cost management and service level agreements

MSDN
- MSDN Platforms is a comprehensive, cost-effective set of resources for setting up development and test environments.
- This will be accessible as a benefit of a pay-as-you-go subscription

## Plan and manage your Azure costs
### Total Cost of Ownership Calcaulator
[TCO Calculator](https://azure.microsoft.com/en-us/pricing/tco/calculator/) helps you estimate the cost savings of operating your solution on Azure over time, instead of in your on-premises datacenter.

### Purchase Azure services
types of Azure subscriptions
- Free trial
- Pa-as-you-go
- Members offer. Your existing membership to certain Microsoft products and services might provide you with credits for your Azure account and reduced rates on Azure services

how to purchase
- Through an Enterprise Agreement
- Directly from the web
- Through a Cloud Solution Provider

cost factors: (Azure provides flexibility for capital expenditure (CapEx) and operating expenditure (OpEx).)
- Resource type. storage account type, performance tier (standard/premium), access tier (hot, cool, archive)
- Usage meters
    - Overall CPU time.
    - Time spent with a public IP address.
    - Incoming (ingress) and outgoing (egress) network traffic in and out of the VM.
    - Disk size and amount of disk read and disk write operations.
- Resource usage. delete VS delocate(temporarily shut down in weekends)
- subscription types
- Azure Marketplace. to purchase Azure-based solutions and services from third-party vendors
- Location. Different regions can have different associated prices
- Zones for billing of network traffic. Some inbound data transfers (data going into Azure datacenters) are free. For outbound data transfers (data leaving Azure datacenters), data transfer pricing is based on zones. A zone is a geographical grouping of Azure regions for billing purposes. The following zones include some of the regions as shown here:
    - Zone 1: Australia Central, West US, East US, Canada West, West Europe, France Central, and others
    - Zone 2: Australia East, Japan West, Central India, Korea South, and others
    - Zone 3: Brazil South, South Africa North, South Africa West, UAE Central, UAE North
    - DE Zone 1: Germany Central, Germany Northeast

### [Manage and minimize total cost on Azure](https://docs.microsoft.com/en-ca/learn/modules/plan-manage-azure-costs/6-manage-minimize-total-cost)
- Understand estimated costs before you deploy
- Use Azure Advisor to monitor your usage
- Use spending limits to restrict your spending
- Use Azure Reservations to prepay
- Choose low-cost locations and regions
- Research available cost-saving offers
- Use Azure Cost Management + Billing to control spending. including:
    - reporting
    - data enrichemnt
    - budgets
    - alerting
    - recommendations
- Apply tags to identify cost owners
- Resize underutilized virtual machines
- Deallocate virtual machines during off hours
- Delete unused resources
- Migrate from IaaS to PaaS services
- Save on licensing costs
- Choose cost-effective operating systems
- Use Azure Hybrid Benefit to repurpose software licenses on Azure


## Choose the right Azure services by examining SLAs and service lifecycle

### [Service-level agreements (SLA)](https://azure.microsoft.com/en-us/support/legal/sla/)
- introduction
- general terms
- SLA details

SLA percentage 	Downtime per week 	Downtime per month 	Downtime per year
- 99 	1.68 hours 	7.2 hours 	3.65 days
- 99.9 	10.1 minutes 	43.2 minutes 	8.76 hours
- 99.95 	5 minutes 	21.6 minutes 	4.38 hours
- 99.99 	1.01 minutes 	4.32 minutes 	52.56 minutes
- 99.999 	6 seconds 	25.9 seconds 	5.26 minutes

service credits: (monthly, credit percentage)
- < 99.99 	10
- < 99 	25
- < 95 	100

Free products typically don't have an SLA.

**Enterprise Agreement (EA) subscriptions** are only available to some users

### deisgn your app to meet SLA
Combine SLAs: production of each SLA

strategies:
- Choose customization options that fit your required SLA
- Build availability requirements into your design
    - Deploying two or more instances of an Azure virtual machine across two or more availability zones raises the virtual machine SLA to 99.99 percent
- Include redundancy to increase availability

## preview services and preview features
to look into new capabilites
- The public preview service is available to all users
- The private preview is only available to some users

### service lifecycle
defines how every Azure service is released for public use: develope and build -> released to preview -> validated and tested

### terms and conditions to expect
- Each Azure preview defines its own terms and conditions.
- All preview-specific terms and conditions supplement your existing Azure service agreement.
- Some previews aren't covered by customer support

### access preview services
1. Azure portal
1. Create a resource
1. enter *preview* in the search box
1. select a service to learn more about it

### access new features for an existing service
These preview features are accessible when you deploy, configure, and manage the service.

### access preview features for the Azure portal
goto [Microsoft Azure (Preview)](https://preview.portal.azure.com/#home)

### feedback
- From the Feedback tab in the Azure portal.
- From the [Azure portal feedback forum](https://azure.microsoft.com/en-us/feedback/).

### stay updated on the latest announcements
[Azure updates](https://azure.microsoft.com/en-us/updates/) to:
- View details about all Azure updates.
- See which updates are in general availability, preview, or development.
- A screenshot of the Azure updates page showing how to filter services by now available, in preview, or in development.
- Browse updates by product category or update type.
- Search for updates by keyword.
- Subscribe to an RSS feed to receive notifications.
- Access the Microsoft Connect page to read Azure product news and announcements.

