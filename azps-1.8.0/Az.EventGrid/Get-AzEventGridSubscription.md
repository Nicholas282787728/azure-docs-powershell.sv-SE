---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754110"
---
# Get-AzEventGridSubscription

## Sammanfattning
Hämtar information om en händelse prenumeration eller hämtar en lista över alla händelse prenumerationer i det aktuella Azure-abonnemanget.

## FRÅGESYNTAXEN

### EventSubscriptionTopicNameParameterSet (standard)
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Get-AzEventGridSubscription-cmdleten får antingen information om ett angivet abonnemang för händelse rutnät eller en lista över alla prenumerationer i det aktuella Azure-abonnemanget eller resurs gruppen.
Om händelse prenumerationens namn anges returneras informationen om ett enskilt rutnäts abonnemang.
Om händelse prenumerationens namn inte anges returneras en lista över alla händelse prenumerationer.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Hämtar information om händelse abonnemangs \` EventSubscription1 \` som har skapats för ämne \` Ämne1 \` i resurs grupp \` MyResourceGroupName \` .

### Exempel 2
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Hämtar information om händelse abonnemangs \` EventSubscription1 \` som har skapats för ämne \` Ämne1 \` i resurs grupps \` MyResourceGroupName \` , inklusive fullständig slut punkts-URL om det är en webhook-baserad händelse prenumeration.

### Exempel 3
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Få en lista över alla händelse prenumerationer som har skapats för ämnet \` Ämne1 \` i resurs gruppen \` MyResourceGroupName \` .

### Exempel 4
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Hämtar information om händelse prenumerations \` EventSubscription1 \` som har skapats för resurs grupps \` MyResourceGroupName \` .

### Exempel 5
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Hämtar information om \` EventSubscription1 som \` skapats för den valda Azure-prenumerationen.

### Exempel 6
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Hämtar listan över alla globala händelse prenumerationer som skapas under resurs gruppen \` MyResourceGroupName \` .

### Exempel 7
```
PS C:\> Get-AzEventGridSubscription
```

Hämtar listan över alla globala händelse prenumerationer som har skapats under det markerade Azure-abonnemanget.

### Exempel 8
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Hämtar listan över alla regionala händelse prenumerationer som skapats under resurs grupp \` MyResourceGroupName \` på den angivna platsen \` westus2 \` .

### Exempel 9
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Hämtar listan över alla händelse prenumerationer som har skapats för det angivna EventHub-namnområdet.

### Exempel 10
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Hämtar listan över alla händelse prenumerationer som har skapats för den angivna ämnes typen (EventHub-namnområden) på den angivna platsen.

### Exempel 11
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Hämtar listan över alla händelse prenumerationer som har skapats för den specifika resurs gruppen.

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

### -EventSubscriptionName
Namnet på händelse prenumerationen

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Ange fullständig slut punkts-URL för händelse prenumerationens destination.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
EventGrid ämne.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Plats
Plats

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identifierare för den resurs som händelse prenumerationer har skapats för.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
Namn på EventGrid-avsnitt.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
TopicType namn

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. EventGrid. Models. PSTopic

## VÄRDEN

### Microsoft. Azure. commands. EventGrid. Models. PSEventSubscription

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
