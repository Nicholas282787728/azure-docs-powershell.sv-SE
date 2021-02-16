---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233639"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
Inaktiverar schemaläggning av aktiviteter på den angivna beräkningsnoden.

## SYNTAX

### ID (standard)
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Disable-AzBatchComputeNodeScheduling** inaktiverar schemaläggning av aktiviteter på den angivna beräkningsnoden.
En beräkningsnod är en virtuell Azure-dator som är dedikerad till en viss programarbetsbelastning.
När du inaktiverar schemaläggning av aktiviteter på en beräkningsnod kan du också bestämma vad du ska göra med jobb som finns i nodens aktivitetskö.
**Disable-AzBatchComputeNodeScheduling** lets you do the following: 
- Avbryt aktiviteterna och placera dem i jobbkön igen.
Det här gör att aktiviteterna schemalades om på en annan beräkningsnod. 
- Avsluta aktiviteterna och ta bort dem från jobbkön.
Uppgifter som stoppas på det här sättet schemalades inte om. 
- Vänta tills alla aktiviteter som körs för närvarande slutförs och inaktivera sedan schemaläggning av aktiviteter på beräkningsnoden. 
- Vänta tills alla aktiviteter som körs slutförs och alla databevarandeperioder upphör att gälla, och inaktivera sedan schemaläggning av aktiviteter på beräkningsnoden.

## EXEMPEL

### Exempel 1: Inaktivera schemaläggning av aktiviteter på en beräkningsnod
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Dessa kommandon inaktiverar aktivitetsschema på compute node tvm-1783593343_34-20151117t222514z.
Det gör du genom att det första kommandot i exemplet skapar en objektreferens till kontonycklarna för batchkontot contosobatchaccount.
Den här objektreferensen lagras i en variabel med namnet $context.
Det andra kommandot använder sedan den här objektreferensen och cmdleten **Disable-AzBatchComputeNodeScheduling** för att ansluta till pool myPool och inaktivera schemaläggning av aktiviteter på node tvm-1783593343_34-2015117t222514z.
Eftersom *parametern DisableComputeNodeSchedulingOptions* inte inkluderades några aktiviteter som körs på beräkningsnoden igen.

### Exempel 2: Inaktivera schemaläggning av aktiviteter på alla beräkningsnoder i en pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

De här kommandona inaktiverar schemaläggning av aktiviteter på alla datornoder i batchpoolen 06.
För att utföra den här uppgiften skapar det första kommandot i exemplet en objektreferens till kontonycklarna för batchkontot contosobatchaccount.
Den här objektreferensen lagras i en variabel med namnet $context.
Det andra kommandot i exemplet använder sedan den här objektreferensen och **Get-AzBatchComputeNode** för att returnera en samling av alla beräkningsnoder som finns i Pool06.
Samlingen förs sedan i en piped till cmdleten **Disable-AzBatchComputeNodeScheduling** för att inaktivera schemaläggning av aktiviteter för varje beräkningsnod i samlingen.
Eftersom *parametern DisableComputeNodeSchedulingOptions* inte inkluderades några uppgifter som körs på beräkningsnoderna igen.

## PARAMETERS

### -BatchContext
Anger den **BatchAccountContext-instans** som denna cmdlet använder för att interagera med batchtjänsten.
Om du använder Get-AzBatchAccount-cmdleten för att hämta BatchAccountContext används Azure Active Directory-autentisering när du interagerar med batchtjänsten. Om du vill använda autentisering med delad nyckel i Get-AzBatchAccountKey använder du cmdleten för att få ett BatchAccountContext-objekt med dess snabbtangenter ifyllda. När du använder autentisering med delad nyckel används primärnyckeln som standard. Om du vill ändra nyckeln som ska användas anger du egenskapen BatchAccountContext.KeyInUse.

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
Anger en objektreferens till beräkningsnoden där schemaläggning av aktiviteter är inaktiverad.
Den här objektreferensen skapas med hjälp Get-AzBatchComputeNode cmdlet och lagrar det returnerade beräkningsnodobjektet i en variabel.

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
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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

### -DisableSchedulingOption
Anger hur den här cmdleten hanterar alla aktiviteter som körs på den datornod där schemaläggningen inaktiveras.
De godtagbara värdena för den här parametern är:
- Requeue.
Aktiviteter stoppas direkt och returneras till jobbkön.
Det här gör att aktiviteterna kan schemaas om på en annan beräkningsnod.
Det här är standardvärdet. 
- Avbryt.
Aktiviteter stoppas omedelbart och tas bort från jobbkön.
De här uppgifterna schemaas inte om. 
- TaskCompletion.
Aktiviteter som för närvarande körs kan slutföras innan schemaläggning av aktiviteter inaktiveras på beräkningsnoden.
Inga nya aktiviteter schemaläggs på den här noden. 
- RetainedData.
Aktiviteter som för närvarande körs kan slutföras och datalagringsperioder kan upphöra innan schemaläggning av aktiviteter inaktiveras på beräkningsnoden.
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

### -Id
Anger ID för beräkningsnoden där schemaläggning av aktiviteter är inaktiverat.

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
Anger ID för batchpoolen som innehåller beräkningsnoden där schemaläggning av aktiviteter inaktiveras.
Om du använder *PoolId-parametern* ska du inte använda *parametern ComputeNode* i samma kommando.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Batkap. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## UTDATA

### System.Void

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


