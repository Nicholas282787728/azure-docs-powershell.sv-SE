---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 2cececec0610b813bf59a1ef8adac59e1fa8ddb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232383"
---
# Add-AzTrafficManagerIpAddressRange

## SYNOPSIS
Lägger till ett adressintervall eller ett undernät till ett lokalt slutpunktsobjekt i Trafikhanteraren.

## SYNTAX

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzTrafficManagerIpAddressRange** lägger till ett IP-adressintervall till ett lokalt slutpunktsobjekt för Azure Traffic Manager.
Du kan få en slutpunkt med hjälp New-AzTrafficManagerEndpoint eller Get-AzTrafficManagerEndpoint cmdlets.

Denna cmdlet fungerar på det lokala slutpunktsobjektet.
Bekräfta ändringarna i slutpunkten för Trafikhanteraren med hjälp av Set-AzTrafficManagerEndpoint cmdleten.

## EXEMPEL

### Exempel 1: Lägga till IP-adressintervall i en slutpunkt
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Det första kommandot skapar en Slutpunkt för Azure Traffic Manager med cmdleten **New-AzTrafficManagerEndpoint.**
Kommandot lagrar den lokala slutpunkten i $TrafficManagerEndpoint variabeln.
Det andra kommandot lägger till IP-adressintervallet 1.2.3.4 till 5.6.7.8 till slutpunkten som lagras i $TrafficManagerEndpoint.
Det tredje kommandot lägger till IP-adressintervallet 9.10.11.0 till 9.10.11.255 till slutpunkten som lagras i $TrafficManagerEndpoint.
Det fjärde kommandot verifierar att omfattningen matchar storleken på intervallet och lägger sedan till IP-adressintervallet 12.13.14.0 till 12.13.14.31 till slutpunkten som lagras i $TrafficManagerEndpoint.
Det femte kommandot lägger till IP-adressintervallet 15.16.17.18 till 15.16.17.18 till slutpunkten som lagras i $TrafficManagerEndpoint.
Det slutliga kommandot uppdaterar slutpunkten i Trafikhanteraren så att den matchar det lokala värdet i $TrafficManagerEndpoint.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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

### -Last
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
Anger omfattningen av det IP-adressintervall som ska läggas till.

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
Anger ett lokalt **TrafficManagerEndpoint-objekt.**
Den här cmdleten ändrar det här lokala objektet.
Om du vill **hämta ett TrafficManagerEndpoint-objekt** använder du Get-AzTrafficManagerEndpoint- New-AzTrafficManagerEndpoint-cmdleten.

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
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

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

### -First
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## UTDATA

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Remove-AzTrafficManagerIpAddressRange](./Remove-AzTrafficManagerIpAddressRange.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
