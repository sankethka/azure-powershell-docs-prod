---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
online version: .\New-AzureRmPolicyAssignment.md
schema: 2.0.0
ms.assetid: 011574C2-C1A3-4EE6-8BC5-FCDD10E0E5D5
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Resources/v2.0.3/Get-AzureRmPolicyAssignment.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Resources/v2.0.3/Get-AzureRmPolicyAssignment.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
---

# Get-AzureRmPolicyAssignment

## SYNOPSIS
Gets policy assignments.

## SYNTAX

### The list all policy assignments parameter set. (Default)
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### The policy assignment name parameter set.
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### The policy assignment Id parameter set.
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.
Identify a policy assignment to get by name and scope or by ID.

## EXAMPLES

### Example 1: Get all policy assignments
```
PS C:\>Get-AzureRmPolicyAssignment
```

This command gets all the policy assignments.

### Example 2: Get a specific policy assignment
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.
The command stores that object in the $ResourceGroup variable.

The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.

## PARAMETERS

### -ApiVersion
Specifies the version of the resource provider API to use.
If you do not specify a version, this cmdlet uses the latest available version.

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

### -Pre
Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.

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

### -Name
Specifies the name of the policy assignment that this cmdlet gets.

```yaml
Type: String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope
Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.

```yaml
Type: String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionId
Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.

```yaml
Type: String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.

```yaml
Type: String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

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

[New-AzureRmPolicyAssignment](./New-AzureRmPolicyAssignment.md)

[Remove-AzureRmPolicyAssignment](./Remove-AzureRmPolicyAssignment.md)

[Set-AzureRmPolicyAssignment](./Set-AzureRmPolicyAssignment.md)


