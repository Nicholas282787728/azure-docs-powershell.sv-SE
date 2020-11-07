---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 23004583a08dbcf5ef8785b62d0457b6b6ee0897
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754108"
---
# Get-AzEventGridTopic

## Sammanfattning
Hämtar information om ett ämne i händelse rutnätet eller hämtar en lista över alla händelse rutnät i det aktuella Azure-abonnemanget.

## FRÅGESYNTAXEN

### ResourceGroupNameParameterSet (standard)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Get-AzEventGridTopic-cmdleten får information om ett visst ämne i händelse rutnät, eller en lista över alla händelse rutnät i det aktuella Azure-abonnemanget.
Om ämnets namn är angivet returneras informationen om ett avsnitt med en enskild händelse.
Om ämnets namn inte anges returneras en lista med avsnitt.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Hämtar information om ämnet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .

### Exempel 2
```
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Hämtar information om ämnet \` Ämne1 \` i MyResourceGroupName i resurs gruppen \` \` .

### Exempel 3
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Lista alla ämnen i MyResourceGroupName i resurs gruppen \` \` .

### Exempel 4
```
PS C:\> Get-AzEventGridTopic
```

Lista alla ämnen för händelse rutnät i prenumerationen.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. EventGrid. Models. PSTopic

### Microsoft. Azure. commands. EventGrid. Models. PSTopicListInstance

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
