# Az900-Module-4-Review

## Azure Security features

### Microsoft Defender for Cloud
- A monitoring service app that provides protection across Azure & on-premise datacenters
- Provides security recommendations
- Detect & block malware
- Analyze & identify potential attacks
- Just-in-time access control for ports
- Monthly payment plan required

### Defender for Cloud Components
- **Secure Score**:
  - Aggregate all security findings into one score
  - Microsoft cloud security benchmark (MCSB) standard is applied by default
- **Multi-cloud coverage**:
  - Most feature including security score supports Azure, AWS, GCP (Google Cloud)
- **Advanced Cloud Security Posture Management**:
  - Identify weaknesses in security posture
  - *Security Governance* to drive actions to improve security
  - *Regulatory Compliance* to standarize environment and configuration
  - *Cloud security explorer* to build a comprehensive view of environment
- **Data-aware Security Posture**:
  - Auto-discovers datastores that has sensitive data
  - Helps reduce risk of data breaches
- **Attack path analysis**:
  - Model traffic on your network to identify potential risks before user make changes
- **Microsoft Entra Permissions Management**:
  - Provide comprehensive visibility and control over permissions for any identity

### Using Defender for Cloud
- **Policy Compliance**: Run policies across management groups, subscriptions, or tenants
- **Continuous Assessments**: Assess new and deployed resources to ensure that they are configure properly
- **Tailored Recommendations**: Recommendations based on existing workload with instructions on how to implement them
- **Threat Protection**: Analyze attempted threats through alerts & impacted resource reports

*Lab - Monitor and Resolve Security Issues by Using Security Center*

### Resource hygiene

-----

### Key Vault
- Stores application secrets in a centralized cloud location
- Controls access permissions & access logging
  - Secrets management
  - Key management
  - Certificate management
  - Storing secrets backed by hardware security modules (HSMs)

*Lab - Manage Encryption by Using an Azure Key Vault*

### Microsoft Sentinel
- A security information & event management (SIEM) solution
- Provides security analytics, threat intelligence across an enterprise
- *Integrations:*
  - Microsoft 365 Defender
  - Azure Active Directory
  - Azure Advanced Threat Protection
  - Microsoft Cloud App Security

### Azure Dedicated Hosts
- Provide physical servers that host Azure VMs that is for a singal workload
- Provides hardware isolation at server level
- Controls over maintenance event timing
- Aligned with Azure Hybrid Use Benefits

-----

<br>

## Azure network security
- A layered multi-level protection approach similar to OSI levels
- Attacks against one layer are isolated from subsequent layers

### Shared Security
- Migrating from customer to cloud datacenters shifts the responsibility for security
- Security becomes a shared concern as the on-premise data
- **Service model dependent:**

| Responsibility                        | On-Premises | IaaS model  | PaaS model  | SaaS model  |
|---------------------------------------|-------------|-------------|-------------|-------------|
| `Data, governance & Rights Mgmt.    ` | Customer    | Customer    | Customer    | Customer    |
| `Client endpoints                   ` | Customer    | Customer    | Customer    | Customer    |
| `Account & access management        ` | Customer    | Customer    | Customer    | Customer    |
| `Identity & directory infrastructure` | Customer    | Customer    | *Ms*/Cs     | *Ms*/Cs     |
| `Application                        ` | Customer    | Customer    | *Ms*/Cs     | *Microsoft* |
| `Network Controls                   ` | Customer    | Customer    | *Ms*/Cs     | *Microsoft* |
| `Operating System                   ` | Customer    | Customer    | *Microsoft* | *Microsoft* |
| `Physical Hosts                     ` | Customer    | *Microsoft* | *Microsoft* | *Microsoft* |
| `Physical Network                   ` | Customer    | *Microsoft* | *Microsoft* | *Microsoft* |
| `Physical Datacenter                ` | Customer    | *Microsoft* | *Microsoft* | *Microsoft* |

-----

### Network Security Groups (NSGs):
- Azure applies default/baseline security rules to new NSGs, Override default rules with new, higher priority rules.
- filter network traffic to and from Azure resources on Azure Virtual Networks
- Set in-outbound rules by destination IP, ports, and protocols
- Add multiple rules, as needed, within subscription limits

*Lab - Implement a Network Security Group*

### Azure Firewall
- A stateful, managed Firewall as a Service (FaaS)
- Grants/denies server access based on originating IP
- Applies in-outbound traffic filtering rules
- Built-in high availability
- Unrestricted cloud scalability
- Uses Azure Monitor logging

### Azure Application Gateway
- Provides a Web Application Firewall (WAF)
- WAF provides centralized, inbound protection for web apps

