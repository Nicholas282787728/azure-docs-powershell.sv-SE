---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099606"
---
# Add-AzureTrafficManagerEndpoint

## Sammanfattning
Lägger till en slut punkt i en Traffic Manager-profil.

## FRÅGESYNTAXEN

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureTrafficManagerEndpoint** lägger till en slut punkt till en Microsoft Azure Traffic Manager-profil.
När du har lagt till en slut punkt skickar du resultatet till cmdleten **set-AzureTrafficManagerProfile** med hjälp av pipeline-operatorn.
Denna cmdlet ansluter till Azure för att spara dina ändringar.

## BESKRIVS

### Exempel 1: lägga till en slut punkt för en profil
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

Det första kommandot använder cmdleten **Get-AzureTrafficManagerProfile** för att hämta profilen med namnet ContosoProfile och lagrar den sedan i $TrafficManagerProfile variabel.

Det andra kommandot lägger till en slut punkt till Traffic Manager-profilen som lagras i $TrafficManagerProfile.
Slut punkten har domän namnet Contoso02App.couldapp.net.
Kommandot anger också om den är aktive rad och dess typ.
Kommandot skickar Profile-objektet till cmdleten **set-AzureTrafficManagerProfile** för att ansluta till Azure för att spara ändringarna.

### Exempel 2: lägga till en slut punkt med en angiven plats och vikt
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Det här kommandot lägger till en slut punkt till en Traffic Manager-profil.
Slut punkten har domän namnet Contoso02App.couldapp.net.
Kommandot anger också om den är aktive rad och dess typ.
Kommandot anger också tjocklek och plats för slut punkten.
Kommandot skickar profil objekt till **set-AzureTrafficManagerProfile** för att kunna spara dina ändringar.

## MALLPARAMETRAR

### -Domän namn
Anger domän namnet för slut punkten som ska läggas till.

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
De möjliga värdena är namnen på Azure-regionen, som finns på https://azure.microsoft.com/regions/ .

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Anger den Traffic Manager-profil som du vill lägga till slut punkten för.

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

Required: True
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

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


