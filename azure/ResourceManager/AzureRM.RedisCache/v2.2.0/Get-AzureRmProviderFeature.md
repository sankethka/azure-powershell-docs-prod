---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
online version: 1f2f7bd8-ba9e-4afd-91cc-6ae4ab89c895
schema: 2.0.0
ms.assetid: 84F0E54B-294C-4FAD-A7D1-FC1B352B1337
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.RedisCache/v2.2.0/Get-AzureRmProviderFeature.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.RedisCache/v2.2.0/Get-AzureRmProviderFeature.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
---

# Get-AzureRmProviderFeature

## SYNOPSIS
Gets information about Azure provider features.

## SYNTAX

### ListAvailableParameterSet (Default)
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [<CommonParameters>]
```

### GetFeature
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String> [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.

## EXAMPLES

### Example 1: Get all available features
```
PS C:\>Get-AzureRmProviderFeature  ¢â‚¬"ListAvailable
```

This command gets all available features.

### Example 2: Get information about a specific feature
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

This command gets information for the feature named AllowPreReleaseRegions for the specified provider.

## PARAMETERS

### -ProviderNamespace
Specifies the namespace for which this cmdlet gets provider features.

```yaml
Type: String
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListAvailable
Indicates that this cmdlet gets all features.

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FeatureName
Specifies the name of the feature to get.

```yaml
Type: String
Parameter Sets: GetFeature
Aliases: 

Required: True
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

[Register-AzureRmProviderFeature](./Register-AzureRmProviderFeature.md)


