---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
online version: d2f47d8a-3029-4bd4-8fbf-d5a25618acf5
schema: 2.0.0
ms.assetid: F278742E-C74D-44B9-A5DB-0BE13254F82E
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.StorSimple/v3.0.0/Import-AzureStorSimpleLegacyVolumeContainer.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.StorSimple/v3.0.0/Import-AzureStorSimpleLegacyVolumeContainer.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Import-AzureStorSimpleLegacyVolumeContainer

## SYNOPSIS
Starts the migration of volume containers.

## SYNTAX

### MigrateSpecificContainer
```
Import-AzureStorSimpleLegacyVolumeContainer [-LegacyConfigId] <String> [-LegacyContainerNames] <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Import-AzureStorSimpleLegacyVolumeContainer [-LegacyConfigId] <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.

## EXAMPLES

### Example 1: Import a legacy volume container
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

This command imports a legacy volume container for the named container.
The cmdlet starts the import, and then returns a message.

### Example 2: Import all legacy volume containers
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

This command imports all legacy volume containers from configuration file imported.
The cmdlet starts the import, and then returns a message.

## PARAMETERS

### -All
Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyConfigId
Specifies the unique ID of the configuration of the legacy appliance.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyContainerNames
Specifies an array of volume container names for which the migration plan applies.

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifies the Azure profile from which this cmdlet reads.
If you do not specify a profile, this cmdlet reads from the local default profile.

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

### -SkipACRs
Indicates that the import process skips access control records for migration.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### String
This command returns the status of the migration import volume container job if it has been successfully started in the appliance.

## NOTES

## RELATED LINKS

[Get-AzureStorSimpleLegacyVolumeContainerStatus](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[Import-AzureStorSimpleLegacyApplianceConfig](./Import-AzureStorSimpleLegacyApplianceConfig.md)


