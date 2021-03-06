---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
online version: .\Add-AzureRmTrafficManagerEndpointConfig.md
schema: 2.0.0
ms.assetid: C500460E-AF54-465C-B269-07DF3EBA75C2
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ResourceManager/AzureRM.TrafficManager/v1.0/Remove-AzureRmTrafficManagerEndpointConfig.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ResourceManager/AzureRM.TrafficManager/v1.0/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
---

# Remove-AzureRmTrafficManagerEndpointConfig

## SYNOPSIS
Removes an endpoint from a local Traffic Manager profile object.

## SYNTAX

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local azure_2 Traffic Manager profile object.
You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.

This cmdlet operates on the local profile object.
Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.
To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.

## EXAMPLES

### Example 1: Remove an endpoint
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

The first command gets an azure_2 Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.
The command stores the local profile in the $TrafficManagerProfile variable.

The second command removes an azure_2 endpoint named contoso from the profile stored in $TrafficManagerProfile.
This command changes only the local object.

The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.

## PARAMETERS

### -EndpointName
Specifies the name of the Traffic Manager endpoint that this cmdlet removes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Specifies a local **TrafficManagerProfile** object.
This cmdlet modifies this local object.
To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Network.TrafficManagerProfile
This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.

## OUTPUTS

### Microsoft.Azure.Commands.Network.TrafficManagerProfile
This cmdlet returns a modified TrafficManagerProfile object.

## NOTES

## RELATED LINKS

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


