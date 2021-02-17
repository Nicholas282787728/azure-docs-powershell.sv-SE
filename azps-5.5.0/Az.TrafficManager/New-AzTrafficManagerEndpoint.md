---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229582"
---
# New-AzTrafficManagerEndpoint

## SYNOPSIS
Skapar en slutpunkt i en Trafikhanteraren-profil.

## SYNTAX

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten New-AzTrafficManagerEndpoint** skapar en slutpunkt i en Azure Traffic Manager-profil.

Den här cmdleten åtar sig varje ny slutpunkt till tjänsten Traffic Manager.
Om du vill lägga till flera slutpunkter i ett lokalt Traffic Manager-profilobjekt och spara ändringar i en enda åtgärd använder du Add-AzTrafficManagerEndpointConfig-cmdleten.

## EXEMPEL

### Exempel 1: Skapa en extern slutpunkt för en profil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Med det här kommandot skapas en extern slutpunkt med namnet contoso i profilen ContosoProfile i resursgruppen ResourceGroup11.

### Exempel 2: Skapa en Azure-slutpunkt för en profil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Det här kommandot skapar en Azure-slutpunkt med namnet contoso i profilen ContosoProfile i resursgruppen ResourceGroup11.
Azure-slutpunkten pekar på den Azure Web App vars Azure Resource Manager-ID anges av URI-sökvägen i *TargetResourceId.*
Kommandot anger inte parametern *EndpointLocation eftersom* Web App-resursen tillhandahåller platsen.

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
Den här parametern gäller endast slutpunkter för typen ExternalEndpoints eller NestedEndpoints.
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
Listan över regioner som mappats till den här slutpunkten när trafikdirigeringsmetoden "Geografisk" används. I dokumentationen till Trafikhanteraren finns en fullständig lista över godkända värden.

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
Ange ett Azure-regionnamn.
En fullständig lista över Azure-regioner finns i Azure-regioner http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .

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

### -Name
Anger namnet på slutpunkten för Trafikhanteraren som denna cmdlet skapar.

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

### -ProfileName
Anger namnet på en Trafikhanteraren-profil som denna cmdlet lägger till en slutpunkt för.
Om du vill skaffa en profil använder du New-AzTrafficManagerProfile eller Get-AzTrafficManagerProfile cmdlets.

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
Anger namnet på en resursgrupp.
Den här cmdleten skapar en slutpunkt för Trafikhanteraren i gruppen som den här parametern anger.

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
Anger slutpunktens fullständigt kvalificerade DNS-namn.
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

### -Type
Anger vilken typ av slutpunkt som denna cmdlet lägger till i profilen i Trafikhanteraren.
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

### Ingen

## UTDATA

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


