---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
online version: 0b6f9e76-995e-4403-8f3f-80c67a698561
schema: 2.0.0
ms.assetid: 76E4B00C-2A3A-4D84-92D2-875181DE1662
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Backup/v2.2.0/Get-AzureRmBackupProtectionPolicy.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Backup/v2.2.0/Get-AzureRmBackupProtectionPolicy.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmBackupProtectionPolicy

## SYNOPSIS
Gets backup policies for a Backup vault.

## SYNTAX

```
Get-AzureRmBackupProtectionPolicy [[-Name] <String>] [-Vault] <AzureRMBackupVault> [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmBackupProtectionPolicy** cmdlet gets backup policies for an Azure Backup vault.

## EXAMPLES

### Example 1: View the policies in a vault
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault 
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
contoso01                 AzureVM            Daily              26-Aug-15 3:00:00 PM
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
WeeklyBkp                 AzureVM            Weekly             26-Aug-15 5:00:00 PM
contoso02                 AzureVM            Daily              26-Aug-15 3:00:00 PM
```

The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.
The command stores that object in the $Vault variable.

The second command gets all the Backup protection policies for the vault in $Vault.

### Example 2: Get a specific policy from a vault
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
```

The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.
The command stores that object in the $Vault variable.

The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.

## PARAMETERS

### -Name
Specifies the name of the policy that this cmdlet gets.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Specifies the Backup vault for which this cmdlet gets policies.
To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### AzureRmBackupVault

## OUTPUTS

### AzureRmBackupProtectionPolicy

## NOTES
* None

## RELATED LINKS

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[New-AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)

[Remove-AzureRmBackupProtectionPolicy](./Remove-AzureRmBackupProtectionPolicy.md)


