---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
online version: .\Resize-AzureRmVirtualNetworkGateway.md
schema: 2.0.0
updated_at: 10/14/2016 7:06 AM
ms.date: 10/14/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v1.0/CmdletMDs/Get-AzureRmVpnClientPackage.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/a56d0e01e65c2c33aa2af13dd29addc94ead6e88/azureps-cmdlets-docs/ResourceManager/AzureRM.Network/v1.0/CmdletMDs/Get-AzureRmVpnClientPackage.md
ms.topic: reference
ms.prod: powershell
ms.service: Azure PowerShell
ms.technology: Azure PowerShell
author: visual-studio-china
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmVpnClientPackage

## SYNOPSIS
Gets information about a VPN client package.

## SYNTAX

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.
Client packages contain configuration data that enable a client computer to make a VPN connection to an azure_2 virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.
Different configuration packages are available based on the client computer's version of Windows (for example, win7_client_secondref or winthreshold_client_2) and on the client computer's processor architecture (AMD64 or x86).
You must specify the architecture type when running **Get-AzureRmVpnClientPackage**.

## EXAMPLES

### Example 1: Get information about a processor architecture VPN client package
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.
To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.

## PARAMETERS

### -ResourceGroupName
Specifies the name of the resource group that the virtual network gateway is assigned to.

Resource groups categorize items to help simplify inventory management and general azure_2 administration.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Specifies the name of the virtual network gateway where the client package information is stored.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProcessorArchitecture
Specifies the type of CPU architecture that the client package is designed for.
Valid values are Amd64 and X86.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
@{Text=}```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@{Text=}```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

###  
**Get-AzureRmVpnClientPackage** returns instances of the System.String object.

## NOTES

## RELATED LINKS

[Resize-AzureRmVirtualNetworkGateway](.\Resize-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](.\Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)
