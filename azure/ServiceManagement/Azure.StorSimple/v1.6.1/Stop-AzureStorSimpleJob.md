---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
online version: .\Get-AzureStorSimpleJob.md
schema: 2.0.0
ms.assetid: FF243961-E44D-4691-B80A-2D5B5AB08638
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.StorSimple/v1.6.1/Stop-AzureStorSimpleJob.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.StorSimple/v1.6.1/Stop-AzureStorSimpleJob.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Stop-AzureStorSimpleJob

## SYNOPSIS
Stops a StorSimple job.

## SYNTAX

```
Stop-AzureStorSimpleJob [-InstanceId] <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.
You can specify a jobs by supplying an instance ID or a job name.

## EXAMPLES

### Example 1: Stop jobs for a device
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.
The command passes the jobs to the current cmdlet by using the pipeline operator.
The current cmdlet stops any jobs that the command passes to it.
The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.

### Example 2: Stop a specific job
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

This command stops the job that has the specified instance ID.

## PARAMETERS

### -Force
ps_force

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Specifies the ID of the device job to stop.

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

### -Profile
Specifies an azure_2 profile.

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

### None

## OUTPUTS

### DeviceJobDetails
This cmdlet gets details of the **DeviceJob** that this cmdlet stops.

## NOTES

## RELATED LINKS

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


