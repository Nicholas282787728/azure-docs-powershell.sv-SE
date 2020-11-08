---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093160"
---
# Set-AzureTrafficManagerEndpoint

## Sammanfattning
Uppdaterar egenskaperna för en slut punkt i en Traffic Manager-profil.

## FRÅGESYNTAXEN

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureTrafficManagerEndpoint** uppdaterar egenskaperna för en slut punkt i en Microsoft Azure Traffic Manager-profil.
Om slut punkten inte finns i den aktuella profilen skapar den här cmdlet den.
När du har lagt till en slut punkt skickar du resultatet till cmdleten **set-AzureTrafficManagerProfile** med hjälp av pipeline-operatorn.
Denna cmdlet ansluter till Azure för att spara dina ändringar.

## BESKRIVS

### Exempel 1: uppdatera en slut punkt för en profil
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Det första kommandot använder cmdleten **Get-AzureTrafficManagerProfile** för att hämta profilen med namnet ContosoProfile och lagrar den sedan i $TrafficManagerProfile variabel.

Det andra kommandot uppdaterar slut punkten i Traffic Manager-profilen som lagras i $TrafficManagerProfile.
Slut punkten har domän namnet ContosoApp02.cloudapp.net.
Kommandot anger också slut punktens status, typ, vikt och plats.
Kommandot skickar den ändrade profilen till cmdleten **set-AzureTrafficManagerProfile** för att ansluta till Azure för att spara ändringarna.

## MALLPARAMETRAR

### -Domän namn
Anger domän namnet för slut punkten som ska ändras.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger platsen för slut punkten som cmdleten lägger till.
Det måste vara en Azure-plats.

Den här parametern måste innehålla ett värde för slut punkter av typen "any" eller av typen "TrafficManager" i en profil som har metod för belastnings utjämning angiven till "prestanda".
De möjliga värdena är namnen på Azure-regionen, som finns på  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Anger det minsta antalet slut punkter som den kapslade profilen måste ha för att den här slut punkten ska kunna anses vara online.

```yaml
Type: Int32
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

### -Status
Anger statusen för övervaknings slut punkten.
Giltiga värden är: 

- Aktiverat
- Aktiv

Om du anger ett värde för aktive rad övervakar trafik hanteraren slut punkten och belastnings Utjämnings metoden när trafiken hanteras.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Anger den Traffic Manager-profil som du vill ändra slut punkten för.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### – Skriv
Anger typen av slut punkt.
Giltiga värden är: 

- CloudService
- AzureWebsite
- TrafficManager

- Eventuell 

Om det finns fler än en AzureWebsite-slutpunkt måste slut punkterna finnas i olika data Center.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vikt
Anger vikten för slut punkten som cmdleten lägger till.
Det giltiga värde intervallet är \[ 1, 1000 \] .

Den här parametern används endast för principer för belastnings utjämning på RoundRobin.

```yaml
Type: Int32
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

### Microsoft. WindowsAzure. commands. Utilities. TrafficManager. Models. IProfileWithDefinition
Denna cmdlet skapar ett profil objekt för Traffic Manager, som innehåller information om den uppdaterade profilen.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


