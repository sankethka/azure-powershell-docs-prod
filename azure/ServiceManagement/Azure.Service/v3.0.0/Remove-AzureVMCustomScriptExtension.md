---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 7cd94e7e-dd05-4050-ac3c-16915ef6a0b3
schema: 2.0.0
ms.assetid: 75BE7685-8632-449C-B5B1-E4BF4DC7E341
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v3.0.0/Remove-AzureVMCustomScriptExtension.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v3.0.0/Remove-AzureVMCustomScriptExtension.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Remove-AzureVMCustomScriptExtension

## SYNOPSIS
Removes the custom script extension from a virtual machine.

## SYNTAX

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureVMCustomScriptExtension** cmdlet removes the custom script extension from a virtual machine.

## EXAMPLES

### Example 1: Remove a virtual machine custom script extension
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

This command removes the Azure virtual machine custom script extension from the specified virtual machine as stored in the variable $VM.

## PARAMETERS

### -VM
Specifies the persistent virtual machine object.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

[Get-AzureVMCustomScriptExtension](./Get-AzureVMCustomScriptExtension.md)

[Set-AzureVMCustomScriptExtension](./Set-AzureVMCustomScriptExtension.md)


