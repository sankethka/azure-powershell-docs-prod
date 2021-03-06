---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: .\Get-AzureRmBatchAccountKeys.md
schema: 2.0.0
ms.assetid: E1B365EF-C6F2-4EA1-A443-8A901DC75598
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Batch/v2.1.0/Get-AzureRmBatchSubscriptionQuotas.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Batch/v2.1.0/Get-AzureRmBatchSubscriptionQuotas.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmBatchSubscriptionQuotas

## SYNOPSIS
Gets the quota for your subscription in the Batch service for a region.

## SYNTAX

```
Get-AzureRmBatchSubscriptionQuotas [-Location] <String> [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmBatchSubscriptionQuotas** cmdlet gets the quota of accounts for your subscription in the Azure Batch service for the specified region.

## EXAMPLES

### Example 1: Get the quota for the subscription in the West US region
```
PS C:\>Get-AzureRmBatchSubscriptionQuotas -Location "westus"
AccountQuota Location
------------ --------
1            westus
```

This command gets the quota for the current subscription in the West US region.
The return value indicates that this subscription can create only one account in that region.

## PARAMETERS

### -Location
Specifies the region for which this cmdlet checks the quota.
For more information, see Azure Regionshttps://azure.microsoft.com/en-us/regions (https://azure.microsoft.com/en-us/regions).

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### PSBatchSubscriptionQuotas

## NOTES

## RELATED LINKS

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Azure Batch Cmdlets](./AzureRM.Batch.md)


