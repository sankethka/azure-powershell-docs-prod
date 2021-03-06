---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
online version: 8228cc98-3c2c-4392-825f-d91ba8136672
schema: 2.0.0
ms.assetid: 5E93CD6F-3D69-4443-BA94-E34D00F59C5B
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.RemoteApp/v3.0.0/Get-AzureRemoteAppVmStaleAdObject.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.RemoteApp/v3.0.0/Get-AzureRemoteAppVmStaleAdObject.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRemoteAppVmStaleAdObject

## SYNOPSIS
Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.

## SYNTAX

```
Get-AzureRemoteAppVmStaleAdObject [-CollectionName] <String> [[-Credential] <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.
This cmdlet displays the name of each object that it gets.

## EXAMPLES

### Example 1: Get stale objects for a collection
```
PS C:\>Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

This second command gets the stale objects for the collection named Contoso.

## PARAMETERS

### -CollectionName
Specifies the name of the Azure RemoteApp collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
Specifies a credential that has rights to perform this action.
To obtain a **Credential** object, use the Get-Credential cmdlet.
If you do not specify this parameter, this cmdlet uses the current user credentials.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
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

### String

## NOTES

## RELATED LINKS

[Clear-AzureRemoteAppVmStaleAdObject](./Clear-AzureRemoteAppVmStaleAdObject.md)


