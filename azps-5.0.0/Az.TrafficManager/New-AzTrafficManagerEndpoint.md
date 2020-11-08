---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269543"
---
# New-AzTrafficManagerEndpoint

## Sammanfattning
Skapar en slut punkt i en Traffic Manager-profil.

## FRÅGESYNTAXEN

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzTrafficManagerEndpoint** skapar en slut punkt i en Azure Traffic Manager-profil.

Denna cmdlet aktiverar varje ny slut punkt till Traffic Manager-tjänsten.
Om du vill lägga till flera slut punkter i ett lokalt Traffic Manager-Profile-objekt och genomföra ändringar i en enskild åtgärd använder du Add-AzTrafficManagerEndpointConfig cmdlet.

## BESKRIVS

### Exempel 1: skapa en extern slut punkt för en profil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Det här kommandot skapar en extern slut punkt som heter Contoso i profilen med namnet ContosoProfile i resurs gruppen med namnet ResourceGroup11.

### Exempel 2: skapa en Azure-slutpunkt för en profil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Det här kommandot skapar en Azure-slutpunkt som heter Contoso i profilen med namnet ContosoProfile i ResourceGroup11 för resurs gruppen.
Azure-slutpunkten pekar på Azure Web App vars Azure Resource Manager-ID anges av URI-sökvägen i *TargetResourceId*.
Kommandot anger inte *EndpointLocation* -parametern eftersom Web App-resursen tillhandahåller platsen.

## MALLPARAMETRAR

### -CustomHeader
Lista över anpassade rubrik namn och värdepar för avsöknings begär Anden.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointLocation
Anger platsen för slut punkten som används i metoden för prestanda trafik-routning.
Den här parametern är endast tillämpbar på slut punkter för ExternalEndpoints-eller NestedEndpoints-typen.
Du måste ange den här parametern när routningsmetoden för prestanda trafik används.

Ange ett Azure region namn.
En fullständig lista över Azure-regioner finns i Azure http://azure.microsoft.com/regions/ -regioner ( http://azure.microsoft.com/regions/) .

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
Listan med regioner som mappats till den här slut punkten med cirkulations metoden "geografisk". Se dokumentationen för Traffic Manager för en fullständig lista över godkända värden.

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
En fullständig lista över Azure-regioner finns i Azure http://azure.microsoft.com/regions/ -regioner ( http://azure.microsoft.com/regions/) .

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

### -Namn
Anger namnet på den Traffic Manager-slutpunkt som denna cmdlet skapar.

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

### -Profilnamn
Anger namnet på en Traffic Manager-profil där denna cmdlet lägger till en slut punkt.
För att få en profil, Använd New-AzTrafficManagerProfile eller Get-AzTrafficManagerProfile cmdletar.

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

### -ResourceGroupName
Anger namnet på en resurs grupp.
Den här cmdleten skapar en Traffic Manager-slutpunkt i gruppen som den här parametern anger.

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

### -SubnetMapping
Listan över adress områden eller undernät som mappats till den här slut punkten vid användning av routing-metoden "subnet".

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
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

### – Skriv
Anger den typ av slut punkt som denna cmdlet lägger till i Traffic Manager-profilen.
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


