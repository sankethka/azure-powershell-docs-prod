---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: .\New-AzureVM.md
schema: 2.0.0
ms.assetid: 0AAEC8E4-13E6-4D24-8026-9CB8D9E24958
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v0.9.8/Remove-AzureVM.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v0.9.8/Remove-AzureVM.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Remove-AzureVM

## SYNOPSIS
Removes an Azure virtual machine.

## SYNTAX

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureProfile>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.
This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.

## EXAMPLES

### Example 1: Remove a virtual machine from a service
```
PS C:\>Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.

### Example 2: Remove a virtual machine and delete the .vhd files
```
PS C:\>Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.

## PARAMETERS

### -Name
Specifies the name of the virtual machine being removed.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeleteVHD
Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Specifies the name of the Azure service from which the virtual machine is being removed.

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

### -Profile
Specifies the Azure profile from which this cmdlet reads.
If you do not specify a profile, this cmdlet reads from the local default profile.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)

[Restart-AzureVM](./Restart-AzureVM.md)

[Start-AzureVM](./Start-AzureVM.md)

[Stop-AzureVM](./Stop-AzureVM.md)

[Update-AzureVM](./Update-AzureVM.md)


