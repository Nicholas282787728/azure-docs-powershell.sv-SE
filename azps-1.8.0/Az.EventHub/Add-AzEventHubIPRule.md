---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 959fcab661139a1cacae46a315db0eaa93f0c09e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754089"
---
# Add-AzEventHubIPRule

## Sammanfattning
Lägga till en enda IPrule i NetworkRuleSet för det angivna namn området

## FRÅGESYNTAXEN

### IPRulePropertiesParameterSet (standard)
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IPRuleInputObjectParameterSet
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Lägga till en enda IPrule i NetworkRuleSet för det angivna namn området

## BESKRIVS

### Exempel 1
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default typ: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules: 

Lägg till IPRule med IpMask "11.22.33.44" och åtgärden tillåter angiven namesapce.

### Exempel 2
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
Namn: standard DefaultAction: Tillåt-ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default typ: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules: 

Lägg till IPRule med IpMask "11.22.33.44" och åtgärden tillåter angiven namesapce.

## MALLPARAMETRAR

### -Åtgärd
Åtgärden IP filter

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -IpMask
ID för under nätet

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpRuleObject
IPRule-konfigurations objekt som ska läggas till

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namn på namn området

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.
Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. EventHub. Models. PSNWRuleSetIpRulesAttributes

## VÄRDEN

### Microsoft. Azure. commands. EventHub. Models. PSNetworkRuleSetAttributes

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
