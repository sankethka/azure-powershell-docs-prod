---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: .\Get-AzureBatchAccountKeys.md
schema: 2.0.0
ms.assetid: B3B1DBB5-6F6C-4B37-A113-AB819C7536D5
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Batch/v0.9.8/New-AzureBatchAccountKey.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Batch/v0.9.8/New-AzureBatchAccountKey.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# New-AzureBatchAccountKey

## SYNOPSIS
Regenerates the specified key of the specified Batch account.

## SYNTAX

```
New-AzureBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-Profile <AzureProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureBatchAccountKey** cmdlet regenerates the specified key of the specified Azure Batch account.
The cmdlet outputs a **BatchAccountContext** object with its **PrimaryAccountKey** and **SecondaryAccountKey** properties populated with the latest access keys.

## EXAMPLES

### Example 1: Regenerate the primary account key on a named batch account
```
PS C:\>New-AzureBatchAccountKey -AccountName "CmdletExample" -KeyType "Primary"
AccountName          Location        ResourceGroupName Tags               TaskTenantUrl
-----------          --------        ----------------- ----               -------------
cmdletexample        westus          CmdletExample                        https://batch.core.contoso.net
```

This command regenerates the primary account key on the Batch account named CmdletExample.

## PARAMETERS

### -AccountName
Specifies the name of the Batch account to regenerate the specified key.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyType
Specifies the type of key to regenerate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

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
Type: AzureProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the resource group of the account.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### BatchAccountContext

## NOTES

## RELATED LINKS

[Get-AzureBatchAccountKeys](./Get-AzureBatchAccountKeys.md)

[Azure Batch Cmdlets](./AzureRM.Batch.md)


