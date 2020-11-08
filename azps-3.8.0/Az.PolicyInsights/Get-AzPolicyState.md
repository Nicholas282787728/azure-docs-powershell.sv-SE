---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090705"
---
# Get-AzPolicyState

## Sammanfattning
Hämtar efterlevnadsprinciper för principer för resurser.

## FRÅGESYNTAXEN

### SubscriptionScope (standard)
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämtar efterlevnadsprinciper för principer för resurser. Poster för princip tillstånd kan frågas efter olika omfattningar. Baserat på det tidsintervall som anges (standard för förra dagen), kan antingen de senaste princip tillstånden eller alla över gångar för princip status ställas till. Resultaten kan filtreras, grupperas och grupp agg regeringar beräknas.

## BESKRIVS

### Exempel 1: Hämta de senaste princip tillstånden till aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyState
```

Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.

### Exempel 2: Hämta de senaste princip tillstånden i den angivna abonnemangs omfattningen
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom det angivna abonnemanget.

### Exempel 3: Hämta alla princip lägen i nuvarande prenumerations omfattning
```powershell
PS C:\> Get-AzPolicyState -All
```

Hämtar alla historiska princip tillstånds poster (inklusive senaste) som genererats av den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.

### Exempel 4: Hämta de senaste princip tillstånden i området hanterings grupp
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Hämtar de senaste princip tillstånds posterna som genererats för alla resurser i den angivna hanterings gruppen.

### Exempel 5: Hämta de senaste princip tillstånden i resurs gruppens omfattning i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser i den angivna resurs gruppen (i prenumerationen i den aktuella sessionen).

### Exempel 6: Hämta de senaste princip tillstånden i resurs gruppens omfattning i det angivna abonnemanget
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser i den angivna resurs gruppen (i det angivna abonnemanget).

### Exempel 7: Hämta de senaste princip tillstånden för en resurs
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Hämtar de senaste princip tillstånds posterna skapade den sista dagen för den angivna resursen.

### Exempel 8: Hämta de senaste princip tillstånden för en definition av en princip uppsättning i aktuellt abonnemang
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättningar (som finns i prenumerationen i den aktuella sessionen).

### Exempel 9: Hämta de senaste princip tillstånden för en definition av en princip uppsättning i det angivna abonnemanget
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättningar (som finns i den angivna prenumerationen).

### Exempel 10: Hämta de senaste princip tillstånden för en princip definition i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i prenumerationen i den aktuella sessionen).

### Exempel 11: Hämta de senaste princip tillstånden för en princip definition i det angivna abonnemanget
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i den angivna prenumerationen).

### Exempel 12: Hämta senaste policy tillstånd för en princip tilldelning i nuvarande abonnemang
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i prenumerationen i den aktuella sessionen).

### Exempel 13: Hämta de senaste princip tillstånden för en princip tilldelning i det angivna abonnemanget
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i den angivna prenumerationen).

### Exempel 14: Hämta de senaste princip tillstånden för en princip tilldelning i den angivna resurs gruppen i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar de senaste princip tillstånds posterna genererade under den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i resurs gruppen i prenumerationen i den aktuella sessionen).

### Exempel 15: Hämta de senaste princip lägena i aktuell prenumerations omfattning med OrderBy, Top och Select Query-alternativ
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen. Kommandot beställer resultaten efter tidsstämpel-och princip tilldelnings namn och tar bara upp 5 av de som listas i den ordningen.
Den väljer också att lista ut en delmängd av kolumnerna för varje post.

### Exempel 16: Hämta de senaste princip lägena i aktuell prenumerations omfattning med alternativen från och till fråga
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Hämtar de senaste princip tillstånds posterna som genererats inom det angivna datum intervallet för alla resurser i prenumerationen i den aktuella sessionen.

### Exempel 17: Hämta de senaste princip stegen i aktuellt prenumerations omfång med alternativet filtrera fråga
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.
Kommandot begränsar resultaten som returneras genom filtrering baserat på princip definitions åtgärden (inklusive neka-eller gransknings åtgärder), kompatibilitetsstatus (inkluderar endast icke-kompatibel status) och resurs plats (utesluter östasiatiska platser).

### Exempel 18: Hämta de senaste princip tillstånden i aktuell prenumerations omfattning med tillämpa ange radantal agg regering
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Hämtar antalet senaste princip status posterna som genererats den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen.
Kommandot returnerar antalet poster för princip tillstånd som returneras i egenskapen AdditionalProperties.

### Exempel 19: Hämta de senaste princip tillstånden i nuvarande prenumerations omfattning, med tillämpa ange gruppering med agg regering
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen. Kommandot begränsar resultaten som returneras genom filtrering baserat på kompatibilitetsstatus (inkluderar endast icke-kompatibel status).
Det grupperar resultaten baserat på princip tilldelning, princip uppsättnings definition och princip definition och beräknar antalet poster i varje grupp, som returneras i egenskapen AdditionalProperties.
Den bevarar resultaten utifrån mängd agg regering i fallande ordning och tar bara upp 5 av de som anges i den ordningen.

### Exempel 20: Hämta de senaste princip tillstånden i nuvarande prenumerations omfattning, med tillämpa ange gruppering utan agg regering
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen. Kommandot begränsar resultaten som returneras genom filtrering baserat på kompatibilitetsstatus (inkluderar endast icke-kompatibel status).
Resultatet grupperas utifrån resurs-ID. Då skapas en lista över alla resurser i prenumerationen som inte är kompatibla för minst en princip.

### Exempel 21: Hämta de senaste princip tillstånden i aktuell prenumerations omfattning, med tillämpa flera grupperingar
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Exempel 22: Hämta de senaste princip staterna inklusive policy utvärderings uppgifter för en resurs
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Hämtar de senaste princip tillstånds posterna skapade den sista dagen för alla resurser inom prenumerationen i den aktuella sessionen. Kommandot begränsar resultaten som returneras genom filtrering baserat på kompatibilitetsstatus (inkluderar endast icke-kompatibel status).
Det grupperar resultaten först baserat på princip tilldelning, princip uppsättnings definition, princip definiering och resurs-ID. Sedan grupperas resultaten av den här grupperingen med samma egenskaper förutom för resurs-ID och det beräknade antalet poster i var och en av de här grupperna, som returneras i egenskapen AdditionalProperties.
Den bevarar resultaten utifrån mängd agg regering i fallande ordning och tar bara upp 5 av de som anges i den ordningen.
Då skapas de 5 främsta principerna med flest antal icke-kompatibla resurser.

## MALLPARAMETRAR

### -Alla
I det angivna tidsintervallet får du alla princip lägen i stället för de senaste.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Expandera
Expandera uttryck med hjälp av OData-notation.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

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

### Microsoft. Azure. commands. PolicyInsights. Models. PolicyState

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
