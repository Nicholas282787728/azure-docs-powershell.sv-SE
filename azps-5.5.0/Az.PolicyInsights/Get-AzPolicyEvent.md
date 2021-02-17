---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227254"
---
# Get-AzPolicyEvent

## SYNOPSIS
Får principutvärderingshändelser som genereras när resurser skapas eller uppdateras.

## SYNTAX

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

## BESKRIVNING
Får principutvärderingshändelser som genereras när resurser skapas eller uppdateras. Principhändelseposter kan tillfrågas med olika omfattningar baserat på det tidsintervall som angetts (standardinställningen är sista dagen). Resultaten kan filtreras, grupperas och gruppaggregeringar kan beräknas.

## EXEMPEL

### Exempel 1: Hämta principhändelser i den aktuella prenumerationsomfånget
```powershell
PS C:\> Get-AzPolicyEvent
```

Får principhändelseposter som genereras under den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget.

### Exempel 2: Hämta principhändelser i den angivna prenumerationsomfånget
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Får principhändelseposter som genereras under den sista dagen för alla resurser inom den angivna prenumerationen.

### Exempel 3: Hämta principhändelser i hanteringsgruppens omfattning
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

Får principhändelseposter som genereras under den sista dagen för alla resurser i den angivna hanteringsgruppen.

### Exempel 4: Hämta principhändelser i resursgruppomfattningen i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

Får principhändelseposter som genererats den sista dagen för alla resurser inom den angivna resursgruppen (i prenumerationen i aktuellt sessionssammanhang).

### Exempel 5: Hämta principhändelser i resursgruppomfattningen i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Får principhändelseposter som genereras under den sista dagen för alla resurser inom den angivna resursgruppen (i den angivna prenumerationen).

### Exempel 6: Hämta principhändelser för en resurs
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Får principhändelseposter som genereras under den sista dagen för den angivna resursen.

### Exempel 7: Hämta principhändelser för en principuppsättningsdefinition i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Får principhändelseposter som genereras den sista dagen för alla resurser (inom klientorganisationen i aktuellt sessionssammanhang) som påverkas av den angivna principuppsättningsdefinitionen (som finns i prenumerationen i det aktuella sessionssammanhanget).

### Exempel 8: Hämta principhändelser för en principuppsättningsdefinition i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Får principhändelseposter som genereras under den sista dagen för alla resurser (inom klientorganisationen i aktuellt sessionssammanhang) som påverkas av den angivna principuppsättningsdefinitionen (som finns i den angivna prenumerationen).

### Exempel 9: Hämta principhändelser för en principdefinition i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Får principhändelseposter som genereras den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) som genereras av den angivna principdefinitionen (som finns i prenumerationen i det aktuella sessionssammanhanget).

### Exempel 10: Hämta principhändelser för en principdefinition i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Får principhändelseposter som genereras den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) som genereras av den angivna principdefinitionen (som finns i den angivna prenumerationen).

### Exempel 11: Hämta principhändelser för en principtilldelning i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Får principhändelseposter som genereras den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) som genereras av den angivna principtilldelningen (som finns i prenumerationen i det aktuella sessionssammanhanget).

### Exempel 12: Hämta principhändelser för en principtilldelning i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Får principhändelseposter som genereras under den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) som genereras av den angivna principtilldelningen (som finns i den angivna prenumerationen).

### Exempel 13: Hämta principhändelser för en principtilldelning i den angivna resursgruppen i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Får principhändelseposter som genereras den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) som genereras av den angivna principtilldelningen (som finns i resursgruppen i prenumerationen i aktuellt sessionssammanhang).

### Exempel 14: Hämta principhändelser i den aktuella prenumerationen med Hjälp av frågealternativen OrderBy, Top och Select
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Får principhändelseposter som genereras under den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget. Kommandot beställer resultatet efter namnegenskaper för tidsstämpel och principtilldelning och tar endast upp 5 av de som visas i den ordningen.
Den väljer också att endast visa en delmängd av kolumnerna för varje post.

