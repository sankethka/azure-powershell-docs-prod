---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: 79bf6173-959c-45ac-b006-07d0d389c321
schema: 2.0.0
ms.assetid: 14506C8E-2707-4C3F-9D65-312C63A3E0CB
updated_at: 10/18/2016 9:38 PM
ms.date: 10/18/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Profile/v2.1.0/Get-AzureRmTenant.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/23cdb8705d4ab9807c0e21b238f3b134a7d49c7d/azureps-cmdlets-docs/ResourceManager/AzureRM.Profile/v2.1.0/Get-AzureRmTenant.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmTenant

## SYNOPSIS
Gets tenants that are authorized for the current user.

## SYNTAX

```
Get-AzureRmTenant [-TenantId <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmTenant** cmdlet gets tenants that are authorized for the current user.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -TenantId
Specifies the ID of the tenant that this cmdlet gets.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

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

###  
This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.

## NOTES

## RELATED LINKS


