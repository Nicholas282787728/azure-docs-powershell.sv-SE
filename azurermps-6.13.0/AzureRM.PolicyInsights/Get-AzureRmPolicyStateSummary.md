---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
ms.openlocfilehash: 4b4d45414a9a27561c3be4be195a1e5f77076e6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575158"
---
# Get-AzureRmPolicyStateSummary

## Sammanfattning
Hämtar den senaste översikten över efterlevnad för principer för resurser.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### SubscriptionScope (standard)
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzureRmPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzureRmPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Får en sammanfattningsvy över de senaste tillstånds numren för policy efterlevnad för olika scope, nedbrutna till princip tilldelningar och princip definitioner. Den innehåller endast icke-kompatibla princip tillstånd.

## BESKRIVS

### Exempel 1: Hämta senaste icke-kompatibla princip status sammanfattning för aktuell prenumeration
```powershell
PS C:\> Get-AzureRmPolicyStateSummary
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser inom prenumerationen i den aktuella sessionskatalogen.

### Exempel 2: Hämta senaste icke-kompatibla princip status sammanfattning för det angivna abonnemanget
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser inom det angivna abonnemanget.

### Exempel 3: Hämta senaste icke-kompatibla princip status sammanfattning i hanterings gruppens omfattning
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser i den angivna hanterings gruppen.

### Exempel 4: Hämta senaste icke-kompatibla princip status sammanfattning i resurs gruppens omfattning i aktuell prenumeration
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser i den angivna resurs gruppen (i prenumerationen i den aktuella sessionen).

### Exempel 5: Hämta senaste icke-kompatibla princip status sammanfattning i resurs gruppens omfattning i det angivna abonnemanget
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser i den angivna resurs gruppen (i den angivna prenumerationen).

### Exempel 6: Hämta senaste icke-kompatibla princip status sammanfattning för en resurs
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för den angivna resursen.

### Exempel 7: Hämta senaste icke-kompatibla princip status sammanfattning för en princip uppsättnings definition i aktuell prenumeration
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (i klient organisationen i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättning (som finns i prenumerationen i den aktuella session-kontexten).

### Exempel 8: Hämta senaste icke-kompatibla princip status sammanfattning för en princip uppsättnings definition i det angivna abonnemanget
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna definitionen för princip uppsättning (som finns i den angivna prenumerationen).

### Exempel 9: Hämta senaste icke-kompatibla princip status sammanfattning för en princip definition i aktuell prenumeration
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i prenumerationen i den aktuella sessionen).

### Exempel 10: Hämta senaste icke-kompatibla princip status sammanfattning för en princip definition i det angivna abonnemanget
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (i klient organisationen i den aktuella sessionsgränsen) som utförs av den angivna princip definitionen (som finns i den angivna prenumerationen).

### Exempel 11: Hämta senaste icke-kompatibla princip status översikt för en princip tilldelning i aktuell prenumeration
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i prenumerationen i aktuell session-kontext).

### Exempel 12: Hämta senaste icke-kompatibla princip tillstånds Sammanfattning för en princip tilldelning i den angivna prenumerationen
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (i klient organisationen i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i den angivna prenumerationen).

### Exempel 13: Hämta senaste icke-kompatibla princip status sammanfattning för en princip tilldelning i den angivna resurs gruppen i den aktuella prenumerationen
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser (inom innehavaren i den aktuella sessionsgränsen) som tillämpas av den angivna princip tilldelningen (som finns i resurs gruppen i prenumerationen i den aktuella sessionen).

### Exempel 14: Hämta senaste icke-kompatibla princip status sammanfattning i den aktuella prenumerations omfattningen, med alternativet Top Query
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Top 5
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser inom prenumerationen i den aktuella sessionskatalogen. Kommandot beställer sammanfattningar av princip tilldelningar i resultaten efter icke-kompatibla resurs räkningar i fallande ordning och endast de 5 högsta av dessa princip tilldelnings sammanfattningar används.

### Exempel 15: Hämta senaste icke-kompatibla princip status sammanfattning i den aktuella prenumerations omfattningen med alternativen från och till fråga
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats inom det datum intervall som anges för alla resurser i prenumerationen i den aktuella sessionen.

### Exempel 16: Hämta senaste icke-kompatibla princip status sammanfattning i aktuell prenumerations omfattning med alternativet filtrera fråga
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Hämtar sammanfattningsvyn av de senaste reglerna för efterlevnadsprinciper som genererats den sista dagen för alla resurser inom prenumerationen i den aktuella sessionskatalogen.
Kommandot begränsar resultaten som returneras genom filtrering baserat på princip definitions åtgärden (inklusive neka-eller gransknings åtgärder) och resurs plats (utesluter östasiatiska platser).

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. PolicyInsights. Models. PolicyStateSummary

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmPolicyState](./Get-AzureRmPolicyState.md)
