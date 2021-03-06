---
Module Name: AzureActiveDirectory
Module Guid: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
Download Help Link: Please enter FwLink manually
Help Version: Please enter version of help manually (X.X.X.X) format
Locale: en-US
ms.assetid: 7D9D9507-ADE5-45BD-97F8-0CCCDA3D3B58
updated_at: 10/27/2016 11:46 PM
ms.date: 10/27/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureAD/v2/AzureActiveDirectory.md
gitcommit: https://github.com/Azure/azure-docs-powershell-azuread/blob/a76928b576fb6d6dd5270c579171107be1494a14/Azure%20AD%20Cmdlets/AzureAD/v2/AzureActiveDirectory.md
ms.topic: conceptual
ms.prod: powershell
ms.service: Azure PowerShell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: visual-studio-china
---

# AzureActiveDirectory Module


## Description

You can use the Azure Active Directory PowerShell Module Version 2.0 for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on. These topics are related to using the version of Azure Active Directory released to preview June 30, 2016. The cmdlets listed here are different than the MSOL cmdlets which are part of Azure Active Directory Version 1.0.

You can use the Azure Active Directory PowerShell Module Version 2.0 for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on.
These topics are related to using the version of Azure Active Directory released to preview June 30, 2016.
The cmdlets listed here are different than the MSOL cmdlets which are part of Azure Active Directory Version 1.0.

Currently the release of the Azure AD PowerShell Version 2 module is in public preview.
It is not recommended to use this version for production scenarios.


## Install the Azure AD Module

