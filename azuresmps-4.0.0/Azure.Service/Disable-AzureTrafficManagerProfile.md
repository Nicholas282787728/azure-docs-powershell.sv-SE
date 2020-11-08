---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093419"
---
# Disable-AzureTrafficManagerProfile

## Sammanfattning
Inaktiverar en Traffic Manager-profil.

## FRÅGESYNTAXEN

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **disable-AzureTrafficManagerProfile** inaktiverar en Microsoft Azure Traffic Manager-profil.
Du kan använda parametern *Passthru* för att visa om åtgärden lyckades.

## BESKRIVS

### Exempel 1: inaktivera en Traffic Manager-profil och visa resultatet
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Det här kommandot inaktiverar Traffic Manager-profilen med namnet min-profil.
Kommandot anger parametern *Passthru* för att visa om kommandot lyckades.

### Exempel 2: inaktivera en Traffic Manager-profil och Visa inga resultat
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

Det här kommandot inaktiverar Traffic Manager-profilen med namnet min profil men visar inte om kommandot lyckades.

## MALLPARAMETRAR

### -Namn
Anger namnet på Traffic Manager-profilen som ska avaktiveras.

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
Returnerar $True om åtgärden lyckades. annars $False.
Denna cmdlet genererar som standard inga utdata.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### System. Boolean
Denna cmdlet skapar $True eller $False.
Om åtgärden lyckas och om du anger parametern *Passthru* returnerar denna cmdlet ett värde för $True.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


