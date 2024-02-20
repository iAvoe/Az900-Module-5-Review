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
- If a user wants to access a resource, then they must perform action by detection of:
  - User or Group Membership
  - IP Location
  - Device Type
  - Application
  - Real-time risk detection
- i.e.: A user wants to access an app like Microsoft 365 --> must perform MFA

-----

<br>

## Azure Governance Methodologies

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
- Assessing compliance by governance at-scale
- Enforcing standards, compliance, service level agreements (SLAs)
- Provides built-in policy & initiative definitions under categories such as:
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
- Sets forth the obligations with respect to the processing & security of customer and personal data

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

## Cloud Adoption Framework for Azure (optional study)
- The Best practices / One Microsoft approach to cloud adoption
- Tools, guidance and narratives for strategies and outcomes

### Strategy
- Motivations
- Business outcomes
- Financial considerations

### Plan
- Rationalize your digital estate
- Organizational alignment
- Skills readiness plan
- DevOps cloud adoption plan

### Ready
- Operating model alignment
- Azure landing zone conceptual architecture
- Azure landing zone design areas
- Implementation options

### Migrate
- Migration scenarios
- Cloud migration best practices
- Process improvements

### Innovate
- Business value consensus
- Build your first MVP
- Measure for customer impact
- Expand digital inventions

### Secure
- Risk insights
- Business resilience
- Asset protection

### Manage
- Business commitments
- Management baseline
- Expand the baseline
- Advance operations and design principles

### Govern
- Benchmark assessment
- Governance foundation
- Improve the foundation

-----

<br>

## Quiz

### Authentication & Authorization features

#### Which Azure Active Directory tool can vary the credentials needed to log in based on signals, such as where the user is located? 
- Conditional Access

#### Which Azure Active Directory (Azure AD) feature is used to provide access to resources based on organizational policies?
- Conditional Access

#### ________ collects signals from the user, makes decisions based on those signals, and then enforces that decision by allowing or denying the access request or challenging for a multifactor authentication response.
- Conditional Access

#### How can the IT department ensure that employees at the company's retail stores can access company applications only from approved tablet devices?
- Conditional Access

#### How can the IT department use biometric properties, such as facial recognition, to enable delivery drivers to prove their identities?
- MFA

#### How can the IT department reduce the number of times users must authenticate to access multiple applications?
- SSO

#### Which is likely the best way for companies to identify which billing department each Azure resource belongs to?
- Tags

#### Which of the following does Azure Active Directory support for passwordless authentication?
- FIDO2 security keys (key providers)
- Microsoft Authenticator
- Windows Hello for Business

#### Which statement describes Azure Resource Locks?
- A feature that allows customers to protect their resources from human-error accidents like modification or deletion of the resources 

#### What kinds of security locks are supported by Azure?
- Read-only
- Delete

#### True or False
- **Read-only locks only allow read actions on resources. Every other action is blocked**
  - True
- **Delete locks only allows resoruces to be deleted but not created or updated.**
  - False

#### Azure Resource Locks can be applied on which scopes?
- Azure Resource
- Azure Resource Gruops
- Azure Subscriptions

-----

<br>

### Authentication & Authorization actions

#### How can companies allow some users to control the VMs in each environment but prevent them from modifying networking and other resources in the same resource group or Azure subscription?
- Create a role assignment through Azure role-based access control (Azure RBAC)

#### Which is the best way for companies to ensure that they only deploy cost-effective virtual machine SKU sizes?
- Create a policy in Azure Policy that specifies the allowed SKU sizes

#### Contoso company wants to protect their production Storage Account from being deleted by accident. Currently their Administrators group has Owner privileges on the entire resource group where the storage account resides.
#### To achieve this they used Delete lock on the Storage Account resource. Will this solution work?
- Yes

-----

<br>

### Security models

#### Each Azure subscription can contain multiple account administrators
- False, 1 account administrator & 1 service administrator

#### Each Azure subscription can be managed by using a Microsoft account only
- False, Azure Active Directory / Azure Entra account is required

#### An Azure Resource group contains multiple Azure subscription
- False, multiple resource-(group)s is/are under Azure subscription

#### Which security model assumes the worst-case security scenario, and protects resources accordingly?
- Zero trust

#### Match description to Zero Trust model's guiding principles:
- **Always authenticate and authorize based on all available data points**
  - Verify explicitly
- **Limit user access with Just-in-time and Just-enough-access, risk-based adaptive policies, and data protection**
  - Use least privilege access
- **Segment access, verify end-to-end encryption, use analytics to get visibility, drive threat detection and improve defenses**
  - Assume Breach

#### True or False:
- **Azure RBAC policies override restrictions defined by resource locks:**
  - False, resource lock cannot be overriden
- **If you place a resource lock on a resource group, all of the resources within the resource group will also have the resource lock applied**
  - True
- **Resource locks can be applied to individual resources, resource groups, or even an entire subscription.**
  - True
- **There are two types of resource locks, one that prevents users from deleting and one that prevents users from changing or deleting a resource.**
  - True

-----

<br>

### Compliance

#### Your company plans to move several servers to Azure. The company's compliance policy states that a server named FinServer must be on a separate network segment.
#### Which Azure solution should you recommend?
- A virtual network for FinServer and another virtual network for all the other servers
Note: Networks in Azure are known as virtual networks. A virtual network can have multiple IP address spaces and multiple subnets. Azure automatically routes traffic between different subnets within a virtual network.

#### Where can a legal team access information around how the Microsoft cloud helps them secure sensitive data and comply with applicable laws and regulations?
- Trust Center

#### Where can you access information about how the Microsoft cloud helps the organization secure sensitive data and comply with applicable laws and regulations? 
- Trust Center

#### Where can you access details about the personal data Microsoft processes and how the company processes it, including for Cortana?
- Microsoft Privacy Statement

#### Where can an IT department find reference blueprints and policy definitions for common standards that it can apply directly to its Azure subscriptions?
- Azure compliance documentation

#### What provide organizations with the ability to manage the compliance of Azure resources across multiple subscriptions.
- Azure Policies

#### Your company plans to migrate to Azure. The company has several departments. All the Azure resources used by each department will be managed by a department administrator.
#### What 2 ways can you segment Azure for the departments?
- Multiple subscriptions
- Multiple resource groups

-----

### Unsorted

#### Your company has virtual machines (VMs) hosted in Microsoft Azure. The VMs are located in a single Azure virtual network named VNet1.
#### The company has users that work remotely. The remote workers require access to the VMs on VNet1. To provide access for the remote workers, you:
- Configure a Point-to-Site (P2S) VPN.

#### You have an Azure environment that contains multiple Azure virtual machines.
#### You plan to implement a solution that enables the client computers on your on-premises network to communicate to the Azure virtual machines.
#### You need to recommend which Azure resources must be created for the planned solution.
#### What 2 Azure resources should you include in the recommendation?
- A virtual network gateway
- A gateway subnet

#### Your company plans to migrate all its network resources to Azure. You need to start the planning process by exploring Azure.
#### What should you create first?
- Subscription