---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214806"
---
# Get-AzEventGridSubscription

## SYNOPSIS
Hämtar information om en händelseprenumeration eller får en lista över alla händelseprenumerationer i den aktuella Azure-prenumerationen.

## SYNTAX

### EventSubscriptionTopicNameParameterSet (Standard)
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Med Get-AzEventGridSubscription-cmdleten får du antingen information om en viss prenumeration på händelserutnätet eller en lista över alla Event Grid-prenumerationer i den aktuella Azure-prenumerationen eller resursgruppen.
Om händelsens prenumerationsnamn anges returneras information om en enskild prenumeration på händelserutnätet.
Om händelsens prenumerationsnamn inte anges returneras en lista över alla händelseprenumerationer. Antalet element som returneras i den här listan kontrolleras av den översta parametern. Om det högsta värdet inte anges $null objekten, innehåller listan alla objekt i händelseprenumerationen. I annat fall anges det högsta antalet element som ska returneras i listan.
Om fler händelseprenumerationer fortfarande är tillgängliga ska värdet i NextLink användas i nästa samtal för att få nästa sida med händelseprenumerationer.
Slutligen används ODataQuery-parametern för att utföra filtrering av sökresultaten. Filtreringsfrågan följer OData-syntaxen med egenskapen Namn. Exempel på åtgärder som stöds: CONTAINS, eq (för lika med), ne (för inte lika med), AND, OR och NOT.

## EXEMPEL

### Exempel 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Hämtar information om händelseprenumeration \` EventSubscription1 som skapats för \` ämne \` Ämne1 i \` \` resursgruppen MyResourceGroupName. \`

### Exempel 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Hämtar information om händelseprenumeration EventSubscription1 som skapats för ämnet Ämne1 i resursgruppen MyResourceGroupName, inklusive den fullständiga slutpunkts-URL:en om det är en \` \` \` \` \` \` webhook-baserad händelseprenumeration.

### Exempel 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Hämta en lista över alla händelseprenumerationer som skapats för \` ämne1 \` i resursgruppen \` MyResourceGroupName \` utan sidbrytning.

### Exempel 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista de första 10 händelseprenumerationer (om några) som skapats för ämne Ämne1 i resursgruppen \` \` \` MyResourceGroupName som uppfyller \` $odataFilter frågan. Om det finns fler resultat $result. NextLink kommer inte att $null. För att få nästa sida eller sida i händelseprenumerationer förväntas användaren ringa Get-AzEventGridSubscription och använder resultat. NextLink från föregående samtal. Uppringaren bör sluta när resultatet är det. NextLink blir $null.

### Exempel 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Hämtar information om händelseprenumeration \` EventSubscription1 \` som skapats för \` resursgruppen MyResourceGroupName. \`

### Exempel 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Hämtar information om händelseprenumerationen \` EventSubscription1 \` som skapats för den valda Azure-prenumerationen.

### Exempel 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Hämtar listan över alla globala händelseprenumerationer som skapats under \` resursgruppen MyResourceGroupName \` utan sidbrytning.

### Exempel 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista de första fem händelseprenumerationer (om det finns) som skapats under resursgruppen \` MyResourceGroupName som uppfyller \` $odataFilter frågan. Om det finns fler resultat $result. NextLink kommer inte att $null. För att få nästa sida eller sida i händelseprenumerationer förväntas användaren ringa Get-AzEventGridSubscription och använder resultat. NextLink från föregående samtal. Uppringaren bör sluta när resultatet är det. NextLink blir $null.

### Exempel 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Hämtar listan över alla globala händelseprenumerationer som skapats under den för tillfället valda Azure-prenumerationen utan sidnumrering.

### Exempel 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista de första 15 globala händelseprenumerationerna (om det finns) som skapats under den valda Azure-prenumerationen och som uppfyller $odataFilter frågan. Om det finns fler resultat $result. NextLink kommer inte att $null. För att få nästa sida eller sida i händelseprenumerationer förväntas användaren ringa Get-AzEventGridSubscription och använder resultat. NextLink från föregående samtal. Uppringaren bör sluta när resultatet är det. NextLink blir $null.