### Exempel 15: Hämta principhändelser i den aktuella prenumerationen med frågealternativen Från och Till
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Får principhändelseposter som genereras inom det datumintervall som har angetts för alla resurser i prenumerationen i det aktuella sessionssammanhanget.

### Exempel 16: Hämta principhändelser i aktuell prenumerations omfattning med alternativet Filtrera fråga
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Får principhändelseposter som genereras under den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget.
Kommandot begränsar resultatet som returneras av filtrering baserat på principdefinitionsåtgärd (omfattar åtgärder för nekad eller granskning) och resursplats (exkluderar plats för öst).

### Exempel 17: Hämta principhändelser i aktuell prenumerationsomfång, med Använd ange aggregering för radantal
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Hämtar antalet principhändelseposter som genereras den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget.
Kommandot returnerar antalet endast för principhändelseposter, som returneras i egenskapen AdditionalProperties.

### Exempel 18: Hämta principhändelser i aktuell prenumerationsomfång, med Använd ange gruppering med aggregering
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Får principhändelseposter som genereras under den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget. Kommandot begränsar resultatet som returneras av filtrering baserat på principdefinitionsåtgärd (omfattar endast gransknings- och neka-händelser).
Grupperar resultaten baserat på principtilldelning, principdefinition, principdefinitionsåtgärd och resurs-ID och beräknar antalet poster i varje grupp, som returneras i egenskapen AdditionalProperties.
Resultatet ordnas efter antal-aggregering i fallande ordning och tar endast upp 5 av de som anges i den ordningen.

### Exempel 19: Hämta principhändelser i aktuell prenumerationsomfång, med Använd ange gruppering utan aggregering
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Får principhändelseposter som genereras under den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget. Kommandot begränsar resultatet som returneras av filtrering baserat på principdefinitionsåtgärd (omfattar endast gransknings- och neka-händelser).
Resultatet grupperar baserat på resurs-ID. Det här genererar listan över alla resurser i prenumerationen som genererade en principhändelse för minst en gransknings- eller neka-princip.

### Exempel 20: Hämta principhändelser i den aktuella prenumerationsomfattningen, med Använd och ange flera gruppering
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Får principhändelseposter som genereras under den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget. Kommandot begränsar resultatet som returneras av filtrering baserat på principdefinitionsåtgärd (omfattar endast nekade händelser).
Den grupperar först resultaten baserat på principtilldelning, principdefinition och resurs-ID. Därefter grupperas resultatet av den här gruppering med samma egenskaper förutom resurs-ID och antalet poster beräknas i var och en av dessa grupper, som returneras i egenskapen AdditionalProperties.
Resultatet ordnas efter antal-aggregering i fallande ordning och tar endast upp 5 av de som anges i den ordningen.
Det här genererar de 5 vanligaste principerna för nekad åtkomst med flest antal nekade resurser.

## PARAMETERS

### -Apply
Använda uttryck för aggregeringar med OData-notation.

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Filteruttryck med OData-notation.

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
ISO 8601-formaterad tidsstämpel som anger starttiden för frågeintervallet.
När parametervärdet "Till" inte anges minus 1 dag.

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
Namn på hanteringsgrupp.

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
Ordningsuttryck med OData-notation.
Ett eller flera kommaavgränsade kolumnnamn med en valfri "desc" (standard) eller "asc".

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
Namn på principtilldelning.

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
Namn på principdefinition.

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
Namn på principuppsättningsdefinition.

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
Resursgruppnamn.

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

### -Select
Markera uttryck med OData-notation.
Ett eller flera kommaavgränsade kolumnnamn.
Begränsar kolumnerna för varje post till endast de som begärs.

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
Prenumerations-ID.

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

### -To
ISO 8601-formaterad tidsstämpel som anger sluttiden för intervallet som ska frågas.
När den inte anges används standardtiden för begäran.

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

### -Top
Maximalt antal poster som ska returneras.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent

## ANTECKNINGAR

## RELATERADE LÄNKAR
