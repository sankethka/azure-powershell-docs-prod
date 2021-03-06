---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
online version: ea9fbeca-a09f-478c-bdde-851a937419ad
schema: 2.0.0
ms.assetid: 893F28DF-70AB-4AA5-8E87-AE1CD921A9CA
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Networking/v3.0.0/Set-AzureApplicationGatewayConfig.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Networking/v3.0.0/Set-AzureApplicationGatewayConfig.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Set-AzureApplicationGatewayConfig

## SYNOPSIS
Configures an application gateway.

## SYNTAX

### configFile
```
Set-AzureApplicationGatewayConfig -Name <String> [-ConfigFile] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### configObject
```
Set-AzureApplicationGatewayConfig -Name <String> [-Config] <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.

## EXAMPLES

### Example 1: Configure an application gateway by using a configuration object
```
PS C:\>$ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the Get-AzureApplicationGatewayConfig cmdlet.
The command stores it in the $ConfigReturnObject variable.

The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.

### Example 2: Configure an application gateway by using a configuration file
```
PS C:\>Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.

### Example 3: Modify a configuration by using a configuration object
```
PS C:\>$ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the Get-AzureApplicationGatewayConfig cmdlet.
The command stores it in the $ConfigReturnObject variable.

The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.

The final command passes the updated $ConfigReturnObject to the current cmdlet.

## PARAMETERS

### -Name
Specifies the name of the application gateway that this cmdlet configures.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Specifies an application gateway configuration object.
This cmdlet assigns the configuration that this parameter specifies to an application gateway.

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigFile
Specifies the path of a configuration file, in XML format, for an application gateway.
This cmdlet assigns the configuration that this parameter specifies to an application gateway.

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
ps_azureprofile_description

```yaml
Type: AzureSMProfile
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

### System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration

## OUTPUTS

### Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse

## NOTES

## RELATED LINKS

[Get-AzureApplicationGatewayConfig](./Get-AzureApplicationGatewayConfig.md)


