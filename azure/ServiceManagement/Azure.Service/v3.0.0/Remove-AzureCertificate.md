---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 2a35b1da-9917-4754-9c56-ef6993dc6e9a
schema: 2.0.0
ms.assetid: 7486FC67-E9FF-4239-B10B-1BC0225C942D
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v3.0.0/Remove-AzureCertificate.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v3.0.0/Remove-AzureCertificate.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Remove-AzureCertificate

## SYNOPSIS
Removes a certificate from an Azure service.

## SYNTAX

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.

## EXAMPLES

### Example 1: Remove a certificate from a service
```
PS C:\>Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

This command removes the certificate object that has the specified thumbprint from the cloud service.

### Example 2: Remove all certificates from a service
```
PS C:\>Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

This command gets all the certificates from the service named ContosoService by using the Get-AzureCertificate cmdlet.
The command passes each certificate to the current cmdlet by using the pipeline operator.
That cmdlet removes each certificate from the cloud service.

### Example 3: Remove all certificates from a service that use a specific thumbprint algorithm
```
PS C:\>Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.
The command passes each certificate to the current cmdlet, which removes each certificate.

## PARAMETERS

### -ServiceName
Specifies the name of the Azure service from which this cmdlet removes a certificate.

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

### -ThumbprintAlgorithm
Specifies the algorithm that is used to create the certificate thumbprint.

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

### -Thumbprint
Specifies the thumbprint of the certificate that this cmdlet removes.

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

### ManagementOperationContext

## NOTES

## RELATED LINKS

[Add-AzureCertificate](./Add-AzureCertificate.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[New-AzureCertificateSetting](./New-AzureCertificateSetting.md)


