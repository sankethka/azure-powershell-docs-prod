---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
online version: .\Add-AutoscaleSetting.md
schema: 2.0.0
ms.assetid: 4CE1D5AA-C597-422A-A2F9-2ED896DEE307
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Insights/v0.9.8/Remove-AutoscaleSetting.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Insights/v0.9.8/Remove-AutoscaleSetting.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Remove-AutoscaleSetting

## SYNOPSIS
Removes an Autoscale setting.

## SYNTAX

```
Remove-AutoscaleSetting -ResourceGroup <String> -Name <String> [-Profile <AzureProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AutoscaleSetting** cmdlet removes an Autoscale setting.
Specifies the resource group name and the setting name of the setting that this cmdlet removes.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -ResourceGroup
Specifies the name of the resource group that contains the Autoscale setting that this cmdlet removes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the name of the setting that this cmdlet removes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AutoscaleSetting](./Add-AutoscaleSetting.md)

[Get-AutoscaleSetting](./Get-AutoscaleSetting.md)

[Get-AutoscaleHistory](./Get-AutoscaleHistory.md)


