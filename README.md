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

## Quiz

### Authentication & Authorization features

#### What Microsoft Entra feature can you use to configure security authentication that requires users to use their mobile phone to sign in?
- Multi-factor Authentication (MFA)

#### How can the IT department use biometric properties, such as facial recognition, to enable delivery drivers to prove their identities?
- Multi-factor Authentication (MFA)

#### How can the IT department use biometric properties, such as facial recognition, to enable delivery drivers to prove their identities?
- Multifactor Authentication (MFA)

#### Which of the following does Microsoft Entra (Azure Active Directory) support for passwordless authentication?
- FIDO2 security keys (key providers)
- Microsoft Authenticator
- Windows Hello for Business

#### How can the IT department reduce the number of times users must authenticate to access multiple applications?
- Single sign-in (SSO)

#### Which two services are provided by Microsoft Entra (Azure Active Directory)?
- Authentication & Single sign-on (SSO)

#### How can the IT department reduce the number of times users must authenticate to access multiple applications?
- Single sign-on (SSO)

#### What enables a user to sign in one time and use that credential to access multiple resources and applications from different providers?
- Single sign-on (SSO)

#### Which Microsoft Entra feature can you use to ensure that users can only access Microsoft Office 365 applications from approved client applications?
- Conditional Access

#### Which Azure Active Directory tool can vary the credentials needed to log in based on signals, such as where the user is located? 
- Conditional Access

#### Which Azure Active Directory (Azure AD) feature is used to provide access to resources based on organizational policies?
- Conditional Access

#### ________ collects signals from the user, makes decisions based on those signals, and then enforces that decision by allowing or denying the access request or challenging for a multifactor authentication response.
- Conditional Access

#### How can the IT department ensure that employees at the company's retail stores can access company applications only from approved tablet devices?
- Conditional Access

#### What can you use to ensure that users authenticate by using multi-factor authentication (MFA) when they attempt to sign in from a specific location?
- Conditional Access

#### What can you use to ensure that a user can only access applications from compliant devices?
- Conditional Access

-----

### Authentication & Authorization actions

#### What can you use to sync identities from an on-premises Active Directory Domain Services (AD DS) domain to Microsoft Entra tenant?
- Microsoft Entra Connect

#### Each Azure subscription can be managed by using a Microsoft account only
- False, Azure Entra (Azure Active Directrory) account is required

#### Which is the best way for companies to ensure that they only deploy cost-effective virtual machine SKU sizes?
- Create a policy in Azure Policy that specifies the allowed SKU sizes

#### You need to recommend a solution for Azure virtual machine deployments. The solution must enforce company standards on the virtual machines. What should you include in the recommendation?
- Azure Policy

#### What can you use to ensure that new and existing Azure resources stay in compliance with corporate standards?
- Azure Policy

#### What can you use to restrict the deployment of a virtual machine to a specific location?
- Azure Policy

#### What can you use to ensure that a development team can only create virtual machines of a certain size?
- Azure Policy

#### ________ enforces standards and assess compliance across your organization
- Azure Policy

#### You need to recommend a solution for Azure virtual machine deployments. The solution must enforce company standards on the virtual machines. What should you include in the recommendation?
- Azure Policy

#### How can you prevent non-compliant resources from being created, without having to manually evaluate each resource as it's created?
- Azure Policy

#### ________ is a repeatable set of governance tools that helps development teams quickly build and create new environments while adhering to organizational compliance to speed up development and deployment.
- Azure Policy

#### You need to ensure that multi-factor authentication (MFA) is enabled on accounts with write permissions in an Azure subscription. What should you implement?
- Azure Policy

#### What provide organizations with the ability to manage the compliance of Azure resources across multiple subscriptions.
- Azure Policies

#### Which of the following is true for Azure Policy?
- A service in Azure that enables you to create, assign, and manage policies that control or audit your resources

-----

### Security models

#### Each Azure subscription can contain multiple account administrators
- False, 1 account administrator & 1 service administrator

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

-----

### Compliance

#### Where can a legal team access information around how the Microsoft cloud helps them secure sensitive data and comply with applicable laws and regulations?
- Trust Center

#### Where can you access information about how the Microsoft cloud helps the organization secure sensitive data and comply with applicable laws and regulations? 
- Trust Center

#### Where can you access details about the personal data Microsoft processes and how the company processes it, including for Cortana?
- Microsoft Privacy Statement

#### Where can an IT department find reference blueprints and policy definitions for common standards that it can apply directly to its Azure subscriptions?
- Azure compliance documentation

#### Your company plans to migrate to Azure. The company has several departments. All the Azure resources used by each department will be managed by a department administrator.
#### What 2 ways can you segment Azure for the departments?
- Multiple subscriptions
- Multiple resource groups

-----

### Azure role-based access control (Azure RBAC)

#### To which object or level is an Azure role-based access control (RBAC) role applied?
- Scope (An area of resource (sets) by the user's role)

#### How can companies allow some users to control the VMs in each environment but prevent them from modifying networking and other resources in the same resource group or Azure subscription?
- Create a role assignment through Azure role-based access control (Azure RBAC)

#### How can Tailwind Traders allow some users to control the virtual machines in each environment but prevent them from modifying networking and other resources in the same resource group or Azure subscription?
- Create a role assignment through Azure RBAC

#### What can you use to allow a user to manage all the resources in a resource group?
- Azure role-based access control (Azure RBAC)

#### (Repeats from M1-2) What can you use to allow a user to manage all the resources in a resource group?
- Azure role-based access control (Azure RBAC)

#### What can you use to allow a user to manage all the resources in a resource group?
- Azure role-based access control (Azure RBAC)

-----

### Resource Locks

#### What can you apply to an Azure virtual machine to ensure that users cannot change or delete the resource?
- A Resource Lock

#### Which of the following is true for Resource locking?
- Prevents resources from being accidentally deleted or changed

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
- Azure Subscriptions
- Azure Resource Groups

#### True or False:
- **Azure RBAC policies override restrictions defined by resource locks:**
  - False, resource lock cannot be overriden
- **If you place a resource lock on a resource group, all of the resources within the resource group will also have the resource lock applied**
  - True
- **Resource locks can be applied to individual resources, resource groups, or even an entire subscription.**
  - True
- **There are two types of resource locks, one that prevents users from deleting and one that prevents users from changing or deleting a resource.**
  - True

#### Contoso company wants to protect their production Storage Account from being deleted by accident. Currently their Administrators group has Owner privileges on the entire resource group where the storage account resides. To achieve this they used Delete lock on the Storage Account resource. Will this solution work?
- Yes

-----

### Microsoft Purview Data Policy

#### Which feature in the Microsoft Purview governance portal should you use to manage access to data sources and datasets?
- Data Policy

#### Which feature in the Microsoft purview governance portal should you use to manage access?
- Collections