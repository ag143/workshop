The support plan must allow for new support requests to be opened.
- All but 'Basic'

You have the following data storage requirements:
✑ Data must be stored on multiple nodes.
✑ Data must be stored on nodes in separate geographic locations.
✑ Data **can be read** from the secondary location as well as from the primary location
Which of the following Azure stored redundancy options should you recommend?
- Read-only geo-redundant storage
- ~~geo-redundant~~


to request an assessment of an Azure environment design from Microsoft: You recommend that the company subscribes to the Professional Direct support plan.
- No. 
- Review is only under Premier.Premier is stil available but only for companies with enterprise agreement.
- Professional DIrect offers only :Guidance from a pool of ProDirect delivery managers". Guidance is not a design review.


have created 10 web applications that must be host on Azure.
You need to determine which Azure web tier plan to host the web apps. The web tier plan must meet the following requirements:
✑ The web apps will use custom domains.
✑ The web apps each require 10 GB of storage.
✑ The web apps must each run in dedicated compute instances.
✑ Load balancing between instances must be included.
✑ Costs must be minimized.
Which web tier plan should you use?
- Basic (10GB http://azure.microsoft.com/en-us/pricing/details/websites/)
- ~~Standard (50GB)~~
- ~~Shared~~
- ~~Free~~


Your company is planning to migrate all their virtual machines to an Azure pay-as-you-go subscription. The virtual machines are currently hosted on the Hyper-V hosts in a data center.
You are required make sure that the intended Azure solution uses the correct expenditure model.
Solution: You should recommend the use of the elastic expenditure model.
Does the solution meet the goal?
- No. (there is no such expenditure model)
-OpEx should be used


You are required to deploy an Artificial Intelligence (AI) solution in Azure.
You want to make sure that you are able to build, test, and deploy predictive analytics for the solution.
- Azure Machine Learning Studio


The remote workers require access to the VMs on VNet1.
- Configure a Point-toSite (P2S) VPN. (A Point-to-Site (P2S) VPN gateway connection lets you create a secure connection to your virtual network from an individual client computer.)


You have been informed that all network resources will be migrated to Azure. Thereafter, the on-premises data center will be retired. You are required to employ a strategy that reduces the effect on users, once the planned migration has been completed.
- ~~Azure MFA~~
- Active Sync should be used?


A platform as a service (PaaS) solution that hosts web  apps in Azure provides professional **development services** to continuously add features to custome applications
- Yes. (PaaS provides a framework that developers can build upon to develop or customize cloud-based applications. PaaS development tools can cut the time it takes to code new apps with pre-coded application components built into the platform, such as workflow, directory services, security features, search and so on.)


Azure Storage accounts
- IaaS


Q49: advantage of using a public cloud service for the servers over an on-premises network?
- The public cloud is a shared entity whereby multiple corporations each use a portion of the resources in the cloud 
- ~~The public cloud is a crowd-sourcing solution that provides corporations with the ability to enhance the cloud~~ (not crowd-sourcing, only owned by MS)


Q31: A platform as a Service (PaaS) solution provides additional memory to apps by changing pricing tiers
- Yes


Q62: To build a hybrid cloud, you must **deploy** resources to the public cloud
- Yes. (Deloy not adding hardwares)


Q66: web applicate requiring several prerequisite
- IaaS needed


What is the first stage in the Microsoft Cloud Adoption Framework for Azure?
- **Define** your strategy


When you need to **delegate permissions to several Azure virtual machines simultaneously, you must deploy the Azure virtual machines
- to the same resource group


You plan to store 20 TB of data in Azure. The data will be accessed infrequently and visualized by using Microsoft Power BI. Tow solution:
- Azure Data Lake
- **Azure SQL Data Warehouse**

Resource groups provide organizations with the ability to manage the compliance of Azure resources across multiple subscriptions?
- No.(Azure policies)
- ~~Management Group~~

a solution that enables the client computers on your on-premises network to communicate to the Azure virtual machines.
- To implement a solution that enables the client computers on your on-premises network to communicate to the Azure virtual machines, you need to configure a VPN (Virtual Private Network) to connect the on-premises network to the Azure virtual network.**The Azure VPN device is known as a Virtual Network Gateway**. The virtual network gateway needs to be located in a dedicated subnet in the Azure virtual network. T**his dedicated subnet is known as a gateway subnet** and must be named 'GateWaySubnet'


Each Azure subscription can contain multiple account **administrators**?
- No.
- You can assign service administrators and co-administrators in the Azure Portal but there can only be one account administrator.


which storage service must be used to store the unmanaged data disks of the virtual machine.?
- Azure **containers** are the backbone of the virtual disks platform for Azure IaaS. Both Azure OS and data disks are implemented as virtual disks where data is durably persisted in the Azure Storage platform and then delivered to the virtual machines for maximum performance. Azure Disks are persisted in Hyper-V VHD format and stored as a page blob in Azure Storage.


Data that is stored in an Azure Storage account automatically has at least three copies
- Yes

All data that is copied to an Azure Storage account is backed up automatically to another Azure data center
- **NO**. (depending on the replication option, Local/Geo-Redundant Storage (LRS/GRS))

A Win Virtual Desktop host pool that includes 20 session hosts supports a maximum of 20 simultaneous user connections
- No. (a session of host can have multiple user session)

Window Virtual Desktop supports desktop and app virtualization
- Yes


To use Azure Active Directory (Azure AD) credentials to sing in to a computer that runs Windows 10, the computer must be joined to Azure AD
- Yes

Azure Active Directory groups support dynamic membership rules.
- Yes

Which Azure service should you use from the Azure portal to view service failure notifications that can affect the availability of VM1?
- Azure virtual machines -> Maintenance Status


Run the powershell script from a computer that runs Linux and has the Azure CLI tools installed.Does this meet the goal?
- No. PowerShell can now be installed on Linux. However, the question states that the computer has Azure CLI tools, not PowerShell installed. Therefore, this solution does not meet the goal.

From azure service health, an administrator can view the health of all the services in an Azure environment
- Yes


Your company plans to deploy several million sensors that will upload data to Azure. two Azure resources
- **Azure Data Lake**
- Azure IoT Hub

Your company plans to deploy an Artificial Intelligence (AI) solution in Azure.
- Azure Machine Learning Designer (Studio?)

You need to create VM1 in Subscription1 by using the command.
Solution: From a computer that runs Windows 10, install Azure CLI. From PowerShell, sign in to Azure and then run the command.
- Yes. The command can be run from PowerShell or the command prompt if you have the Azure CLI


powershell core + az powershell module can work


You can use Azure Cost Management to view costs associated to management groups.
- No. (only Subscription and below)

Q169:
✑ Secures websites from attacks
✑ Generates reports that contain details of attempted attacks
What should you include in the solution?
- DDoS protection.
- DDoS basic is free, but Standard supports logging, alerting, and telemetry.
- ~~Azure Firewall (not to generate report)~~


Q170: Monitor threats by using sensors:
- Azure Advanced Threat Protection (**ADP**)


Q172: Enable just in time VM access by
- Azure security center


Q173: You can associate a network security goup to:
- virtual network subnet
- virtual network interface
- ~~virtual network~~


to store secrets for Azure Active Directory (Azure AD) user accounts
- **server applications**
- ~~Azure Key Vault~~. (Key Vault is designed to store configuration secrets for server apps. It's not intended for storing data belonging to your app's users, and it shouldn't be used in the client-side part of an app.)

Q179:A resource group can have **only one Owner** role



collect and automatically analyze security events from Azure Active Directory
- Azure Sentinel


Which service provides network traffic filtering across multiple Azure subscriptions and virtual networks?
- Azure firewall. (**filtering**, and overall VNet)


Q190: Azure Sentinel can
- stores collected events in an Azure Storage Account
- can **remediate** incidents automatically
- can collect Window Defender Firewall logs from Azure virtual machines


Q192: Azure VM that run Win Server 2016 can encrypt network traffic sent to the Internet:
- No.(The question is rather vague as it would depend on the configuration of the host on the Internet. Windows Server does come with a VPN client and it also supports other encryption methods such IPSec encryption or SSL/TLS so it could encrypt the traffic if the Internet host was configured to require or accept the encryption. However, the VM could not encrypt the traffic to an Internet host that is not configured to require the encryption.)


Q193: Only two 'Azure Security Center' features: Continuous assessment and security recommendations, and Azure secure score, are free.

From Azure Security Center, you can download a Regulatory Compliance report.
- Yes.


Q194: Defence in depth layers (from bottom to top). (https://github.com/undergroundwires/Azure-in-bullet-points/blob/master/AZ-900%20Microsoft%20Azure%20Fundamentals/4.2.%20Defence%20in%20Depth.md)


Q195: You plan to encrypt VM1 by using Azure Disk Encryption. Which Azure resource must you create first?
- an Azure Key Vault (Azure Disk Encryption requires an Azure Key Vault to control and manage disk encryption keys and secrets.) 

Q196: **Which resources can be used as a source for a Network security group inbound security rule?** **
- IP Addresses, Service tags and Application security groups
- (Source or destination: Any, or an individual IP address, classless inter-domain routing (CIDR) block (10.0.0.0/24, for example), service tag, or application security group.)

Q198: azure Sentinel uses **playbooks** to automatically respond to threats


Q198: **Network Address Translation (NAT) rules** in Azure Firewall enables users on the internet to access a server on a virtual network


Q199: DDoS is implemented at the *network layer*


Q202: from **Compliance Manager**, you can track your company's regulatory standards and regulations


Q203: You **cannot join** Android devices to Azure AD.
- (Azure AD **join** only applies to Win 10 devices)

Q207: **Azure policies** provide organizations with the ability to manage the compliance of Azure resources across multiple subscriptions
- ~~Management groups~~


Q209:
- you **can** add **ARM** template to an Azure blueprint
- you **cannot** assign an Azure blueprint to a resource group
    - Management group or Subscription levels
    - Create a new resource group for use by other artifacts WITHIN the blueprint. When creating a blueprint definition, you'll define where the blueprint is saved. Blueprints can be saved to a management group or subscription that you have Contributor access to. If the location is a management group, the blueprint is available to assign to any child subscription of that management group. Each Published Version of a blueprint can be assigned (with a max name length of 90 characters) to an existing management group or subscription. 
- you **can** use Azure Blueprints to grant **permission** to a resource


Q211:
- Az resource **can** have **mutliple** Delete locks. (different people apply and revoke for different reason)
- locks is inherited
- if exists a Read-only lock, you **can** andd a delete lock

Q215: Azure Germany can be used by legal residents of Germany only.
- false. ( applied to any user or enterprise that requires its data to reside in Germany )


Q222: ways to implement Azure MFA:
- Az AD alone
- Sync with AD on premise
- Federation with ad


Q225: To what should an application connect to retrieve security tokens?
- Azure Key Vault

Q227: you **can** confugre the Az AD activity logs to appear in Azure Monitor

Q235: **IOS devices** can be registered in Azre AD
- Windows 10, iOS, Android, and macOS (**registrater**)


Q238: Azure free account includes a specified quantity of free services for 12 months and a set of services that are always free

Q239:
- Services in private preview can be viewed in the regular Azure portal. However, you need to be signed up for the feature in private preview before you can view it.
- (Only the preview that impact the UI are accessed from a different portal (not the services))

Q241: Users with any type of Azure subscription (pay-as-you-go, Enterprise Agreement, Microsoft Customer Agreement etc.) can get support from the MSDN forums


Q244: 
- You need to be an administrator of the billing account that has the subscription to be able to transfer the subscription. This could be a Billing Administrator or Global Administrator. A subscription owner can manage all resources and permissions within the subscription but cannot transfer ownership of the subscription.
- can not change the spending limit (You can remove the spending limit, but you canג€™t increase or decrease it. The spending limit in Azure prevents spending over your credit amount. All new customers who sign up for an Azure free account or subscription types that include credits over multiple months have the spending limit turned on by default. The spending limit is equal to the amount of credit and it canג€™t be changed. For example, if you signed up for Azure free account, your spending limit is $200 and you can't change it to $500. However, you can remove the spending limit. So, you either have no limit, or you have a limit equal to the amount of credit.)


Q245: you are not charged for unused network interfaces.

Q248: "Maximum Available Minutes" is the total accumulated minutes during a billing month.


Q250: A basic support plan provides:
- 24x7 access to billing and subscription support, online self-help, documentation, whitepapers, and support forums
- Best practices: Access to full set of Azure Advisor recommendations
- Health Status and Notifications: Access to personalized Service Health Dashboard & Health API


Q258: Access to Support Engineers via email or phone is available in the following support plans: Premier, Professional Direct and **standard**.


Q261: request an architectural **review** of an Azure environment from Microsoft.
- premier


Q263: Azure customers with an Azure Enterprise Agreement (EA), Microsoft Customer Agreement (MCA), or Microsoft Partner agreement (MPA) can use Azure Cost Management


Q268: Azure free account limit:
- 200usd or 150GBP, spending limit
- 5GB blob storage, 5GB file storage
- 10 web, mobile or API apps