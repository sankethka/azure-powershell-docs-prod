---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
online version: .\Get-AzureRemoteAppTemplateImage.md
schema: 2.0.0
ms.assetid: 654C490B-1C87-4920-B525-C12DB1152AB1
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.RemoteApp/v0.9.8/Rename-AzureRemoteAppTemplateImage.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.RemoteApp/v0.9.8/Rename-AzureRemoteAppTemplateImage.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Rename-AzureRemoteAppTemplateImage

## SYNOPSIS
Renames a RemoteApp template image.

## SYNTAX

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureProfile>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Rename-AzureRemoteAppTemplate** cmdlet renames an Azure RemoteApp template image.

## EXAMPLES

### Example 1: Rename a RemoteApp template image
```
PS C:\>Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

This command renames the RemoteApp template image named ContosoApps to ContosoFinanceApps.

## PARAMETERS

### -ImageName
Specifies the name of a RemoteApp template image to rename.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NewName
Specifies a new name for a RemoteApp template image.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureRemoteAppTemplateImage](./Get-AzureRemoteAppTemplateImage.md)

[New-AzureRemoteAppTemplateImage](./New-AzureRemoteAppTemplateImage.md)

[Remove-AzureRemoteAppTemplateImage](./Remove-AzureRemoteAppTemplateImage.md)


