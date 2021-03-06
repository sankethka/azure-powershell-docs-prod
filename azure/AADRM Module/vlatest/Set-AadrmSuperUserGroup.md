---
external help file: Microsoft.RightsManagementServices.Online.Admin.PowerShell.dll-Help.xml
online version: http://go.microsoft.com/fwlink/?LinkId=722838
schema: 2.0.0
ms.assetid: 23E946A0-E6FC-4F8C-8F3B-352AD48CE426
updated_at: 10/24/2016 10:52 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-aip/blob/master/Azure%20Information%20Protection/AADRM%20Module/vlatest/Set-AadrmSuperUserGroup.md
gitcommit: https://github.com/Azure/azure-docs-powershell-aip/blob/5e6ef5e3f1d6768f64c5d14aab4fd3e58b8fa0c3/Azure%20Information%20Protection/AADRM%20Module/vlatest/Set-AadrmSuperUserGroup.md
ms.topic: reference
ms.prod: powershell
ms.service: rights-management
ms.technology: Azure Powershell
author: visual-studio-china
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Set-AadrmSuperUserGroup

## SYNOPSIS
Sets the super user group for Rights Management.

## SYNTAX

```
Set-AadrmSuperUserGroup -GroupEmailAddress <String> [<CommonParameters>]
```

## DESCRIPTION
The **Set-AadrmSuperUserGroup** cmdlet sets the super user group for your organization in Azure Rights Management.
If a super user group already exists, this operation overwrites it.
This cmdlet does not affect users that are individually assigned as super users with the Add-AadrmSuperUser cmdlet.

An organization can have only one super user group in addition to multiple users who are assigned the privilege individually, but you can nest groups.

For more information about super users, see Configuring super users for Azure Rights Management and discovery services or data recoveryhttps://docs.microsoft.com/rights-management/deploy-use/configure-super-users (https://docs.microsoft.com/rights-management/deploy-use/configure-super-users) on the Microsoft documentation site.

## EXAMPLES

### Example 1: Set the super user group
```
PS C:\>Set-AadrmSuperUserGroup -GroupEmailAddress "SuperUserGroup@contoso.com"
```

This command sets the super user group for the organization to SuperUserGroup@contoso.com.

## PARAMETERS

### -GroupEmailAddress
Specifies the group email address for the super user group.
*GroupEmailAddress* can specify a group that contains individual users or other nested groups.

The *GroupEmailAddress* must be a valid group email address in the organization.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-AadrmSuperUser](./Add-AadrmSuperUser.md)

[Clear-AadrmSuperUserGroup](./Clear-AadrmSuperUserGroup.md)

[Get-AadrmSuperUserGroup](./Get-AadrmSuperUserGroup.md)


