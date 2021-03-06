---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
online version: 851398c2-2daf-4f3d-acad-e440c8ae736e
schema: 2.0.0
ms.assetid: 1BB29A20-68C9-46F4-93F7-B3FD04BC5348
updated_at: 10/20/2016 12:12 AM
ms.date: 10/20/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.StreamAnalytics/v0.9.8/Get-AzureStreamAnalyticsQuota.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/831f900c1a4babea8fcc8817cfbc25252a1aa872/azureps-cmdlets-docs/ResourceManager/AzureRM.StreamAnalytics/v0.9.8/Get-AzureStreamAnalyticsQuota.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureStreamAnalyticsQuota

## SYNOPSIS
Gets information about the Streaming Unit quota of a specified region.

## SYNTAX

```
Get-AzureStreamAnalyticsQuota [-Location] <String> [-Profile <AzureProfile>] [-PipelineVariable <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureStreamAnalyticsQuota** cmdlet gets the streaming unit quota for a specified Azure region.

## EXAMPLES

### Example 1: Get the streaming unit quota for a region
```
PS C:\>Get-AzureStreamAnalyticsQuota -Location "West US"
```

This command gets the streaming unit quota and usage for the West US region.

## PARAMETERS

### -Location
Specifies the name of an Azure region/Azure data center location to get Streaming Unit quota information for.
See Azure Regionshttp://azure.microsoft.com/en-us/regions/#services at http://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -PipelineVariable
Not Specified

```yaml
Type: String
Parameter Sets: (All)
Aliases: pv

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

### System.Collections.Generic.List`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics, Version=0.8.11.0, Culture=neutral, PublicKeyToken=null]]Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota

## NOTES

## RELATED LINKS


