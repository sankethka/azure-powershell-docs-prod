---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
online version: .\Get-AzureRmBackupVault.md
schema: 2.0.0
updated_at: 10/14/2016 7:06 AM
ms.date: 10/14/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Backup/v2.0/CmdletMDs/Remove-AzureRmBackupVault.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/a56d0e01e65c2c33aa2af13dd29addc94ead6e88/azureps-cmdlets-docs/ResourceManager/AzureRM.Backup/v2.0/CmdletMDs/Remove-AzureRmBackupVault.md
ms.topic: reference
ms.prod: powershell
ms.service: Azure PowerShell
ms.technology: Azure PowerShell
author: visual-studio-china
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Remove-AzureRmBackupVault

## SYNOPSIS
Deletes a Backup vault.

## SYNTAX

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.

Before you can delete a Backup vault, it must be empty.
Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.
Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.

## EXAMPLES

### Example 1: Delete an Azure Backup vault
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.
The command passes that vault to the current cmdlet by using the pipeline operator.
The current cmdlet removes the vault.

## PARAMETERS

### -Vault
Specifies a Backup vault that this cmdlet removes.
To obtain an **AzureRmBackupVault**, use the Get-AzureRmBackupVault cmdlet.

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
@{Text=}

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### AzureRMBackupVault

## OUTPUTS

### None

## NOTES
* None

## RELATED LINKS

[Get-AzureRmBackupVault](.\Get-AzureRmBackupVault.md)

[New-AzureRmBackupVault](.\New-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](.\Set-AzureRmBackupVault.md)
