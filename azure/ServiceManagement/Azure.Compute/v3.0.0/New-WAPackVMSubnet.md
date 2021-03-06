---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
online version: a81b12ab-3de2-4e0d-872e-cea5c12f9ed4
schema: 2.0.0
ms.assetid: 661DC1FD-294C-4953-8393-82B9B8DCF857
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Compute/v3.0.0/New-WAPackVMSubnet.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Compute/v3.0.0/New-WAPackVMSubnet.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# New-WAPackVMSubnet

## SYNOPSIS
Creates a virtual machine subnet.

## SYNTAX

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.

## EXAMPLES

### Example 1: Create a virtual machine subnet
```
PS C:\>$VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\>New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.
This virtual machine network is named ContosoVNet01.
The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.

## PARAMETERS

### -VNet
Specifies a VNet associated with the virtual machine subnet.

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name for the virtual machine subnet.

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

### -Subnet
Specifies a subnet for the virtual machine subnet.

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

[Get-WAPackVMSubnet](./Get-WAPackVMSubnet.md)

[Get-WAPackVNet](./Get-WAPackVNet.md)

[Remove-WAPackVMSubnet](./Remove-WAPackVMSubnet.md)


