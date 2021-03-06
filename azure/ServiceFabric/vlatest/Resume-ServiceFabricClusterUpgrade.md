---
external help file: Microsoft.ServiceFabric.Powershell.dll-Help.xml
online version: ./Connect-ServiceFabricCluster.md
schema: 2.0.0
ms.assetid: 25F1C2E1-5AB4-42AF-AD53-4AAA1EBE8B4B
updated_at: 10/24/2016 10:54 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/master/Service-Fabric-cmdlets/ServiceFabric/vlatest/Resume-ServiceFabricClusterUpgrade.md
gitcommit: https://github.com/Azure/azure-docs-powershell-servicefabric/blob/865a3e19e58e9be5871c4d9834591e4ba1c1b9ec/Service-Fabric-cmdlets/ServiceFabric/vlatest/Resume-ServiceFabricClusterUpgrade.md
ms.topic: reference
ms.prod: powershell
ms.service: service-fabric
ms.technology: Azure Powershell
author: visual-studio-china
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Resume-ServiceFabricClusterUpgrade

## SYNOPSIS
Resumes an unmonitored Service Fabric cluster upgrade.

## SYNTAX

```
Resume-ServiceFabricClusterUpgrade [-UpgradeDomainName] <String> [-TimeoutSec <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Resume-ServiceFabricClusterUpgrade** cmdlet resumes an unmonitored manual Service Fabric cluster upgrade.
Service Fabric upgrades one upgrade domain at a time.
For unmonitored manual upgrades, after Service Fabric finishes an upgrade domain, it waits for you to run this cmdlet to proceed to the next upgrade domain.

Before you perform any operation on a Service Fabric cluster, establish a connection to the cluster by using the Connect-ServiceFabricCluster cmdlet and then the Get-ServiceFabricClusterConnection cmdlet.

## EXAMPLES

### Example 1: Resume an upgrade
```
PS C:\>Resume-ServiceFabricClusterUpgrade -UpgradeDomainName "MYUD02"
```

This command resumes the upgrade process after it finishes an upgrade domain.
The command specifies MYUD02 as the next upgrade domain.

## PARAMETERS

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

### -UpgradeDomainName
Specifies the name of the next upgrade domain to upgrade.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
You cannot pipe input to this cmdlet.

## OUTPUTS

### System.Object
This cmdlet returns the status of the operation as a string.

## NOTES

## RELATED LINKS

[Connect-ServiceFabricCluster](./Connect-ServiceFabricCluster.md)

[Get-ServiceFabricClusterConnection](./Get-ServiceFabricClusterConnection.md)

[Get-ServiceFabricClusterUpgrade](./Get-ServiceFabricClusterUpgrade.md)

[Start-ServiceFabricClusterUpgrade](./Start-ServiceFabricClusterUpgrade.md)


