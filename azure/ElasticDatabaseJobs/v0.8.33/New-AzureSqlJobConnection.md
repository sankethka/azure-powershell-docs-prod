---
external help file: Microsoft.Azure.SqlDatabase.Jobs.PowerShell.dll-Help.xml
online version: ./Use-AzureSqlJobConnection.md
schema: 2.0.0
ms.assetid: 3B81E55B-8CA2-42A1-92E1-231C3BA04A06
updated_at: 10/24/2016 10:53 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell-elasticdb/blob/master/ElasticDB/ElasticDatabaseJobs/v0.8.33/New-AzureSqlJobConnection.md
gitcommit: https://github.com/Azure/azure-docs-powershell-elasticdb/blob/21fb425e1aa4eed4def521cf4515fe66d60846c7/ElasticDB/ElasticDatabaseJobs/v0.8.33/New-AzureSqlJobConnection.md
ms.topic: reference
ms.prod: powershell
ms.service: active-directory
ms.technology: Azure Powershell
author: visual-studio-china
ms.author: PowerShellHelpPub
keywords: powershell, cmdlet
manager: visual-studio-china
---

# New-AzureSqlJobConnection

## SYNOPSIS
Creates a connection to an Elastic Database jobs database.

## SYNTAX

### CurrentAzureSubscription
```
New-AzureSqlJobConnection [-CurrentAzureSubscription] [-ResourceGroupName <String>] -Credential <PSCredential>
 [<CommonParameters>]
```

### ConnectionDetails
```
New-AzureSqlJobConnection -ServerName <String> -DatabaseName <String> [-LiteralServerName]
 -Credential <PSCredential> [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureSqlJobConnection** cmdlet creates a connection to an Elastic Database jobs database.

Different elastic database jobs use the object that this cmdlet creates within the *AzureSqlDatabaseJobConnection* optional parameter. 
Alternatively, you can use the Use-AzureSqlJobConnection cmdlet to set the job connection within the Azure PowerShell session context and avoid having to pass the connection as a parameter to subsequent elastic database job cmdlet invocations.

## EXAMPLES

### Example 1: Get a connection to the Elastic Database Jobs database
```
PS C:\>New-AzureSqlJobConnection -CurrentAzureSubscription
ServerName                    DatabaseName                  UserName                                           Password
----------                    ------------                  --------                                           --------
edj0acd6992d61445a7b3b4a.d... edj0acd6992d61445a7b3b4a      PattiFul                         System.Security.SecureString
```

This command gets a connection to the Elastic Database Jobs database previously installed within the current Azure subscription within the __ElasticDatabaseJobs resource group. 
This cmdlet prompts you for credentials.

### Example 2: Get a connection to an Elastic Database Jobs database that exists on a server
```
PS C:\>New-AzureSqlJobConnection -ServerName "MyServer" -DatabaseName "MyDatabase"
ServerName                    DatabaseName                  UserName                                           Password
----------                    ------------                  --------                                           --------
myServer                      myDatabase                    PattiFul                         System.Security.SecureString
```

This command gets a connection to an Elastic Database Jobs database named myDatabase that exists on server MyServer. 
This cmdlet prompts you for credentials.

## PARAMETERS

### -Credential
Specifies the **PSCredential** containing the username and password for the elastic database job control database connections.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CurrentAzureSubscription
Indicates that the elastic database jobs control database is looked up within the current subscription by finding the Azure SQL Database within the __ElasticDatabaseJobs resource group.

```yaml
Type: SwitchParameter
Parameter Sets: CurrentAzureSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Specifies the database name of the elastic database jobs control database.

```yaml
Type: String
Parameter Sets: ConnectionDetails
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the Azure resource group that contains the Elastic Database Jobs control database. 
The cmdlet identifies the Elastic Database Jobs control database within the resource group.

```yaml
Type: String
Parameter Sets: CurrentAzureSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Specifies the database server name of the Elastic Database Jobs control database.

```yaml
Type: String
Parameter Sets: ConnectionDetails
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
Parameter Sets: ConnectionDetails
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

[Use-AzureSqlJobConnection](./Use-AzureSqlJobConnection.md)

[Azure Elastic Database Jobs Cmdlets](./ElasticDatabaseJobs.md)


