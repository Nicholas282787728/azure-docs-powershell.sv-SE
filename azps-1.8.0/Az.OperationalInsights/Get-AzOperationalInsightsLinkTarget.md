---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: beb4fad10424a94b2623070508ac827ea7b15306
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755171"
---
# Get-AzOperationalInsightsLinkTarget

## Sammanfattning
Hämtar konton som inte är kopplade till ett abonnemang.

## FRÅGESYNTAXEN

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzOperationalInsightsLinkTarget** innehåller befintliga konton som inte är associerade med en Azure-prenumeration.
Om du vill länka en ny arbets yta till ett befintligt konto använder du ett kund-ID som returneras av den här åtgärden i egenskapen kund-ID för en ny arbets yta.

## BESKRIVS

### Exempel 1: Hämta olänkade konton
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

Det här kommandot får olänkade konton som ägs av anroparens ID.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. OperationalInsights. Models. PSAccount

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Cmdlets för Azure Operational Insights](/powershell/module/az.operationalinsights)


