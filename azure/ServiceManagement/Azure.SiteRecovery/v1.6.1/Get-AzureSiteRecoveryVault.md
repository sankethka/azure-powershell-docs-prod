---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
online version: .\New-AzureSiteRecoveryVault.md
schema: 2.0.0
ms.assetid: 7671EEE8-83DA-4055-951E-395F9FE5CFFB
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.SiteRecovery/v1.6.1/Get-AzureSiteRecoveryVault.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.SiteRecovery/v1.6.1/Get-AzureSiteRecoveryVault.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureSiteRecoveryVault

## SYNOPSIS
Gets the active Azure Site Recovery vault.

## SYNTAX

### Default (Default)
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByName
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureSiteRecoveryVault** cmdlet gets the active Azure Site Recovery vault.

## EXAMPLES

### Example 1: Get the active vault
```
PS C:\>Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

This command gets the active Azure Site Recovery vault.

## PARAMETERS

### -Name
Specifies the name of the vault to get.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifies an Azure profile.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-AzureSiteRecoveryVault](./New-AzureSiteRecoveryVault.md)

[Get-AzureSiteRecoveryVaultSettingsFile](./Get-AzureSiteRecoveryVaultSettingsFile.md)


