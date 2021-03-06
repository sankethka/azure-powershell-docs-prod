---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
online version: e01b6a99-bcaf-4b73-9a28-f6cd56389d4a
schema: 2.0.0
ms.assetid: ABC26AB8-D8A7-42B9-8540-E8DA91D8092B
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v3.0.0/Set-AzureRmNetworkInterface.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v3.0.0/Set-AzureRmNetworkInterface.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Set-AzureRmNetworkInterface

## SYNOPSIS
Sets the goal state for a network interface.

## SYNTAX

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureRmNetworkInterface** sets the goal state for an Azure network interface.

## EXAMPLES

### Example 1: Configure a network interface
```
PS C:\>$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
PS C:\> $Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
PS C:\> $Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
PS C:\> $Nic.Tag = @{Name = "Name"; Value = "Value"}
PS C:\> Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

This example configures a network interface.
The first command creates a network interface named NetworkInterface1 in resource group ResourceGroup1.

The second command sets the private IP address of the IP configuration.

The third command sets the private IP allocation method to Static.

The fourth command sets a tag on the network interface.

The fifth command uses the information stored in the $Nic variable to set the network interface.

## PARAMETERS

### -NetworkInterface
Specifies a **NetworkInterface** object that represents the goal state for a network interface.

```yaml
Type: PSNetworkInterface
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

[Get-AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[Get-AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[New-AzureRmNetworkInterface](./New-AzureRmNetworkInterface.md)

[Remove-AzureRmNetworkInterface](./Remove-AzureRmNetworkInterface.md)


