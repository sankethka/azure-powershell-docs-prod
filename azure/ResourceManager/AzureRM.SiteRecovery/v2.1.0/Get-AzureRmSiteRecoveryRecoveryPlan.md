---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
online version: .\New-AzureRmSiteRecoveryRecoveryPlan.md
schema: 2.0.0
ms.assetid: 5DA460AF-2DB1-4303-B9D9-C51FD9674E4B
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.SiteRecovery/v2.1.0/Get-AzureRmSiteRecoveryRecoveryPlan.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.SiteRecovery/v2.1.0/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmSiteRecoveryRecoveryPlan

## SYNOPSIS
Gets a recovery plan in Site Recovery.

## SYNTAX

### Default (Default)
```
Get-AzureRmSiteRecoveryRecoveryPlan [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Path <String>] [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [-Path <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -FriendlyName
Specifies the friendly name of the recovery plan that this cmdlet gets.

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the recovery plan that this cmdlet gets.

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

### -Path
Specifies the file path to which this cmdlet saves the recovery plan.

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
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

[New-AzureRmSiteRecoveryRecoveryPlan](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[Remove-AzureRmSiteRecoveryRecoveryPlan](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[Update-AzureRmSiteRecoveryRecoveryPlan](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


