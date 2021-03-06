---
Module Name: AzureActiveDirectory
Module Guid: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
Download Help Link: Please enter FwLink manually
Help Version: Please enter version of help manually (X.X.X.X) format
Locale: en-US
ms.assetid: BB86A603-6CD9-4299-89B8-30A2B4A011A0
updated_at: 10/27/2016 10:50 PM
ms.date: 10/27/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-azuread/blob/master/Azure%20AD%20Cmdlets/AzureADPreview/v1.0.0/AzureActiveDirectory.md
gitcommit: https://github.com/Azure/azure-docs-powershell-azuread/blob/668db84069263de3dc6030a9b21361f0d122563c/Azure%20AD%20Cmdlets/AzureADPreview/v1.0.0/AzureActiveDirectory.md
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

You can use the Azure Active Directory Module for Windows PowerShell cmdlets for Azure AD administrative tasks such as user management, domain management and for configuring single sign-on.
This topic includes information about how to install these cmdlets for use with your directory.


## Install the Azure AD Module

The Azure AD Module is supported on the following Windows operating systems with the default version of Microsoft .NET Framework and Windows PowerShell: Windows 8.1, Windows 8, Windows 7, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2.

There are two versions of the Azure Active Directory Module for Windows PowerShell available: a General Availability version and a Public Preview Version.
The Public Preview version contains cmdlets that have not yet been released for General Availability.

