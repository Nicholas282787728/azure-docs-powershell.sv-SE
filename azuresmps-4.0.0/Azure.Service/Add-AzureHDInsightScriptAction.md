---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093446"
---
# Add-AzureHDInsightScriptAction

## Sammanfattning
Lägger till en HDInsight-skript åtgärd.

## FRÅGESYNTAXEN

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Den här versionen av Azure PowerShell HDInsight är inaktuell.
Dessa cmdletar tas bort den 1 januari 2017.
Använd den nyare versionen av Azure PowerShell HDInsight.

Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Cmdleten **Add-AzureHDInsightScriptAction** tillhandahåller Azure HDInsight-funktioner som används för att installera ytterligare program vara eller för att ändra konfigurationen för program som körs i ett Hadoop-kluster med hjälp av Windows PowerShell-skript.

En skript åtgärd körs på klusternoderna när HDInsight-kluster distribueras och körs efter noder i klustrets fullständiga HDInsight-konfiguration.
Skript åtgärden körs under administratörs behörighet och ger full åtkomst till klusternoderna.
Du kan tillhandahålla varje kluster med en lista med skript åtgärder som ska köras i en viss sekvens.

## BESKRIVS

### Exempel 1: lägga till en skript åtgärd i ett kluster
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

I det första kommandot används cmdleten **New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration och sedan lagras den i $config variabel.

Med det andra kommandot används cmdleten **Add-AzureHDInsightScriptAction** för att lägga till skript åtgärden med namnet TestScriptAction i $config.

I det sista kommandot används cmdleten **New-AzureHDInsightCluster** för att skapa ett nytt HDInsight-kluster som kör skript åtgärden som lagras i $config.

### Exempel 2: lägga till flera skript åtgärder i ett kluster
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

I det första kommandot används cmdleten **New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration och sedan lagras den i $config variabel.

Med det andra kommandot används cmdleten **Add-AzureHDInsightScriptAction** för att lägga till den angivna skript åtgärden i $config och sedan används pipeline-operatorn för att skicka $config till **AzureHDInsightScriptAction** en andra gång för att lägga till en andra skript åtgärd för $config.

Det sista kommandot använder cmdleten **New-AzureHDInsightCluster** för att skapa ett kluster som kör skript åtgärderna i $config.

## MALLPARAMETRAR

### -ClusterRoleCollection
Anger de noder som du vill köra ett skript för.
De acceptabla värdena för den här parametern är: HeadNode eller DataNode.

Du kan ange ett eller båda värden.

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Anger ett konfigurations objekt.
Denna cmdlet lägger till skript åtgärds information till det objekt som den här parametern anger.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Anger namnet på en skript åtgärd.

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

### -Parametrar
Anger de parametrar som krävs för en skript åtgärd.

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

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

### -URI
Anger URI-platsen för ett skript som ska köras.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[New-AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)


