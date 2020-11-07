---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: 1a68b5ca391e6c09673f07f0469035e0f96c1562
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745991"
---
# Enable-AzDataCollection

## Sammanfattning
Gör att Azure PowerShell samlar in data för att förbättra användar upplevelsen med AzurePowerShell cmdlets.
Kör den här cmdleten till data insamling för den aktuella användaren på den aktuella datorn.
Inga data samlas in om du inte uttryckligen väljer.

## FRÅGESYNTAXEN

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Du kan förbättra upplevelsen för att använda Microsoft Cloud och Azure PowerShell genom att vanligt in i data insamling.
Azure PowerShell samlar inte in data utan ditt medgivande-du måste uttryckligen välja att inaktivera Enable-AzDataCollection eller genom att svara Ja när du uppmanas att samla in data första gången du kör en cmdlet.
Microsoft samlar in data för att identifiera användnings mönster, för att identifiera vanliga problem och för att förbättra upplevelsen för användning av Azure PowerShell.
Microsoft Azure PowerShell samlar inte in några privata data eller personlig information.
Kör cmdleten Enable-AzDataCollection för att aktivera data insamling för den aktuella användaren på den aktuella datorn.
Detta gör att den aktuella användaren inte tillfrågas om data insamling första gången cmdletar körs.
Kör cmdleten Disable-AzDataCollection om du vill inaktivera data insamling för den aktuella användaren.

## BESKRIVS

### Exempel 1: Aktivera data insamling för den aktuella användaren
```
PS C:\> Enable-AzDataCollection
```

Det här exemplet visar hur du aktiverar data insamling för den aktuella användaren.

## MALLPARAMETRAR

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

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### System. Void

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Disable-AzDataCollection](./Disable-AzDataCollection.md)

