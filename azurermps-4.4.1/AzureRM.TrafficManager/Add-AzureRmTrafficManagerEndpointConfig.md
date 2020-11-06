---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: f2abe6acd0406f78ba2bb691b562cd0bcbffeb35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573616"
---
# Add-AzureRmTrafficManagerEndpointConfig

## Sammanfattning
Lägger till en slut punkt till ett lokalt Traffic Manager-Profile-objekt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmTrafficManagerEndpointConfig** lägger till en slut punkt till ett lokalt Azure Traffic Manager-Profile-objekt.
Du kan hämta en profil med hjälp av New-AzureRmTrafficManagerProfile eller Get-AzureRmTrafficManagerProfile cmdletar.

Denna cmdlet fungerar på det lokala profilens objekt.
Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzureRmTrafficManagerProfile cmdlet.
Om du vill skapa en slut punkt och bekräfta ändringen i en enskild åtgärd, Använd cmdleten New-AzureRmTrafficManagerEndpoint.

## BESKRIVS

### Exempel 1: lägga till en slut punkt för en profil
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzureRmTrafficManagerProfile** .
Kommandot lagrar den lokala profilen i $TrafficManagerProfile variabel.

Det andra kommandot lägger till en slut punkt med namnet contoso till profilen som lagras i $TrafficManagerProfile.
Kommandot innehåller konfigurations data för slut punkten.
Det här kommandot ändrar bara det lokala objektet.

Det sista kommandot uppdaterar Traffic Manager-profilen i Azure så att den matchar det lokala värdet i $TrafficManagerProfile.

## MALLPARAMETRAR

### -EndpointLocation
Anger platsen för slut punkten som används i metoden för prestanda trafik-routning.
Den här parametern är endast tillämpbar på slut punkter för ExternalEndpoints eller NestedEndpoints-typen.
Du måste ange den här parametern när routningsmetoden för prestanda trafik används.

Ange ett Azure region namn.
En fullständig lista över Azure-regioner finns i Azure https://azure.microsoft.com/regions/ -regioner ( https://azure.microsoft.com/regions/) .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
Anger namnet på den Traffic Manager-slutpunkt som denna cmdlet lägger till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointStatus
Anger statusen för slut punkten.
Giltiga värden är: 

- Aktiverat 
- Aktiv 

Om statusen är aktive rad avsöks slut punkten för slut punkts tillstånd och är inkluderad i Traffic routing-metoden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Polymappning
Listan med regioner som mappats till den här slut punkten med cirkulations metoden "geografisk". Se dokumentationen för Traffic Manager för en [fullständig lista över godkända värden](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Ange ett Azure region namn.
En fullständig lista över Azure-regioner finns i Azure https://azure.microsoft.com/regions/ -regioner ( https://azure.microsoft.com/regions/) .

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Prioritet
Anger den prioritet som trafik hanteraren tilldelar slut punkten.
Den här parametern används endast om Traffic Manager-profilen är konfigurerad med metoden för prioritets cirkulation.
Giltiga värden är heltal från 1 till 1000.
Lägre värden är högre prioritet.

Om du anger en prioritet måste du ange prioritet för alla slut punkter i profilen, och två slut punkter kan inte dela samma prioritets värde.
Om du inte anger prioriteringar tilldelar trafik hanteraren standardvärden för prioritet till slut punkterna, med start från ett (1), i den ordning som profilen listar slut punkter.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mål
Anger slut punktens fullständiga DNS-namn.
Traffic Manager returnerar detta värde i DNS-svar när det dirigerar trafik till slut punkten.
Ange endast den här parametern för slut punkts typen ExternalEndpoints.
Ange parametern *TargetResourceId* i stället för andra slut punkts typer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceId
Anger målets resurs-ID.
Ange endast den här parametern för slut punkts typerna AzureEndpoints och NestedEndpoints.
Ange parametern *target* för slut punkts typen ExternalEndpoints.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Anger ett lokalt **TrafficManagerProfile** -objekt.
Denna cmdlet ändrar detta lokala objekt.
För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzureRmTrafficManagerProfile.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Skriv
Anger den typ av slut punkt som denna cmdlet lägger till i Azure Traffic Manager-profilen.
Giltiga värden är: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vikt
Anger den vikt som trafik hanteraren tilldelar slut punkten.
Giltiga värden är heltal från 1 till 1000.
Standardvärdet är ett (1).
Den här parametern används endast om Traffic Manager-profilen är konfigurerad med den viktade trafikdragnings metoden.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Network. TrafficManagerProfile
Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt till denna cmdlet.

## VÄRDEN

### Microsoft. Azure. commands. Network. TrafficManagerProfile
Denna cmdlet returnerar ett ändrat **TrafficManagerProfile** -objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


