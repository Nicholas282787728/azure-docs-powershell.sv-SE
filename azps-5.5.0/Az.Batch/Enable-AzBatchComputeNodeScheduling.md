---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100251668"
---
# Enable-AzBatchComputeNodeScheduling

## SYNOPSIS
Aktiverar schemaläggning av aktiviteter på den angivna beräkningsnoden.

## SYNTAX

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

## BESKRIVNING
**Cmdleten Enable-AzBatchComputeNodeScheduling** aktiverar schemaläggning av aktiviteter på den angivna beräkningsnoden.
En beräkningsnod är en virtuell Azure-dator som är dedikerad till en viss programarbetsbelastning.

## EXEMPEL

### Exempel 1: Aktivera schemaläggning av aktiviteter på en beräkningsnod
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

De här kommandona aktiverar schemaläggning av aktiviteter på compute node tvm-1783593343_34-20151117t222514z.
Det gör du genom att det första kommandot i exemplet skapar en objektreferens som innehåller kontonycklarna för batchkontot contosobatchaccount.
Den här objektreferensen lagras i en variabel med namnet $context.
Det andra kommandot använder sedan den här objektreferensen och cmdleten **Enable-AzBatchComputeNodeScheduling** för att ansluta till pool myPool och aktivera schemaläggning av aktiviteter på tvm-1783593343_34-2015117t222514z.

### Exempel 2: Aktivera schemaläggning av aktiviteter på beräkningsnoder i en pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

De här kommandona aktiverar schemaläggning av aktiviteter på alla beräkningsnoder som finns i poolpoolen06.
För att utföra den här uppgiften skapar det första kommandot i exemplet en objektreferens som innehåller kontonycklarna för batchkontot contosobatchaccount.
Den här objektreferensen lagras i en variabel med namnet $context.
Det andra kommandot i exemplet använder sedan den här objektreferensen och **Get-AzBatchComputeNode** för att returnera en samling av alla beräkningsnoder som finns i Pool06.
Samlingen piperas sedan till cmdleten **Enable-AzBatchComputeNodeScheduling,** som aktiverar schemaläggning av aktiviteter för varje beräkningsnod i samlingen.

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
Anger en objektreferens till beräkningsnoden där schemaläggning av aktiviteter är aktiverat.
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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -Id
Anger ID för beräkningsnoden där schemaläggning av aktiviteter är aktiverat.

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
Anger ID för batchpoolen som innehåller beräkningsnoden där schemaläggning av aktiviteter är aktiverat.

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

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


