---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: .\Get-AzureStorageCORSRule.md
schema: 2.0.0
ms.assetid: FD109B34-042A-4157-B0C1-2CBF29894B52
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/Storage/Azure.Storage/v2.2.0/Set-AzureStorageCORSRule.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/Storage/Azure.Storage/v2.2.0/Set-AzureStorageCORSRule.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Set-AzureStorageCORSRule

## SYNOPSIS
Sets the CORS rules for a type of Storage service.

## SYNTAX

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <AzureStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.
The types of storage services for this cmdlet are Blob, Table, Queue, and File.
This cmdlet overwrites the existing rules.
To see the current rules, use the Get-AzureStorageCORSRule cmdlet.

## EXAMPLES

### Example 1: Assign CORS rules to the blob service
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

The first command assigns an array of rules to the $CorsRules variable.
This command uses standard extends over several lines in this code block.

The second command assigns the rules in $CorsRules to the Blob service type.

### Example 2: Change properties of a CORS rule for blob service
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.
The command stores the rules in the $CorsRules array variable.

The second and third commands modify the first rule in $CorsRules.

The final command assigns the rules in $CorsRules to the Blob service type.
The revised rules overwrite the current CORS rules.

## PARAMETERS

### -ServiceType
Specifies the Azure Storage service type for which this cmdlet assigns rules.
The acceptable values for this parameter are:

- Blob 
- Table 
- Queue 
- File

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CorsRules
Specifies an array of CORS rules.
You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.

```yaml
Type: PSCorsRule[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Indicates that this cmdlet returns a Boolean that reflects the success of the operation.
By default, this cmdlet does not return a value.

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
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Specifies the length of the time-out period for the server part of a request.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Specifies the client-side time-out interval, in seconds, for one service request.
If the previous call fails in the specified interval, this cmdlet retries the request.
If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Specifies the maximum concurrent network calls.
You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.
The specified value is an absolute count and is not multiplied by the core count.
This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.
The default value is 10.

```yaml
Type: Int32
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

[Get-AzureStorageCORSRule](./Get-AzureStorageCORSRule.md)

[New-AzureStorageContext](./New-AzureStorageContext.md)

[Remove-AzureStorageCORSRule](./Remove-AzureStorageCORSRule.md)