### DDoS protection
- Sanitizes unwanted network traffic before it impacts service availability
- Basic service tier is automatically enabled in Azure
- Standard service tier adds mitigation capabilities
  - tuned to protect Azure Virtual Network resources

-----

### Defense in depth
- NSGs + Azure Firewall
- **Perimeter layer:**
  - By Azure DDoS Protection + Azure Firewall
  - Protects network boundaries
- **Networking layer:**
  - By Network Security Group (NSG)'s in-outbound rules
  - Permits traffic to pass between networked resources

-----

<br>

## Quiz

### Azure Logic Apps / Functions

#### Within Microsoft Sentinel, which Azure product is used to run automated playbooks in response to alerts? 
- Azure Logic Apps

#### ________ is a serverless, no-code solution for automating workflows. It integrates with hundreds of other services, making it a powerful solution for SOAR.
- Azure Logic Apps

#### You want to orchestrate a workflow by using APIs from several well-known services. Which is the best option for this scenario?
- Azure Logic Apps

#### Your team has limited experience with writing custom code, but it sees tremendous value in automating several important business processes. Which of the following options is your team's best option?
- Azure Logic Apps

#### What is the difference between Azure Functions and Azure Logic Apps?
- You can call Azure Functions from Azure Logic Apps, and vice versa
- They differ at intent:
  - Azure Functions is a serverless compute service
  - Azure Logic Apps is intended to be a serverless orchestration service

#### You need to process messages from a queue, parse them by using some existing imperative logic written in Java, and then send them to a third-party API. Which serverless option should you choose?
- Azure Functions

-----

### Microsoft Sentinel

#### What does Microsoft Sentinel provide?
- An end-to-end solution for security operations

#### Which language is used to query data within Microsoft Sentinel?
- KQL

#### What is SIEM?
- Security Information and Event Management

#### What is Microsoft Sentinel?
- cloud-native SIEM system

#### What is the first step of data ingestion for Microsoft Sentinel?
- Data connectors

#### If you want to collect event data from various sources, and perform security operations on that data to identify suspicious activity, you should use ________________
- Microsoft Sentinel

####  The single most important option when creating a new Log Analytics Workspace is
- the region

#### To enable Microsoft Sentinel, you need ________ permissions to the subscription in which the Microsoft Sentinel workspace resides
- Contributor

#### To use Microsoft Sentinel, you need either ________ permissions on the resource group that the workspace belongs
- contributor or reader

#### After data is ingested into Microsoft Sentinel, where is it stored?
- Log Analytics

#### What language does Log Analytics use?
- Kusto Query Language (KQL)

#### What is used to create dashboards and visualization in Microsoft Sentinel?
- Workbooks

#### Which Azure service stores the log data that is ingested into Microsoft Sentinel?
- Log Analytics

#### Where is your log data stored?
- Log Analytics workspace

#### What’s the easiest way for Tailwind Traders to combine security data from all of its monitoring tools into a single report that it can take action on?
- Collect security data in Azure Sentinel

-----

### Perimeter Layer Security

#### An ASG enables you to group servers with similar ________ requirement, and group together servers with similar ________.
- port filtering, functions

#### The ________ layer is about protecting organizations from network-based attacks against your resources.
- Network Perimeter

#### Which layer of Defense-in-depth is focused on preventing network-based attacks? 
- Perimeter layer (Perimeter Security)

#### What are network security groups?
- Enables you to filter network traffic to and from Azure resources within an Azure virtual network

#### Rules are processed by in what order?
- By order of priority number (100 - 4096, Lower to high numbers)

#### When you create a network security group what does Azure create to provide a baseline level of security?
- A series of default rules

#### How can Tailwind Traders most easily implement a deny by default policy so that VMs can't connect to each other? 
- Create a network security group rule that prevents access from another VM on the same network

#### Can you remove default rules Azure sets for Network Security groups?
- No, but you can override them by creating new rules with high priorities

#### ________ allow you to filter network traffic to and from Azure resources in an Azure virtual network. IT can contain multiple inbound and outbound security rules that enable you to filter traffic to and from resources by source destination IP address, port, and protocol.
- Network security groups

#### What's the best way for Tailwind Traders to limit all outbound traffic from VMs to known hosts?
- Create application rules in Azure Firewall

#### Use perimeter ________ with ________ to identify and alert on malicious attacks against your network.
- firewalls, Azure firewall

#### Azure Application Gateway also provides a firewall called:
- Web application firewall

#### You typically deploy Azure Firewall on a central virtual network to control:
- General Network Access

#### Azure Firewall Privides many features, including:
- Built-in *High-Aavailability*
- Unrestricted cloud *scalability*
- Inbound and outbound *filtering* rules
- Azure Monitoring *logging*

#### Azure Firewall is fully integrated with  ________ for logging and analytics.
- Azure Monitor

