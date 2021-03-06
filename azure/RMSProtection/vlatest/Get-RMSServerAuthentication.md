---
external help file: RMSProtection.dll-Help.xml
online version: http://go.microsoft.com/fwlink/?LinkID=623204
schema: 2.0.0
ms.assetid: 015252D1-EF22-4060-84E5-619C8C66CEDF
updated_at: 10/18/2016 11:27 PM
ms.date: 10/18/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-aip/blob/master/aip-cmdlets/RMSProtection/vlatest/Get-RMSServerAuthentication.md
gitcommit: https://github.com/Azure/azure-docs-powershell-aip/blob/3cd0578639ed506752c7be4e6fb9013725a24d6f/aip-cmdlets/RMSProtection/vlatest/Get-RMSServerAuthentication.md
ms.topic: reference
ms.prod: powershell
ms.service: rights-management
ms.technology: Azure Powershell
author: visual-studio-china
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-RMSServerAuthentication

## SYNOPSIS
Gets the status of your service principal authentication to Azure RMS.

## SYNTAX

```
Get-RMSServerAuthentication [<CommonParameters>]
```

## DESCRIPTION
The **Get-RMSServerAuthentication** cmdlet gets the status and details of your service principal authentication to Azure Rights Management (Azure  RMS) that was previous set by using Set-RMSServerAuthentication.
The status must be ON for you to protect or unprotect files for Azure RMS by using a service principal rather than your user account.
This status remains on for the duration of your Windows PowerShell session.

This cmdlet applies to Azure  RMS only and does not apply to AD RMS.
This cmdlet also does not apply if you are authenticating to Azure RMS by using your user account.
For more information, see about_RMSProtection_AzureRMS.

## EXAMPLES

### Example 1: Get the status of your service principal authentication to Azure RMS
```
PS C:\>Get-RMSServerAuthentication
The RmsServerAuthentication is ON

Base64Key                               AppPrincipalId                          BposTenantId
---------                               --------------                          ------------
zIeMu8zNJ6U377CLtppkhkbl4gjodmYSXUVwAO5ycgA=                         b5e3f76a-b5c2-4c96-a594-a0807f65bba4                                23976bc6-dcd4-4173-9d96-dad1f48efd42
```

This command gets the status of the service principal authentication and outputs the currently used identifiers, if authentication is successful.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-RMSServerAuthentication](.\Set-RMSServerAuthentication.md)


