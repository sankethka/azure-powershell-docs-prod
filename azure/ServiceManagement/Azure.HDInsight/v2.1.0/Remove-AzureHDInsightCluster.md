---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 55981C68-5D82-4EC4-8083-3DC9989CCBC4
updated_at: 10/24/2016 11:55 PM
ms.date: 10/24/2016
content_git_url: https://github.com/Azure/azure-docs-powershell/blob/master/azureps-cmdlets-docs/ServiceManagement/Azure.HDInsight/v2.1.0/Remove-AzureHDInsightCluster.md
gitcommit: https://github.com/Azure/azure-docs-powershell/blob/4377291ee360e58e2c1c5d644155daf6a0279055/azureps-cmdlets-docs/ServiceManagement/Azure.HDInsight/v2.1.0/Remove-AzureHDInsightCluster.md
ms.topic: reference
ms.prod: powershell
ms.service: azure-powershell
ms.technology: Azure PowerShell
author: visual-studio-china
ms.author: 
keywords: powershell, cmdlet
manager: visual-studio-china
---

# Remove-AzureHDInsightCluster

## SYNOPSIS
Deletes an HDInsight cluster from a subscription.

## SYNTAX

```
Remove-AzureHDInsightCluster [[-Certificate] <X509Certificate2>] [[-HostedService] <String>]
 [[-Endpoint] <Uri>] [-IgnoreSslErrors <Boolean>] [-Name] <String> [[-Subscription] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIPTION
This version of Azure PowerShell HDInsight is deprecated.
These cmdlets will be removed by January 1, 2017.
Please use the newer version of Azure PowerShell HDInsight.

For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in HDInsight using Azure PowerShellhttps://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/.
For information about how to submit jobs by using Azure PowerShell and other approaches, see Submit Hadoop jobs in HDInsighthttps://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/.
For reference information about Azure PowerShell HDInsight, see Azure HDInsight Cmdletshttps://msdn.microsoft.com/en-us/library/mt438705.aspx.

The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.
This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.
Data stored in the associated Azure Storage account is not deleted.

## EXAMPLES

### Example 1: Remove a cluster
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

This command deletes the HDInsight cluster named HDICluster.

## PARAMETERS

### -Certificate
Specifies the management certificate for an Azure subscription.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Specifies the namespace of an HDInsight service if you do not want to use the default namespace.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint
Specifies the endpoint to use to connect to Azure.
If you do not specify this parameter, this cmdlet uses the default endpoint.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the HDInsight cluster to remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Subscription
Specifies the subscription account that contains the HDInsight cluster to remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSslErrors
Indicates whether Secure Sockets Layer (SSL) errors are ignored.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureHDInsightCluster](./Get-AzureHDInsightCluster.md)

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Use-AzureHDInsightCluster](./Use-AzureHDInsightCluster.md)