#### ________ is a managed, cloud-based, network security service that protects your Azure Virtual Network resources. It is a fully stateful firewall as a service with built-in high availability & unrestricted cloud scalability.
- Azure Firewall

#### A ________ is a service that grants server access based on the originating IP address of each request.
- Firewall

#### What type of data is actively moving from one location to another, such as across the internet or through a private network?
- In transit

#### How can Tailwind Traders ensure that certain VM workloads are physically isolated from workloads being run by other Azure customers?
- Run the VMs on Azure Dedicated Host

#### How can Tailwind Traders allow some users to control the virtual machines in each environment but prevent them from modifying networking and other resources in the same resource group or Azure subscription?
- Create a role assignment through Azure role-based access control (Azure RBAC)

-----

### Access Management Layer Security

#### ________ & ________ controls access to infrastructure and change control.
- Identity, Access

#### How can the IT department ensure that employees at the company's retail stores can access company applications only from approved tablet devices?
- Conditional Access

#### How can the IT department use biometric properties, such as facial recognition, to enable delivery drivers to prove their identities?
- Multifactor authentication

#### How can the IT department reduce the number of times users must authenticate to access multiple applications?
- SSO

-----

### Data & other Layers' security

#### Defense in depth can be visualized as:
- A set of layers with the data to be secured in the center

#### ________ is the first line of defense to protect computing hardware in the data center.
- Physical layer security

#### ________ ensures applications are secure and free from vulnerabilities.
- Application layer

#### ________ layer secures access to virtual machines.
- Computer

#### ________ layer limits communication between resources through segmentation and access control.
- Networking

#### ________ layer uses distributed denial-of-service (DDoS) protection to filter large-scale attacks before they can cause a denial of service for end users.
- Perimeter

#### What is SOAR?
- Security, Orchestration, Automation, Response

####  Which is the best way for Tailwind Traders to safely store its certificates so that they're accessible to cloud VMs?
- Store the certificates in Azure Key Vault

#### What strategy employs a series of mechanisms to slow the advance of an attack aimed at acquiring unauthorized access to data?
- Defense-in-depth (combining measures)

#### ________ is a monitoring service that provides threat protection across both Azure and on-premises datacenters 
- Microsoft Defender for Cloud

#### How can Tailwind Traders enforce having only certain applications run on its VMs?
- Create an application control rule in Azure Security Center

#### Features of Application security groups allow you to reuse your security policy at scale with out manual maintenance of what?
- explicit IP addresses

#### Use Azure ________ to filter large-scale attacks before they can cause a denial of service for end users.
- DDos protection

#### ________ target web application packets to disrupt the transmission of data between hosts.
- Resource layer attacks

####  ________ render a target inaccessible, by exploiting a weakness in the layer 3 and layer 4 protocol stack.
- Protocol Attacks

#### ________ goal is to flood the network layer with substantial amount of seemingly legitimate traffic.
- Volumetric Attacks

#### DDos standard protection can mitigate what three types of attacks?
- Volumetric Attacks, Protocol Attacks, and Resource (application) Layer Attacks

#### ________ enable you to configure network security as a natural extension of an application's structure, allowing you to group virtual machines and define network security policies based on those groups.
- Application Security groups

#### An attacker can bring down your website by sending a large volume of network traffic to your servers. Which Azure service can help Tailwind Traders protect its App Service instance from this kind of attack?
- Azure DDoS Protection

#### The ________ service tier of Azure DDos Protection provides additional mitigation capabilities that are tuned specifically to Microsoft Azure Virtual Network resources. Protection policies are tuned through dedicated traffic monitoring and machine learning algorithms.
- standard

#### The ____ service tier of Azure DDos Protection is automatically enabled as part of the Azure platform. Always-on traffic monitoring and real-time mitigation of common network-level attacks provide the same defenses that Microsoft's online services use.
- basic

#### What are the service tiers of Azure DDos Protection?
- standard, basic

#### How does Azure DDos protection service protect your Azure applications?
- By scrubbing traffic at the Azure network edge

#### DDos attacks can be targeted at any _____ that is publicly reachable through the internet. Thus any resourced exposed to the internet, such as a website, is potentially at risk from a DDos attack.
- endpoint

#### ______ attacks attempt to overwhelm and exhaust an application's resources, making the application slow or unresponsive to legitimate users.
- DDoS

-----

### Others

#### Which of the following is true for AzureHDInsight?
- Open-source analytics service to analyze streaming or historical data

#### Which of the following is true for Resource locking?
- Prevents resources from being accidentally deleted or changed

#### Which of the following is true for Azure Policy?
- A service in Azure that enables you to create, assign, and manage policies that control or audit your resources
