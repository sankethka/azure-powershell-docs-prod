---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: .\New-AzureStorageContext.md
schema: 2.0.0
ms.assetid: 4FB064F5-94BC-4D8F-9EF6-2611F8AAB99C
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/Storage/Azure.Storage/v2.2.0/New-AzureStorageFileSASToken.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/Storage/Azure.Storage/v2.2.0/New-AzureStorageFileSASToken.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# New-AzureStorageFileSASToken

## SYNOPSIS
Generates a shared access signature token for a Storage file.

## SYNTAX

### NameSasPermission
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <AzureStorageContext>] [<CommonParameters>]
```

### NameSasPolicy
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <AzureStorageContext>] [<CommonParameters>]
```

### FileSasPermission
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### FileSasPolicy
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.

## EXAMPLES

### Example 1: Generate a shared access signature token that has full file permissions
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

This command generates a shared access signature token that has full permissions for the file that is named FilePath.

### Example 2: Generate a shared access signature token that has a time limit
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

The first command creates a **DateTime** object by using the Get-Date cmdlet.
The command stores the current time in the $StartTime variable.

The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.
This object is a time two hours in the future.

The third command generates a shared access signature token that has the specified permissions.
This token becomes valid at the current time.
The token remains valid until time stored in $EndTime.

## PARAMETERS

### -ShareName
Specifies the name of the Storage share.

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Path
Specifies the path of the file relative to a Storage share.

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Policy
Specifies the stored access policy for a file.

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
@{Text=}

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
@{Text=}

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

### -StartTime
Specifies the time at which the shared access signature becomes valid.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
Specifies the time at which the shared access signature becomes invalid.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
Indicates that this cmdlet return the full blob URI and the shared access signature token.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Specifies an Azure Storage context.
To obtain a context, use the New-AzureStorageContext cmdlet.

```yaml
Type: AzureStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Permission
Specifies the permissions for a Storage file.

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -File
Specifies a **CloudFile** object.
You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-AzureStorageContext](./New-AzureStorageContext.md)

[New-AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)


