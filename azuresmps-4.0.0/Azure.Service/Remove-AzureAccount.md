---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099100"
---
# Remove-AzureAccount

## Sammanfattning
Tar bort ett Azure-konto från Windows PowerShell.

## FRÅGESYNTAXEN

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Med cmdleten **Remove-AzureAccount** tar du bort ett Azure-konto och dess abonnemang från filen med den centrala användar profilen.
Kontot tas inte bort från Microsoft Azure eller så kan du inte ändra det faktiska kontot på något sätt.

Att använda denna cmdlet är mycket som att logga ut från ditt Azure-konto.
Om du vill logga in på kontot igen använder du **AzureAccount** eller **import-AzurePublishSettingsFile** för att lägga till kontot i Windows PowerShell igen.

Du kan också använda cmdleten **Remove-AzureAccount** för att ändra hur Azure PowerShell-cmdlet loggar in på ditt Azure-konto.
Om ditt konto har både ett Management-certifikat från **import-AzurePublishSettingsFile** och en åtkomsttoken från **Add-AzureAccount** använder Azure PowerShell-cmdletar bara åtkomsttoken; de ignorerar hanterings certifikatet.
Kör **Remove-AzureAccount** om du vill använda hanterings certifikatet.
När **AzureAccount** hittar både ett hanterings certifikat och en åtkomsttoken tar det bara bort åtkomsttoken i stället för att ta bort kontot.
Hanterings certifikatet är fortfarande där, så kontot är fortfarande tillgängligt för Windows PowerShell.

I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

## BESKRIVS

### Exempel 1: ta bort ett konto
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

Det här kommandot tar bort admin@contoso.com från din prenumerations data fil.
När kommandot är klart är kontot inte längre tillgängligt för Windows PowerShell.

## MALLPARAMETRAR

### -Force
Inaktiverar uppmaningen om att bekräfta.
Som standard uppmaningar AzureAccount om att **ta** bort kontot från Windows PowerShell.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på kontot som ska tas bort.
Parametervärdet är Skift läges känsligt.
Jokertecken stöds inte.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Returnerar $True om kommandot lyckas och $False om det inte fungerar.
Denna cmdlet returnerar som standard inga utdata.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.

## VÄRDEN

### Ingen eller system. Boolean
Om du använder parametern *Passthru* returnerar denna cmdlet ett Boolean-värde.
Annars returnerar den inte några resultat.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureAccount](./Get-AzureAccount.md)


