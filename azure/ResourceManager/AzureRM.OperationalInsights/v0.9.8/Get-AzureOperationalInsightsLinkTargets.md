---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
online version: .\New-AzureOperationalInsightsWorkspace.md
schema: 2.0.0
ms.assetid: 9D7C6F12-BB94-435D-90BD-518523B73033
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.OperationalInsights/v0.9.8/Get-AzureOperationalInsightsLinkTargets.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.OperationalInsights/v0.9.8/Get-AzureOperationalInsightsLinkTargets.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureOperationalInsightsLinkTargets

## SYNOPSIS
Gets accounts that are not associated with an Azure subscription.

## SYNTAX

```
Get-AzureOperationalInsightsLinkTargets [-Profile <AzureProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureOperationalInsightsLinkTargets** cmdlet gets existing accounts that are not associated with an Azure subscription.

To link a new workspace to an existing account, use a customer ID that is returned by this operation for the *CustomerID* parameter in the New-AzureOperationalInsightsWorkspace cmdlet.

## EXAMPLES

### Example 1: Get unlinked accounts
```
PS C:\>Get-AzureOperationalInsightsLinkTargets
```

This command gets unlinked accounts that are owned by the caller's ID.

## PARAMETERS

### -Profile
Specifies the Azure profile from which this cmdlet reads.
If you do not specify a profile, this cmdlet reads from the local default profile.

```yaml
Type: AzureProfile
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

[New-AzureOperationalInsightsWorkspace](./New-AzureOperationalInsightsWorkspace.md)


