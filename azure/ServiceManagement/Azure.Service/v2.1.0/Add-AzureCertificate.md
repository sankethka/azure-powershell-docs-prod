---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: .\Get-AzureCertificate.md
schema: 2.0.0
ms.assetid: 2A35B1DA-9917-4754-9C56-EF6993DC6E9A
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v2.1.0/Add-AzureCertificate.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v2.1.0/Add-AzureCertificate.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Add-AzureCertificate

## SYNOPSIS
Uploads a certificate to an Azure cloud service.

## SYNTAX

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-AzureCertificate** cmdlet uploads a certificate for an Azure service.

## EXAMPLES

### Example 1: Upload a certificate and password
```
PS C:\>Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

This command uploads the certificate file ContosoCertificate.pfx to a cloud service.
The command specifies the password for the certificate.

### Example 2: Upload a certificate file
```
PS C:\>Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

This command uploads the certificate file ContosoCertificate.cer to a cloud service.
The command specifies the password for the certificate.

### Example 3: Upload a certificate object
```
PS C:\>$Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

The first command gets a certificate from the MY store of a user by using the Windows PowerShell core Get-Item cmdlet.
The command stores the certificate in the $Certificate variable.

The second command uploads the certificate in $certificate to a cloud service.

## PARAMETERS

### -ServiceName
Specifies the name of the Azure service to which this cmdlet adds a certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertToDeploy
Specifies the certificate to deploy.
You can specify the full path of a certificate file, such as a file that has a *.cer or *.
pfx file name extension, or an X.509 Certificate object.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password
Specifies the certificate password.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### -InformationAction
@{Text=}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

### ManagementOperationContext

## NOTES

## RELATED LINKS

[Get-AzureCertificate](./Get-AzureCertificate.md)

[New-AzureCertificateSetting](./New-AzureCertificateSetting.md)

[Remove-AzureCertificate](./Remove-AzureCertificate.md)


