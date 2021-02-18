---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252109"
---
# Get-AzPolicyStateSummary

## SYNOPSIS
Hämtar den senaste sammanfattningen av efterlevnadsprinciper för resurser.

## SYNTAX

### SubscriptionScope (standard)
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Hämtar en sammanfattning av de senaste numren för efterlevnadstillstånd för olika omfattningar, indeade i principtilldelningar och principdefinitioner. Den innehåller endast policyer som inte är kompatibla.

## EXEMPEL

### Exempel 1: Hämta den senaste sammanfattningen av policyer som inte är kompatibla i den aktuella prenumerationsomfånget
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Hämtar sammanfattningsvyn över de senaste statusarna för policyefterlevnad som genererades den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget.

### Exempel 2: Hämta den senaste sammanfattningen av icke-kompatibla policyer i den angivna prenumerationsomfånget
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadslägena som genererades den sista dagen för alla resurser inom den angivna prenumerationen.

### Exempel 3: Hämta den senaste sammanfattningen av icke-kompatibla principstater i hanteringsgruppens omfattning
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadslägena som genererades den sista dagen för alla resurser i den angivna hanteringsgruppen.

### Exempel 4: Hämta den senaste sammanfattningen av icke-kompatibla principstater i resursgruppomfattningen i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadslägena som genererades den sista dagen för alla resurser inom den angivna resursgruppen (i prenumerationen i aktuellt sessionssammanhang).

### Exempel 5: Hämta den senaste sammanfattningen av icke-kompatibla principstater i resursgruppomfattningen i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadslägena som genererades den sista dagen för alla resurser inom den angivna resursgruppen (i den angivna prenumerationen).

### Exempel 6: Hämta den senaste sammanfattningen av icke-kompatibla principstater för en resurs
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadslägena som genererades den sista dagen för den angivna resursen.

### Exempel 7: Hämta den senaste sammanfattningen av policyer som inte är kompatibla för en principuppsättningsdefinition i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadsfaserna som genererades den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) som verkställs av den angivna principuppsättningsdefinitionen (som finns i prenumerationen i det aktuella sessionssammanhanget).

### Exempel 8: Hämta den senaste sammanfattningen av icke-kompatibla principstater för en principuppsättningsdefinition i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadsfaserna som genererades den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) som skulle påverkas av den angivna principuppsättningsdefinitionen (som finns i den angivna prenumerationen).

### Exempel 9: Hämta den senaste sammanfattningen av policyer som inte är kompatibla för en principdefinition i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Får sammanfattningsvyn över de senaste principefterlevnadslägena som genererades den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) påverkas av den angivna principdefinitionen (som finns i prenumerationen i det aktuella sessionssammanhanget).

### Exempel 10: Hämta den senaste sammanfattningen av policyer som inte är kompatibla för en principdefinition i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadsfaserna som genererades den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) genom den angivna principdefinitionen (som finns i den angivna prenumerationen).

### Exempel 11: Hämta den senaste sammanfattningen av policyer som inte är kompatibla för en principtilldelning i aktuell prenumeration
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadslägena som genererades den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) genom den angivna principtilldelningen (som finns i prenumerationen i det aktuella sessionssammanhanget).

### Exempel 12: Hämta den senaste sammanfattningen av policyer som inte är kompatibla för en principtilldelning i den angivna prenumerationen
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadslägena som genererades den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) genom den angivna principtilldelningen (som finns i den angivna prenumerationen).

### Exempel 13: Hämta den senaste sammanfattningen av policyer som inte är kompatibla för en principtilldelning i den angivna resursgruppen i den aktuella prenumerationen
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadslägena som genererades den sista dagen för alla resurser (inom klientorganisationen i det aktuella sessionssammanhanget) genom den angivna principtilldelningen (som finns i resursgruppen i prenumerationen i det aktuella sessionssammanhanget).

### Exempel 14: Hämta den senaste sammanfattningen av policyer som inte är kompatibla i den aktuella prenumerationen med alternativet Top query
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Hämtar sammanfattningsvyn över de senaste statusarna för policyefterlevnad som genererades den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget. Kommandot beställer sammanfattningar av principtilldelningen i resultatet efter att icke-kompatibla resurser räknas i fallande ordning och tar endast upp 5 av dessa sammanfattningar av principtilldelningen.

### Exempel 15: Hämta den senaste sammanfattningen av policyer som inte är kompatibla i den aktuella prenumerationen med frågealternativ från och till
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Hämtar sammanfattningsvyn över de senaste principefterlevnadslägena som genereras inom det datumintervall som angetts för alla resurser i prenumerationen i det aktuella sessionssammanhanget.

### Exempel 16: Hämta den senaste sammanfattningen av policyer som inte är kompatibla i den aktuella prenumerationen med alternativet Filtrera fråga
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Hämtar sammanfattningsvyn över de senaste statusarna för policyefterlevnad som genererades den sista dagen för alla resurser i prenumerationen i det aktuella sessionssammanhanget.
Kommandot begränsar resultatet som returneras av filtrering baserat på principdefinitionsåtgärd (omfattar åtgärder för nekad eller granskning) och resursplats (exkluderar östbaserad plats).

## PARAMETERS

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzPolicyState](./Get-AzPolicyState.md)
