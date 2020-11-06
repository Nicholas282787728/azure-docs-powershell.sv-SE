---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583307"
---
# Get-AzureRmEventHubNamespace

## Sammanfattning
Hämtar information om namn området för en händelse hubb eller hämtar en lista över alla namn rymder för händelser i det aktuella Azure-abonnemanget.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## PROBLEMBESKRIVNING
Get-AzureRmEventHubNamespace-cmdleten får antingen information om ett angivet namn område för händelse nav, eller en lista över alla namn områden i det aktuella Azure-abonnemanget.
Om namn områdes namnet är angivet returneras informationen om ett namn område med en enskild händelse.
Om namn områdes namnet inte anges returneras en lista med namn områden.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

Hämtar information om namn området för Event Hub \` MyNamespaceName \` i resurs gruppen \` MyResourceGroupName \` .

## MALLPARAMETRAR

### -ResourceGroupName
Resurs grupps namn.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Namn område för EventHub.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## KOSTNADS

### System. String

## VÄRDEN

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. NamespaceAttributes, Microsoft. Azure. commands. EventHub, version = 0.0.1.0, Culture = neutralt, PublicKeyToken = null]]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

