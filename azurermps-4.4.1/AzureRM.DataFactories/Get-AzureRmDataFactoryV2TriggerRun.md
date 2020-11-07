---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
ms.openlocfilehash: 7d3f1ca73712753ad38b46c186a51bd7aa159b46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755502"
---
# Get-AzureRmDataFactoryV2TriggerRun

## Sammanfattning
Returnerar information om trigger körs.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByFactoryName (standard)
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Kommandot **Get-AzureRmDataFactoryV2TriggerRun** returnerar detaljerad information om trigger körs för den angivna utlösaren under den angivna tids perioden.

## BESKRIVS

### Exempel 1: få information om trigger-körning
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

Det här kommandot visar information om hur du kör "WikiTrigger" i fabriken "WikiADF" som startade med "2017-09-01" och "2019-09-30".

## MALLPARAMETRAR

### -DataFactory
Data fabriks objekt.

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DataFactoryName
Namnet på data fabriken.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Utlösarens namn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs gruppens namn.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TriggerRunStartedAfter
Den tid eller det klock slag då trigger körs i ISO8601-format.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TriggerRunStartedBefore
Den tid som en utlöses innan körningen körs i ISO8601-format.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
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

### Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
System. String

## VÄRDEN

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Start-AzureRmDataFactoryV2Trigger]()

[Stopp-AzureRmDataFactoryV2Trigger]()

