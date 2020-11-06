---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 8ea4fc7674af247ffded2c6c4317f07a831adf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582448"
---
# Get-AzureRmEventGridTopic

## Sammanfattning
Hämtar information om ett ämne i händelse rutnätet eller hämtar en lista över alla händelse rutnät i det aktuella Azure-abonnemanget.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ResourceGroupNameParameterSet (standard)
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Get-AzureRmEventGridTopic-cmdleten får information om ett visst ämne i händelse rutnät, eller en lista över alla händelse rutnät i det aktuella Azure-abonnemanget.
Om ämnets namn är angivet returneras informationen om ett avsnitt med en enskild händelse.
Om ämnets namn inte anges returneras en lista med avsnitt.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Hämtar information om ämnet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .

### Exempel 2
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Hämtar information om ämnet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .

### Exempel 3
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

Lista alla ämnen i MyResourceGroupName i resurs gruppen \` \` .

### Exempel 4
```
PS C:\> Get-AzureRmEventGridTopic
```

Lista alla ämnen för händelse rutnät i prenumerationen.

## MALLPARAMETRAR

### -Namn
Namn på EventGrid-avsnitt.

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Resurs-ID som representerar avsnittet händelse rutnät.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String
Microsoft. Azure. commands. EventGrid. Models. PSTopic

## VÄRDEN

### Microsoft. Azure. commands. EventGrid. Models. PSTopic
System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventGrid. Models. PSTopicListInstance, Microsoft. Azure. commands. EventGrid, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

