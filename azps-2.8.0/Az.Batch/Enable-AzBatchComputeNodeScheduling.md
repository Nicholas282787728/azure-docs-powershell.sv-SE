---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2922e9b1a37f714b1ccfb19aea86556b9988ccca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745434"
---
# Enable-AzBatchComputeNodeScheduling

## Sammanfattning
Aktiverar schemaläggning av aktiviteter på angiven datornod.

## FRÅGESYNTAXEN

### ID (standard)
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Enable-AzBatchComputeNodeScheduling** aktiverar aktivitets schemaläggning på den angivna noden för beräkning.
En datornod är en virtuell Azure-dator avsedd för en viss program belastning.

## BESKRIVS

### Exempel 1: Aktivera schemaläggning av en datornod
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

De här kommandona aktiverar schemaläggning av aktivitet på TVM-1783593343_34-20151117t222514z.
Det första kommandot i exemplet skapar en objekt referens som innehåller konto nycklarna för batch-contosobatchaccount.
Denna objekt referens lagras i en variabel som heter $context.
Det andra kommandot använder då den här objekt referensen och cmdleten **Enable-AzBatchComputeNodeScheduling** för att ansluta till poolen för pool och aktivera schemaläggning för TVM-1783593343_34-20151117t222514z.

### Exempel 2: Aktivera schemaläggning av aktiviteter på datornoder i en pool
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

De här kommandona aktiverar schemaläggning av aktiviteter på alla datornoder som finns i poolens Pool06.
För att utföra den här åtgärden skapar det första kommandot i exemplet en objekt referens som innehåller konto nycklarna för batch-contosobatchaccount.
Denna objekt referens lagras i en variabel som heter $context.
Med det andra kommandot i exemplet används den här objekt referensen och **Get-AzBatchComputeNode** för att returnera en samling av alla datornoder som finns i Pool06.
Samlingen är då piped till cmdleten **Enable-AzBatchComputeNodeScheduling** , som aktiverar schemaläggning av aktiviteter på varje datornod i samlingen.

## MALLPARAMETRAR

### -BatchContext
Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.
Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten. Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda. När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard. Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
Anger en objekt referens till noden Compute där schemaläggning av aktiviteter är aktiverat.
Den här objekt referensen skapas med Get-AzBatchComputeNode cmdlet och det returnerade datornoder-objektet sparas i en variabel.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Anger ID för den datornod där aktivitets schemaläggningen är aktive rad.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Anger ID för den gruppbearbetningssekvens som innehåller den datornod där aktivitets schemaläggningen är aktive rad.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## VÄRDEN

### System. Void

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


