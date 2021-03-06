---
external help file: Microsoft.RightsManagementServices.Online.Admin.PowerShell.dll-Help.xml
online version: http://go.microsoft.com/fwlink/?LinkId=400604
schema: 2.0.0
ms.assetid: 34D77711-B96A-43E8-B5FD-8CF5013EB7E3
updated_at: 10/18/2016 11:27 PM
ms.date: 10/18/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-aip/blob/master/aip-cmdlets/AADRM/vlatest/Enable-AadrmSuperUserFeature.md
gitcommit: https://github.com/Azure/azure-docs-powershell-aip/blob/3cd0578639ed506752c7be4e6fb9013725a24d6f/aip-cmdlets/AADRM/vlatest/Enable-AadrmSuperUserFeature.md
ms.topic: reference
ms.prod: powershell
ms.service: rights-management
ms.technology: Azure Powershell
author: visual-studio-china
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Enable-AadrmSuperUserFeature

## SYNOPSIS
Enables the super user feature for Rights Management.

## SYNTAX

```
Enable-AadrmSuperUserFeature [<CommonParameters>]
```

## DESCRIPTION
The **Enable-AadrmSuperUserFeature** cmdlet enables the super user feature.
With this feature enabled, you can add or remove super users for Azure Rights Management.
By default, the super users feature is not enabled, and no users are assigned to this feature.

Super users have full control over all rights-protected content managed by Azure Rights Management.
These users are granted full owner rights for all use licenses that are issued by the subscriber organization.
Super users can decrypt any rights-protected content file and remove rights-protection from it for content previously protected within that organization, even if an expiration date has been set and expired.
Typically, this level of access is required for legal eDiscovery and by auditing teams.

Caution: We recommend that you enable the super user feature on an as-needed basis.
During standard operations, we recommend that you disable the super user feature, unless you use it to provide a trusted application with the ability to decrypt rights-protected content, such as to enable this application to scan the contents of a file for malware.

## EXAMPLES

### Example 1: Enable super user feature
```
PS C:\>Enable-AadrmSuperUserFeature
```

This command enables the super user feature for your organization.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-AadrmSuperUserFeature](.\Disable-AadrmSuperUserFeature.md)

[Get-AadrmSuperUserFeature](.\Get-AadrmSuperUserFeature.md)


