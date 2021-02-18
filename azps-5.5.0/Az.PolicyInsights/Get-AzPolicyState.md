---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252113"
---
# Get-AzPolicyState

## SYNOPSIS
Får principens efterlevnads tillstånd för resurser.

## SYNTAX

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

## BESKRIVNING
Får principens efterlevnads tillstånd för resurser. Poster i principtillstånd kan tillfrågas i olika omfattningar. Baserat på det tidsintervall som angetts (standardinställningen till sista dagen), kan du antingen fråga om senaste principtillstånd eller alla principtillståndsövergångar. Resultaten kan filtreras, grupperas och gruppaggregeringar kan beräknas.

## EXEMPEL

### Exempel 1: Hämta de senaste policyerna i den aktuella prenumerationsomfånget
```powershell
PS C:\> Get-AzPolicyState
```

Får de senaste posterna för policytillstånd som genereras under den sista dagen för alla resurser i prenumerationen i aktuellt sessionssammanhang.

### Exempel 2: Hämta de senaste policyerna för den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Får de senaste posterna för policytillstånd som genereras under den sista dagen för alla resurser inom den angivna prenumerationen.

### Exempel 3: Få alla policyer i den aktuella prenumerationsomfånget
```powershell
PS C:\> Get-AzPolicyState -All
```

Får alla historiska policyposter (inklusive senaste) som genereras under den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget.

### Exempel 4: Hämta de senaste principstaterna i hanteringsgruppens omfattning
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser inom den angivna hanteringsgruppen.

### Exempel 5: Hämta de senaste principstaterna i resursgruppomfattningen i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser inom den angivna resursgruppen (i prenumerationen i aktuellt sessionssammanhang).

### Exempel 6: Hämta de senaste principstaterna i resursgruppomfattningen i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser inom den angivna resursgruppen (i den angivna prenumerationen).

### Exempel 7: Hämta de senaste principstaterna för en resurs
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Får de senaste statusposterna för principen som genererades den sista dagen för den angivna resursen.

### Exempel 8: Hämta de senaste principstaterna för en principuppsättningsdefinition i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser (inom klientorganisationen i aktuellt sessionssammanhang) som påverkas av den angivna principuppsättningsdefinitionen (som finns i prenumerationen i det aktuella sessionssammanhanget).

### Exempel 9: Hämta de senaste principstaterna för en principuppsättningsdefinition i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser (inom klientorganisationen i aktuellt sessionssammanhang) som påverkas av den angivna principuppsättningsdefinitionen (som finns i den angivna prenumerationen).

### Exempel 10: Hämta de senaste principstaterna för en principdefinition i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser (inom klientorganisationen i aktuellt sessionssammanhang) som påverkas av den angivna principdefinitionen (som finns i prenumerationen i det aktuella sessionssammanhanget).

### Exempel 11: Hämta de senaste principstaterna för en principdefinition i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser (inom klientorganisationen i aktuellt sessionssammanhang) som påverkas av den angivna principdefinitionen (som finns i den angivna prenumerationen).

### Exempel 12: Hämta de senaste principstaterna för en principtilldelning i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser (inom klientorganisationen i aktuellt sessionssammanhang) som påverkas av den angivna principtilldelningen (som finns i prenumerationen i aktuellt sessionssammanhang).

### Exempel 13: Hämta de senaste principstaterna för en principtilldelning i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser (inom klientorganisationen i aktuellt sessionssammanhang) som påverkas av den angivna principtilldelningen (som finns i den angivna prenumerationen).

### Exempel 14: Hämta de senaste principstaterna för en principtilldelning i den angivna resursgruppen i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser (inom klientorganisationen i aktuellt sessionssammanhang) som påverkas av den angivna principtilldelningen (som finns i resursgruppen i prenumerationen i aktuellt sessionssammanhang).

### Exempel 15: Hämta de senaste principstaterna i den aktuella prenumerationen med OrderBy, Top och Select-frågealternativ
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget. Kommandot beställer resultatet efter namnegenskaper för tidsstämpel och principtilldelning och tar endast upp 5 av de som visas i den ordningen.
Den väljer också att endast visa en delmängd av kolumnerna för varje post.

### Exempel 16: Hämta de senaste policyerna i den aktuella prenumerationen med frågealternativen Från och Till
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Får de senaste statusposterna för principen som genereras inom datumintervallet som angetts för alla resurser i prenumerationen i aktuellt sessionssammanhang.

### Exempel 17: Hämta de senaste policyerna i aktuell prenumerationsomfattning med alternativet Filtrera fråga
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget.
Kommandot begränsar resultatet som returneras av filtrering baserat på principdefinitionsåtgärd (omfattar nekade eller granskningsåtgärder), efterlevnadsstatus (omfattar endast icke-kompatibla status) och resursplats (exkluderar östasiatiska platser).

### Exempel 18: Hämta de senaste principstaterna i den aktuella prenumerationsomfattningen, med Använd specificerad aggregering för radantal
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Får de senaste statusposterna för principen som genererats den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget.
Kommandot returnerar antalet endast principtillståndsposter, som returneras i egenskapen AdditionalProperties.

### Exempel 19: Hämta de senaste principstaterna i den aktuella prenumerationsomfattningen, med Använd ange gruppering med aggregering
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Får de senaste statusposterna för principen som genereras under den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget. Kommandot begränsar resultatet som returneras av filtrering baserat på efterlevnadsstatus (omfattar endast status som inte är kompatibel).
Grupperar resultaten baserat på principtilldelning, principuppsättningsdefinition och principdefinition, och beräknar antalet poster i varje grupp, som returneras i egenskapen AdditionalProperties.
Resultatet ordnas efter antal-aggregering i fallande ordning och tar endast upp 5 av de som anges i den ordningen.

### Exempel 20: Hämta de senaste principstaterna i den aktuella prenumerationsomfattningen, med Använd ange gruppering utan aggregering
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Får de senaste posterna för policytillstånd som genereras under den sista dagen för alla resurser i prenumerationen i aktuellt sessionssammanhang. Kommandot begränsar resultatet som returneras av filtrering baserat på efterlevnadsstatus (omfattar endast status som inte är kompatibel).
Resultatet grupperar baserat på resurs-ID. Det här genererar listan över alla resurser i prenumerationen som inte följer minst en princip.

### Exempel 21: Hämta de senaste principstaterna i den aktuella prenumerationsomfattningen, med Använd och ange flera gruppering
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Exempel 22: Hämta de senaste principprinciperna inklusive information om principutvärdering för en resurs
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Får de senaste posterna för policytillstånd som genereras under den sista dagen för alla resurser i prenumerationen i aktuellt sessionssammanhang. Kommandot begränsar resultatet som returneras av filtrering baserat på efterlevnadsstatus (omfattar endast status som inte är kompatibel).
Den grupperar först resultaten baserat på principtilldelning, principuppsättningsdefinition, principdefinition och resurs-ID. Därefter grupperas resultatet av den här gruppering med samma egenskaper förutom resurs-ID och antalet poster beräknas i var och en av dessa grupper, som returneras i egenskapen AdditionalProperties.
Resultatet ordnas efter antal-aggregering i fallande ordning och tar endast upp 5 av de som anges i den ordningen.
Det här genererar de 5 vanligaste principerna med flest antal icke-kompatibla resurser.

## PARAMETERS

### -All
Inom det angivna tidsintervallet ska du hämta alla principstater i stället för de senaste.

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

### -Expand
Expandera uttryck med OData-notation.

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
