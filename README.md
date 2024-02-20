# Az900-Module-5-Review

## Identity

### Authentication vs Authorization
- Authentication verifies identity and credentials
- Authorization verifies level of access

### Multi-Factor Authentication (MFA)
- Username (identity)
- Password (credentials)
- Keys (certificate or personal questions)

### Azure Entra (Azure Active Directory / AAD)
- A cloud-based identity and access management service
- *Authentication*: Employees' sign-in
- *Single sign-on (SSO)*
- *Application management*
- *Business to Business (B2B)*
- *Business to Customer (B2C) identity services*
- *Device Management*

### Conditional Access
- If a user wants to access a resource, then they must complete an action by detection:
  - User or Group Membership
  - IP Location
  - Device Type
  - Application
  - Real-time risk detection
- i.e.: A user wants to access an app like Microsoft 365 --> must perform MFA

-----

### Azure Governance Methodologies

### Role-Based Access Control (RBAC)
- A fine-grained access management that inherits Active Directory
- Segragate duties by:
  - User-groups
  - Apps
  - Individual-user
  - Resource-group
  - Individual-resources

### Resource locks
- A locking feature that prevents accidental deletion
- Manage locks at subscription, resource group, or individual resource levels

| Lock Types   | Read | Update | Delete |
|--------------|------|--------|--------|
| CanNotDelete | Yes  | Yes    | No     |
| ReadOnly     | Yes  | No     | No     |

### Tags
- Metadata for Azure resources
- Organizes resources into a taxonomy
- Consists of a name-value pair
- Very useful for rolling up billing info

### Azure Policy
- Enforce org. standards by assessing compliance at-scale
- Provides governance & resource consistency with:
  - Regulatory compliance
  - Security
  - Cost
  - Management
- Provides built-in policy & initiative definitions, under:
  - Storage
  - Networking
  - Compute
  - Security Center
  - Monitoring

### Azure Blueprints
- To rapidly build and stand up new environments
- (?) Similar to Ansible
- Build trust through org. compliance with a set of components:
  - Role Assignments
  - Policy Assignments
  - Azure Resource Manager Templates
  - Resource Groups

### Cloud Adoption Framework for Azure
- The Best practices / One Microsoft approach to cloud adoption
- Tools, guidance and narratives for strategies and outcomes
- **Strategy**
  - Motivations
  - Business outcomes
  - Financial considerations
- **Plan**
  - Rationalize your digital estate
  - Organizational alignment
  - Skills readiness plan
  - DevOps cloud adoption plan
- **Ready**
  - Operating model alignment
  - Azure landing zone conceptual architecture
  - Azure landing zone design areas
  - Implementation options
- **Migrate**
  - Migration scenarios
  - Cloud migration best practices
  - Process improvements
- **Innovate**
  - Business value consensus
  - Build your first MVP
  - Measure for customer impact
  - Expand digital inventions
- **Secure**
  - Risk insights
  - Business resilience
  - Asset protection
- **Manage**
  - Business commitments
  - Management baseline
  - Expand the baseline
  - Advance operations and design principles
- **Govern**
  - Benchmark assessment
  - Governance foundation
  - Improve the foundation

-----

<br>

## Privacy, compliance, data protection standards

### Security
- Azure has built in intelligent security that helps to protect against cyberthreats, using automation & AI.

### Privacy
- Azure committs to ensure the privacy of org. through:
  - Contractual agreements
  - Providing user control & transparency

### Compliance
- Azure respects local laws & regulations
- Azure provides comprehensive coverage of compliance offerings

### Compliance Terms and Requirements
- Criminal Justice Information Services (CJIS)
- Health Insurance Portability & Accountability Act (HIPAA)
- CSA STAR Certification
- ISO/IEC 27018
- EU Model Clauses
- National Institute of Standards and Technology (NIST)

### Microsoft privacy statement
- Provides openness & honesty about how Microsoft handles user data, explains:
  - What data Microsoft processes
  - How Microsoft processes it
  - Purposes/uses of the data

### Online Services Terms
- The licensing terms define the terms & conditions for your purchase:
  - Products
  - Online Services

### Data Protection Addendum (DPA)
- Sets forth the obligations with respect to the processing & security of:
  - Customer and Personal Data

### Trust Center
- Place to learn in-depth, expert information for Microsoft products:
  - Security
  - Privacy
  - Compliance
  - Policies
  - Features
  - Practices
- Role-specific information for:
  - Musiness managers
  - Administrators
  - Engineers
  - Risk assessors
  - Privacy officers
  - Legal teams

### Azure Compliance Documentation
- A comprehensive set of compliance offerings to help orgs to comply with:
  - National requirements
  - Regional requirements
  - Industry-specific requirements

### Sovereign Regions - US Government services
- Meets the security & compliance needs of:
  - US federal agencies
  - US state and local governments
  - US solution providers
- Azure Governmnet:
  - Separate instance of Azure
  - Physically isolated from non-US government deployments
  - Accessible only to screened, authorized personnel

### Sovereign Regions - Azure China
- Physically separated instance of Azure cloud services
- Operated by 21Vianet
- All data stays within China to ensure compliance

-----

<br>

## Quiz

### Security

#### Which Azure Active Directory tool can vary the credentials needed to log in based on signals, such as where the user is located? 
- Conditional Access

#### Which Azure Active Directory (Azure AD) feature is used to provide access to resources based on organizational policies?
- Conditional Access

#### ________ collects signals from the user, makes decisions based on those signals, and then enforces that decision by allowing or denying the access request or challenging for a multifactor authentication response.
- Conditional Access

#### True or False:
- **Azure RBAC policies override restrictions defined by resource locks:**
  - False, resource lock cannot be overriden
- **If you place a resource lock on a resource group, all of the resources within the resource group will also have the resource lock applied**
  - True
- **Resource locks can be applied to individual resources, resource groups, or even an entire subscription.**
  - True
- **There are two types of resource locks, one that prevents users from deleting and one that prevents users from changing or deleting a resource.**
  - True

#### Which security model assumes the worst-case security scenario, and protects resources accordingly?
- Zero trust

#### Match description to Zero Trust model's guiding principles:
- **Always authenticate and authorize based on all available data points**
  - Verify explicitly
- **Limit user access with Just-in-time and Just-enough-access, risk-based adaptive policies, and data protection**
  - Use least privilege access
- **Segment access, verify end-to-end encryption, use analytics to get visibility, drive threat detection and improve defenses**
  - Assume Breach

-----

### Compliance

#### Where can you access details about the personal data Microsoft processes and how the company processes it, including for Cortana?
- Microsoft Privacy Statement

#### Where can you access information about how the Microsoft cloud helps the organization secure sensitive data and comply with applicable laws and regulations? 
- True Center

#### Where can an IT department find reference blueprints and policy definitions for common standards that it can apply directly to its Azure subscriptions?
- Azure compliance documentation

#### Which of the following does Azure Active Directory support for passwordless authentication?
- User X509 Certificates

#### Which of the following does Azure Active Directory support for passwordless authentication?
- FIDO2 security keys (key providers)
- Microsoft Authenticator
- Windows Hello for Business

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
