---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
online version: .\Register-AzureAutomationScheduledRunbook.md
schema: 2.0.0
ms.assetid: AF10C3C5-8025-410E-8B56-7A2930E429D8
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Automation/v0.9.8/Get-AzureAutomationScheduledRunbook.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Automation/v0.9.8/Get-AzureAutomationScheduledRunbook.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Get-AzureAutomationScheduledRunbook

## SYNOPSIS
Gets Azure Automation runbooks and associated schedules.

## SYNTAX

### ByAll (Default)
```
Get-AzureAutomationScheduledRunbook [-AutomationAccountName] <String> [-Profile <AzureProfile>]
 [<CommonParameters>]
```

### ByJobScheduleId
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> [-AutomationAccountName] <String>
 [-Profile <AzureProfile>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> [-AutomationAccountName] <String>
 [-Profile <AzureProfile>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-AutomationAccountName] <String> [-Profile <AzureProfile>] [<CommonParameters>]
```

### ByScheduleName
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> [-AutomationAccountName] <String>
 [-Profile <AzureProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules. 
By default, all scheduled runbooks are returned.
To get a specific scheduled runbook, specify the runbook name and the schedule name. 
To get all schedules associated with a runbook, specify just the runbook name. 
To get all runbooks associated with a schedule, specify just the schedule name.

## EXAMPLES

### Example 1: Get all scheduled runbooks
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

This command gets all scheduled runbooks in the Azure Automation account named Contoso17.

### Example 2: Get all schedules associated with a runbook
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"  ¢â‚¬"RunbookName "Runbk01"
```

This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.

### Example 3: Get all runbooks associated with a schedule
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"  ¢â‚¬"ScheduleName "Schedule01"
```

This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.

## PARAMETERS

### -AutomationAccountName
Specifies the name of an Azure Automation account.

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

### -JobScheduleId
Specifies the Id of a scheduled job.

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunbookName
Specifies the name of a runbook.

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Specifies the name of a schedule.

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
In-memory profile.

```yaml
Type: AzureProfile
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

### Microsoft.Azure.Commands.Automation.Model.JobSchedule

## NOTES

## RELATED LINKS

[Register-AzureAutomationScheduledRunbook](./Register-AzureAutomationScheduledRunbook.md)

[Unregister-AzureAutomationScheduledRunbook](./Unregister-AzureAutomationScheduledRunbook.md)