Select the version you want from the [Azure Active Directory Connection download page](http://connect.microsoft.com/site1164/Downloads/DownloadDetails.aspx?DownloadID=59185), download its .msi file, and click **Run** to run the installer package.

**Important**

Effective October 20, 2014, the [Azure Active Directory Module for Windows PowerShell (32-bit version)](http://go.microsoft.com/fwlink/p/?linkid=236298) is discontinued.
Support for the 32-bit version will no longer occur, and future updates to the Azure Active Directory Module will be released only for the 64-bit version.

We strongly recommend you install the 64-bit version to ensure future support and compatibility.

You can also access previous versions of the Azure AD module from the [Microsoft Azure Active Directory PowerShell Module Version Release History](http://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx) on the TechNet Wiki.


## Updating the Azure AD Module

You can run the **Get-Item** cmdlet to check the version of the DLL files of the module that you have currently installed:

```PowerShell
(Get-item C:\Windows\System32\WindowsPowerShell\v1.0\Modules\MSOnline\Microsoft.Online.Administration.Automation.PSModule.dll).VersionInfo.FileVersion
```

If the version number is lower than 1.0.8070.2, remove the existing version and re-install the module using the link in the previous section.
Use **Add/Remove Programs** in Control Panel to remove **Azure Active Directory Module for Windows PowerShell**, or if you have an older installation, to remove **Microsoft Online Services Module for Windows PowerShell**.
Uninstalling removes both the **MSOnline** and **MSOnlineExtended** modules.

The **Remove-Module** cmdlet removes the **MSOnline** cmdlets from the session but it does not uninstall the module.


## Connect to Azure AD

Before you can run any of the cmdlets discussed in this article, you must first connect to your online service.
To do so, run the cmdlet **Connect-MsolService** at the Windows PowerShell command prompt.
You will then be prompted for your credentials.
If you want, you can supply your credentials in advance, for example:

```PowerShell
$Msolcred = Get-credential
Connect-MsolService -Credential $MsolCred
```

The first command prompts for credentials and stores them as $Msolcred.
The next command uses those credentials as $Msolcred to connect to the service.

To connect to a specific environment of Azure Active Directory, use the AzureEnvironment parameter, as follows:

`Connect-MsolService -AzureEnvironment "AzureGermanyCloud"`

This example connects your PowerShell session to the German AzureAD environment.

See [Connect-MsolService](https://msdn.microsoft.com/en-us/library/azure/dn194123(v=azure.98).aspx) for more information.

For more information about the cmdlets, you can do the following:

* To create a folder for help, list the cmdlets, and then open the file in notepad, you can run the following commands at the Windows PowerShell command prompt:

```PowerShell
New-Item c:\MsolHelp -Type directory
Get-command | Where-Object {$_.name -like "*msol*"} | Format-List | Out-File c:\MsolHelp\msolcmdlets.txt
Notepad c:\MsolHelp\msolcmdlets.txt
```

* View the examples for a cmdlet, run the following command at the Windows PowerShell command prompt: `Get-Help <cmdlet-name> -Examples`

* View the name, synopsis, description, parameter descriptions, and any examples provided for a cmdlet, run the following command at the Windows PowerShell command prompt: `Get-Help <cmdlet-name> -Detailed`

* View the name, synopsis, description, detailed parameters, and any examples provided for a cmdlet, run the following command at the Windows PowerShell command prompt: `Get-Help <cmdlet-name> -Full`


## More about Windows PowerShell

Windows PowerShell is a task-based command-line shell and scripting language designed for system administration.
Unlike most shells, which accept and return text, Windows PowerShell is built on top of the .NET Framework, and accepts and returns .NET Framework objects.
Windows PowerShell introduces the concept of a cmdlet (pronounced "command-let"), a simple, single-function command-line tool built into the shell.
Cmdlets have the following naming convention: a verb and noun separated by a dash (-), such as Get-Help, Get-Process, and Start-Service.
Windows PowerShell includes more than one hundred basic core cmdlets.
For more information about Windows PowerShell, see [Getting Started with Windows PowerShell](https://msdn.microsoft.com/powershell/scripting/getting-started/getting-started-with-windows-powershell).


## AzureActiveDirectory Cmdlets
### [Disable-MsolDevice](./Disable-MsolDevice.md)
Disables a device object in Azure Active Directory.


### [Enable-MsolDevice](./Enable-MsolDevice.md)
Enables a device object in Azure Active Directory.


### [Get-MsolAllSettings](./Get-MsolAllSettings.md)
Gets all directory settings object associated with tenant or group/user/service principal/application/device.


### [Get-MsolAllSettingTemplate](./Get-MsolAllSettingTemplate.md)
Gets all the directory setting templates that a tenant owns.


### [Get-MsolDeviceRegistrationServicePolicy](./Get-MsolDeviceRegistrationServicePolicy.md)
Gets the Azure Active Directory device registration service settings.


### [Get-MsolDevice](./Get-MsolDevice.md)
Gets an individual device, or a list of devices.


### [Get-MsolDirSyncConfiguration](./Get-MsolDirSyncConfiguration.md)



### [Get-MsolDirSyncFeatures](./Get-MsolDirSyncFeatures.md)
Gets the status of identity synchronization features for a tenant.


### [Get-MsolDirSyncProvisioningError](./Get-MsolDirSyncProvisioningError.md)
Checks for objects with synchronization provisioning errors in a tenant.


### [Get-MsolHasObjectsWithDirSyncProvisioningErrors](./Get-MsolHasObjectsWithDirSyncProvisioningErrors.md)



### [Get-MsolSettings](./Get-MsolSettings.md)
Gets a directory setting.


### [Get-MsolSettingTemplate](./Get-MsolSettingTemplate.md)
Gets a directory setting template.


### [Get-MsolUserByStrongAuthentication](./Get-MsolUserByStrongAuthentication.md)



### [New-MsolSettings](./New-MsolSettings.md)
Creates a directory setting.


### [New-MsolWellKnownGroup](./New-MsolWellKnownGroup.md)



### [Remove-MsolApplicationPassword](./Remove-MsolApplicationPassword.md)



### [Remove-MsolDevice](./Remove-MsolDevice.md)
Remove a device object from Azure Active Directory.


### [Remove-MsolForeignGroupFromRole](./Remove-MsolForeignGroupFromRole.md)



### [Remove-MsolSettings](./Remove-MsolSettings.md)
Removes a directory setting.


### [Reset-MsolStrongAuthenticationMethodByUpn](./Reset-MsolStrongAuthenticationMethodByUpn.md)



### [Set-MsolDeviceRegistrationServicePolicy](./Set-MsolDeviceRegistrationServicePolicy.md)
Sets the Azure Active Directory device registration service settings.


### [Set-MsolDirSyncConfiguration](./Set-MsolDirSyncConfiguration.md)



### [Set-MsolDirSyncFeature](./Set-MsolDirSyncFeature.md)
Sets identity synchronization features for a tenant.


### [Set-MsolSettings](./Set-MsolSettings.md)
Updates a directory setting in Azure Active Directory.

## Additional Resources

There are several other places you can get more information and help.
These include the following:

* [Azure Active Directory Forum](http://aka.ms/aadforum)
* [Azure AD Community Information Center](http://aka.ms/aadcommunity)
* [Azure Active Directory Community scripts](http://aka.ms/aadscripts)
* [Microsoft Azure Active Directory PowerShell Module Version Release History](http://social.technet.microsoft.com/wiki/contents/articles/28552.microsoft-azure-active-directory-powershell-module-version-release-history.aspx)

## See Also

[Administering your Azure AD directory](https://msdn.microsoft.com/en-us/library/azure/hh967611(v=azure.98).aspx)

[Install Windows PowerShell for directory synchronization](https://msdn.microsoft.com/en-us/library/azure/jj151828(v=azure.98).aspx)
