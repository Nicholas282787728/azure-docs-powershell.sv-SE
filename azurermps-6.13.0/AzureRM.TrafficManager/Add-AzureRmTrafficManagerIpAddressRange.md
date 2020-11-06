---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 213e959ecfec178644246f56be11e5b7306ef07f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573854"
---
# Add-AzureRmTrafficManagerIpAddressRange

## Sammanfattning
Lägger till ett adress intervall eller ett undernät i ett lokalt Traffic Manager-slutobjekt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmTrafficManagerIpAddressRange** lägger till ett IP-adressintervall till ett lokalt objekt i Azure Traffic Manager.
Du kan få en slut punkt genom att använda New-AzureRmTrafficManagerEndpoint eller Get-AzureRmTrafficManagerEndpoint cmdletar.

Denna cmdlet fungerar med det lokala slutpunktsmapparen.
Bekräfta dina ändringar av slut punkten för Traffic Manager genom att använda Set-AzureRmTrafficManagerEndpoint cmdlet.

## BESKRIVS

### Exempel 1: lägga till IP-adressintervall i en slut punkt
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Det första kommandot skapar en slut punkt för Azure Traffic Manager genom att använda cmdlet **New-AzureRmTrafficManagerEndpoint** .
Kommandot lagrar den lokala slut punkten i $TrafficManagerEndpoint variabel.
Det andra kommandot lägger till IP-adressintervallet 1.2.3.4 för att 5.6.7.8 till slut punkten som lagras i $TrafficManagerEndpoint.
Det tredje kommandot lägger till IP-adressintervallet 9.10.11.0 till 9.10.11.255 slut punkten som lagras i $TrafficManagerEndpoint.
Det fjärde kommandot verifierar att scopet matchar storleken på intervallet och lägger till IP-adressintervallet 12.13.14.0 till 12.13.14.31 till slut punkten som lagras i $TrafficManagerEndpoint.
Det femte kommandot lägger till IP-adressintervallet 15.16.17.18 till 15.16.17.18 slut punkten som lagras i $TrafficManagerEndpoint.
Kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.

## MALLPARAMETRAR

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

### -Senaste
Anger den sista IP-adressen i intervallet som ska läggas till.

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

### -Omfattning
Anger omfattningen för det IP-adressintervall som ska läggas till.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Anger ett lokalt **TrafficManagerEndpoint** -objekt.
Denna cmdlet ändrar detta lokala objekt.
Du kan hämta ett **TrafficManagerEndpoint** -objekt med hjälp av Get-AzureRmTrafficManagerEndpoint eller New-AzureRmTrafficManagerEndpoint cmdlet.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Först
Anger den första IP-adressen i intervallet som ska läggas till.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Network. TrafficManagerEndpoint
Denna cmdlet accepterar ett **TrafficManagerEndpoint** -objekt till denna cmdlet.

## VÄRDEN

### Microsoft. Azure. commands. Network. TrafficManagerEndpoint
Denna cmdlet returnerar ett ändrat **TrafficManagerEndpoint** -objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Remove-AzureRmTrafficManagerIpAddressRange](./Remove-AzureRmTrafficManagerIpAddressRange.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
