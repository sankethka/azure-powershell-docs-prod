---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: BC7092A8-72ED-48E9-BA38-55866B5B6F08
updated_at: 10/18/2016 9:38 PM
ms.date: 10/18/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.UsageAggregates/v1.0/Get-UsageAggregates.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/23cdb8705d4ab9807c0e21b238f3b134a7d49c7d/azureps-cmdlets-docs/ResourceManager/AzureRM.UsageAggregates/v1.0/Get-UsageAggregates.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-UsageAggregates

## SYNOPSIS
Gets the reported azure_2 subscription usage details.

## SYNTAX

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-UsageAggregates** cmdlet gets aggregated azure_2 subscription usage data by the following properties: 

- Start and end times of when the usage was reported.

- Aggregation precision, either daily or hourly.

- Instance level detail for multiple instances of the same resource.

For consistent results, the returned data is based on when the usage details were reported by the azure_2 resource.

For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.

## EXAMPLES

### Example 1: Retrieve subscription data
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.

## PARAMETERS

### -AggregationGranularity
Specifies the aggregation precision of the data.
Valid values are: Daily and Hourly.

The default value is Daily.

```yaml
Type: AggregationGranularity
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
Specifies the continuation token that was retrieved from the response body in the previous call.
For a large result set, responses are paged by using continuation tokens.
The continuation token serves as a bookmark for progress.
If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.
We recommend that you follow the next link in the response to page though the data.

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

### -ReportedEndTime
Specifies the reported end time for when resource usage was recorded in the azure_2 billing system.

azure_2 is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.
In order to get all usage events for a subscription that are reported for a time period, you query by reported time.
Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.
The resource usage data is the useful pivot for analyzing the data.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
Specifies the reported start time for when resource usage was recorded in the azure_2 billing system.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowDetails
Indicates whether this cmdlet returns instance-level details with the usage data.

The default value is $True.

If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.
For example, if you are running three websites, by default you will get three line items for website consumption.
However, when the value is $False, all the data for the same **subscriptionId**, **meterId**, **usageStartTime**, and **usageEndTime** is collapsed into a single line item.

```yaml
Type: Boolean
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


