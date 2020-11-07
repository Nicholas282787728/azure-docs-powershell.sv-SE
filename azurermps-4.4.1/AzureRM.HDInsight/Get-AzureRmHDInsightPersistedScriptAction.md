---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: d0ca241cc29bedcd3a34f866fa2b7a19fceb0745
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758078"
---
# Get-AzureRmHDInsightPersistedScriptAction

## Sammanfattning
Hämtar de beständiga skript åtgärderna för ett kluster och visar dem i kronologisk ordning, eller hämtar information om en viss beständiga skript åtgärd.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmHDInsightPersistedScriptAction** hämtar de beständiga skript åtgärderna för ett Azure HDInsight-kluster och visar dem i kronologisk ordning, eller hämtar information om en viss beständiga skript åtgärd.

## BESKRIVS

### Exempel 1: Hämta de beständiga skript åtgärderna i ett kluster
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

Det här kommandot hämtar beständiga skript åtgärder i klustret som heter din-Hadoop-001.

## MALLPARAMETRAR

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
Anger namnet på den beständiga skript åtgärden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzureRmHDInsightPersistedScriptAction](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[Set-AzureRmHDInsightPersistedScriptAction](./Set-AzureRmHDInsightPersistedScriptAction.md)