The Azure AD Module is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell: Windows 8.1, Windows 8, Windows 7, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2.
The Azure AD PowerShell Version 2 preview module can be downloaded from the PowerShell Gallery at the [AzureADPreview](https://www.powershellgallery.com/packages/AzureADPreview) page.
For instructions on how to install the module, see [The PowerShell Gallery](https://msdn.microsoft.com/powershell/gallery/readme).
Please ensure that you have followed these steps before installing the module on your computer.
You can also access previous versions of the Azure AD module from the Microsoft Azure Active Directory PowerShell Module Version Release History on the TechNet Wiki.


## Updating the Azure AD Module

You can check the version of the module you have installed on your computer by running this command:

```PowerShell
PS C:\WINDOWS\system32> Get-Module AzureADdPreview

ModuleType Version Name                ExportedCommands
---------- ------- ----                ----------------
Binary     2.0.0.7 azureadpreview     {Add-AzureADAdmini...
```

To update the version of the Azure AD PowerShell module on your computer, re-run the **Install-Module** cmdlet:

```PowerShell
PS C:\WINDOWS\system32> Install-Module AzureADPreview
```
This command checks the PowerShell gallery to see if a newer version is available and installs it on your computer if the version on the PowerShell Gallery is newer than the one installed on your computer.


## Connect to Azure AD

Before you can run any of the cmdlets discussed in this article, you must first connect to your online service.
To do so, run the cmdlet **Connect-AzureAD** at the Windows PowerShell command prompt. You will then be prompted for your credentials. If you want, you can supply your credentials in advance, for example:

```PowerShell
$AzureAdCred = Get-Credential
Connect-AzureADService -Credential $AzureAdCred
```

The first command prompts for credentials and stores them as $AzureAdCred.
The next command uses those credentials as $azureadcred to connect to the service.

To connect to a specific environment of Azure Active Directory, use the _AzureEnvironment_ parameter, as follows:

```PowerShell
Connect-AzureADService -AzureEnvironment "AzureGermanyCloud"
```

This example connects your PowerShell session to the German AzureAD environment.
See **Connect-AzureADService** for more information.


## More about Windows PowerShell

Windows PowerShell is a task-based command-line shell and scripting language designed for system administration.
Unlike most shells, which accept and return text, Windows PowerShell is built on top of the .NET Framework, and accepts and returns .NET Framework objects.

Windows PowerShell introduces the concept of a cmdlet (pronounced "command-let"), a simple, single-function command-line tool built into the shell.
Cmdlets have the following naming convention: a verb and noun separated by a dash (-), such as **Get-Help**, **Get-Process**, and **Start-Service**.
Windows PowerShell includes more than one hundred basic core cmdlets.

For more information about, or for the syntax of, any of the cmdlets, use the `Get-Help <cmdlet name>` command, where `<cmdlet name>` is the name of the cmdlet that you want to research.
For more detailed information, you can run any of the following commands:

* `Get-Help <cmdlet name> -Detailed`
* `Get-Help <cmdlet name> -Examples`
* `Get-Help <cmdlet name> -Full`

For more information about Windows PowerShell, see the [Getting Started with Windows PowerShell](https://msdn.microsoft.com/en-us/powershell/scripting/getting-started/getting-started-with-windows-powershell).


## AzureActiveDirectory Cmdlets
### [Add-AzureADAdministrativeUnitMember](./Add-AzureADAdministrativeUnitMember.md)
Add an administrativeUnit member


### [Add-AzureADApplicationOwner](./Add-AzureADApplicationOwner.md)
Add an owner to an application


### [Add-AzureADApplicationPolicy](./Add-AzureADApplicationPolicy.md)



### [Add-AzureADDeviceRegisteredOwner](./Add-AzureADDeviceRegisteredOwner.md)



### [Add-AzureADDeviceRegisteredUser](./Add-AzureADDeviceRegisteredUser.md)



### [Add-AzureADDirectoryRoleMember](./Add-AzureADDirectoryRoleMember.md)
Add a member to a directory role


### [Add-AzureADGroupMember](./Add-AzureADGroupMember.md)
Add a member to a group


### [Add-AzureADGroupOwner](./Add-AzureADGroupOwner.md)
Add an owner to a group


### [Add-AzureADScopedRoleMembership](./Add-AzureADScopedRoleMembership.md)
Add a scopedRoleMembership to an administrativeUnit


### [Add-AzureADServicePrincipalOwner](./Add-AzureADServicePrincipalOwner.md)
Add an owner to a service principal


### [Add-AzureADServicePrincipalPolicy](./Add-AzureADServicePrincipalPolicy.md)



### [Confirm-AzureADDomain](./Confirm-AzureADDomain.md)
Validate the ownership of the domain.


### [Connect-AzureAD](./Connect-AzureAD.md)
Connect with an authenticated account to use Azure Active Directory cmdlet requests.


### [Disconnect-AzureAD](./Disconnect-AzureAD.md)
Disconnects the current session from an Azure AD tenant


### [Enable-AzureADDirectoryRole](./Enable-AzureADDirectoryRole.md)
Activates an existing directory role in Azure Active Directory


### [Get-AzureADAdministrativeUnitMember](./Get-AzureADAdministrativeUnitMember.md)
Get administrativeUnit members.


### [Get-AzureADAdministrativeUnit](./Get-AzureADAdministrativeUnit.md)
Get an Administrative Unit by objectId


### [Get-AzureADApplicationExtensionProperty](./Get-AzureADApplicationExtensionProperty.md)
Get group extension properties


### [Get-AzureADApplicationKeyCredential](./Get-AzureADApplicationKeyCredential.md)
Het an application's key credentials


### [Get-AzureADApplicationOwner](./Get-AzureADApplicationOwner.md)
Get owners of an application.


### [Get-AzureADApplicationPasswordCredential](./Get-AzureADApplicationPasswordCredential.md)
Get and application's password credentials


### [Get-AzureADApplicationPolicy](./Get-AzureADApplicationPolicy.md)



### [Get-AzureADApplication](./Get-AzureADApplication.md)
Get an application by objectId


### [Get-AzureADContactDirectReport](./Get-AzureADContactDirectReport.md)
Get the contact's direct reports.


### [Get-AzureADContactManager](./Get-AzureADContactManager.md)
Retrieves the manager of a contact from Azure Active Directory


### [Get-AzureADContactMembership](./Get-AzureADContactMembership.md)
Get contact memberships.


### [Get-AzureADContact](./Get-AzureADContact.md)
Retrieves a specific contact from Azure Active Directory


### [Get-AzureADContract](./Get-AzureADContract.md)
Retrieves a specific contract from Azure Active Directory


### [Get-AzureADDeviceRegisteredOwner](./Get-AzureADDeviceRegisteredOwner.md)



### [Get-AzureADDeviceRegisteredUser](./Get-AzureADDeviceRegisteredUser.md)



### [Get-AzureADDevice](./Get-AzureADDevice.md)
Retrieves a specific device from Azure Active Directory


### [Get-AzureADDirectoryRoleMember](./Get-AzureADDirectoryRoleMember.md)
Get the members of a directory role.


### [Get-AzureADDirectoryRoleTemplate](./Get-AzureADDirectoryRoleTemplate.md)
Retrieves a list of directory role templates in Azure Active Directory


### [Get-AzureADDirectoryRole](./Get-AzureADDirectoryRole.md)
Retrieves a specific directory role from Azure Active Directory


### [Get-AzureADDirectorySettingTemplate](./Get-AzureADDirectorySettingTemplate.md)
Retrieves directory setting template from Azure Active Directory.


### [Get-AzureADDirectorySetting](./Get-AzureADDirectorySetting.md)
Retrieves a directory setting from Azure Active Directory.


### [Get-AzureADDomain](./Get-AzureADDomain.md)
Get an domain by objectId


### [Get-AzureADGroupAppRoleAssignment](./Get-AzureADGroupAppRoleAssignment.md)
Get group application role assignments.


### [Get-AzureADGroupMember](./Get-AzureADGroupMember.md)
Get members of a group.


### [Get-AzureADGroupOwner](./Get-AzureADGroupOwner.md)
Get owners of a group.


### [Get-AzureADGroup](./Get-AzureADGroup.md)
Get a group by objectId


### [Get-AzureADOAuth2PermissionGrant](./Get-AzureADOAuth2PermissionGrant.md)
Get a list of all oAuth2PermissionGrants granted by users within the directory.


### [Get-AzureADObjectSetting](./Get-AzureADObjectSetting.md)
Retrieves a object setting from Azure Active Directory.


### [Get-AzureADPolicyAppliedObject](./Get-AzureADPolicyAppliedObject.md)



### [Get-AzureADPolicy](./Get-AzureADPolicy.md)



### [Get-AzureADScopedRoleMembership](./Get-AzureADScopedRoleMembership.md)
Retrieves a specific ScopedRoleMemberships from AdministrativeUnit


### [Get-AzureADServiceAppRoleAssignment](./Get-AzureADServiceAppRoleAssignment.md)
Get service principal application role assignments.


### [Get-AzureADServiceConfigurationRecord](./Get-AzureADServiceConfigurationRecord.md)
Get serviceConfigurationRecords


### [Get-AzureADServicePrincipalCreatedObject](./Get-AzureADServicePrincipalCreatedObject.md)
Get objects created by the service principal.


### [Get-AzureADServicePrincipalKeyCredential](./Get-AzureADServicePrincipalKeyCredential.md)
Get a service principal's key credentials


### [Get-AzureADServicePrincipalMembership](./Get-AzureADServicePrincipalMembership.md)
Get service principal memberships.


### [Get-AzureADServicePrincipalOAuth2PermissionGrant](./Get-AzureADServicePrincipalOAuth2PermissionGrant.md)
Get the list of the oAuth2PermissionGrants that a user granted this service principal.


### [Get-AzureADServicePrincipalOwnedObject](./Get-AzureADServicePrincipalOwnedObject.md)
Get objects owned by the service principal.


### [Get-AzureADServicePrincipalOwner](./Get-AzureADServicePrincipalOwner.md)
Get owners of a service principal.


### [Get-AzureADServicePrincipalPasswordCredential](./Get-AzureADServicePrincipalPasswordCredential.md)
Get a service principal's password credentials


### [Get-AzureADServicePrincipalPolicy](./Get-AzureADServicePrincipalPolicy.md)



### [Get-AzureADServicePrincipal](./Get-AzureADServicePrincipal.md)
Get a service principal by objectId


### [Get-AzureADSubscribedSku](./Get-AzureADSubscribedSku.md)
Retrieves a list of subscribed skus (subscriptions) to Microsoft services.


### [Get-AzureADTenantDetail](./Get-AzureADTenantDetail.md)
Retrieves the details of a tenant in Azure Active Directory


### [Get-AzureADTrustedCertificateAuthority](./Get-AzureADTrustedCertificateAuthority.md)



### [Get-AzureADUserAppRoleAssignment](./Get-AzureADUserAppRoleAssignment.md)
Get user application role assignments.


### [Get-AzureADUserCreatedObject](./Get-AzureADUserCreatedObject.md)
Get objects created by the user.


### [Get-AzureADUserDirectReport](./Get-AzureADUserDirectReport.md)
Get the user's direct reports.


### [Get-AzureADUserExtension](./Get-AzureADUserExtension.md)



### [Get-AzureADUserManager](./Get-AzureADUserManager.md)
Retrieves the manager of a user from Azure Active Directory


### [Get-AzureADUserMembership](./Get-AzureADUserMembership.md)
Get user memberships.


### [Get-AzureADUserOAuth2PermissionGrant](./Get-AzureADUserOAuth2PermissionGrant.md)
Get the list of the oAuth2PermissionGrants that the user granted applications.


### [Get-AzureADUserOwnedDevice](./Get-AzureADUserOwnedDevice.md)
Get registered devices owned by the user.


### [Get-AzureADUserOwnedObject](./Get-AzureADUserOwnedObject.md)
Get objects owned by the user.


### [Get-AzureADUserRegisteredDevice](./Get-AzureADUserRegisteredDevice.md)
Get registered devices registered by the user.


### [Get-AzureADUser](./Get-AzureADUser.md)
Retrieves a specific user from Azure Active Directory


### [Get-AzureADVerificationDnsRecord](./Get-AzureADVerificationDnsRecord.md)
Get verificationDnsRecords


### [New-AzureADAdministrativeUnit](./New-AzureADAdministrativeUnit.md)
Create a new administrativeUnit in Azure Active Directory


### [New-AzureADApplicationExtensionProperty](./New-AzureADApplicationExtensionProperty.md)
Create application extension property


### [New-AzureADApplicationKeyCredential](./New-AzureADApplicationKeyCredential.md)
Create a new key credential for an application


### [New-AzureADApplicationPasswordCredential](./New-AzureADApplicationPasswordCredential.md)
Create a new password credential for an application


### [New-AzureADApplication](./New-AzureADApplication.md)
Create a new application in Azure Active Directory


### [New-AzureADDevice](./New-AzureADDevice.md)
Create a new device in Azure Active Directory


### [New-AzureADDirectorySetting](./New-AzureADDirectorySetting.md)
Creates a directory settings object in Azure Active Directory.


### [New-AzureADDomain](./New-AzureADDomain.md)
Create a new domain in Azure Active Directory


### [New-AzureADGroupAppRoleAssignment](./New-AzureADGroupAppRoleAssignment.md)
Assign a group of users to an application role.


### [New-AzureADGroup](./New-AzureADGroup.md)
Create a new group in Azure Active Directory


### [New-AzureADObjectSetting](./New-AzureADObjectSetting.md)
Creates a settings object in Azure Active Directory.


### [New-AzureADPolicy](./New-AzureADPolicy.md)



### [New-AzureADServiceAppRoleAssignment](./New-AzureADServiceAppRoleAssignment.md)
Assign a service principal to an application role.


### [New-AzureADServicePrincipalKeyCredential](./New-AzureADServicePrincipalKeyCredential.md)
Create a new key credential for a service principal


### [New-AzureADServicePrincipalPasswordCredential](./New-AzureADServicePrincipalPasswordCredential.md)
Create a new password credential for a service principal


### [New-AzureADServicePrincipal](./New-AzureADServicePrincipal.md)
Create a new application in Azure Active Directory


### [New-AzureADTrustedCertificateAuthority](./New-AzureADTrustedCertificateAuthority.md)



### [New-AzureADUserAppRoleAssignment](./New-AzureADUserAppRoleAssignment.md)
Assign a user to an application role.


### [New-AzureADUser](./New-AzureADUser.md)
Create a new user in Azure Active Directory


### [Remove-AzureADAdministrativeUnitMember](./Remove-AzureADAdministrativeUnitMember.md)
Removes an administrativeUnit member.


### [Remove-AzureADAdministrativeUnit](./Remove-AzureADAdministrativeUnit.md)
Delete an administrativeUnit by objectId.


### [Remove-AzureADApplicationExtensionProperty](./Remove-AzureADApplicationExtensionProperty.md)
Delete an application extension property.


### [Remove-AzureADApplicationKeyCredential](./Remove-AzureADApplicationKeyCredential.md)
Remove a key credential from an application


### [Remove-AzureADApplicationOwner](./Remove-AzureADApplicationOwner.md)
Removes an owner from an application.


### [Remove-AzureADApplicationPasswordCredential](./Remove-AzureADApplicationPasswordCredential.md)
Remove a password credential from an application


### [Remove-AzureADApplicationPolicy](./Remove-AzureADApplicationPolicy.md)



### [Remove-AzureADApplication](./Remove-AzureADApplication.md)
Delete an application by objectId.


### [Remove-AzureADContactManager](./Remove-AzureADContactManager.md)
Deletes the contact's manager in Azure Active Directory


### [Remove-AzureADContact](./Remove-AzureADContact.md)
Deletes a specific contact in Azure Active Directory


### [Remove-AzureADDeviceRegisteredOwner](./Remove-AzureADDeviceRegisteredOwner.md)



### [Remove-AzureADDeviceRegisteredUser](./Remove-AzureADDeviceRegisteredUser.md)



### [Remove-AzureADDevice](./Remove-AzureADDevice.md)
Deletes a specific device in Azure Active Directory


### [Remove-AzureADDirectoryRoleMember](./Remove-AzureADDirectoryRoleMember.md)
Removes a specific member of a directory role.


### [Remove-AzureADDirectorySetting](./Remove-AzureADDirectorySetting.md)
Deletes a directory setting in Azure Active Directory.


### [Remove-AzureADDomain](./Remove-AzureADDomain.md)
Delete an domain by objectId.


### [Remove-AzureADGroupAppRoleAssignment](./Remove-AzureADGroupAppRoleAssignment.md)
Delete a group application role assignment.


### [Remove-AzureADGroupMember](./Remove-AzureADGroupMember.md)
Removes a member from a group.


### [Remove-AzureADGroupOwner](./Remove-AzureADGroupOwner.md)
Removes an owner from a group.


### [Remove-AzureADGroup](./Remove-AzureADGroup.md)
Delete a group by objectId.


### [Remove-AzureADOAuth2PermissionGrant](./Remove-AzureADOAuth2PermissionGrant.md)
Delete an oAuth2PermissionGrant.


### [Remove-AzureADObjectSetting](./Remove-AzureADObjectSetting.md)
Deletes settings in Azure Active Directory.


### [Remove-AzureADPolicy](./Remove-AzureADPolicy.md)



### [Remove-AzureADScopedRoleMembership](./Remove-AzureADScopedRoleMembership.md)
Removes a scopedRoleMembership.


### [Remove-AzureADServiceAppRoleAssignment](./Remove-AzureADServiceAppRoleAssignment.md)
Delete a service principal application role assignment.


### [Remove-AzureADServicePrincipalKeyCredential](./Remove-AzureADServicePrincipalKeyCredential.md)
Remove a key credential from a service principal


### [Remove-AzureADServicePrincipalOwner](./Remove-AzureADServicePrincipalOwner.md)
Removes an owner from a service principal.


### [Remove-AzureADServicePrincipalPasswordCredential](./Remove-AzureADServicePrincipalPasswordCredential.md)
Remove a password from a service principal


### [Remove-AzureADServicePrincipalPolicy](./Remove-AzureADServicePrincipalPolicy.md)



### [Remove-AzureADServicePrincipal](./Remove-AzureADServicePrincipal.md)
Delete an application by objectId.


### [Remove-AzureADTrustedCertificateAuthority](./Remove-AzureADTrustedCertificateAuthority.md)



### [Remove-AzureADUserAppRoleAssignment](./Remove-AzureADUserAppRoleAssignment.md)
Delete a user application role assignment.


### [Remove-AzureADUserExtension](./Remove-AzureADUserExtension.md)



### [Remove-AzureADUserManager](./Remove-AzureADUserManager.md)
Deletes the user's manager in Azure Active Directory


### [Remove-AzureADUser](./Remove-AzureADUser.md)
Deletes a specific user in Azure Active Directory


### [Select-AzureADGroupIdsContactIsMemberOf](./Select-AzureADGroupIdsContactIsMemberOf.md)
From a list of groups Ids select those that the contact is a member of.


### [Select-AzureADGroupIdsGroupIsMemberOf](./Select-AzureADGroupIdsGroupIsMemberOf.md)
From a list of groups Ids select those that the group is a member of.


### [Select-AzureADGroupIdsServicePrincipalIsMemberOf](./Select-AzureADGroupIdsServicePrincipalIsMemberOf.md)
From a list of groups Ids select those that the service principal is a member of.


### [Select-AzureADGroupIdsUserIsMemberOf](./Select-AzureADGroupIdsUserIsMemberOf.md)
From a list of groups Ids select those that the user is a member of.


### [Set-AzureADAdministrativeUnit](./Set-AzureADAdministrativeUnit.md)
Updates a specific administrativeUnit in Azure Active Directory


### [Set-AzureADApplication](./Set-AzureADApplication.md)
Updates a specific application in Azure Active Directory


### [Set-AzureADContactManager](./Set-AzureADContactManager.md)
Updates the contact's manager in Azure Active Directory


### [Set-AzureADContact](./Set-AzureADContact.md)
Updates a specific contact in Azure Active Directory


### [Set-AzureADDevice](./Set-AzureADDevice.md)
Updates a specific device in Azure Active Directory


### [Set-AzureADDirectorySetting](./Set-AzureADDirectorySetting.md)
Updates a directory setting in Azure Active Directory.


### [Set-AzureADDomain](./Set-AzureADDomain.md)
Updates a specific domain in Azure Active Directory


### [Set-AzureADGroup](./Set-AzureADGroup.md)
Updates a specific group in Azure Active Directory


### [Set-AzureADObjectSetting](./Set-AzureADObjectSetting.md)
Updates settings in Azure Active Directory.


### [Set-AzureADPolicy](./Set-AzureADPolicy.md)



### [Set-AzureADServicePrincipal](./Set-AzureADServicePrincipal.md)
Updates a service principal in Azure Active Directory


### [Set-AzureADTrustedCertificateAuthority](./Set-AzureADTrustedCertificateAuthority.md)



### [Set-AzureADUserExtension](./Set-AzureADUserExtension.md)



### [Set-AzureADUserLicense](./Set-AzureADUserLicense.md)
Add and remove one or more licenses for a Microsoft online service to the list of assigned licenses for the user.


### [Set-AzureADUserManager](./Set-AzureADUserManager.md)
Updates the user's manager in Azure Active Directory


### [Set-AzureADUserPassword](./Set-AzureADUserPassword.md)
Sets the password of a user in Azure AD


### [Set-AzureADUser](./Set-AzureADUser.md)
Updates a specific user in Azure Active Directory


### [Update-AzureADSignedInUserPassword](./Update-AzureADSignedInUserPassword.md)
Updates the password for the signed in user in Azure AD


## Additional Resources

There are several other places you can get more information and help. These include:

* [Azure Active Directory Forum](https://social.msdn.microsoft.com/forums/azure/en-us/home?forum=windowsazuread)

* [Windows Azure AD Community Information Center](https://social.technet.microsoft.com/forums/azure/en-us/1bb6e693-eb7b-4379-8c6a-f78277365fed/windows-azure-ad-community-information-center?forum=windowsazureaditpro)

* [Azure Active Directory Community Scripts](http://social.technet.microsoft.com/wiki/contents/articles/tags/aad%20how%20to%20script/default.aspx)

* [Microsoft Azure Active Directory PowerShell Module Version Release History](http://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx)

* [Administering Your Azure AD Directory](https://msdn.microsoft.com/en-us/library/azure/hh967611(v=azure.98).aspx)

* [Install Windows PowerShell on the Directory Sync Computer](https://msdn.microsoft.com/en-us/library/azure/jj151828(v=azure.98).aspx)
 
