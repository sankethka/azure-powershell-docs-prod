---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
online version: .\Stop-AzureApplicationGateway.md
schema: 2.0.0
ms.assetid: 9257F010-9013-4837-B648-A9053D6576A8
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v0.9.8/Start-AzureApplicationGateway.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v0.9.8/Start-AzureApplicationGateway.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Start-AzureApplicationGateway

## SYNOPSIS
Starts an application gateway.

## SYNTAX

```
Start-AzureApplicationGateway -ApplicationGateway <PSApplicationGateway> [-Profile <AzureProfile>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Start-AzureApplicationGateway** cmdlet starts an Azure application gateway

## EXAMPLES

### Example1: Start an application gateway
```
PS C:\> $ AppGw = Start-AzureApplicationGateway -ApplicationGateway $AppGw
```

This command starts the application gateway stored in the $AppGw variable.

## PARAMETERS

### -ApplicationGateway
Specifies the application gateway to start.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### System.String

## OUTPUTS

## NOTES

## RELATED LINKS

[Stop-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)


