https://github.com/wzlwit/workshop/blob/main/Az%20Fundamentals/AZ900_fundamentals_learnPath.md

The Azure Import / Export service can securely import large amounts of data (**CSV File**) into Azure Blob Storage and Azure Files by sending disk drives to your Azure datacenter.  

users need to create a TXT (DNS) record type so that their custom domain can join Azure Active Directory

Azure Information Protection (**AIP**)
- a cloud-based solution that allows organizations to label (watermark) content to detect, classify, and protect **documents** and **emails**
- part of the Microsoft Information Protection (MIP) solution, and extends the labeling and classification functionality provided by Microsoft 365
- **can not** encrypt: 
    - records in Azure SQL Database
    - Azure storage account (to Encrypt stored data using the encryption service implemented in Azure services Encryption at Rest)
    - network traffic (To encrypt network traffic, you need to configure TLS - Transport Layer Security.)

Azure Application Insights
- an application performance management (APM) service, a service for sending telemetry information from application source code to Azure
- a feature of *Azure Monitor* and uses Azure Monitor under the hood, 
- allows you to monitor running applications and automatically detect performance anomalies
- use built-in analytics tools to view what your users do on your app.
- can monitor and analyze **telemetry** from mobile apps by integrating with *Visual Studio App Center*

Knowledge Center. a collection of common questions and answers about Azure

No access:
- Azure does not have permission to access the data of datacenter

End-to-end: describes a process that takes a system or service from beginning to end and delivers a complete functional solution, usually without needing to obtain anything from a third party

Shared Responsibility model
- Provider
    - Maintenance of the physical hosts
- shared
    - manangement of Accounts and Identities
- customer
    - Management of information and data


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
- **Be ready for the future**: Continuous innovation from Microsoft supports your development today and your product visions for tomorrow.
- **Build on your terms**: You have choices. With a commitment to open source, and support for all languages and frameworks, you can build how you want and deploy where you want to.
- **Operate hybrid seamlessly**: On-premises, in the cloud, and at the edge--we'll meet you where you are. Integrate and manage your environments with tools and services designed for a hybrid cloud solution.
- **Trust your cloud**: Get security from the ground up, backed by a team of experts, and proactive compliance trusted by enterprises, governments, and startups.


### Azure work
https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/what-is-microsoft-azure

Fabric controller > orchestrator

### Azure portal
The Azure portal is a web-based, unified console that provides an alternative to command-line tools. With the Azure portal, you can manage your Azure subscription by using a graphical user interface. You can:
- Build, manage, and monitor everything from simple web apps to complex cloud deployments.
- Create custom dashboards for an organized view of resources.
- Configure accessibility options for an optimal experience.

#### Azure Cloud Shell
- can be used on iOS
- Cloud Shell is a management machine for Azure, managed by Microsoft.
- Azure Cloud Shell gives you the flexibility to choose the best shell operation for your business.
- Both Bash and PowerShell are options for this.

#### Azure PowerShell
- **can execute commands** called cmdlets (pronounced command-lets). 
- Azure PowerShell is available for Windows, Linux, and Mac, and you can access it in a web browser via Azure Cloud Shell.
- to orchestrate:
    - The routine setup, teardown, and maintenance of a single resource or multiple connected resources.
    - The deployment of an entire infrastructure, which might contain dozens or hundreds of resources, from imperative code.

#### The Azure CLI

#### [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/)
- a set of commands used to create and manage Azure resources; ms cross-platform command-line experience for managing Azure Resources
- **cannot** be installed on iOS, works on Win, macOS and Linux
- can use Bash from Cloud Shell (works in **CloudShell**) by logging in to the Azure portal from your Android laptop. Then you can create a new virtual machine from Bash with CLI.
- e.g.
    the IT Engineer has a Windows desktop and has installed the Azure **Command Line interface**. IT engineer cna use the Azure CLI from:
    - Powershell
    - Command prompt

### Power Apps portal
- to create external websites that allow users outside your organization to sign in with different identities, create and view data in Microsoft Dataverse, and browse content anonymously.
- This is not the mechanism to use when creating a virtual machine


### [Azure Marketplace](https://azuremarketplace.microsoft.com/en-US/)
Azure Marketplace customers can find, try, purchase, and provision applications and services from hundreds of leading service providers. All solutions and services are certified to run on Azure

### [Azure services](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/tour-of-azure-services)

Resource groups:
- Resources with the same life cycle can be grouped together on the same resource group
- When you delete a resource group, all the resources on it are also deleted

#### Compute
Azure Service Fabric:
- Build and operate always-on, scalable, distributed apps (micro service)
- Cluster management for VMs that run containerized services.
- Distributed systems platform that runs in Azure or on-premises.

#### Networking
Azure Load Balancer: 
- Balances inbound and outbound connections to applications or service endpoints. (port forwarding)
- *can increase availability* of resources

Azure DNS: Provides ultra-fast DNS responses and ultra-high domain availability.

Azure Content Delivery Network (CDN): 
- PaaS
- a secure, reliable, and fast network to deliver high-bandwidth content to customers globally. 
- reduce load times, save bandwidth, and improve responsiveness.
- develop and manage websites and mobile apps
- accelerate streaming media and game software, firmware updates, and IoT endpoint encoding and delivery. 


Azure DDoS Protection: Protects Azure-hosted applications from distributed denial of service (DDOS) attacks.

Azure Traffic Manager: Distributes network traffic across Azure **regions worldwide**.

Azure ExpressRoute: Connects to Azure over high-bandwidth dedicated secure connections.
- transfer data from your on-premises datacenter to Azure Public Cloud
- not charged for inbound data transfer

Azure Network Watcher: Monitors and diagnoses network issues by using **scenario-based** analysis.

Azure Firewall: Implements high-security, high-availability firewall with unlimited scalability.

Azure Virtual WAN: Creates a unified wide area network (WAN) that connects **local and remote sites**.


#### Storage
##### Azure Blob storage:
- Storage service for very large objects, such as video files or bitmaps.
-  used to store blob type data and acts as an Azure virtual machine disk - data disk:
    - attached to VMs
    - stored in the Blob service of Azure storage accounts

##### Azure File storage:
- used for files that can be accessed via the *SMB 3.0, HTTPS protocol or network File System (NFS) protocol*
    - SMB: provides a way for a computer's client applications to read and write to files and to request services from server programs
- File shares that can be accessed and managed like a file server.
- Azure file can be mounted simultaneously via cloud or on-premises deployments on Windows, Linux, and macOS
- use **Azure File Sync** to cache your Azure file on Windows Server for quick access to where your data is being used

Azure file share can be used to:
- Replace or supplement on-premises file servers
- "lift and shift" applications. (move both the application and its data to cloud)
- Simplify cloud development:
    - Shared application settings
    - Diagnostic share
    - Dev/Test/Debug
- Containerization: 
    - Azure file shares can be used as persistent volumes for stateful containers. Containers deliver "build once, run anywhere" capabilities that enable developers to accelerate innovation. For the containers that access raw data at every start, a shared file system is required to allow these containers to access the file system no matter which instance they run on
    
##### Azure Queue storage:
- A data store for queuing and reliably delivering messages between applications.
- one queue is max 64kb, including a list (milions) of messages  to be processed asynchronously
- For example,  you want to create thumbnails for each picture uploaded by customers. 
    - You can let customers wait for you to create a thumbnail while uploading a picture.
    - Another option is to use queues: 
        1. After the client finishes uploading, a message is written to the queue.
        1. Then let the Azure function retrieve the message from the queue and create the thumbnail.
    - Each part of the above process can be scaled separately to give you more control when adjusting and using it 

