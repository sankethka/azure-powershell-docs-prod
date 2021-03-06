---
external help file: Microsoft.Azure.SqlDatabase.Jobs.PowerShell.dll-Help.xml
online version: ./Get-AzureSqlJob.md
schema: 2.0.0
ms.assetid: EAA47557-0286-4A6E-BC2C-7A74DA74B8A6
updated_at: 10/24/2016 10:53 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-elasticdb/blob/master/ElasticDB/ElasticDatabaseJobs/v0.8.33/New-AzureSqlJob.md
gitcommit: https://github.com/Azure/azure-docs-powershell-elasticdb/blob/21fb425e1aa4eed4def521cf4515fe66d60846c7/ElasticDB/ElasticDatabaseJobs/v0.8.33/New-AzureSqlJob.md
ms.topic: reference
ms.prod: powershell
ms.service: active-directory
ms.technology: Azure Powershell
author: visual-studio-china
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: visual-studio-china
---

# New-AzureSqlJob

## SYNOPSIS
Creates a job definition to be used for subsequent job runs.

## SYNTAX

### TargetId
```
New-AzureSqlJob -JobName <String> -CredentialName <String> -ContentName <String> -TargetId <Guid>
 [-ExecutionPolicyName <String>] [[-AzureSqlJobConnection] <AzureSqlJobConnection>] [<CommonParameters>]
```

### TargetIdWithResultSetDestination
```
New-AzureSqlJob -JobName <String> -CredentialName <String> -ContentName <String> -TargetId <Guid>
 [-ExecutionPolicyName <String>] -ResultSetDestinationServerName <String>
 -ResultSetDestinationDatabaseName <String> -ResultSetDestinationCredentialName <String>
 -ResultSetDestinationSchemaName <String> -ResultSetDestinationTableName <String> [-LiteralServerName]
 [[-AzureSqlJobConnection] <AzureSqlJobConnection>] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureSqlJob** cmdlet creates a job definition to be used for subsequent job runs.

Job execution can be requested through the Start-AzureSqlJobExecution cmdlet or through creation of a trigger in combination with a schedule using the New-AzureSqlJobTrigger cmdlet.

## EXAMPLES

### Example 1: Create a job using the specified content
```
PS C:\>ew-AzureSqlJob -JobName "MyJob" -CredentialName "MyCredential" -ContentName "MyScript" -TargetId (Get-AzureSqlDatabaseJobTarget -CustomCollectionName "MyCustomCollection").TargetId
JobName              : MyJob
ContentName          : MyScript
ContentVersionNumber : 
TargetDescription    : {"CustomCollectionName":"myCustomCollection"}
TargetId             : b525727e-6ed0-44cc-94da-63c543e383d7
CredentialName       : MyCredential
ExecutionPolicyName  : Default execution policy
ResultSetDestination :
```

This command creates a job using the specified content to execute across the specified custom collection using the specified credentials.

### Example 2: Create a job using the specified content
```
PS C:\>New-AzureSqlJob -JobName "MyResultsJob" -CredentialName "MyCredential" -ContentName MyScript -ResultSetDestinationServerName "MyResultsServerName.database.windows.net" -ResultSetDestinationDatabaseName "MyResultsDatabaseName" -ResultSetDestinationCredentialName "MyResultsCredential" -ResultSetDestinationSchemaName "DBO" -ResultSetDestinationTableName "MyResultsTable" -TargetId (Get-AzureSqlDatabaseJobTarget -CustomCollectionName "MyCustomCollection").TargetId
JobName              : MyResultsJob
ContentName          : MyScript

