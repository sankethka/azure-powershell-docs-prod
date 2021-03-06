---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 5291dc55-5d40-462b-9e22-61a4c0236ab9
schema: 2.0.0
ms.assetid: 688BE4C0-0390-4DB2-97B7-81E05E8D796B
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v3.0.0/Reset-AzureRoleInstance.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v3.0.0/Reset-AzureRoleInstance.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Reset-AzureRoleInstance

## SYNOPSIS
Requests a reboot or reimage of a single role instance or all role instances of a specific role.

## SYNTAX

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.
This operation executes synchronously.
When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.
Any data that is written to the local disk persists across reboots.
Any data that is in-memory is lost.

Reimaging a role instance results in different behavior depending on the type of role.
For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.
The role is then brought back online.
For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.

Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.
If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.
Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.

## EXAMPLES

### Example 1: Reboot a role instance
```
PS C:\>ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.

### Example 2: Reimage a role instance
```
PS C:\>ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

This command reimages the role instances in the staging deployment of the MySvc01 cloud service.

### Example 3: Reimage all role instances
```
PS C:\>ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

This command reimages all role instances in the production deployment of the MySvc01 service.

## PARAMETERS

### -ServiceName
Specifies the name of the service.

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

### -Slot
Specifies the deployment environment where the role instances run.
Valid values are: Production and Staging.
You can include either the *DeploymentName* or *Slot* parameter, but not both.

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

### -InstanceName
Specifies the name of the role instance to reimage or reboot.

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

### -Reboot
Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.
You must include either a *Reboot* or *Reimage* parameter, but not both.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Reimage
Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.
You must include either a *Reboot* or *Reimage* parameter, but not both.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-AzureRole](./Set-AzureRole.md)


