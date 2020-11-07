---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 51bfee17e33afcb93b90c36198e9352c3fca5fc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755452"
---
# Add-AzureRmHDInsightScriptAction

## Sammanfattning
Lägger till en skript åtgärd i ett kluster konfigurations objekt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmHDInsightScriptAction** lägger till skript åtgärder i HDInsight-konfigurationsobjektet som skapas av New-AzureRmHDInsightClusterConfig cmdlet.

Skript åtgärder tillhandahåller funktioner som används för att installera ytterligare program vara eller för att ändra konfigurationen för program som körs i ett Hadoop-kluster med hjälp av Windows PowerShell-eller bash-skript (för Windows-eller Linux-kluster).

En skript åtgärd körs på klusternoderna när HDInsight-kluster distribueras och körs efter noder i klustrets fullständiga HDInsight-konfiguration.
Skript åtgärden körs under administratörs behörighet och ger full åtkomst till klusternoderna.
Du kan tillhandahålla varje kluster med en lista med skript åtgärder som ska köras i en viss sekvens.

## BESKRIVS

### Exempel 1: lägga till en skript åtgärd i ett kluster konfigurations objekt
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

Det här kommandot lägger till en skript åtgärd för Head-och Worker-noder i ditt-Hadoop-001-kluster och körs när klustret skapas.

## MALLPARAMETRAR

### -Config
Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.
Det här objektet skapas av cmdlet **New-AzureRmHDInsightClusterConfig** .

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Anger namnet på skript åtgärden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeType
Anger nodtyp för körning av skript åtgärden.
De acceptabla värdena för den här parametern är:

- HeadNode
- WorkerNode
- ZookeeperNode

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parametrar
Anger parametrar för skript åtgärden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -URI
Anger den offentliga URI: n för skript åtgärden (ett PowerShell-eller bash-skript).

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### AzureHDInsightConfig
Parametern ' config ' godkänner värdet av typen ' AzureHDInsightConfig ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmHDInsightClusterConfig](./New-AzureRmHDInsightClusterConfig.md)


