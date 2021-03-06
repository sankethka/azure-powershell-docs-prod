---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
online version: .\Set-AzureApplicationGatewayConfig.md
schema: 2.0.0
ms.assetid: EA9FBECA-A09F-478C-BDDE-851A937419AD
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Networking/v0.9.8/Get-AzureApplicationGatewayConfig.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Networking/v0.9.8/Get-AzureApplicationGatewayConfig.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureApplicationGatewayConfig

## SYNOPSIS
Gets application gateway configuration.

## SYNTAX

```
Get-AzureApplicationGatewayConfig [-Name] <String> [-ExportToFile <String>] [-Profile <AzureProfile>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureApplicationGatewayConfig** cmdlet gets an application gateway configuration context.
A context includes both a configuration object and XML configuration.
You can save the XML configuration to a file.

## EXAMPLES

### Example 1: Get an application gateway configuration and save it to a file
```
PS C:\>Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

This command gets the configuration for an application gateway named ApplicationGateway06.
The command saves it in the file in the specified path.

## PARAMETERS

### -Name
Specifies the name of the application gateway for which this cmdlet gets configuration information.

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

### -ExportToFile
Specifies a file path to which this cmdlet saves the configuration in XML format.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext

## NOTES

## RELATED LINKS

[Set-AzureApplicationGatewayConfig](./Set-AzureApplicationGatewayConfig.md)


