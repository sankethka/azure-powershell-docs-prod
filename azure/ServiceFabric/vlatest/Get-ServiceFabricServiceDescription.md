---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
online version: ./Get-ServiceFabricService.md
schema: 2.0.0
ms.assetid: A7669F75-A5B3-4574-8444-CD15A04DF0EE
updated_at: 10/24/2016 10:54 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceDescription.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/865a3e19e58e9be5871c4d9834591e4ba1c1b9ec/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricServiceDescription.md
ms.topic: reference
ms.prod: powershell
ms.service: service-fabric
ms.technology: Azure Powershell
author: visual-studio-china
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-ServiceFabricServiceDescription

## SYNOPSIS
Gets the Service Fabric service description of a service that is running.

## SYNTAX

```
Get-ServiceFabricServiceDescription [-ServiceName] <Uri> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricServiceDescription** cmdlet gets the Service Fabric service description of a service that is running.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the Connect-ServiceFabricCluster cmdlet.

## EXAMPLES

### Example 1: Get a service description
```
PS C:\>Get-ServiceFabricServiceDescription -ServiceName fabric:/CalcApp/CalcService
```

The command gets Service Fabric service description for service named fabric:/CalcApp/CalcService.

## PARAMETERS

### -ServiceName
Specifies the Uniform Resource Identifier (URI) of a Service Fabric service.
This cmdlet gets the service description for the service that you specify.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeoutSec
Specifies the time-out period, in seconds, for the operation.

```yaml
Type: Int32
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

### System.Uri
This cmdlet accepts a URI that represents the name of a Service Fabric service.

## OUTPUTS

### System.Object
This cmdlet returns **System.Fabric.Description.ServiceDescription** object for a Service Fabric service.

## NOTES

## RELATED LINKS

[Get-ServiceFabricService](./Get-ServiceFabricService.md)

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)


