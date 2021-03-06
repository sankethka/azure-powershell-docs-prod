---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
online version: .\New-AzureRemoteAppCollection.md
schema: 2.0.0
ms.assetid: C9EE0B8C-96EB-4F1A-84CF-5F7056167AEB
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.RemoteApp/v1.6.1/Get-AzureRemoteAppCollection.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.RemoteApp/v1.6.1/Get-AzureRemoteAppCollection.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRemoteAppCollection

## SYNOPSIS
Retrieves information about an azure_2 RemoteApp collection.

## SYNTAX

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRemoteAppCollection** cmdlet retrieves information about azure_2 RemoteApp collections in Microsoft Azure.
It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.

## EXAMPLES

### Example 1: Get a list of all collections
```
PS C:\>Get-AzureRemoteAppCollection
```

This command returns a list of all azure_2 RemoteApp collections in the subscription.

### Example 2: Get information about a specified collection
```
PS C:\>Get-AzureRemoteAppCollection ContosoApps
```

This command returns information about the azure_2 RemoteApp collection named ContosoApps.

### Example 3: Get a list of collections by using a wildcard
```
PS C:\>Get-AzureRemoteAppCollection Finance*
```

This command returns a list of all azure_2 RemoteApp collections matching Finance*.

## PARAMETERS

### -CollectionName
Specifies the name of the azure_2 RemoteApp collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -Profile
ps_azureprofile_description

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

[New-AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


