---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
online version: .\New-AzureRmStreamAnalyticsInput.md
schema: 2.0.0
ms.assetid: E10BBD12-0078-4E95-98CB-85A1AC7B23F6
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.StreamAnalytics/v1.0.12/Remove-AzureRmStreamAnalyticsInput.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.StreamAnalytics/v1.0.12/Remove-AzureRmStreamAnalyticsInput.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Remove-AzureRmStreamAnalyticsInput

## SYNOPSIS
Deletes an input from a Stream Analytics job.

## SYNTAX

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-PipelineVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in azure_2.

## EXAMPLES

### EXAMPLE 1: Remove an input stream from a job
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

This command removes the input EventStream from StreamingJob.

## PARAMETERS

### -JobName
Specifies the name of the azure_2 Stream Analytics job to which the azure_2 Stream Analytics input belongs.

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
Specifies the name of the azure_2 Stream Analytics input to remove.

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

### -Force
If this parameter is specified, the cmdlet will delete the specified Azure Stream Analytics input without asking for confirmation.

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

### -ResourceGroupName
Specifies the name of the resource group to which the azure_2 Stream Analytics input belongs.

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

### -PipelineVariable
Not Specified

```yaml
Type: String
Parameter Sets: (All)
Aliases: pv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
psdx_confirmdesc

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
psdx_whatifdesc

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[New-AzureRmStreamAnalyticsInput](./New-AzureRmStreamAnalyticsInput.md)

[Get-AzureRmStreamAnalyticsInput](./Get-AzureRmStreamAnalyticsInput.md)

[Test-AzureRmStreamAnalyticsInput](./Test-AzureRmStreamAnalyticsInput.md)


