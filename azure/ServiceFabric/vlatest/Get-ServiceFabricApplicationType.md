---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
online version: ./Connect-ServiceFabricCluster.md
schema: 2.0.0
ms.assetid: 377D093A-8D81-4CDA-842B-EF8A9FF2585C
updated_at: 10/24/2016 10:54 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricApplicationType.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/865a3e19e58e9be5871c4d9834591e4ba1c1b9ec/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricApplicationType.md
ms.topic: reference
ms.prod: powershell
ms.service: service-fabric
ms.technology: Azure Powershell
author: visual-studio-china
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-ServiceFabricApplicationType

## SYNOPSIS
Gets the Service Fabric application types registered on the Service Fabric cluster.

## SYNTAX

```
Get-ServiceFabricApplicationType [[-ApplicationTypeName] <String>] [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricApplicationType** cmdlet gets the Service Fabric application types registered on the Service Fabric cluster.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the Connect-ServiceFabricCluster cmdlet.

## EXAMPLES

### Example 1: Get application types
```
PS C:\>Get-ServiceFabricApplicationType
```

This command gets all registered application types.

### Example 2: Get application type with specified type names
```
PS C:\>Get-ServiceFabricApplicationType -ApplicationTypeName "TestApp"
```

This command gets the  registered application type named TestApp.

## PARAMETERS

### -ApplicationTypeName
Specifies the name of a Service Fabric application type.
The cmdlet gets the application type that you specify.
If you do not specify this parameter, this cmdlet gets all application types.

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

### String
This cmdlet accepts a string that represents the application type name filter.

## OUTPUTS

### System.Object
This cmdlet returns **System.Fabric.Query.ApplicationType** objects that represent the Service Fabric application types.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Register-ServiceFabricApplicationType](./Register-ServiceFabricApplicationType.md)

[Unregister-ServiceFabricApplicationType](./Unregister-ServiceFabricApplicationType.md)


