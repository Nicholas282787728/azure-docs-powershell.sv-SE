---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228495"
---
# Get-AzEventGridTopic

## SYNOPSIS
Hämtar information om ett avsnitt i händelserutnätet eller får en lista över alla avsnitt i händelserutnätet i den aktuella Azure-prenumerationen.

## SYNTAX

### ResourceGroupNameParameterSet (standard)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Med Get-AzEventGridTopic-cmdleten får du antingen information om ett visst ämne i händelserutnätet eller en lista över alla avsnitt i händelserutnätet i den aktuella Azure-prenumerationen.
Om ämnesnamnet anges returneras information om ett enskilt händelserutnätsämne.
Om ämnesnamnet inte anges returneras en lista med ämnen. Antalet element som returneras i den här listan kontrolleras av den översta parametern. Om det översta värdet inte anges eller $null innehåller listan alla avsnittsobjekt. I annat fall anges det högsta antalet element som ska returneras i listan.
Om fler ämnen fortfarande är tillgängliga, ska värdet i NextLink användas i nästa samtal för att få nästa sida med ämnen.
Slutligen används ODataQuery-parametern för att utföra filtrering av sökresultaten. Filtreringsfrågan följer OData-syntaxen med egenskapen Namn. Exempel på åtgärder som stöds är: CONTAINS, eq (för lika med), ne (för inte lika med), AND, OR och NOT.

## EXEMPEL

### Exempel 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Hämtar information om ämnet Händelserutnät \` ämne1 \` i resursgruppen \` MyResourceGroupName. \`

### Exempel 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Hämtar information om ämnet Händelserutnät \` ämne1 \` i resursgruppen \` MyResourceGroupName. \`

### Exempel 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Lista alla avsnitt i händelserutnätet i resursgruppen \` MyResourceGroupName \` utan sidbrytning.

### Exempel 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Lista de första 10 avsnitten i händelserutnätet (om sådana finns) i resursgruppen \` MyResourceGroupName som uppfyller \` $odataFilter frågan. Om det finns fler resultat $result. NextLink kommer inte att $null. För att få nästa sida(er) med ämnen förväntas användaren ringa Get-AzEventGridTopic och använder resultat. NextLink från föregående samtal. Uppringaren bör sluta när resultatet är det. NextLink blir $null.

### Exempel 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Lista alla avsnitt i händelserutnätet i prenumerationen utan sidbrytningar.

### Exempel 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Lista de första tio avsnitten i händelserutnätet (om några) i prenumerationen som motsvarar $odataFilter frågan. Om det finns fler resultat $result. NextLink kommer inte att $null. För att få nästa sida(er) med ämnen förväntas användaren ringa Get-AzEventGridTopic och använder resultat. NextLink från föregående samtal. Uppringaren bör sluta när resultatet är det. NextLink blir $null.

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

### -Name
EventGrid Topic Name.

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
OData-frågan som används för att filtrera listresultaten. Filtrering är för närvarande endast tillåtet för egenskapen Namn. Exempel på åtgärder som stöds är: CONTAINS, eq (för lika med), ne (för inte lika med), AND, OR och NOT.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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
Resursidentifierare som representerar ämnet i händelserutnätet.

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

### -Top
Maximalt antal resurser som ska erhållas. Giltigt värde är mellan 1 och 100. Om det högsta värdet har angetts och fler resultat fortfarande är tillgängliga innehåller resultatet en länk till nästa sida som du vill fråga i NextLink. Om det högsta värdet inte anges returneras den fullständiga listan med resurser på en gång.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
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

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## UTDATA

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance

## ANTECKNINGAR

## RELATERADE LÄNKAR
