---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
online version: 49a6efcc-b273-40c0-ad5b-9ef9689f9ae9
schema: 2.0.0
ms.assetid: 67276B0C-B5DB-4C5F-8959-F88462B72499
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Storage/v2.2.0/New-AzureRmStorageAccountKey.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Storage/v2.2.0/New-AzureRmStorageAccountKey.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# New-AzureRmStorageAccountKey

## SYNOPSIS
Regenerates a storage key for an Azure Storage account.

## SYNTAX

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.

## EXAMPLES

### Example 1: Regenerate a storage key
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

This command regenerates a storage key for the specified Storage account.

## PARAMETERS

### -ResourceGroupName
Specifies the name of the resource group that contains the Storage account.

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

### -Name
Specifies the name of the Storage account for which to regenerate a storage key.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyName
Specifies which key to regenerate.
The acceptable values for this parameter are:

- key1 
- key2

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureRmStorageAccountKey](./Get-AzureRmStorageAccountKey.md)


