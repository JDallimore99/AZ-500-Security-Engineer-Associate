# Azure Active Directory features
Azure Active Directory (Azure AD) is Microsoft’s multi-tenant cloud-based directory and identity management service. For IT Admins, Azure AD provides an affordable, easy to use solution to give employees and business partners single sign-on (SSO) access to thousands of cloud SaaS Applications like Office365, Salesforce, DropBox, and Concur.
For application developers, Azure AD lets you focus on building your application by making it fast and simple to integrate with a world class identity management solution used by millions of organizations around the world.
- Azure Active Directory Free – Provides user and group management, on-premises directory synchronization, basic reports, and single sign-on across Azure, Microsoft 365, and many popular SaaS apps.
- Azure Active Directory Microsoft 365 Apps - This edition is included with O365. In addition to the Free features, this edition provides Identity & Access Management for Microsoft 365 apps including branding, MFA, group access management, and self-service password reset for cloud users.
- Azure Active Directory Premium P1 - In addition to the Free features, P1 also lets your hybrid users access both on-premises and cloud resources. It also supports advanced administration, such as dynamic groups, self-service group management, Microsoft Identity Manager (an on-premises identity and access management suite) and cloud write-back capabilities, which allow self-service password reset for your on-premises users.
- Azure Active Directory Premium P2 - In addition to the Free and P1 features, P2 also offers Azure Active Directory Identity Protection to help provide risk-based Conditional Access to your apps and critical company data and Privileged Identity Management to help discover, restrict, and monitor administrators and their access to resources and to provide just-in-time access when needed.

# Compare Azure AD vs Active Directory Domain Services
Characteristics of Azure AD that make it different.
- **Identity solution**. Azure AD is primarily an identity solution, and it is designed for Internet-based applications by using HTTP and HTTPS communications.
- **REST API Querying**. Because Azure AD is HTTP/HTTPS based, it cannot be queried through LDAP. Instead, Azure AD uses the REST API over HTTP and HTTPS.
- **Communication Protocols.** Because Azure AD is HTTP/HTTPS based, it does not use Kerberos authentication. Instead, it uses HTTP and HTTPS protocols such as SAML, WS-Federation, and OpenID Connect for authentication (and OAuth for authorization).
- **Authentication Services**. Include SAML, WS-Federation, or OpenID.
- **Authorization Service**. Uses OAuth.
- **Federation Services**. Azure AD includes federation services, and many third-party services (such as Facebook).
- **Flat structure.** Azure AD users and groups are created in a flat structure, and there are no Organizational Units (OUs) or Group Policy Objects (GPOs).

The following table summarizes the differences:

|Azure Active Directory| Active Directory Domain Services|
|:---|:---|
|Cloud|On-Premises|
|Designed for HTTP & HTTPS|Query via LDAP|
|Queried via REST API's|Used Kerberos for Authentication|
|Uses SAML, WS-Federation, or OpenID for authentication|No Federated Services|
|Uses OAuth for authorization|Organizational Units (OU's)|
|Includes federation services|Group Policy (GPO's)|
|Flat Structure||

# Investigate roles in Azure AD
## Available Roles
- Application Administrator - Users in this role can create and manage all aspects of enterprise applications, application registrations, and application proxy settings.
- Application Developer - Can create application registrations independent of the 'Users can register applications' setting.
- Authentication Administrator - Users with this role can set or reset any authentication method (including passwords) for non-administrators and some roles. - Authentication Administrators can require users who are non-administrators or assigned to some roles to re-register against existing non-password credentials (for example, multi-factor authentication or Fast Identity Online), and can also revoke remember multi-factor authentication on the device, which prompts for multi-factor authentication on the next sign-in.
- Azure DevOps Administrator - Users with this role can manage the Azure DevOps policy to restrict new Azure DevOps organization creation to a set of configurable users or groups.
- Azure Information Protection Administrator - Users with this role have all permissions in the Azure Information Protection service.
- B2C User Flow Administrator - Users with this role can create and manage B2C User Flows (also called "built-in" policies) in the Azure portal.
- B2C User Flow Attribute Administrator - Users with this role add or delete custom attributes available to all user flows in the tenant.
- B2C IEF Keyset Administrator - User can create and manage policy keys and secrets for token encryption, token signatures, and claim encryption/decryption.
- B2C IEF Policy Administrator - Users in this role can create, read, update, and delete all custom policies in Azure AD B2C and therefore have full control over the Identity Experience Framework in the relevant Azure AD B2C tenant.
- Billing Administrator - Makes purchases, manages subscriptions, manages support tickets, and monitors service health.
- Cloud Application Administrator - Users in this role have the same permissions as the Application Administrator role, excluding the ability to manage application proxy.
- Cloud Device Administrator - Users in this role can enable, disable, and delete devices in Azure AD and read Windows 10 BitLocker keys (if present) in the Azure portal.
- Compliance Administrator - Users with this role have permissions to manage compliance-related features in the Microsoft 365 compliance center, Microsoft 365 admin center, Azure, and Microsoft 365 Security & Compliance Center.
- Compliance Data Administrator - Users with this role have permissions to track data in the Microsoft 365 compliance center, Microsoft 365 admin center, and Azure. Users can also track compliance data within the Exchange admin center,
- Conditional Access Administrator - Users with this role have the ability to manage Azure Active Directory Conditional Access settings
- Exchange Administrator - Users with this role have global permissions within Microsoft Exchange Online when the service is present.
- Directory Readers - Users in this role can read basic directory information.
- Global Administrator / Company Administrator - Users with this role have access to all administrative features in Azure Active Directory, as well as services that use Azure Active Directory identities like Microsoft 365 security center, Microsoft 365 compliance center, Exchange Online, SharePoint Online, and Skype for Business Online.
- Groups Administrator - Users in this role can create/manage groups and its settings like naming and expiration policies.
- Security Administrator - Users with this role have permissions to manage security-related features in the Microsoft 365 security center, Azure Active Directory Identity Protection, Azure Information Protection, and Microsoft 365 Security & Compliance Center.

