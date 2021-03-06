---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: e8a607af-4739-4fb0-a4ea-a8382b69f081
schema: 2.0.0
ms.assetid: CA32A23B-631A-4C8C-A045-719E7FEEF2CC
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v2.2.0/Get-AzureRmAvailabilitySet.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v2.2.0/Get-AzureRmAvailabilitySet.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmAvailabilitySet

## SYNOPSIS
Gets Azure availability sets in a resource group.

## SYNTAX

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.
You can specify the name of a specific availability set to get.

## EXAMPLES

### Example 1: Get a specific availability set
```
PS C:\>Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.

### Example 2: Get all availability sets
```
PS C:\>Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

This command gets all the availability sets in the resource group named ResourceGroup11.

## PARAMETERS

### -Name
Specifies the name of an availability set that this cmdlet gets.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of a resource group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-AzureRmAvailabilitySet](./New-AzureRmAvailabilitySet.md)

[Remove-AzureRmAvailabilitySet](./Remove-AzureRmAvailabilitySet.md)


