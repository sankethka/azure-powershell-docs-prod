---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
online version: .\New-AzureRmCognitiveServicesAccountKey.md
schema: 2.0.0
ms.assetid: 35F33DDA-691E-4D12-A585-D9525DD0B721
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.CognitiveServices/v0.1.3/Get-AzureRmCognitiveServicesAccountKey.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.CognitiveServices/v0.1.3/Get-AzureRmCognitiveServicesAccountKey.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmCognitiveServicesAccountKey

## SYNOPSIS
Gets the API keys for an account.

## SYNTAX

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.

A Cognitive Services account has two API keys: Key1 and Key2.
The keys enable interaction with the Cognitive Services account endpoint.

Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -ResourceGroupName
Specifies the name of the resource group the account is assigned to.

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

### -Name
Specifies the name of the account.
This cmdlet gets the keys for this account.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
@{Text=}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

[New-AzureRmCognitiveServicesAccountKey](./New-AzureRmCognitiveServicesAccountKey.md)


