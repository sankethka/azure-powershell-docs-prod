---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
online version: ./Get-ServiceFabricRegisteredClusterConfigVersion.md
schema: 2.0.0
ms.assetid: D1A0F338-F89D-40F0-8C1A-AF5453E61092
updated_at: 10/24/2016 10:54 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricRegisteredClusterCodeVersion.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/865a3e19e58e9be5871c4d9834591e4ba1c1b9ec/Service-Fabric-cmdlets/ServiceFabric/vlatest/Get-ServiceFabricRegisteredClusterCodeVersion.md
ms.topic: reference
ms.prod: powershell
ms.service: service-fabric
ms.technology: Azure Powershell
author: visual-studio-china
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-ServiceFabricRegisteredClusterCodeVersion

## SYNOPSIS
Gets all provisioned fabric code versions in a Service Fabric cluster.

## SYNTAX

```
Get-ServiceFabricRegisteredClusterCodeVersion [[-CodeVersion] <String>] [-TimeoutSec <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-ServiceFabricRegisteredClusterCodeVersion** cmdlet gets provisioned fabric code versions in a Service Fabric cluster.
You can specify a particular code version to get.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the Connect-ServiceFabricCluster cmdlet.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -CodeVersion
Specifies a code version.
This cmdlet gets only the provisioned fabric code versions that match the code version that this parameter specifies.

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
This cmdlet accepts the version of a Service Fabric cluster code as a string.

## OUTPUTS

### System.Object
This cmdlet returns a list of **System.Fabric.Query.ProvisionedFabricCodeVersion** objects that represent registered cluster code versions.

## NOTES

## RELATED LINKS

[Get-ServiceFabricRegisteredClusterConfigVersion](./Get-ServiceFabricRegisteredClusterConfigVersion.md)

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)


