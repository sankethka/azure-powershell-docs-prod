---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: .\Set-AzureRmVmssVM.md
schema: 2.0.0
ms.assetid: D83F7342-AA85-4AE1-A190-72BDDF6F61A2
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v2.1.0/Get-AzureRmVmssVM.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Compute/v2.1.0/Get-AzureRmVmssVM.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmVmssVM

## SYNOPSIS
Gets the properties of a VMSS virtual machine.

## SYNTAX

### InvokeByDynamicParameters (Default)
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [<CommonParameters>]
```

### InvokeByDynamicParametersForFriendMethod
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [<CommonParameters>]
```

### InvokeByStaticParametersForFriendMethod
```
Get-AzureRmVmssVM [-InstanceView] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.
The model view is the user specified properties of the virtual machine.
The instance view is the instance level status of the virtual machine.
Specify the *Status* parameter to get only the instance view of a virtual machine.

## EXAMPLES

### Example 1: Get the properties of a VMSS virtual machine
```
PS C:\>Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.
Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.

### Example 2: Get the model view properties of a VMSS virtual machine
```
PS C:\>Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.
The command gets the instance ID stored in the variable $ID for which to get the model view.

### Example 3: Get the instance view properties of a VMSS virtual machine
```
PS C:\>Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.
Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.
The command gets the instance ID stored in the variable $ID for which to get the instance view.

## PARAMETERS

### -InstanceId
Specifies the instance ID for which to get the model view.

```yaml
Type: String
Parameter Sets: InvokeByDynamicParameters, InvokeByDynamicParametersForFriendMethod
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceView
Indicates that this cmdlet gets only the instance view of the virtual machine.

```yaml
Type: SwitchParameter
Parameter Sets: InvokeByDynamicParametersForFriendMethod, InvokeByStaticParametersForFriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the Resource Group of the VMSS.

```yaml
Type: String
Parameter Sets: InvokeByDynamicParameters, InvokeByDynamicParametersForFriendMethod
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Species the name of the VMSS.

```yaml
Type: String
Parameter Sets: InvokeByDynamicParameters, InvokeByDynamicParametersForFriendMethod
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### This cmdlet does not generate any output.

## NOTES

## RELATED LINKS

[Set-AzureRmVmssVM](./Set-AzureRmVmssVM.md)

[Get-AzureRmVmss](./Get-AzureRmVmss.md)


