---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758086"
---
# Get-AzureRmEventHubNamespaceAuthorizationRule

## Sammanfattning
Hämtar information om en auktoriseringsregel för Eventubs, eller hämtar en lista över auktoriseringsregler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## PROBLEMBESKRIVNING
Get-AzureRmEventHubNamespaceAuthorizationRule-cmdleten får antingen information om en angiven regel för en namnrymd eller en lista över auktoriseringsregler för ett namn område.
Om namnet på auktoriseringsregeln anges returneras informationen om en enda auktoriseringsregel.
Om namnet på en auktoriseringsregel inte anges returneras en lista över alla auktoriseringsregler i namn området.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

Returnerar \` MyAuthRuleName \` i \` MyNamespaceName \` , med resurs gruppen \` MyResourceGroupName \` .

### Exempel 2
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

Returnerar standard regeln för \` RootManageSharedAccessKey \` i namn området för Event Hubs \` \` , med resurs gruppen \` MyResourceGroupName \` .

### Exempel 3
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

Returnerar alla auktoriseringsregler i MyNamespaceName för Event Hubs \` \` , med resurs gruppen \` MyResourceGroupName \` .

## MALLPARAMETRAR

### -AuthorizationRuleName
Namn på auktoriseringsregeln för händelse nav.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
Namn områdes namn för Event Hub.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## KOSTNADS

### System. String

## VÄRDEN

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. EventHub, version = 0.0.1.0, Culture = neutralt, PublicKeyToken = null]]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

