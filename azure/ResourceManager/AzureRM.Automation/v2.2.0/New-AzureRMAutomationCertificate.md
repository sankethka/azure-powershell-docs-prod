---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
online version: 7e2d3105-ae14-40c6-a715-57d63c178cde
schema: 2.0.0
ms.assetid: 4316D596-2954-42E8-905F-840853DAB7D5
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Automation/v2.2.0/New-AzureRMAutomationCertificate.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Automation/v2.2.0/New-AzureRMAutomationCertificate.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
---

# New-AzureRmAutomationCertificate

## SYNOPSIS
Creates an Automation certificate.

## SYNTAX

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in azure_2 Automation.
Provide the path to a certificate file to upload.

## EXAMPLES

### Example 1: Create a new certificate
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.
The command stores that object in the $Password variable.

The second command creates a certificate named ContosoCertificate.
The command uses the password stored in $Password.
The command specifies the account name and the path of the file that it uploads.

## PARAMETERS

### -AutomationAccountName
Specifies the name of the Automation account for which this cmdlet stores the certificate.

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

### -Description
Specifies a description for the certificate.

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

### -Exportable
Specifies whether the certificate can be exported.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the name for the certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Password
Specifies the password for the certificate file.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Specifies the path to a script file that this cmdlet uploads.
The file can be a .cer or a .pfx file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the resource group for which this cmdlet creates a certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Azure.Commands.Automation.Model.CertificateInfo

## NOTES

## RELATED LINKS

[Get-AzureRmAutomationCertificate](./Get-AzureRMAutomationCertificate.md)

[Remove-AzureRmAutomationCertificate](./Remove-AzureRMAutomationCertificate.md)

[Set-AzureRmAutomationCertificate](./Set-AzureRMAutomationCertificate.md)


