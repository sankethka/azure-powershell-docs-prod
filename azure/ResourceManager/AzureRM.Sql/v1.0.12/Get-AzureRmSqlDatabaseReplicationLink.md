---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
online version: c4c541a5-61cd-41dc-a7fe-b938a7db3a28
schema: 2.0.0
ms.assetid: B518AB6E-F4B8-4FD5-98AE-A1D75BDB12A7
updated_at: 10/20/2016 12:12 AM
ms.date: 10/20/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Sql/v1.0.12/Get-AzureRmSqlDatabaseReplicationLink.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/831f900c1a4babea8fcc8817cfbc25252a1aa872/azureps-cmdlets-docs/ResourceManager/AzureRM.Sql/v1.0.12/Get-AzureRmSqlDatabaseReplicationLink.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmSqlDatabaseReplicationLink

## SYNOPSIS
Gets the geo-replication links between an ssSDS and a resource group or ssNoVersion.

## SYNTAX

### ByDatabaseName (Default)
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### ByPartnerServerName
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.
It gets all geo-replication links between the specified ssSDS and a resource group or azure_2ssNoVersion.

## EXAMPLES

### 1:
```

```

## PARAMETERS

### -DatabaseName
Specifies the name of the nextref_database for which to retrieve links.

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

### -PartnerResourceGroupName
Specifies the name of the resource group to which the partner is assigned.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Specifies the name of the ssNoVersion for the database to retrieve links for.

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

### -ResourceGroupName
Specifies the name of the azure_2 resource group for the database for which to retrieve links.

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

### -PartnerServerName
Specifies the name of the azure_2 SQL Server for the partner.

```yaml
Type: String
Parameter Sets: ByPartnerServerName
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

###  
This cmdlet accepts instances of the **ReplicationLink** or the **Database** object for the primary or secondary database.

## OUTPUTS

###  
This cmdlet returns a **ReplicationLink** object.

## NOTES

## RELATED LINKS


