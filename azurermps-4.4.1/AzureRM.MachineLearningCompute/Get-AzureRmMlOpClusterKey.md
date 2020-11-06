---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582356"
---
# Get-AzureRmMlOpClusterKey

## Sammanfattning
Hämtar åtkomst nycklar som är kopplade till ett operationalization-kluster.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Skaffa operationalization för klustret från cmdlet input Parameters.
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### Skaffa operationalization för klustret från en OperationalizationCluster.
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### Skaffa operationalization kluster nycklar från ett Azure Resource-ID.
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## PROBLEMBESKRIVNING
Nycklarna för lagrings kontot, behållar registret och andra tjänster som är kopplade till operationalization-klustret returneras inte när du hämtar kluster egenskaperna. Ett specifikt samtal att hämta nycklar måste göras sedan de är känslig information.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

Returnerar hemliga nycklar för de tjänster som är kopplade till operationalization-klustret.

## MALLPARAMETRAR

### -InputObject
Operationalization.

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namnet på operationalization-klustret.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resurs gruppen för operationalization-klustret.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Azure Resource ID för operationalization-klustret.

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## KOSTNADS

### Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster
System. String


## VÄRDEN

### Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials


## ANMÄRKNINGAR

## RELATERADE LÄNKAR

