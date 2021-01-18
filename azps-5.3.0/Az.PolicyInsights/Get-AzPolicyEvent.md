---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521788"
---
# Get-AzPolicyEvent

## Sammanfattning
Hämtar princip utvärderings händelser som uppstår när resurser skapas eller uppdateras.

## FRÅGESYNTAXEN

### SubscriptionScope (standard)
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämtar princip utvärderings händelser som uppstår när resurser skapas eller uppdateras. Poster i princip händelser kan frågas efter olika omfattningar baserat på det tidsintervall du angett (standard). Resultaten kan filtreras, grupperas och grupp agg regeringar beräknas.

## BESKRIVS

### Exempel 1: Hämta princip händelser i aktuell prenumerations omfattning
```powershell
PS C:\> Get-AzPolicyEvent
```

Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.

### Exempel 2: Hämta princip händelser i den angivna abonnemangs omfattningen
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Hämtar princip händelse poster genererade under den sista dagen för alla resurser inom det angivna abonnemanget.

### Exempel 3: Hämta princip händelser i omfattning för hanterings grupp
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

Hämtar princip händelser genererade den sista dagen för alla resurser i den angivna hanterings gruppen.

### Exempel 4: Hämta princip händelser i resurs gruppens omfattning i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

Hämtar princip händelse poster genererade under den sista dagen för alla resurser i den angivna resurs gruppen (i prenumerationen i den aktuella sessionen).

### Exempel 5: Hämta princip händelser i resurs gruppens omfattning i det angivna abonnemanget
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Hämtar princip händelse poster genererade under den sista dagen för alla resurser i den angivna resurs gruppen (i det angivna abonnemanget).

### Exempel 6: Hämta princip händelser för en resurs
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Hämtar princip händelser genererade den sista dagen för den angivna resursen.

### Exempel 7: Hämta princip händelser för en definition av en princip uppsättning i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättning (som finns i prenumerationen i den aktuella session-kontexten).

### Exempel 8: Hämta princip händelser för en definition av en princip uppsättning i det angivna abonnemanget
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättningar (som finns i den angivna prenumerationen).

### Exempel 9: Hämta princip händelser för en princip definition i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i prenumerationen i den aktuella sessionen).

### Exempel 10: Hämta princip händelser för en princip definition i det angivna abonnemanget
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i det angivna abonnemanget).

### Exempel 11: Hämta princip händelser för en princip tilldelning i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i prenumerationen i den aktuella sessionen).

### Exempel 12: Hämta princip händelser för en princip tilldelning i det angivna abonnemanget
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i den angivna prenumerationen).

### Exempel 13: Hämta princip händelser för en princip tilldelning i den angivna resurs gruppen i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar princip händelse poster som genereras under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionskatalogen) som tillämpas av den angivna princip tilldelningen (som finns i resurs gruppen i prenumerationen i den aktuella sessionen).

### Exempel 14: Hämta princip händelser i aktuell prenumerations omfattning med OrderBy, Top och Select Query-alternativ
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen. Kommandot beställer resultaten efter tidsstämpel-och princip tilldelnings namn och tar bara upp 5 av de som listas i den ordningen.
Den väljer också att lista ut en delmängd av kolumnerna för varje post.

### Exempel 15: Hämta princip händelser i aktuell prenumerations omfattning med alternativen från och till fråga
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Hämtar princip händelse poster som genereras inom det datum intervall som anges för alla resurser i prenumerationen i den aktuella sessionen.

### Exempel 16: Hämta princip händelser i aktuell prenumerations omfattning med alternativet filtrera fråga
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.
Kommandot begränsar resultaten som returneras genom filtrering baserat på princip definitions åtgärden (inklusive neka-eller gransknings åtgärder) och resurs plats (exklusive östasiatiska platser).

### Exempel 17: Hämta princip händelser i aktuell prenumerations omfattning med tillämpa ange radantal agg regering
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Hämtar antalet princip händelse poster som genererats under den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.
Kommandot returnerar antalet princip poster, som returneras i egenskapen AdditionalProperties.

### Exempel 18: Hämta princip händelser i aktuell prenumerations omfattning med tillämpa ange gruppering med agg regering
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen. Kommandot begränsar resultaten som returneras genom filtrering baserat på princip definitions åtgärden (inkluderar endast gransknings-och avvisa händelser).
Det grupperar resultaten baserat på princip tilldelning, princip definiering, princip definierings åtgärd och resurs-ID, och beräknar antalet poster i varje grupp, som returneras i egenskapen AdditionalProperties.
Den bevarar resultaten utifrån mängd agg regering i fallande ordning och tar bara upp 5 av de som anges i den ordningen.

### Exempel 19: Hämta princip händelser i aktuell prenumerations omfattning med tillämpa ange gruppering utan agg regering
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen. Kommandot begränsar resultaten som returneras genom filtrering baserat på princip definitions åtgärden (inkluderar endast gransknings-och avvisa händelser).
Resultatet grupperas utifrån resurs-ID. Då skapas en lista över alla resurser i prenumerationen som genererade en princip händelse för minst en gransknings-eller nekande policy.

### Exempel 20: Hämta princip händelser i aktuell prenumerations omfattning med tillämpa flera grupperingar
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Hämtar princip händelse poster genererade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen. Kommandot begränsar resultatet som returneras genom filtrering baserat på princip definitions åtgärden (inkluderar endast neka-händelser).
Resultatet grupperas först baserat på princip tilldelning, princip definiering och resurs-ID. Sedan grupperas resultaten av den här grupperingen med samma egenskaper förutom för resurs-ID och det beräknade antalet poster i var och en av de här grupperna, som returneras i egenskapen AdditionalProperties.
Den bevarar resultaten utifrån mängd agg regering i fallande ordning och tar bara upp 5 av de som anges i den ordningen.
Då skapas de 5 högsta neka-principerna med flest nekade resurser.

## MALLPARAMETRAR

### -Koppla
Använd uttryck för agg regeringar med OData-notation.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -Filter
Filter uttryck med hjälp av OData-notation.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Från
ISO 8601 formaterad tidsstämpel anger start tiden för det intervall som ska frågas.
Om du inte anger något värde används värdet "till" minus 1 dag.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
Namn på hanterings grupp.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
Beställnings uttryck med hjälp av OData-notation.
Ett eller flera kommaseparerade kolumn namn med "DESC" (standard) eller "ASC".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyAssignmentName
Namn på princip tilldelning.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
Princip definitions namn.

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
Definitions namn för princip uppsättning.

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Resurs-ID.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Välj
Välj uttryck med hjälp av OData-notation.
Ett eller flera kommaseparerade kolumn namn.
Begränsar kolumnerna för varje post till de begärda.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Abonnemangs-ID.

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -För att
ISO 8601 formaterad tidsstämpel som anger slut tiden för intervallet att fråga.
Om du inte anger det här är standardvärdet för tid.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Överst
Maximalt antal poster att returnera.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. PolicyInsights. Models. PolicyEvent

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