##### Azure Table storage:
- ideal service for storage of user related data
- a cloud-based NoSQL datastore you can use to store large amounts of structured, non-relational data (structured NoSQL data)
- providing a **key/attribute** store with a **schemaless** design.

###### Azure Data Lake / Data Lake Storage:
- storage repository suitable for holding large amounts of data. 
- With 30TB of data stored, the data lake can scale up to terabytes and petabytes of data.
- e.g.: data infreuqently used which needs to be accessd via Power BI
- [Azure Data Lake Storage Gen2](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction)
    - a set of capabilities dedicated to big data analytics, built on Azure Blob Storage
    - converge two features:
        - Azure Data Lake Storage Gen1: file system semantics, file-level security, and scale
        - Blob storage: low-cost, tiered storage, with high availability/disaster recovery capabilities

#### characteristics of Storage:
- **Durable** and highly available with redundancy and replication.
- **Secure** through automatic encryption and role-based access control.
- **Scalable** with virtually unlimited storage.
- **Managed**, handling maintenance and any critical problems for you.
- **Accessible** from anywhere in the world over HTTP or HTTPS.

#### Azure storage account and copies
- Data in your Azure Storage account is always replicated three times in the primary region and keeps them synchronous.
- It is also asynchronously copied to the *secondary* region (another copy).
- An Azure storage account contains all Azure Storage data objects (blobs, files, queues, tables, and disks).

#### Mobile
- developers can create mobile back-end services for iOS, Android, and Windows apps quickly and easily.
- Features that used to take time and increase project risks, such as adding corporate sign-in and then connecting to on-premises resources such as SAP, Oracle, SQL Server, and SharePoint, are now simple to include.
- other features include:
    - Offline data synchronization.
    - Connectivity to on-premises data.
    - Broadcasting push notifications.
    - Autoscaling to match business needs.

