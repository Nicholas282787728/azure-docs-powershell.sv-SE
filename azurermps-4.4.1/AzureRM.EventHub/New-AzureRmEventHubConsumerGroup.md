---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758085"
---
# New-AzureRmEventHubConsumerGroup

## Sammanfattning
Skapar en ny konsument grupp för den angivna Händelsehubben.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## PROBLEMBESKRIVNING
New-AzureRmEventHubConsumerGroup-cmdleten skapar en ny konsument grupp för den angivna Händelsehubben.

## BESKRIVS

### Exempel 1
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

Skapar gruppen konsument MyConsumerGroupName i MyEventHubName som bevaras \` \` \` \` till namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .

## MALLPARAMETRAR

### -ResourceGroupName
Resurs grupps namn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserMetadata
Användarens metadata för konsument gruppen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventHub
Namn på EventHub.

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
ConsumerGroup namn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namnrymd
Namn på namn området.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. EventHub. Models. ConsumerGroupAttributes

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