ContentVersionNumber : 
TargetDescription    : {"CustomCollectionName":"myCustomCollection"}
TargetId             : b525727e-6ed0-44cc-94da-63c543e383d7
CredentialName       : MyCredential
ExecutionPolicyName  : Default execution policy
ResultSetDestination : Microsoft.Azure.SqlDatabase.Jobs.Client.ResultSetDestination
```

This command creates a job using the specified content to run across the specified custom collection using the specified credentials, where the result set from each database is stored into the specified result set destination table.

### Example 3: Create a job using the specified content to execute across the specified elastic scale shard map collection
```
PS C:\>New-AzureSqlJob -JobName "MyResultsJobAcrossShardMap" -CredentialName "MyCredential" -ContentName "MyScript" -ResultSetDestinationServerName "MyResultsServerName.database.windows.net" -ResultSetDestinationDatabaseName "MyResultsDatabaseName" -ResultSetDestinationCredentialName myResultsCredential -ResultSetDestinationSchemaName "DBO" -ResultSetDestinationTableName "MyResultsTable" -TargetId (Get-AzureSqlDatabaseJobTarget -ShardMapManagerServerName "MyShardMapManagerServer.database.windows.net" -ShardMapManagerDatabaseName "MyShardMapManagerDatabase" -ShardMapName "MyShardMap").TargetId
JobName              : MyResultsJobAcrossShardMap
ContentName          : MyScript
ContentVersionNumber : 
TargetDescription    : {"ShardMapName":"MyShardMap","ShardMapManagerServerName":"MyShardMapManagerServer.database.windows.net","ShardMapManagerDatabaseName":
                       "MyShardMapManagerDatabase"}
TargetId             : 1afd9326-1277-4344-832f-8170d0375ff7
CredentialName       : MyCredential
ExecutionPolicyName  : Default execution policy
ResultSetDestination : Microsoft.Azure.SqlDatabase.Jobs.Client.ResultSetDestination
```

This command creates a job using the specified content to execute across the specified elastic scale shard map collection using the specified credentials, where the result set from each database is stored into the specified result set destination table.

## PARAMETERS

### -AzureSqlJobConnection
Specifies the connection state object for the job.
You can get the connection state object through the New-AzureSqlJobConnection cmdlet.
If you do not specify this parameter, the connection state is used from a prior call to the Use-AzureSqlJobConnection cmdlet.

```yaml
Type: AzureSqlJobConnection
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentName
Specifies the name of the content to run or be applied during the job.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CredentialName
Specifies the name of the credentials to use when connecting to target databases.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExecutionPolicyName
Specifies the name of the execution policy to use during job execution. 
If you do not specify this parameter, the default job execution policy is used.

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

### -JobName
Specifies the name to use for the new job.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResultSetDestinationCredentialName
Specifies the name of the credential to use for the database connection used for insertion of the first result set obtained during job execution.

```yaml
Type: String
Parameter Sets: TargetIdWithResultSetDestination
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResultSetDestinationDatabaseName
Specifies the database name to use for insertion of the first result set obtained during job execution.

```yaml
Type: String
Parameter Sets: TargetIdWithResultSetDestination
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResultSetDestinationSchemaName
Specifies the database schema name to use for insertion of the first result set obtained during job execution.

```yaml
Type: String
Parameter Sets: TargetIdWithResultSetDestination
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResultSetDestinationServerName
Specifies the database schema name to use for insertion of the first result set obtained during job execution.

```yaml
Type: String
Parameter Sets: TargetIdWithResultSetDestination
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResultSetDestinationTableName
Specifies the database table name to use for insertion of the first result set obtained during job execution. 
If the table does not exist during job execution, the system automatically creates it using a schema matching the result set.

```yaml
Type: String
Parameter Sets: TargetIdWithResultSetDestination
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetId
Specifies the target ID to use for execution or application of the content during job execution.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LiteralServerName
{{Fill LiteralServerName Description}}

```yaml
Type: SwitchParameter
Parameter Sets: TargetIdWithResultSetDestination
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

[Get-AzureSqlJob](./Get-AzureSqlJob.md)

[Remove-AzureSqlJob](./Remove-AzureSqlJob.md)

[Set-AzureSqlJob](./Set-AzureSqlJob.md)


