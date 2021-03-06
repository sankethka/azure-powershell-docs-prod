---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
online version: http://go.microsoft.com/fwlink/?LinkId=404172
schema: 2.0.0
ms.assetid: CD68129A-CC88-4127-ADC4-D2ADDB20935D
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.Tags/v2.2.0/New-AzureRmTag.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.Tags/v2.2.0/New-AzureRmTag.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# New-AzureRmTag

## SYNOPSIS
Creates a predefined azure_2 tag or adds values to an existing tag.

## SYNTAX

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureRmTag** cmdlet creates a predefined azure_2 tag with an optional predefined value.
You can also use it to add additional values to existing predefined tags.
To create a predefined tag, enter a unique tag name.
To add a value to an existing predefined tag, specify the name of the existing tag and the new value.

This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.

The azure_2 Tags module that **New-AzureRmTag** is part of can help you manage predefined azure_2 tags.
An azure_2 tag is a name-value pair that you can use to categorize your azure_2 resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.

You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.
If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.

To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.
To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.

Every tag has a name.
The values are optional.
A predefined azure_2 tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.
For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.
When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.

## EXAMPLES

### Example 1: Create a predefined tag
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

This command creates a predefined tag named FY2015.
This tag has no values.
You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.
You can also specify a value when you apply the tag to the resource or resource group.

### Example 2: Create a predefined tag with a value
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

This command creates a predefined tag named Department with a value of Finance.

### Example 3: Add a value to a predefined tag
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

These commands create a predefined tag named Department with two values.
If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.

### Example 4: Use a predefined tag
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

The commands in this example create and use a predefined tag.

## PARAMETERS

### -Name
Specifies the tag name.
To create a new predefined tag, enter a unique name.

To add a value to an existing tag, enter the name of the existing tag.
If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.

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

### -Value
Specifies a tag value.
Predefined tags can have multiple values, but you can enter only one value in each command.
This parameter is optional, because tags can have names without values.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Azure.Commands.Tags.Model.PSTag

## NOTES

## RELATED LINKS

[Get-AzureRmTag](./Get-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


