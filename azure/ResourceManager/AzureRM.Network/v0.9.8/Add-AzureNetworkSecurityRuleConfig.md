---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
online version: .\Get-AzureNetworkSecurityRuleConfig.md
schema: 2.0.0
ms.assetid: D9F468BC-12F4-4A9A-9B1D-1C1D1A9068F5
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v0.9.8/Add-AzureNetworkSecurityRuleConfig.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v0.9.8/Add-AzureNetworkSecurityRuleConfig.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Add-AzureNetworkSecurityRuleConfig

## SYNOPSIS
Adds a network security rule configuration to a network security group.

## SYNTAX

```
Add-AzureNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String>] [-DestinationPortRange <String>]
 [-SourceAddressPrefix <String>] [-DestinationAddressPrefix <String>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-Profile <AzureProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Add-AzureNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -Access
Specifies whether network traffic is allowed or denied.
The acceptable values for this parameter are:Allow and Deny.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description of a network security rule configuration.

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

### -DestinationAddressPrefix
Specifies a destination address prefix.
The acceptable values for this parameter are:

- A Classless Interdomain Routing (CIDR) address 
- A destination IP address range 
- A wildcard character (*) to match any IP address

You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.

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

### -DestinationPortRange
Specifies a destination port or range.
The acceptable values for this parameter are:

- An integer 
- A range of integers between 0 and 65535
- A wildcard character (*) to match any port

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

### -Direction
Specifies whether a rule is evaluated on incoming or outgoing traffic.
The acceptable values for this parameter are:Inbound and Outbound.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a network security rule configuration.

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

### -NetworkSecurityGroup
Specifies a **NetworkSecurityGroup** object.
This cmdlet adds a network security rule configuration to the object that this parameter specifies.

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Priority
Specifies the priority of a rule configuration.
The acceptable values for this parameter are:An integer between 100 and 4096.

The priority number must be unique for each rule in the collection.
The lower the priority number, the higher the priority of the rule.

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

### -Protocol
Specifies the network protocol that a rule configuration applies to.
The acceptable values for this parameter are:

- Tcp
- Udp
- Wildcard character (*) to match both

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
Specifies a source address prefix.
The acceptable values for this parameter are:

- A CIDR
- A source IP range
- A wildcard character (*) to match any IP address.

You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.

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

### -SourcePortRange
Specifies a source port or range.
This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (*) to match any source port.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureNetworkSecurityRuleConfig](./Get-AzureNetworkSecurityRuleConfig.md)

[New-AzureNetworkSecurityRuleConfig](./New-AzureNetworkSecurityRuleConfig.md)

[Remove-AzureNetworkSecurityRuleConfig](./Remove-AzureNetworkSecurityRuleConfig.md)

[Set-AzureNetworkSecurityRuleConfig](./Set-AzureNetworkSecurityRuleConfig.md)


