---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
online version: .\New-AzureRmSiteRecoveryVault.md
schema: 2.0.0
updated_at: 10/14/2016 7:06 AM
ms.date: 10/14/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.SiteRecovery/v2.0/CmdletMDs/Get-AzureRmSiteRecoveryVault.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/a56d0e01e65c2c33aa2af13dd29addc94ead6e88/azureps-cmdlets-docs/ResourceManager/AzureRM.SiteRecovery/v2.0/CmdletMDs/Get-AzureRmSiteRecoveryVault.md
ms.topic: reference
ms.prod: powershell
ms.service: Azure PowerShell
ms.technology: Azure PowerShell
author: visual-studio-china
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmSiteRecoveryVault

## SYNOPSIS
Gets Site Recovery vaults from the current subscription.

## SYNTAX

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmSiteRecoveryVault** gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -Name
Specifies the name of the vault.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the Azure resource group from which to retrieve the recovery services object.

```yaml
Type: String
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

[New-AzureRmSiteRecoveryVault](.\New-AzureRmSiteRecoveryVault.md)

[Remove-AzureRmSiteRecoveryVault](.\Remove-AzureRmSiteRecoveryVault.md)
