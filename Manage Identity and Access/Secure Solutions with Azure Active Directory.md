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

# Deploy Azure AD Domain Services
Azure Active Directory Domain Services (Azure AD DS) provides managed domain services such as domain join, group policy, lightweight directory access protocol (LDAP), and Kerberos / NTLM authentication that is fully compatible with Windows Server Active Directory. You use these domain services without the need to deploy, manage, and patch domain controllers in the cloud. Azure AD DS integrates with your existing Azure AD tenant, which makes it possible for users to sign in using their existing credentials. You can also use existing groups and user accounts to secure access to resources, which provides a smoother lift-and-shift of on-premises resources to Azure.

Azure AD DS replicates identity information from Azure AD, so it works with Azure AD tenants that are cloud-only, or synchronized with an on-premises Active Directory Domain Services (AD DS) environment. The same set of Azure AD DS features exist for both environments.
- If you have an existing on-premises AD DS environment, you can synchronize user account information to provide a consistent identity for users.
- For cloud-only environments, you don't need a traditional on-premises AD DS environment to use the centralized identity services of Azure AD DS.

### Azure AD DS features and benefits
The following features of Azure AD DS simplify deployment and management operations:
- **Simplified deployment experience**: Azure AD DS is enabled for your Azure AD tenant using a single wizard in the Azure portal.
- **Integrated with Azure AD**: User accounts, group memberships, and credentials are automatically available from your Azure AD tenant. New users, groups, or changes to attributes from your Azure AD tenant or your on-premises AD DS environment are automatically synchronized to Azure AD DS.
- **Use your corporate credentials/passwords**: Passwords for users in Azure AD DS are the same as in your Azure AD tenant. Users can use their corporate credentials to domain-join machines, sign in interactively or over remote desktop, and authenticate against the Azure AD DS managed domain.
- **NTLM and Kerberos authentication**: With support for NTLM and Kerberos authentication, you can deploy applications that rely on Windows-integrated authentication.
- **High availability**: Azure AD DS includes multiple domain controllers, which provide high availability for your managed domain. This high availability guarantees service uptime and resilience to failures.

> Important: Azure AD DS integrates with Azure AD, which itself can synchronize with an on-premises AD DS environment. This ability extends central identity use cases to traditional web applications that run in Azure as part of a lift-and-shift strategy. 

# Create and Manage Azure AD users
Add new users or delete existing users from your Azure Active Directory (Azure AD) tenant. To add or delete users, you must be a User Administrator or Global Administrator.
## Add a new user
You can create a new user for your organization or invite an external user from the same starting point.
1. Sign in to the Azure portal in the User Administrator role.
2. Navigate to Azure Active Directory > Users.
3. Select either Create new user or Invite external user from the menu.

![image](https://user-images.githubusercontent.com/118181672/224755803-6fc03061-2b8b-4a16-9d6a-7ac0753bbd36.png)

4. On the New User page, provide the new user's information:
- Identity: Add a user name and display name for the user. User name and Name are required and can't contain accent characters. You can also add a first and last name.
The domain part of the user name must use either the initial default domain name, <yourdomainname>.onmicrosoft.com, or a custom domain name, such as contoso.com.
- Groups and roles: Optional. Add the user to one or more existing groups. Group membership can be set at any time.
- Settings: Optional. Toggle the option to block sign-in for the user or set the user's default location.
- Job info: Optional. Add the user's job title, department, company name, and manager. These details can be updated at any time.

5. Copy the autogenerated password provided in the Password box. You'll need to give this password to the user to sign in for the first time.
6. Select Create.
The user is created and added to your Azure AD organization. 
## Add a new guest user
You can also invite the new guest user to collaborate with your organization by selecting Invite user from the New user page. If your organization's external collaboration settings are configured to allow guests, the user will be emailed an invitation they must accept in order to begin collaborating.

## Add other users
There might be scenarios where you want to manually create consumer accounts in your Azure Active Directory B2C (Azure AD B2C) directory. If you have an environment with Azure Active Directory (cloud) and Windows Server Active Directory (on-premises), you can add new users by syncing the existing user account data.

## Delete a user
You can delete an existing user using the Azure Active Directory portal.
- You must have a Global Administrator, Privileged Authentication Administrator, or User Administrator role assignment to delete users in your organization.
- Global Admins and Privileged Authentication Admins can delete any users, including other admins.
- User Administrators can delete any non-admin users, Helpdesk Administrators, and other User Administrators.
 
1. Sign in to the Azure portal using one of the appropriate roles listed above.
2. Go to Azure Active Directory > Users.
3. Search for and select the user you want to delete from your Azure AD tenant.
4. Select Delete user.
![image](https://user-images.githubusercontent.com/118181672/224756383-28e22836-6578-4dae-b087-97062ef4187e.png)

The user is deleted and no longer appears on the Users - All users page. The user can be seen on the Deleted users page for the next 30 days and can be restored during that time.

When a user is deleted, any licenses consumed by the user are made available for other users.