### Exempel 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Hämtar listan över alla regionala händelseprenumerationer som skapats under resursgruppen \` MyResourceGroupName på den \` angivna platsen \` westus2 \` utan sidbrytning.

### Exempel 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista de första 15 regionala händelseprenumerationer (om några) som skapats under resursgruppen MyResourceGroupName på den angivna platsen westus2 som uppfyller \` \` $odataFilter \` \` frågan. Om det finns fler resultat $result. NextLink kommer inte att $null. För att få nästa sida eller sida i händelseprenumerationer förväntas användaren ringa Get-AzEventGridSubscription och använder resultat. NextLink från föregående samtal. Uppringaren bör sluta när resultatet är det. NextLink blir $null.

### Exempel 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Hämtar listan över alla händelseprenumerationer som skapats för det angivna EventHub-namnområdet utan sidbrytning.

### Exempel 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista de första 25 händelseprenumerationer (om det finns) som skapats för det angivna Namnområdet i EventHub som uppfyller $odataFilter frågan. Om det finns fler resultat $result. NextLink kommer inte att $null. För att få nästa sida eller sida i händelseprenumerationer förväntas användaren ringa Get-AzEventGridSubscription och använder resultat. NextLink från föregående samtal. Uppringaren bör sluta när resultatet är det. NextLink blir $null.

### Exempel 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Hämtar listan över alla händelseprenumerationer som skapats för den angivna ämnestypen (EventHub-namnområden) på den angivna platsen utan sidbrytning.

### Exempel 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista de första 15 händelseprenumerationer (om det finns) som skapats för den angivna ämnestypen (EventHub-namnområden) på den angivna platsen som motsvarar $odataFilter frågan. Om det finns fler resultat $result. NextLink kommer inte att $null. För att få nästa sida eller sida i händelseprenumerationer förväntas användaren ringa Get-AzEventGridSubscription och använder resultat. NextLink från föregående samtal. Uppringaren bör sluta när resultatet är det. NextLink blir $null.

### Exempel 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Hämtar listan över alla händelseprenumerationer som skapats för den specifika resursgruppen utan sidbrytning.

### Exempel 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista de första 100 händelseprenumerationer (om det finns) som skapats för den specifika resursgrupp som uppfyller $odataFilter frågan. Om det finns fler resultat $result. NextLink kommer inte att $null. För att få nästa sida eller sida i händelseprenumerationer förväntas användaren ringa Get-AzEventGridSubscription och använder resultat. NextLink från föregående samtal. Uppringaren bör sluta när resultatet är det. NextLink blir $null.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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

### -DomainInputObject
EventGrid Domain-objekt.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainName
EventGrid-domännamn.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
EventGrid Domain Topic-objekt.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
Domännamn för EventGrid-domän.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
Namnet på händelseprenumerationen

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Inkludera hela slutpunkts-URL:en för målet för händelseprenumerationen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
EventGrid Topic-objekt.

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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Länken för nästa sida med resurser som ska erhållas. Det här värdet inhämtas med det Get-AzEventGrid cmdlet-anropet när fler resurser fortfarande är tillgängliga för frågor.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
OData-frågan som används för att filtrera listresultaten. Filtrering är för närvarande endast tillåtet för egenskapen Namn. Exempel på åtgärder som stöds: CONTAINS, eq (för lika med), ne (för inte lika med), AND, OR och NOT.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resursgruppnamn.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identifierare för resursen som händelseprenumerationer har skapats för.

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

### -Top
OData-frågan som används för att filtrera listresultaten. Filtrering är för närvarande endast tillåtet för egenskapen Namn. Exempel på åtgärder som stöds: CONTAINS, eq (för lika med), ne (för inte lika med), AND, OR och NOT.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
EventGrid Topic Name.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
TopicType-namn

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## UTDATA

### Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription

## ANTECKNINGAR

## RELATERADE LÄNKAR
