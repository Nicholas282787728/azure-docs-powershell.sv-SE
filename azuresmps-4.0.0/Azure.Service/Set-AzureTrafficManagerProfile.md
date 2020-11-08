---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099024"
---
# Set-AzureTrafficManagerProfile

## Sammanfattning
Uppdaterar egenskaperna för en Traffic Manager-profil.

## FRÅGESYNTAXEN

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureTrafficManagerProfile** uppdaterar egenskaperna för en Microsoft Azure Traffic Manager-profil.

För profiler för vilka du har angett *LoadBalancingMethod* -värdet till "failover" kan du bestämma växlings ordningen för slut punkter som du har lagt till i din profil med Add-AzureTrafficManagerEndpoint cmdlet.
Mer information finns i exempel 3 nedan.

## BESKRIVS

### Exempel 1: ange TTL för en Traffic Manager-profil
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

Det här kommandot anger TTL till 60 sekunder för Traffic Manager-MyTrafficManagerProfile.

### Exempel 2: ange flera värden för en profil
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

Det här kommandot får en Traffic Manager-profil med namnet min profil med cmdleten **Get-AzureTrafficManagerProfile** .
Profilen använder belastnings Utjämnings metoden RoundRobin, ett TTL-värde på 30 sekunder, Monitor Protocol HTTP, Monitor port och den relativa sökvägen för en Traffic Manager-profil.

### Exempel 3: ändra ordning på slut punkter till önskad redundansväxling
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

I det här exemplet ordnas de slut punkter som läggs till i min profil i den önskade failover-ordningen.

Det första kommandot får Traffic Manager-Profile-objektet som heter min profil och lagrar objektet i $Profile variabel.

Det andra kommandot ändrar änd punkterna från matrisen slut punkter till den ordning som redundans ska utföras.

Det senaste kommandot uppdaterar Traffic Manager-profilen som lagras i $Profile med den nya slut punkts ordningen.

## MALLPARAMETRAR

### -LoadBalancingMethod
Anger den metod för belastnings utjämning som ska användas för att distribuera anslutningen.
Giltiga värden är: 

- Prestandaräknare
- Återställning
- RoundRobin

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

### -MonitorPort
Anger vilken port som används för att övervaka slut punktens status.
Giltiga värden är heltal som är större än 0 och mindre än eller lika med 65 535.

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

### -MonitorProtocol
Anger vilket protokoll som ska användas för att övervaka slut punktens status.
Giltiga värden är: 

- Inkommande
- Https

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

### -MonitorRelativePath
Anger sökvägen i förhållande till slut punktens domän namn till Avsök för hälso tillstånd.
Sökvägen måste uppfylla följande begränsningar: 

- Sökvägen måste vara mellan 1 och 1000 tecken.
- Det måste börja med ett snedstreck (/).
- Det får inte innehålla XML-element, \<\> .
- Det får inte innehålla dubbla snedstreck,//.
- Det får inte innehålla några ogiltiga HTML-escape-tecken.
Till exempel% XY.

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

### -Namn
Anger namnet på den Traffic Manager-profil som ska uppdateras.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -TrafficManagerProfile
Anger den Traffic Manager-profil som du använder för att ange profilen.

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

### -TTL
Anger det TTL-värde (Time to Live) för DNS som informerar den lokala DNS-matcharen hur länge DNS-posterna ska cachelagras.
Giltiga värden är ett heltal mellan 30 och 999 999.

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
Denna cmdlet skapar ett profil objekt för Traffic Manager.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)


