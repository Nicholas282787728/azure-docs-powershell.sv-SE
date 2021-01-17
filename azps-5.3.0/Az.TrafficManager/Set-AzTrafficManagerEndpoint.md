---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423779"
---
# Set-AzTrafficManagerEndpoint

## Sammanfattning
Uppdaterar en hanterings slut punkt för trafik.

## FRÅGESYNTAXEN

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzTrafficManagerEndpoint** uppdaterar en slut punkt i Azure Traffic Manager.
Denna cmdlet uppdaterar inställningarna från ett lokalt slut punkts objekt.
Du kan ange ett slut punkts objekt genom att använda parametern *TrafficManagerEndpoint* eller genom att använda pipeline.

Du kan hämta ett lokalt objekt som representerar en slut punkt med hjälp av Get-AzTrafficManagerEndpoint cmdlet.
Ändra objektet lokalt och Använd sedan **set-AzTrafficManagerEndpoint** för att bekräfta dina ändringar.

## BESKRIVS

### Exempel 1: uppdatera en slut punkt
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Det första kommandot får en slut punkt för Azure Traffic Manager genom att använda cmdleten **Get-AzTrafficManagerEndpoint** .
Kommandot lagrar slut punkten lokalt i $TrafficManagerEndpoint variabel.

Det andra kommandot ändrar slut punkten lokalt.
Det här kommandot ändrar slut punkts vikten till 20.

Det tredje kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.

## MALLPARAMETRAR

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

### -TrafficManagerEndpoint
Anger ett lokalt **TrafficManagerEndpoint** -objekt.
Denna cmdlet uppdaterar trafik hanteraren så att den matchar detta lokala objekt.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint

## VÄRDEN

### Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerEndpoint

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
