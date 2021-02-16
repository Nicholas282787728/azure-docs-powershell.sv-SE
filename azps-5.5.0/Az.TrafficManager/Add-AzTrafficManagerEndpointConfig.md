---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252736"
---
# Add-AzTrafficManagerEndpointConfig

## SYNOPSIS
Lägger till en slutpunkt i ett lokalt Traffic Manager-profilobjekt.

## SYNTAX

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Add-AzTrafficManagerEndpointConfig** lägger till en slutpunkt till ett lokalt Azure Traffic Manager-profilobjekt.
Du kan få en profil med hjälp New-AzTrafficManagerProfile eller Get-AzTrafficManagerProfile cmdlets.

Den här cmdleten fungerar på det lokala profilobjektet.
Spara dina ändringar i profilen för Traffic Manager med hjälp av Set-AzTrafficManagerProfile cmdleten.
Om du vill skapa en slutpunkt och spara ändringen i en enda åtgärd använder du New-AzTrafficManagerEndpoint cmdleten.

## EXEMPEL

### Exempel 1: Lägga till en slutpunkt i en profil
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Det första kommandot får en Azure Traffic Manager-profil med cmdleten **Get-AzTrafficManagerProfile.**
Kommandot lagrar den lokala profilen i den $TrafficManagerProfile variabeln.

Med det andra kommandot läggs en slutpunkt med namnet Contoso till i den profil som lagras i $TrafficManagerProfile.
Kommandot innehåller konfigurationsdata för slutpunkten.
Det här kommandot ändrar bara det lokala objektet.

Det slutliga kommandot uppdaterar Traffic Manager-profilen i Azure så att den matchar det lokala värdet i $TrafficManagerProfile.

## PARAMETERS

### -CustomHeader
Lista över anpassade sidhuvudnamn och värdepar för avsökningsförfrågningar.

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Anger platsen för slutpunkten som ska användas i prestandatrafikdirigeringsmetoden.
Den här parametern gäller endast slutpunkter för ExternalEndpoints- eller NestedEndpoints-typen.
Du måste ange den här parametern när trafikdirigeringsmetoden för prestanda används.

Ange ett Azure-regionnamn.
En fullständig lista över Azure-regioner finns i Azure-regioner http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

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
Anger namnet på trafikhanterarens slutpunkt som denna cmdlet lägger till.

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
Anger slutpunktens status.
Giltiga värden är: 

- Aktiverad 
- Inaktiverad 

Om statusen är Aktiverad söker slutpunkten efter slutpunktens hälsa och ingår i metoden för trafikdirigering.

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

### -GeoMapping
Listan över regioner som mappats till den här slutpunkten när trafikdirigeringsmetoden "Geografisk" används. I dokumentationen till Trafikhanteraren finns en [fullständig lista över godkända värden.](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)

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

### -MinKontrollenEndpoints
Det minsta antalet slutpunkter som måste vara tillgängliga i den underordnade profilen för att den kapslade slutpunkten i den överordnade profilen ska anses vara tillgänglig.
Endast tillämpligt för slutpunkt av typen 'NestedEndpoints'.

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

### -Priority
Anger prioriteten som Trafikhanteraren tilldelar till slutpunkten.
Den här parametern används endast om profilen Traffic Manager är konfigurerad med metoden för trafikdirigering prioriterad.
Giltiga värden är heltal från 1 till 1 000.
Lägre värden representerar högre prioritet.

Om du anger en prioritet måste du ange prioritet för alla slutpunkter i profilen, och inga två slutpunkter kan dela samma prioritetsvärde.
Om du inte anger prioriteringar tilldelar Trafikhanteraren standardprioritetsvärden till slutpunkterna, med början från en (1), i den ordning som profilen listar slutpunkterna.

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

### -SubnetMapping
Listan med adressintervall eller undernät som mappas till den här slutpunkten när trafikdirigeringsmetoden "Undernät" används.

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

### -Target
Anger det fullständigt kvalificerade DNS-namnet för slutpunkten.
Trafikhanteraren returnerar det här värdet i DNS-svar när den dirigerar trafik till den här slutpunkten.
Ange endast den här parametern för slutpunktstypen ExternalEndpoints.
För andra slutpunktstyper anger du *parametern TargetResourceId i* stället.

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
Ange endast den här parametern för slutpunktstyperna AzureEndpoints och NestedEndpoints.
Ange målparametern i stället för  slutpunktstypen ExternalEndpoints.

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
Anger ett lokalt **TrafficManagerProfile-objekt.**
Den här cmdleten ändrar det här lokala objektet.
Om du vill **hämta ett TrafficManagerProfile-objekt** använder du Get-AzTrafficManagerProfile cmdleten.

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

### -Type
Anger vilken typ av slutpunkt som denna cmdlet lägger till i Azure Traffic Manager-profilen.
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

### -Weight
Anger den vikt som Trafikhanteraren tilldelar till slutpunkten.
Giltiga värden är heltal från 1 till 1 000.
Standardvärdet är ett (1).
Den här parametern används endast om profilen Traffic Manager är konfigurerad med metoden Viktad trafikdirigering.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## UTDATA

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


