---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
online version: .\Get-AzureNetworkSecurityGroupForSubnet.md
schema: 2.0.0
ms.assetid: 66AD8A8A-1097-4806-89E0-B31F6CC71C82
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Networking/v2.1.0/Remove-AzureNetworkSecurityGroupFromSubnet.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Networking/v2.1.0/Remove-AzureNetworkSecurityGroupFromSubnet.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Remove-AzureNetworkSecurityGroupFromSubnet

## SYNOPSIS
Dissociates a network security group from a subnet.

## SYNTAX

```
Remove-AzureNetworkSecurityGroupFromSubnet [-Name] <String> [-VirtualNetworkName] <String>
 [-SubnetName] <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -Name
Specifies the name of the network security group that this cmdlet dissociates from a subnet.

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

### -VirtualNetworkName
Specifies the name of a virtual network.
This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Specifies the name of a subnet from which this cmdlet dissociates a network security group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

```yaml
Type: SwitchParameter
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

## NOTES

## RELATED LINKS

[Get-AzureNetworkSecurityGroupForSubnet](./Get-AzureNetworkSecurityGroupForSubnet.md)

[Set-AzureNetworkSecurityGroupToSubnet](./Set-AzureNetworkSecurityGroupToSubnet.md)


