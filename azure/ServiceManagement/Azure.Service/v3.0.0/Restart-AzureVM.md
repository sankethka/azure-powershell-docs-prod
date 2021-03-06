---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 7f8a5fbb-7f93-40f7-a5d7-8e19fd65b65e
schema: 2.0.0
ms.assetid: 247FAC9D-2E66-42D6-9D4A-87E96C08F6FA
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v3.0.0/Restart-AzureVM.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.Service/v3.0.0/Restart-AzureVM.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Restart-AzureVM

## SYNOPSIS
Restarts an Azure virtual machine.

## SYNTAX

### ByName (Default)
```
Restart-AzureVM [-ServiceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### RestartByName
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### RedeployByName
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### RedeployInput
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### RestartInput
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.

## EXAMPLES

### Example 1: Restart a virtual machine
```
PS C:\>Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.

### Example 2: Restart a virtual machine by using a virtual machine object
```
PS C:\>Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.

## PARAMETERS

### -ServiceName
Specifies the name of the Azure service that contains the virtual machine to restart.

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

### -Name
Specifies the name of the virtual machine to restart.

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Redeploy
Indicates that the cmdlet redeploys the virtual machine.

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Specifies a virtual machine object that identifies the virtual machine to restart.

```yaml
Type: PersistentVM
Parameter Sets: RedeployInput, RestartInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureVM](./Remove-AzureVM.md)

[Start-AzureVM](./Start-AzureVM.md)

[Stop-AzureVM](./Stop-AzureVM.md)

[Update-AzureVM](./Update-AzureVM.md)


