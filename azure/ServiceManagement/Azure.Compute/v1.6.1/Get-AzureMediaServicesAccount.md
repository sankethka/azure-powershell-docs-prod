---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
online version: http://go.microsoft.com/fwlink/?LinkId=324179
schema: 2.0.0
ms.assetid: D3235DBB-E211-4ABB-A370-772564BBD2D5
updated_at: 10/20/2016 12:12 AM
ms.date: 10/20/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Compute/v1.6.1/Get-AzureMediaServicesAccount.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/831f900c1a4babea8fcc8817cfbc25252a1aa872/azureps-cmdlets-docs/ServiceManagement/Azure.Compute/v1.6.1/Get-AzureMediaServicesAccount.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureMediaServicesAccount

## SYNOPSIS
Gets the available Azure Media Services accounts.

## SYNTAX

```
Get-AzureMediaServicesAccount [[-Name] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
powershell_prelim

To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.
To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.

## EXAMPLES

### Example 1: List all Media Services accounts
```
PS C:\> Get-AzureMediaServicesAccount
```

This command lists all available Media Services accounts.

### Example 2: Get detailed information about a Media Services account
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

This command displays properties of a Media Services account.

## PARAMETERS

### -Name
The Media Services account name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
In-memory profile.

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

[How to use Azure PowerShell for Media Services](http://go.microsoft.com/fwlink/?LinkId=324179)


