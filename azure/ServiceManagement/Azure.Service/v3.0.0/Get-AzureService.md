---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 024358c8-a520-4886-a7d6-73636c4fb073
schema: 2.0.0
ms.assetid: 897DAE20-FB00-4C04-A1BB-06723119B19A
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v3.0.0/Get-AzureService.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v3.0.0/Get-AzureService.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureService

## SYNOPSIS
Returns an object with information about the cloud services for the current subscription.

## SYNTAX

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.
If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.

## EXAMPLES

### Example 1: Get information about all services
```
PS C:\>Get-AzureService
```

This command returns an object that contains information about all of the Azure services associated with the current subscription.

### Example 2: Get information about a specified service
```
PS C:\>Get-AzureService -ServiceName $MySvc
```

This command returns information about the $MySvc service.

### Example 3: Display available methods and properties
```
PS C:\>Get-AzureService | Get-Member
```

This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.

## PARAMETERS

### -ServiceName
Specifies the name of a service on which to return information.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifies the Azure profile from which this cmdlet reads.
If you do not specify a profile, this cmdlet reads from the local default profile.

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

## OUTPUTS

### HostedServiceContext

## NOTES

## RELATED LINKS

[New-AzureService](./New-AzureService.md)

[Set-AzureService](./Set-AzureService.md)


