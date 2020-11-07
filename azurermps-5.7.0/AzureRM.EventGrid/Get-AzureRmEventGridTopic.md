---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: e71c479624cd77e25adbd4fbfdc609cfa89918b3
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93758445"
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

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -Namn
Namn på EventGrid-avsnitt.

```yaml
Type: String
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
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
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
Type: String
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
Microsoft. Azure. commands. EventGrid. Models. PSTopic

## VÄRDEN

### Microsoft. Azure. commands. EventGrid. Models. PSTopic
System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventGrid. Models. PSTopicListInstance, Microsoft. Azure. commands. EventGrid, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

