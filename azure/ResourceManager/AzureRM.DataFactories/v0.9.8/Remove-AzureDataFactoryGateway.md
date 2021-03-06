---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
online version: 4076bd7c-248e-4f9f-b93a-7f2ffb9b0a51
schema: 2.0.0
ms.assetid: 059810A5-891B-429D-8B60-505AE0178B43
updated_at: 10/18/2016 9:38 PM
ms.date: 10/18/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.DataFactories/v0.9.8/Remove-AzureDataFactoryGateway.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/23cdb8705d4ab9807c0e21b238f3b134a7d49c7d/azureps-cmdlets-docs/ResourceManager/AzureRM.DataFactories/v0.9.8/Remove-AzureDataFactoryGateway.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Remove-AzureDataFactoryGateway

## SYNOPSIS
Removes the specified gateway from an Azure data factory.

## SYNTAX

### ByFactoryName (Default)
```
Remove-AzureDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-Profile <AzureProfile>] [<CommonParameters>]
```

### ByFactoryObject
```
Remove-AzureDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-Profile <AzureProfile>] [<CommonParameters>]
```

## DESCRIPTION
The Remove-AzureDataFactoryGateway cmdlet removes the specified gateway from an Azure data factory.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
PS C:\> Remove-AzureDataFactoryGateway -Name gatewaySample -DataFactoryName WikiADF -ResourceGroupName ADF
```

Removes the gateway 'gatewaySample' from the Azure data factory 'WikiADF'.

## PARAMETERS

### -DataFactory
Specifies a  object.
This cmdlet removes a gateway from the data factory that this parameter specifies.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Name of the data factory.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Indicates that this cmdlet removes a gateway without prompting you for confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name of the gateway.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name of the resource group.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
@{Text=}

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

### System.Boolean

## NOTES

## RELATED LINKS