#### Databases
[ Features comparison: Azure SQL Database and Azure SQL Managed Instance](https://docs.microsoft.com/en-us/azure/azure-sql/database/features-comparison)

[why Azure Sql databasie is PaaS not SaaS](https://docs.microsoft.com/en-us/answers/questions/243089/azure-sql-managed-instance-paas-or-saas.html)
- can configure High Availability, Disaster Recovery, and configure options for Business Continuity
- Azure SQL offers a good amount of management options that are not available on SaaS
- the **security of the data** on Azure SQL Database is not at responsibility of Microsoft as service provider

##### **Azure Database Migration Service**
can be used to migrate on-premise sql server ( or native backup and restore) to cloud (Azure Sql or Managed Instance) with no application code changes

##### Azure SQL Database (PaaS): 
- 99.99%
- Fully managed relational database with auto-scale, integral intelligence, and robust security.
- enables you to process both relational data and non-relational structures, such as graphs, JSON, spatial, and XML.
- only uses the default SQL_Latin1_General_CP1_CI_AS server collation

##### [Azure SQL Elastic Pool](https://docs.microsoft.com/en-us/azure/azure-sql/database/elastic-pool-overview)
- a simple, cost-effective solution for managing and scaling multiple databases that have varying and unpredictable usage demands
- DTUs or VCores

##### Azure SQL Managed Instance
- PaaS, 99.99%
- provides several options that might not be available to Azure SQL Database (collation)
- provides *native virtual network implementation*

##### Azure SQL Data Warehouse
a fully managed cloud data warehouse to get query results in a short time across terabytes and petabytes of data. with decoupled storage and compute , SQL Data Warehouse can (Scalability):
- Independently size compute power irrespective of your storage needs
- Grow or shrink compute power without moving data
- Pause compute capacity while leaving data intact, so you only pay for storage
- Resume compute capacity during operational hours

[SQL Database VS SQL Data Warehouse](https://stackify.com/azure-sql-database-vs-warehouse/)

##### Azure Cosmos DB:
- a fully managed globally distributed, **multi-model database** service that supports NoSQL options.
- can create different types of data stores such as Mongo DB and Cassandra
- no access to the underlying database server.
- supports schema-less data, build highly responsive and "Always On" applications 
- The data is abstracted and projected as an API, include SQL, MongoDB, Cassandra, Tables, and Gremlin
- *Guaranteed single-digit millisecond responsetime  (low latency)* and 99.99% availability.
- Azure Cosmos DB can store JSON documents.

##### Azure Database for MySQL: 
- Fully managed and scalable MySQL relational database with high availability (99.99%) and security with no additional cost.
- Predictable performance and inclusive, pay-as-you-go pricing.

##### Azure Database for PostgreSQL:
- Fully managed and scalable PostgreSQL relational database with high availability and security.
- single server. 3 pricing tiers: Basics, General Purpose, **Memory Optimized**
- hyper scale. 
    - horizontally scales queries across multiple machines by using sharding
    - can serve worklods exceeding 100GB data
    - supports multi-tenant applications, real-time operational analytics, and high throughput transactional workloads

##### Azure Database for MariaDB: Fully managed and scalable MariaDB relational database with high availability and security.

##### Azure Cache for Redis: 
- Fully managed service caches frequently used and static data to reduce data and application latency.
- in-memory data store
- Not suitable for storing JSON documents

#### Web
The following Azure services are focused on web hosting:  
Azure App Service: Quickly create powerful cloud web-based apps.
- 99.95%
- fully managed **platform** service (**PaaS**), fast-building, deploying, and scaling service for *web applications*, *mobile backend* and *RESTful API* at scale
- does not provide a serverless environment
- *when to use*:
    1. (Windows/Linux) Web apps
    2. API apps
    3. Mobile apps (quickly build a back end for iOS and Android app)
        - Store mobile app data in a cloud-based SQL database.
        - Authenticate customers against common social providers, such as MSA, Google, Twitter, and Facebook.
        - Send push notifications.
        - Execute custom back-end logic in C# or Node.js.
    4. Logic Apps
    - Dock container
    - Functions
    - WebJobs (run a progrom/script in the same context as w Web App; can be scheduled or run by a trigger)
- Benifits
    - Deployment and management are integrated into the platform.
    - Endpoints can be secured.
    - Sites can be scaled quickly to handle high traffic loads.
    - The built-in load balancing and traffic manager provide high availability. 
- [pricing](https://docs.microsoft.com/en-us/azure/app-service/overview-hosting-plans)
    - Shared compute
    - Dedicated Compute: Basic, Standard, Premium, PremiumV2, Premium V3
    - Isolated


Azure Notification Hubs: a massively scalable mobile push notification engine for quickly sending millions of notifications to any platform (iOS, Android, Windows, or Kindle devices) from any back end

Azure API Management: Publish APIs to developers, partners, and employees securely and at scale.

Azure SignalR Service: Add real-time web functionalities (communications to web application) easily.


#### Internet of Things (IoT)
the internet allows any item that's online-capable to access valuable information. This ability for devices to garner and then relay information for data analysis is referred to as IoT.  

IoT hub: 
- a central message hub for *bi-directional* communication/monitor* between IoT application and devices it manages, supporting multiple messaging patterns: 
    - device-to-cloud telemetry
    - file upload from devices
    - and request-reply methods to control your devices from the cloud. As a cloud-to-device perspective, IoT Hub allows for *command and control*
        - either manual or automated remote control of connected devices
        - can instruct the device to open valves, set target temperatures, restart stuck devices, and so on
- IoT hub can route messages received from devices to other Azure services.

IoT Central: 
- Fully managed global IoT software as a service (**SaaS**) solution that makes it easy to connect, monitor, and manage IoT assets at scale.
- builds on top of IoT Hub by adding a dashboard to connect, monitor, and manage your IoT devices.
- UI helps to monitor, aggregate, alert and push notifications and firmware updates.
- provides starter templates for different business types.
- use of device templates to construct the dashboards, alerts, and so on. Device developers still need to create code to run on the devices, and that code must match the device template specification.

Azure Sphere (hardware)
- a secured, high-level application platform with built-in communication and security features for internet-connected devices
- it comprises:
    - Azure Sphere micro-controller unit (MCU).  responsible for processing the operating system and signals from attached sensors.
    - customized Linux operating system (OS).  handles communication with the security service and can run the vendor's software
    - Azure Sphere Security Services, also known as AS3

IoT Edge: 
- Fully managed service 
- allows data analysis models to be pushed directly **onto IoT devices**
- which allows them to react quickly to state changes without needing to consult cloud-based AI models.
- Used to analyze data on End user devices

Azure Time Series Insights (IoT deployments)
- an end-to-end PaaS
- to ingest, process, store and query highly contexualized, time-series-optimized IoT-scale data.
- is ideal for ad-hoc data exploration and operational analysis

#### Big data (and analytics)
Azure Synapse Analytics: Fully managed data warehouse with integral security at every level of scale at no extra cost.  Run analytics at a massive scale by using a cloud-based enterprise data warehouse that takes advantage of massively parallel processing to run complex queries quickly across petabytes of data.
- query data on your terms by using either serverless or provisioned resources at scale
- unified experience to ingest, prepare, manage, and serve data for immediate business intelligence and machine learning needs
- an Azure analytics service that combines data integration (data collection, exploration, preparation, and management), big data analytics and an **enterprise data warehouse** (EDW)
- significantly reducing the time it takes to develop your project with an integrated experience that supports the development of **end-to-end** analytics solutions
- cannot be used for a predictive analytics model

Azure HDInsight:
- Provide a cloud service that makes it easy, fast, and cost-effective to analyse *streaming data* and to process *massive amounts of data* with managed Hadoop clusters in the cloud.
- run open-source frameworks and create cluster as Apache (Spark, Hadoop, Kafa, HBase, Storm), and Machine learning services
- supports a broad range of scenarios such as <ins>ETL, data warehousing, machine learning, and IoT</ins>.

Azure Databricks:
- a fast, easy-to-use Apache Spark-based big data analytics service designed for data engineering.
- Python, Scala, R, Java, and SQL
- data science frameworks and libraries: TensorFlow, PyTorch, and scikit-learn.

Azure Data Lake Analytics. 
- an on-demand analytics job service that simplifies **big data**.
- Easily develop and run massively parallel data transformation and processing programs
- write queries to transform your data and **extract valuable insights** without taking care of hardwares
- pay for your job when it's running 

Azure Event Hubs
- a fully managed, real-time data ingestion service that’s simple, trusted, and scalable;  a big data streaming platform and event capture service.
- Stream/process millions of events per second from any source into a centralized repository to build dynamic data pipelines and immediately respond to business challenges
- can monitor the activities performed by users and store that data

[Azure Event Grid](https://docs.microsoft.com/en-us/azure/event-grid/overview)
- kind of infrustracture to build applications with event-based architectures
- use filters to route specific events to different endpoints, multicast to multiple endpoints, and make sure your events are reliably delivered.
- collect events from multiple sources and then relay them to an application

#### AI
the core of which is machine learning, which is a data science technique that allows computers to use existing datato to train a model, test it, and then apply the model to new data to forecast future behaviors, outcomes, and trends. Using machine learning, computers learn without being explicitly programmed  


**Azure Machine Learning Service**: Cloud-based environment you can use to develop, train, test, deploy, manage, and track machine learning models. It can auto-generate a model and auto-tune it for you. It will let you start training on your local machine, and then scale out to the cloud.
- a development platform for coding machine learning
- to build a predictive analytics model that uses past user behavior data
You can:
- Create a process that defines how to obtain data, how to handle missing or bad data, how to split the data into either a training set or test set, and deliver the data to the training process.
- Train and evaluate predictive models by using tools and programming languages familiar to data scientists.
- Create pipelines that define where and when to run the compute-intensive experiments that are required to score the algorithms based on the training and test data.
- Deploy the best-performing algorithm as an API to an endpoint so it can be consumed in real time by other applications.

**deep learning**, which is modeled on the neural network of the human mind, enabling it to discover, learn, and grow through experience

Azure ML Studio: 
- data science solution that enables users to build and deploy a machine learning (ML) without coding
- Collaborative visual workspace where you can build, test, and deploy machine learning solutions by using prebuilt machine learning algorithms and data-handling modules.

**cognitive Services**
an AI platform that can be used by all developers without needing any machine learning expertise via APIs. You can embed AI functions such as image identification in the app with this

A closely related set of products are the **Azure Cognitive** services. You can use these prebuilt APIs in your applications to solve complex problems: 
- incorporate mechanisms such as image identification into your applications from APIs without any machine learning expertise.
- **Vision**: Use image-processing algorithms to smartly identify, caption, index, and moderate your **pictures** and **videos**.
    - customize and embed state-of-the-art computer vision image analysis for specific domains
    - build a smooth customer experiences, optimize manufacturing processes, drive digital marketing campaigns
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
- Provisioning pre-created lab environments (pre-built template) with their required configurations and tools already installed is a huge time saver
- no need to wai for approvals for creating the machines

### Azure accounts
Azure free account includes:
- Free access to popular Azure products for **12 months**.
- A **credit** (USD200) to spend for the **first 30 days**.
- Access to more than 25 products that are always free.
- host production-based resources
    - need to pay for any extra charges that don't come under the Free Account conditions

The Azure free student account offer includes:
- Free access to certain Azure services for 12 months.
- A credit to use in the first 12 months.
- Free access to certain software developer tools.

## Discuss Azure fundamental concepts
### cloud models
- Public cloud: Services are offered over the public internet and available to anyone who wants to purchase them. Cloud resources, such as servers and storage, are owned and operated by a third-party cloud service provider, and delivered over the internet.
    - the cloud vendor manages the data center
    - No capital expenditures to scale up.
    - Applications can be quickly provisioned and deprovisioned.
    - Organizations pay only for what they use.
- Private cloud: A private cloud consists of computing resources used exclusively by users from one business or organization. A private cloud can be physically located at your organization's on-site (on-premises) datacenter, or it can be hosted by a third-party service provider.
    - requires a data center in order to host infrastruture
    - Hardware must be purchased for start-and maintenance.
    - Organizations have complete control over resources and security.
    - Organizations are responsible for hardware maintenance and updates.
- Hybrid cloud: A hybrid cloud is a computing environment that combines combines on-premises infrastructure—or a private cloud—with a public cloud by allowing data and applications to be shared between them.
    - pros:
        - better Control
        - Flexibility: take advantage of additional resources in public cloud
        - Cost-effectiveness: pay when cloud resources is needed
        - Ease: migrate gradually
    - Provides the most flexibility.
    - Organizations determine where to run their applications.
    - Organizations control security, compliance, or legal requirements.
    - You can also build a hybrid cloud configuration by using *multiple public clouds*

### cloud computing advantages
*a consumption-based model*
- **High availability**: Depending on the service-level agreement (SLA) that you choose, your cloud-based apps can provide a continuous user experience with no apparent downtime, even when things go wrong.
- **Reliability** depends on the service level agreement you choose, but in the event of a problem, your cloud-based application will continue to provide the user experience without any obvious downtime
- **resiliency** 
    - Continuing service in the event of a failure
    - Maintaining a DR (Disaster Recovery) configuration in other regions
- **Fault Tolerance**
    - the ability of a system to remain operational after a critical failure through configurations and other measures such as redundant hardware
- **Scalability**: Apps in the cloud can scale vertically and horizontally:
    - *not necessarily atutamted*
    - Scale vertically (up-down) to increase compute capacity by adding RAM or CPUs to a virtual machine.
    - Scaling horizontally (in-out) increases compute capacity by adding instances of resources, such as adding VMs to the configuration.
- **Elasticity** or **flexibility**: You can configure cloud-based apps to take advantage of autoscaling, so your apps always have the resources they need.
    - *automatic*
    - cloud-based applications can be configured to always have the resources they need
    - the ability of services to automatically scale resources based on changing demand. (resource on demand)
    - ScalingSet helps automate the process of adding or removing virtual machines as demand increases or decreases
    - to change resource allocation is an example of cloud flexibility or elasticity.
- **Agility**: 
    - Deploy and configure cloud-based resources quickly as your app requirements change.
    - The ability to respond to and drive **market change quickly**
- **Geo-distribution**: You can deploy apps and data to regional datacenters around the globe, thereby ensuring that your customers always have the best performance in their region.
- **Disaster recovery**: By taking advantage of cloud-based backup services, data replication, and geo-distribution, you can deploy your apps with the confidence that comes from knowing that your data is safe in the event of disaster.

### CapEx VS OpEx
- Enterprise Agreement (EA) subscriptions and Azure Reserved Instances are CapEx solutions
- pay-as-you-go subscriptions are also available and are considered OpEx.
- Azure gives you the *flexibility* to choose.
- In CapEx, costs are fixed
- You must wait over a period of years to depreciate that investment (CapEx) on your taxes

### different cloud services / service type:
[pros and cons](https://docs.microsoft.com/en-ca/learn/modules/fundamental-azure-concepts/categories-of-cloud-services)
- **Serveless**. enables developers to build applications faster by eliminating the need for them to manage infrastructure. With serverless applications, the cloud service provider automatically provisions, scales, and manages the infrastructure required to run the code
- **IaaS**: provider will keep the hardware up-to-date, but operating system maintenance and network configuration is up to you
    - Virtual Machines. rapid deployment
    - Kubernets
    - Azure Storage Accounts
- **PaaS**: providers manage the VMs and network; tenant deploys their applications into the managed hosting environment
    - Azure app services
    - Azure web apps. build applications on the Azure platform without deploying, configuring, and maintaining their own Azure virtual machines.
    - Azure Logic Apps. schedule, automate, and coordinate tasks, business processes, and workflows when you need to integrate apps, data, systems, and services across your enterprise or organization
    - Azure SQL
        - Azure SQL Managed Instance
    - content delivery network (cdn)
- **Saas**: provider manages all aspects; tenant only needs to provide their data to the application managed by the cloud provider
    - no worry about the solution itself, the scalability or availability
    - just manage the *configuration*
    - charged monthly/yearly, no pay-as-you-go
    - e.g.
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
    - can't merge two subscriptions in Azure. ach subscription is a separate entity that cannot be merged. 
    - can **transfer (billing or) ownership** of a subscription to another account
    - can have more than one license. (because a license can be assigned to each user account individualy)
        
- Resource groups: Resources are combined into resource groups, which act as a logical container into which Azure resources like web apps, databases, and storage accounts are deployed and managed.
- Resources: Resources are instances of services that you create, like virtual machines, storage, or SQL databases.

#### Geography
- any region of the world that contains at least one Azure region
- Regions define individual markets and maintain boundaries between data location and compliance
- 10+ geographies

#### Zone
A zone are regional groups of Azure regions for billing. Data transfer charges are based on the zone.

#### Region
- The cost for resources differs from region to region.
- A group of data centers connected by a **high-speed** network
- geographically separated from each other
- Each region has at least **three** separate zones.
- customer cannot decide on the region pairs used by the underlying Azure storage services
- multi-region support is not optimal in terms of architectural configuration because it is difficult to link virtual machines across regions
- 60+ regions


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
- **not** enabled in all the regions
- (unique) physical locations within a unique physical region. Availability Zones within the region are geographically close and connected by a **leased line**
- Each zone consists of one or more data centers with **independent** power supplies, cooling means, and networks
- Availability zones are connected through *high-speed, private fiber-optic* networks.
- to prevent a single data center failure, you only need to use multiple availability zones and do not need to have a multi-region configuration
- By default, Azure Availability Zones are used to replicate applications and data only within the Azure region. (not differe region)

Azure services that support availability zones fall into three categories:
- Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).
- Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database). 
- Non-regional services: Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages.
- Not every region has support for Availability Zone

#### [Availablity SET](https://k21academy.com/microsoft-azure/az-303/azure-availability-zones-and-regions/)
- An Availability Set is a logical grouping capability for isolating VM resources from each other when they’re deployed.
- By deploying your VMs across multiple hardware nodes Azure ensures that if hardware or software failure happens within Azure, only a sub-set of your virtual machines is impacted and your overall solution is safe and in working condition.
- It provides redundancy for your **virtual machines**; An Availability set spreads your virtual machines across multiple *fault domains* (FD) and *update domains* (UD).
- If you want to leverage Microsoft’s 99.95% SLA from Microsoft you must place your VMs inside availability set except your VMs are having premium storage. (both Availability Set and Mutli-AZ can increase SLA)


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

### Azure Maps
Azure Maps is a collection of geospatial services and SDKs that use fresh mapping data to provide geographic context to web and mobile applications.
- SLA 99.9%

### resource,Resource Group ARM
[benefits of using Resource Manager](https://docs.microsoft.com/en-ca/learn/modules/azure-architecture-fundamentals/resources-resource-manager)

#### Resource Manager
- deployment and management service that provides a way to organize and secure your cloud resources.
- access Resource Manager from the Azure portal, Azure Cloud Shell, Azure PowerShell, and the Azure CLI
- It provides the following functions:
    - Use ARM template to implement the infrastructure as code for your Azure solution.
    - Resource group setting, resource management by tagging and locking is possible.
    - You can use *Azure managed applications* to provide cloud solutions that users can easily deploy and operate.
    - The A*zure Custom Resource Provider* allows you to define custom APIs that you can use to enhance your default Azure experience.  

all the tools that can deploy resources:
- Azure Portal
- **Powershell**
- CLI
- REST API
- **SDK**. (a collection of libraries built to make it easy to use Azure services in your language of choice)


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
- SLA:
    - 99.9% (only one using Premium SSD or Ultra Disk)
    - **99.95% (more than one, Scale Set)**
    - 99.99% (over 2 AZs)

[Just-In-Time (JIT)](https://docs.microsoft.com/en-us/azure/security-center/security-center-just-in-time?tabs=jit-config-asc%2Cjit-request-asc) 
- Just-in-time access provides access to the virtual machine only for a specified amount of time. This is one of the security methods you can use to protect your VMs in Azure
- Use the Azure Security Center's Just-In-Time (JIT) Virtual Machine (VM) access feature to lock down inbound traffic to Azure Virtual Machines. This makes it easier to connect to the VM when needed, while reducing the risk of exposure.

attention:
- By default, all inbound connections are not allowed on L4, so unless you have a *network interface*, you need to modify the rules of the **network security group** so that all inbound connections from port 80/8080 can reach the VM. 


**Azure Virtual machine scale sets**
- deploy and manage a set of identical VMs
- easier to build large-scale services targeting big compute, big data, and containerized workloads
- easy to maintain route request. (load balancer)
- more VM instances can be added or removed. The number of VM instances can automatically increase or decrease in response to demand or a defined schedule
- The process can be manual, automated, or a combination of both.
- **LIMIT**
    - 1000. up to 1,000 VM instances for standard marketplace images and custom images through the Shared Image Gallery
    - 600. using a managed image, the limit is 600 VM instances.

**[Azure Spot Virtual Machines](https://azure.microsoft.com/en-us/services/virtual-machines/spot/)**
    ideal for workloads that can be *interrupted* if the machines are taken away because of Azure having less capacity

**Hyper V host**
is a hypervisor that provides a virtualized environment

**Azure Batch**: enables large-scale parallel and high-performance computing (HPC) batch jobs with the ability to scale to tens, hundreds, or thousands of VMs. When you're ready to run a job, Batch does the following:
- Starts a pool of compute VMs for you.
- Installs applications and staging data.
- Runs jobs with as many tasks as you have.
- Identifies failures.
- Requeues work.
- Scales down the pool as work completes.

**Azure Container**

**Azure Kubernetes Service**
- IaaS
- a managed service that can orchestrate the deployment and management of the containers
- to deploy and manage containers (lightweight, virtualized application environment)
- multiple container in one host

**[microservice] (https://docs.microsoft.com/en-ca/learn/modules/azure-compute-fundamentals/azure-container-services)**
**Azure App Service**
**Azure Functions** (serverless computing)
- can
    - solve complex orchestration problems to develop serverless applications
    - Can edit the code right in the Azure Portal using a code editor
- Abstraction of servers, an event-driven serverless computing platform. Event-driven scale
    - Timers, for example, if a function needs to run every day at 10:00 AM UTC.
    - HTTP, for example, API and webhook scenarios.
    - Queues, for example, with order processing.
    - And much more.
- micro-billing
- you write code to complete each step
**Azure Logic Apps** (serverless computing)
    - Servless model
    - designed in a web-based designer
    - can execute logic triggered by Azure services without writing any code.
    - you use a GUI to define the actions and how they relate to one another.
**Azure Virtual Desktop**
- simplified management
- performance management. gives you options to load balance users on your VM host pools. Host pools are collections of VMs with the same configuration assigned to multiple users.
- Multi-session Win10 Deployment

**Azure Service Bus**
- Enterprise messaging solution. (message service)
- 

## networking services
Encryption:
- You can install roles such as the Remote Access Server for VPN to ensure traffic is encrypted when it flows out of the server
-  https://docs.microsoft.com/en-us/windows-server/remote/remote-access/vpn/always-on-vpn/deploy/vpn-deploy-ras

Azure Virtual Network: 
- a private isolated network in Azure
- Connects VMs to incoming virtual private network (VPN) connections
- enable Azure resources, such as VMs, web apps, and databases, to communicate with each other, with users on the internet, and with your on-premises client computers.
- think of an Azure network as a set of resources that links other Azure resources.

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
    - **Route tables**. define rules about how traffic should be directed. control how packets are routed between subnets. Azure automatically creates a route table for each subnet within an Azure virtual network and adds system default routes to the table. You can add custom route tables to modify traffic between virtual networks. only contains a set of rules (routes) that specify how packets are routed in the virtual network
    - **Border Gateway Protocol** Border Gateway Protocol (BGP) works with Azure VPN gateways or ExpressRoute to propagate on-premises BGP routes to Azure virtual networks.
- Filter network traffic. filter traffic between subnets by using the following approaches:
    - **Network security groups**
        - A network security group is an Azure resource that can contain multiple inbound and outbound security rules. You can define these rules to allow or block traffic, based on factors such as source and destination IP address, port, and protocol.
        - You create the network security group separately, Then you associate it with the virtual network. (can only be applied at the Network)Interface layer or the Subnet layer
    - **Network virtual appliances** A network virtual appliance is a specialized VM that can be compared to a hardened network appliance. A network virtual appliance carries out a particular network function, such as running a firewall or performing wide area network (WAN) optimization.

- Connect virtual networks
    - virtual network *peering*, which links virtual networks and enables resources in each vNet to communicate
    - the vNets can be in separate regions, which allows to create a global interconnected network through Azure
    - user-defined Routing (UDR). a significant update to Azure’s Virtual Networks; allows allows network admins to control the routing tables between subnets within a VNet, as well as between VNets, allowing for greater control over network traffic flow.
    - https://docs.microsoft.com/en-ca/learn/modules/azure-networking-fundamentals/azure-virtual-network-fundamentals
- [Azure virtual network peering](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-peering-overview)
    - establish communication between two Azure virtual networks


Routing talbe: 
- the routing table is the routing route information recorded in the router itself. it only contains a set of rules (routes) that specify how packets are routed in the virtual network
- It is the table to be referred to when performing the routing process but it does not identify the IP address of the VPN appliance.

[Azure Virtual Network settings](https://docs.microsoft.com/en-ca/learn/modules/azure-networking-fundamentals/azure-virtual-network-settings)

Azure Bation
- PaaS
- a service you deploy that lets you connect to a virtual machine using your browser and the Azure portal
- provides secure and seamless RDP/SSH connectivity to your virtual machines directly from the Azure portal over TLS.
- When you connect via Azure Bastion, your virtual machines do not need a public IP address, agent, or special client software
- provides secure RDP and SSH connectivity to all of the VMs in the virtual network in which it is provisioned. 
- Using Azure Bastion protects your virtual machines from exposing RDP/SSH ports to the outside world, while still providing secure access using RDP/SSH.

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

focus on two different layers of the Open Systems Interconnection (OSI) model (L2, L3)
- Layer 7: Application Layer. Human-computer Interation layer, where applications can access the network services
- Layer 5: Presentation Layer. Ensures that data is in a usable format and is where data encryption occurs
- Layer 6: Session Layer. Maintains connections and is reponsible for controlling ports and sessions
- Layer 4: Trasport Layer. Transmits data using transmission protocols, which acts as a **security layer**
    - Azure Firewall
- Layer 3: Network  Layer. Decides which physical path the data will take
    - Virtual network
    - Subnet
    - CDN (content delivery network)
- Layer 2: Data Link Layer. Defines the format of data on the network
- Layer 1: Physical Layer

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
- pricing depends on:
    - The amount of data stored per month.
    - The number and type of *operations* performed, and the cost of data *transfer*.
    - The selected data redundancy option.
- Each **object** that then be accessed via a **unique URL**
- a blob max 200TB, and no limit for number of blobs

### Azure Files
use for:
- Many on-premises applications use file shares.
- Store configuration files on a file share and access them from multiple VMs
- Write data to a file share, and process or analyze the data later.
- ACCESS:
    - can access the files from anywhere in the world, by using a URL (not unique, ust url of container) that points to the file.
    - can also use Shared Access Signature (SAS) tokens to allow access to a private asset for a specific amount of time.

### Access tiers
 - Hot access tier
 - Cool access tier
 - Archive access tier
    - **Rehydrate** data from the archive layer (Rehydrate archived blobs hot or cool by changing the tier using the Set Blob Tier operation)
    - Copy Blobs operation to make a new copy of the archived blobs. Specify a different blob name and hot or cool as the destination layer
 
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

### ARM templates
- describe the resources you want to use in a declarative JSON format
- he entire ARM template is verified before any code is executed to ensure that the resources will be created and connected correctly

**Infrastructure coding** is used to facilitate environmental automation

## best monitoring service for visibility, insight and outage mitigation
### Azure Advisor
available for **free** and provides:
- solutions to improve *cost-effectiveness, performance, high availability, reliability, and security*. designed to help you save time on cloud *optimization*
    - Operational Excellence:  achieve process and workflow efficiency, resource manageability, and deployment best practices.
    - Azure Advisor integrates with Azure Security Center to give security recommendations. (it's alone cannot achive this task)
    - actually give you a purchase recommendation on how you can reduce costs
- cannot file a cap relaxation request for resource limit
- access the Advisor using the Azure portal, the Azure command line interface (CLI), or the *Advisor API*. 
- configure alerts to automatically notify you of new recommendations
- doesn't provide a way to improve the security of your Azure Active Directory (Azure AD) environment. Azure Active Directory has a function called Identity Protection, which allows you to obtain analysis information on the security structure of your organization. It helps you identify potential attacks and understand the effectiveness of your policies.

### Azure Monitor
- a platform for collecting, analyzing, visualizing, and potentially taking action based on the metric and logging data from your entire *Azure* and *on-premises* environment.
- collects what is known as "application monitoring data" (data about the performance and functionality of the code you write, regardless of platform).
- collect monitoring data about applications, guest operating systems, Azure resources, Azure subscriptions, and Azure tenants and will not help with monitoring security threats. 
- **It does not have the ability to centrally manage events**

Scenarios:
- measure custom events alongside other usage metrics
- **set up alerts** for outages or when autoscaling is about to deploy new instances
    - can create alerts in Azure Monitor based on the virtual machine metrics

### Azure Monitor Metrics
- a feature of Azure Monitor that collects numeric data from monitored resources into a time series database
- Metrics are numerical values that are collected at regular intervals and describe some aspect of a system at a particular time

### Azure Service Health
provides a personalized view of the health of the Azure services, regions, and resources you rely on; displays both major and smaller, localized issues that affect you:
- **Service issues** are problems in Azure, such as outages, that affect you right now. You can drill down to the affected services, regions, updates from your engineering teams, and find ways to share and track the latest information.
- **Planned maintenance events** can affect your availability. You can drill down to the affected services, regions, and details to show how an event will affect you and what you need to do. Most of these events occur without any impact to you and aren't shown here. In the rare case that a reboot is required, Service Health allows you to choose when to perform the maintenance to minimize the downtime.
- **Health advisories** are issues that require you to act to avoid service interruption, including service retirements (deprecated) and breaking changes. Health advisories are announced far in advance to allow you to plan.
- scenario:
    - You can view the current status of the Azure services you rely on, upcoming planned outages, and services that will be sunset. 
    - You can set up alerts that help you stay on top of incidents and upcoming downtime without having to visit the dashboard regularly.
- access also via
    - Help + Support
    - Notification
- be comprised of:
    - Azure Service Health
    - Azure Status
    - Service health service
    - Resource Health 

### Azure Logs Analytics
- stored in the *container* 'Log analytics workspace'. (under Azure portal)
- a service that can collect and analyze *logs and metric data* of Azure services, can view all of the control plane activities. (direct the application and virtual machines logs to a central repository)
- possible to collect and analyze logs of Windows and Linux severs, of not only those on Azure but also on-premises and other cloud services.
- can acquire logs by installing an agent on the targeted server, set a threshold for the collected data, and have an alert issued. 
- it makes it easier to understand the log status by aggregating the collected data on the dashboard and graphing it.

### Azure Serivce Bus. 
fully managed enterprise integration message broker with message queues and publish / subscribe topics

# Part 4: Describe general security and network security features
## Protect agains security threats on Azure
### Azure Security Center
a monitoring service that provides visibility of your security posture across all of your services, both on *Azure* and *on-premises*

Security Center can:
- Monitor security settings across on-premises and cloud workloads.
- view the regulatory compliance of your Azure resources
- Automatically apply required security settings to new resources as they come online.
- Provide security recommendations that are based on your current configurations, resources, and networks.
- Continuously monitor your resources and perform automatic security assessments to identify potential vulnerabilities before those vulnerabilities can be exploited.
- Use machine learning to detect and block malware from being installed on your virtual machines (VMs) and other resources.
- You can also use **adaptive application controls** to define rules that list allowed applications to run.
- Detect and analyze potential inbound attacks and investigate threats and any post-breach activity that might have occurred.
- Provide *just-in-time* access control for network ports to reduces your attack surface by ensuring that the network only allows traffic that you require at the time that you need it to.

cannot:
- create network rules


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
- It also provides capabilities for threat detection and response. (security orchestration automated response)

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
- Manage SSL/TLS certificates. easily provision, manage, and deploy public and private Transport Layer Security/Secure Sockets Layer (TLS/SSL) certificates for use iwth Azure and your internal connected resources
- Store secrets backed by hardware security modules (HSMs)

### Azure Dedicated Host
A dedicated host is mapped to a physical server in an Azure datacenter. A host group is a collection of dedicated hosts. Benifits:
- Gives you visibility into, and control over, the server infrastructure that's running your Azure VMs.
- Helps address compliance requirements by deploying your workloads on an *isolated* server.
- Lets you choose the number of processors, server capabilities, VM series, and VM sizes within the same host.
- Be able to control the maintenance events initiated by the Azure platform

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
- cannot
    - encrypt all network traffic sent from Azure to the Internet

With Azure Firewall, you can configure:
- Application rules that define fully qualified domain names (FQDNs) that can be accessed from a subnet.
- Network rules that define source address, protocol, destination port, and destination address.
- Network Address Translation (NAT) rules that define destination IP addresses and ports to translate inbound requests.
    - transfer all RDP connections to only one virtual machine


Azure Firewall provides:
- Inbound protection for non-HTTP/S protocols (for example, RDP, SSH, and FTP).
- Outbound network-level protection for all ports and protocols.
- Application-level protection for outbound HTTP/S.

*Azure Application Gateway*: Accesses Azure Virtual Networks through high-performance VPN gateways.
- 99.95%
- also provides a firewall that's called the web application firewall (WAF). **WAF** provides centralized, inbound protection for your web applications against common exploits and vulnerabilities.
- used to **load balance** traffic to various web applications (web load balancer).
- It does not identify the IP address of the VPN appliance

Route filtering. a way to take advantage of a subset of the services supported through Microsoft peering

*Azure Front Door* and *Azure Content Delivery Network* also provide WAF services.

Azure Front Door:
- a global, scalable entry-point that uses the Microsoft global edge network to create fast, secure, and widely scalable web applications
- With Front Door, you can transform your global consumer and enterprise applications into robust, high-performing personalized modern applications with contents that reach a global audience through Azure

### DDoS protection
Always-on traffic monitoring and real-time mitigation of common network-level attacks provide the same defenses that Microsoft's online services use.The Azure global network is used to distribute and mitigate attack traffic across Azure regions.
- protection against DDoS attacks
- protects your website from a variety of **malicious** attacks 
- produces detailed **reports** on these attacks.
- *cannot* create Application and Network Rules that applies to the entire virtual network

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
- can be applied to the network interface attached to the virtual machines and to the subnet that holds the Azure virtual machines
- cannot:
    - cannot encrypt all network traffic sent from Azure to the Internet


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
- 99.99% for all pricing and tier
- With Azure AD, you control the identity accounts, but Microsoft ensures that the service is available globally
- When you connect Active Directory with Azure AD, Microsoft can help protect you by detecting suspicious sign-in attempts at no extra cost.
- Azure Active Directory manages how cloud or on-premises devices access your company's data. Register your device ID and provide a centralized place to manage it.
- feature:
    - Custome banned password list
    - Smart lockout
    - **Device Management**
    - Single sing-on
- can
    - create users and groups
    - have built-in capabilities for securing authentication and authorization to resources
- Cannot
    - cannot create Log Alert Rule
- [pricing and tier](https://azure.microsoft.com/en-us/pricing/details/active-directory)
    - Free, Office 365 Apps, premium 1, Premium 2

who uses Azure AD
- IT administrators
- App developers
- Users
- Online service subscriblers

tenant
- A tenant is a representation of an organization
- A tenant is typically separated from other tenants and has its own identity.
- Each Microsoft 365, Office 365, Azure, and Dynamics CRM Online tenant is automatically an Azure AD tenant.
- Azure Tenant is a dedicated and trusted instance of Azure Active Directory that's automatically created when your organization signs up for a Microsoft cloud service subscription.

Tenancy
- defines how instances are distributed across physical hardware

services Azure AD provide:
- Authentication
- Single Sing-on (SSO)
- retrieval of **security tokens**
- Application management. You can manage your cloud and on-premises apps by using Azure AD. Features like Application Proxy, SaaS apps, the My Apps portal (also called the access panel), and single sign-on provide a better user experience.
- **Device management**. Along with accounts for individual people, Azure AD supports the registration of devices. Registration enables devices to be managed through tools like **Microsoft Intune**. It also allows for **device-based Conditional Access** policies to restrict access attempts to only those coming from known devices, regardless of the requesting user account.

Group:
- Azure Active Directory (Azure AD) enables identity management and security with single sign-on and multi-factor authentication. However, it is not possible to divide users into groups and grant permissions.
- To divide users into groups and set permissions on a per-group basis, it is recommended that you take advantage of managed group or Azure role-based access management controls.

Azure AD B2C:
- 99.9%
- To authenticate user logins and manage profiles.

#### Azure Active Directory ID Protection
- allows you to apply MFA conditionally. 
- It is also used to detect risks such as *anonymous IP* address logins, unfamiliar sign-ins, and credential leaks.
- requires users who sign from the Internet with an *anonymous IP* address to change their password and "self-heal". 
- Identity Protection is a tool that allows organizations to perform three main tasks:
    - Automate identity-based risk detection and action.
    - Investigate risk using portal data.
    - Export risk detection data to third-party utilities for further analysis.



#### Azure AD Connect
- a way to connect your existing Active Directory installation with Azure AD
- synchronizes user identities **between** on-premises Active Directory and Azure AD.

- **Azure AD Connect Health**. used to monitor identity governance or identity infrastructure for on-premises resources or servers. You can use the Azure AD Connect Health portal to view alerts, performance monitoring, usage analysis, and other information.
- **Azure AD privileged ID management**. used to provide just-in-time access, prevent malicious activity, and provide a fully integrated review of "privileged roles" in real time. It also helps you manage privileged **administrator** roles across Azure resources and Azure AD
- Azure **Advanced Threat Protection** (ATP).
    - monitors user activity across the Azure network
    - detect suspicious user activity and malicious attacks within your organization
    - protect Azure Active Directory (AD) user identities. 
    - used to detect threats from on-premises resources. It is incorrect because the questions is not regarding internal sources.

##### Synchronization Service Manager
- used to configure the more advanced aspects of the synchronization engine and to verify the operational aspects of the service. 
- allows you to check the synchronization execution details and status.

#### Azure AD Fedearatioln Services

### Multifactor authentication
provides additional security for your identities by requiring two or more elements to fully authenticate.
- Something the user knows. This might be an email address and password.
- Something the user has. This might be a code that's sent to the user's mobile phone.
- Something the user is. This is typically some sort of biometric property, such as a fingerprint or face scan that's used on many mobile devices.

the services that provice Azure AD Multi-Factor Authentication:
- Azure Active Directory.
    - Azure Active Directory free edition enables Azure AD Multi-Factor Authentication for administrators with the global admin level of access, via the Microsoft Authenticator app, phone call, or SMS code. You can also enforce Azure AD Multi-Factor Authentication for all users via the Microsoft Authenticator app only, by enabling security defaults in your Azure AD tenant.
    - Azure Active Directory Premium (P1 or P2 licenses) allows for comprehensive and granular configuration of Azure AD Multi-Factor Authentication through Conditional Access policies (explained shortly).
    - Azure Active Directory Premium **P2** also includes advanced identity protection and Privileged Identity Management features.
- [Mutifactor authentication](https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-howitworks) for office 365
    - A subset of Azure AD Multi-Factor Authentication capabilities is part of your Office 365 subscription.
    - forms of verification                 (Self-service Password Reset)
        - password                          (MFA and SSPR)
        - SMS                               (MFA and SSPR)
        - Voice Call                        (MFA and SSPR)
        - Microsoft Authentication app      (MFA and public preview for SSPR)
        - App passwords                     (MFA only in certain cases)
        - Security Questions                (SSPR only)
        - Email address                     (SSPR only)
        - OATH Hardware token               (Public preview for MFA and SSPR)
    - enabled via '*Azure Privileged Identity Management*'
- hybrid identities - federation services
    - For hybrid identities, you can configure MFA when deployed while synchronized or federated with on-premises Active Directory Domain Services and Azure Active Directory.


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
- Administrators can lock subscriptions, resource groups, or resources
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

policy definitions examples:
- Allowed virtual machine SKUs
- Allowed locations
- MFA should be enabled on accounts with write permissions on your subscription
- CORS should not allow every resource to access your web applications (Cross-origin resource sharing)
- System updates should be installed on your machines

### Azure Blueprints
- *can*
    - define the set of standard Azure resources that your organization requires
    - deploy **resource groups** to newer subscriptions
    - deploy **Role assignments** to newer subscriptions
    - deploy **Policy assignments** to newer subscriptions
    - deploy **Azure Resource Manager** to newer subscriptions
- e.g.
    - define a blueprint that specifies that a certain resource lock must exist. Azure Blueprints can automatically replace the resource lock if that lock is removed.

Azure Blueprints orchestrates the deployment of various resource templates and other artifacts, such as:
- Role assignments (RBAC)
- Policy assignments
- Azure Resource Manager templates (ARM)
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
- Azure ExpressRoute circuits per subscription: 10
- max Azure storage spaces: almost unlimited

## Examine privacy, compliance, and data protection standards on Azure

Security & Compliance Center. provides operations related to security and regulatory compliance

Compliance Manager. 
- a workflow-based risk assessment tool listed on Microsoft's Microsoft Service Trust Portal
- allows you to track, assign, and validate regulatory compliance activities for organizations related to Microsoft cloud services. such as Microsoft Office 365, Microsoft Dynamics 365, and Microsoft Azure, as well as Microsoft Cloud Services.

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
- provides reference blueprints, or policy definitions, for common standards that you can apply to your Azure subscription. 
- provides you with detailed documentation about legal and regulatory standards and compliance on Azure, across:
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
a legal agreement between Microsoft and the customer that details the obligations by both parties with respect to the processing and security of customer data and personal data

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
It implements Microsoft's principles for maintaining data integrity in the cloud and Microsoft implements security, privacy, compliance, and transparency in all Microsoft cloud products and services. it is a web page that contains information and details about how Microsoft supports security, privacy, compliance, and transparency in all Microsoft cloud products and services, and is not relevant here.

The Trust Center is an important part of the Microsoft Trusted Cloud Initiative, providing support and resources to the legal and compliance community
- don't require Azure subscription
- In-depth information about security, privacy, compliance offerings, policies, features, and practices across Microsoft cloud products.
- Additional resources for each topic.
- Links to the security, privacy, and compliance blogs and upcoming events.
- is a great resource for people in your organization who might play a role in security, privacy, and compliance

#### Microsoft Service Trust Portal
- Documentation that can be used to show Microsoft's compliance efforts
- **Penetration test results**. you can see the results of penetration testing by an independent third party. 
- **Security Evaluation**. 
- review the available independent audit reports for Microsoft’s Cloud services
- [hierachy:](https://servicetrust.microsoft.com/)
    - Compliance Manager
    - Trust Documents
        - Audit Reports
        - Data Protection
        - Azure Stack
    - Industries & Regions
    - Trust Center
        - [Home](https://www.microsoft.com/en-ca/trust-center)
        - Privacy
            - Privacy Overview
            - Data Management
            - GDPR
            - Resources
        - Security
        - Compliance
            - ...
        - Resources

access [Trust Center](https://www.microsoft.com/en-ca/trust-center?rtc=1)

### Azure Security Center
- provides general security recommendations and suggests remediations to better secure the resources
- Azure Security Center offers free and paid services
    - The free tier only provides security policies, ongoing security assessments, and practical security features that help protect your Azure resources
    -  Paid services extend the free tier functionality and add:
        - **threat protection**. It uses built-in behavioral analytics and machine learning to identify attacks and zero-day exploits, and uses access and application control to reduce exposure to network attacks and malware.
        - **virtual machine vulnerability scan**.

#### Regulatory Compliance Dashboard
    - continuously monitors your Azure and hybrid environment against specific compliance requirements
    - also provide security assessments and recommendations as needed

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

MSDN Platforms
- a comprehensive, cost-effective set of resources for setting up development and test environments.
- This will be accessible as a benefit of a *pay-as-you-go subscription*

You can access the MSDN Support Forums by setting up a *pay-as-you-go* subscription.


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

charge begin:
- Public IP address
    - Static public IP addresses in the ARM deployment model and reserved IP addresses in the ASM deployment model begin billing the from the second hour after the IP address has been created, taking into account the time needed to properly allocate the IP address.  Billing for this ends when you delete the IP address resource.
    - For all other public IP addresses, billing begins when the associated resource is started and ends when the associated resource is deleted or stopped and then deallocated. Therefore, it is possible to stop billing by deleting unused public IP addresses.  
- exp
    - There is no charge for private IP, whether static or dynamic.
    - Azure Virtual Network is **free**. You can create up to **50** virtual networks in all regions with each subscription.  
    - the network interface is **free** to use.

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
    - budgets. (there is a **default spending limit** when ti comest to the spending limit)
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

service without SLA
- Free products typically don't have an SLA.
- Service Level Agreements are not in place for services that are in *public preview*.

**Enterprise Agreement (EA) subscriptions** are only available to some users

### deisgn your app to meet SLA
Combine SLAs: production of each SLA

strategies:
- Choose customization options that fit your required SLA
- Build availability requirements into your design
    - Deploying two or more instances of an Azure virtual machine across two or more availability zones raises the virtual machine SLA to 99.99 percent
- Include redundancy to increase availability

Availability metrics: Use these measures to plan for redundancy and determine customer SLAs.
- Mean time to recover (MTTR) is the average time it takes to restore a component after a failure.
- Mean time between failures (MTBF) is how long a component can reasonably expect to last between outages.


## preview services and preview features
to look into new capabilites
- The public preview service is available to all users
    - no SLA or guarantee
    - not recommended for production usage
- The private preview
    - this feature is always free.
    - the number of customers invited to private previews is limited, and these customers are expected to spend time with the product to provide feedback.
    - usually the first release of a product and are to help customers try out the service, provide feedback, verify if the service is actually needed, and shape the future of the product.
    - When the service becomes publicly available, it will be in full production mode. Fully supported by SLAs, customer support, and run on production workloads. 
    - Since the service is now running normally, you will be charged for it.

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

## Azure public review
- With public review of Azure, you can use the target service at a lower price than the general availability.
- There is a usage fee for public reviews of Azure. 
- open to all users. 
- available from the regular Azure portal. 

## Azure Support
### Professional Direct (ProDirect) Advisory
- Only Professional Direct (ProDirect) Advisory support provides architectural support for Azure environments. 
- This plan provides access to Azure support guidance based on publicly available best practice documentation for Microsoft Azure and information from the Azure forums.
- ProDirect advisors support users based on their access to Microsoft-related documentation, Microsoft Azure support engineers, and Microsoft Azure product groups.

Azure support request:
- Azure portal
- Azure support ticket REST API

[Support Plans:](https://azure.microsoft.com/en-us/support/plans/)
- Basic Plan
    - 99.9%
    - default one for all and free.
- Developer Support Plan
    - only email is available during business hours
    - includes "Billing and Subscription Management Support", "24/7 self-help resources, Microsoft Learn, Azure portal instructions on how to use videos, documentation, community support", and "Ability to send as many support tickets as you need" 
- Standard Plan
    - 24/7 access to technical support by email and phone
    - **Save** on montly cost
- Professional Direct Plan.($1000/month, all supported). response within 1 hour

Billing accounts supported by the Azure portal
- The Azure portal supports the Microsoft Online Services Program. This creates a separate billing account for the Microsoft Online Services Program when you sign up for Azure from the Azure website. For example, you can sign up for an Azure free account, a pay-as-you-go account, or sign up as a Visual Studio subscriber.
- Microsoft Customer Agreement is supported. When your organization works with a Microsoft representative to enter into a Microsoft Customer Agreement, a Microsoft Customer Agreement billing account is created. In some regions, a Microsoft Customer Agreement billing account may also be created if you sign up for a pay-as-you-go account from the Azure website, or if you upgrade your Azure free account. 
- Microsoft enterprise contracts are supported. When your organization enters into an Enterprise Agreement (EA) to use Azure, an Enterprise Agreement billing account is created.
- Microsoft Partner Agreement is supported. Microsoft Partner Agreement billing accounts are created by cloud solution provider (CSP) partners to manage their customers with a new commerce experience.
