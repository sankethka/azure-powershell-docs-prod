---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
online version: .\Get-AzureVirtualNetwork.md
schema: 2.0.0
ms.assetid: 41C807E1-A852-40DB-983E-E89DEAD074A7
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v0.9.8/Set-AzureVirtualNetwork.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v0.9.8/Set-AzureVirtualNetwork.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Set-AzureVirtualNetwork

## SYNOPSIS
Sets the goal state for a virtual network.

## SYNTAX

```
Set-AzureVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-Profile <AzureProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -Profile
Specifies an Azure profile.

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

### -VirtualNetwork
Specifies a **VirtualNetwork** object that represents the goal state.

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureVirtualNetwork](./Get-AzureVirtualNetwork.md)

[New-AzureVirtualNetwork](./New-AzureVirtualNetwork.md)

[Remove-AzureVirtualNetwork](./Remove-AzureVirtualNetwork.md)


