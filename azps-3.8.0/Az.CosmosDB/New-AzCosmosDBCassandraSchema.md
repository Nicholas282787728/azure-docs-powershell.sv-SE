---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088284"
---
# New-AzCosmosDBCassandraSchema

## Sammanfattning
Skapar ett nytt CosmosDB Cassandra-schema.

## FRÅGESYNTAXEN

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**New-AzCosmosDBCassandraSchema** skapar ett nytt CosmosDB Cassandra-schema.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## MALLPARAMETRAR

### -ClusterKey
Matris med PSClusterKey-objekt.

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kolumn
PSColumn-objekt.

```yaml
Type: PSColumn[]
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionKey
Matris med strängar som innehåller partitionsalternativ.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. CosmosDB. Models. PSCassandraSchema

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
