---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571032"
---
# Save-AzureRmContext

## Sammanfattning
Sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.

## FRÅGESYNTAXEN

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## PROBLEMBESKRIVNING
Save-AzureRmContext cmdlet sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.

## BESKRIVS

### Exempel 1: Spara den aktuella sessionens kontext
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

I det här exemplet sparas den aktuella sessionens Azure-kontext till den JSON-fil som tillhandahålls.

### Exempel 2: Spara en given kontext
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

I det här exemplet sparas Azure-kontexten som skickas till cmdleten till den JSON-fil som tillhandahålls.

## MALLPARAMETRAR

### -Force
Skriv över den angivna filen om den finns

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Anger sökvägen till filen där autentiseringsinformationen ska sparas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-kontext från vilken denna cmdlet läser.
Om du inte anger en kontext läser denna cmdlet från den lokala standard kontexten.

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## KOSTNADS

### Microsoft. Azure. kommandon. Common. autentiseringsprovider. Models. AzureRMProfile

## VÄRDEN

### Microsoft. Azure. commands. Profile. Models. PSAzureProfile

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

