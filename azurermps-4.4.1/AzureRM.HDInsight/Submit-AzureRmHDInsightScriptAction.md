---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 4739d5d6780caa85820c37974d9a8b69d2816e38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758066"
---
# Submit-AzureRmHDInsightScriptAction

## Sammanfattning
Skickar en ny skript åtgärd till ett Azure HDInsight-kluster.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Submit-AzureRmHDInsightScriptAction** skickar en ny skript åtgärd till ett Azure HDInsight-kluster.
Använd *PersistOnSuccess* för att köra skript åtgärden varje gång klustret skalas, så länge skript åtgärden lyckas.

## BESKRIVS

### Exempel 1: skicka en ny skript åtgärd till ett pågående HDInsight-kluster
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

Det här kommandot skickar en skript åtgärd till ett HDInsight-kluster som körs.

## MALLPARAMETRAR

### -ApplicationName
Anger programmets namn för skript åtgärden.
När *ApplicationName* är angivet ska *PersistOnSuccess* vara inställt på false, noderna får innehålla högst 1.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kluster namn
Anger namnet på klustret.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på skript åtgärden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeTypes
Anger de nodtyper som skript åtgärden ska köras på.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PersistOnSuccess
Anger att skript åtgärden ska köras varje gång klustret skal för änd ras.
Denna växel parameter ignoreras om skript åtgärden från början Miss lyckas.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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
Accept pipeline input: True (ByPropertyName)
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

## VÄRDEN

### Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmHDInsightScriptAction](./Add-AzureRmHDInsightScriptAction.md)


