---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 778347394e9793b95434e1b308bbdb4e28fc0915
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583368"
---
# Disable-AzureBatchComputeNodeScheduling

## Sammanfattning
Inaktiverar schemaläggning av aktiviteter på angiven datornod.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ID (standard)
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **disable-AzureBatchComputeNodeScheduling** inaktiverar schemaläggning av aktiviteter på angiven datornod.
En datornod är en virtuell Azure-dator avsedd för en viss program belastning.
När du inaktiverar schemaläggning av aktiviteter på en datornod kan du välja att ta reda på vad som är möjligt för de jobb som finns i nodens uppgifts köer.
**Disable – AzureBatchComputeNodeScheduling** gör att du kan göra följande: 

- Avsluta uppgifterna och placera dem i jobbkön igen.
Detta gör att aktiviteterna kan schemaläggas om på en annan datornod. 
- Avsluta aktiviteterna och ta bort dem från jobbkön.
Aktiviteter som stoppats på det här sättet ändras inte. 
- Vänta tills alla aktiviteter som körs för tillfället utförs och inaktivera schemaläggning på noden beräkning. 
- Vänta tills alla aktiviteter som körs ska slutföras och alla tids perioder för data upphör att gälla och inaktivera sedan schemaläggning på noden beräkning.

## BESKRIVS

### Exempel 1: inaktivera schemaläggning av aktiviteter på en datornod
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Dessa kommandon inaktiverar aktivitets schema för noden Compute, TVM-1783593343_34-20151117t222514z.
För att göra detta skapar det första kommandot i exemplet en objekt referens till konto nycklarna för batch-contosobatchaccount.
Denna objekt referens lagras i en variabel som heter $context.

Det andra kommandot använder då den här objekt referensen och cmdleten **disable-AzureBatchComputeNodeScheduling** för att ansluta till poolens icke-grupppool och inaktivera schemaläggning av aktivitet på noden TVM-1783593343_34-20151117t222514z.

Eftersom *DisableComputeNodeSchedulingOptions* -parametern inte inkluderade de uppgifter som för närvarande körs på noden beräkning, köas.

### Exempel 2: inaktivera schemaläggning av aktiviteter på alla datornoder i en pool
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

De här kommandona inaktiverar schemaläggning av aktiviteter på alla noder i grupppoolens Pool06.
För att utföra den här åtgärden skapar det första kommandot i exemplet en objekt referens till konto nycklarna för batch-contosobatchaccount.
Denna objekt referens lagras i en variabel som heter $context.

Med det andra kommandot i exemplet används den här objekt referensen och **Get-AzureBatchComputeNode** för att returnera en samling av alla datornoder som finns i Pool06.
Samlingen **avaktiverar sedan-AzureBatchComputeNodeScheduling-** cmdlet för att inaktivera schemaläggning av aktiviteter för varje datornod i samlingen.

Eftersom *DisableComputeNodeSchedulingOptions* -parametern inte inkluderade de uppgifter som för närvarande körs på datornoderna köas.

## MALLPARAMETRAR

### -BatchContext
Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.
Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.

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
Anger en objekt referens till noden Compute där aktivitets schemaläggningen är inaktive rad.
Den här objekt referensen skapas med Get-AzureBatchComputeNode cmdlet och det returnerade datornoder-objektet sparas i en variabel.

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

### -DisableSchedulingOption
Anger hur den här cmdleten hanterar aktiviteter som körs på den dator nod där schemaläggning inaktive ras.
De acceptabla värdena för den här parametern är:

- Köa om.
Uppgifter stoppas direkt och återgår till jobbkön.
Detta gör att aktiviteter kan schemaläggas om på en annan datornod.
Det här är standardvärdet. 
- Säga upp.
Uppgifter stoppas direkt och tas bort från jobbkön.
De här aktiviteterna kommer inte att schemaläggas om. 
- TaskCompletion.
För tillfället pågående uppgifter kan slutföras innan aktivitets schemaläggningen är inaktive rad på noden Compute.
Inga nya aktiviteter schemaläggs på den här noden. 
- RetainedData.
Aktiviteter som körs för tillfället kan slutföras och data lagrings perioderna kan upphöra innan aktivitets schemaläggningen är inaktive rad på noden Compute.
Inga nya aktiviteter schemaläggs på den här noden.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Anger ID för den datornod där aktivitets schemaläggningen är inaktive rad.

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
Anger ID för den gruppbearbetningssekvens som innehåller den datornod där aktivitets schemaläggningen är inaktive rad.

Om du använder parametern *PoolId* ska du inte använda parametern *ComputeNode* i samma kommando.

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

### BatchAccountContext
Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline

### PSComputeNode
Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Enable-AzureBatchComputeNodeScheduling](./Enable-AzureBatchComputeNodeScheduling.md)


