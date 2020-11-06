---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 7cf3a056ec4266cccac577920f2f5b9292ce03be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583215"
---
# Enable-AzureBatchComputeNodeScheduling

## Sammanfattning
Aktiverar schemaläggning av aktiviteter på angiven datornod.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ID (standard)
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Enable-AzureBatchComputeNodeScheduling** aktiverar aktivitets schemaläggning på den angivna noden för beräkning.
En datornod är en virtuell Azure-dator avsedd för en viss program belastning.

## BESKRIVS

### Exempel 1: Aktivera schemaläggning av en datornod
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

De här kommandona aktiverar schemaläggning av aktivitet på TVM-1783593343_34-20151117t222514z.
Det första kommandot i exemplet skapar en objekt referens som innehåller konto nycklarna för batch-contosobatchaccount.
Denna objekt referens lagras i en variabel som heter $context.

Det andra kommandot använder då den här objekt referensen och cmdleten **Enable-AzureBatchComputeNodeScheduling** för att ansluta till poolen för pool och aktivera schemaläggning för TVM-1783593343_34-20151117t222514z.

### Exempel 2: Aktivera schemaläggning av aktiviteter på datornoder i en pool
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

De här kommandona aktiverar schemaläggning av aktiviteter på alla datornoder som finns i poolens Pool06.
För att utföra den här åtgärden skapar det första kommandot i exemplet en objekt referens som innehåller konto nycklarna för batch-contosobatchaccount.
Denna objekt referens lagras i en variabel som heter $context.

Med det andra kommandot i exemplet används den här objekt referensen och **Get-AzureBatchComputeNode** för att returnera en samling av alla datornoder som finns i Pool06.
Samlingen är då piped till cmdleten **Enable-AzureBatchComputeNodeScheduling** , som aktiverar schemaläggning av aktiviteter på varje datornod i samlingen.

## MALLPARAMETRAR

### -BatchContext
Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.
Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten. Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda. När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard. Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.

```yaml
Type: BatchAccountContext
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
Den här objekt referensen skapas med Get-AzureBatchComputeNode cmdlet och det returnerade datornoder-objektet sparas i en variabel.

```yaml
Type: PSComputeNode
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Anger ID för den datornod där aktivitets schemaläggningen är aktive rad.

```yaml
Type: String
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
Type: String
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

### BatchAccountContext
Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline

### PSComputeNode
Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Disable-AzureBatchComputeNodeScheduling](./Disable-AzureBatchComputeNodeScheduling.md)


