---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
online version: .\New-AzureRmStreamAnalyticsFunction.md
schema: 2.0.0
ms.assetid: 87E95D58-00AA-4A5A-9527-94CA53522A64
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.StreamAnalytics/v2.1.0/Get-AzureRmStreamAnalyticsFunction.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.StreamAnalytics/v2.1.0/Get-AzureRmStreamAnalyticsFunction.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureRmStreamAnalyticsFunction

## SYNOPSIS
Gets functions in a Stream Analytics job.

## SYNTAX

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.

## EXAMPLES

### Example 1: Get all Stream Analytics functions
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

This command gets the functions defined on the job named StreamJob22.

### Example 2: Get a specific Stream Analytics function
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

This command gets information about the function named ScoreTweet defined on the job named StreamJob22.

## PARAMETERS

### -JobName
Specifies the name of the Stream Analytics job to which functions belong.
This cmdlet gets functions for the job that this parameter specifies.

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

### -Name
Specifies the name of the Stream Analytics function that this cmdlet gets.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the resource group to which Stream Analytics functions belongs.
This cmdlet gets functions for the group that this parameter specifies.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction

## NOTES

## RELATED LINKS

[New-AzureRmStreamAnalyticsFunction](./New-AzureRmStreamAnalyticsFunction.md)

[Remove-AzureRmStreamAnalyticsFunction](./Remove-AzureRmStreamAnalyticsFunction.md)

[Test-AzureRmStreamAnalyticsFunction](./Test-AzureRmStreamAnalyticsFunction.md)


