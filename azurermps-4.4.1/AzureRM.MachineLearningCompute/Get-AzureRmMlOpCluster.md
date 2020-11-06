---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581411"
---
# Get-AzureRmMlOpCluster

## Sammanfattning
Hämtar ett operationalization.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämtar ett operationalization-kluster objekt efter namn eller resurs grupp eller efter abonnemang.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

Hämtar ett specifikt operationalization-kluster efter namn.

### Exempel 2
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

Hämtar alla operationalization-kluster i en resurs grupp.

### Exempel 3
```
PS C:\> Get-AzureRmMlOpCluster
```

Hämtar alla operationalization-kluster i ett abonnemang.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på operationalization-klustret.

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resurs gruppen för operationalization-klustret.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster, Microsoft. Azure. commands. MachineLearningCompute, version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

