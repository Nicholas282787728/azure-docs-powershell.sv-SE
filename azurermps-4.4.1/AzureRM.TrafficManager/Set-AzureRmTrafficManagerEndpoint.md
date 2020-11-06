---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 8856a2f9f1a65d6d312571d75e2400a7dcf30bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580496"
---
# Set-AzureRmTrafficManagerEndpoint

## Sammanfattning
Uppdaterar en hanterings slut punkt för trafik.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmTrafficManagerEndpoint** uppdaterar en slut punkt i Azure Traffic Manager.
Denna cmdlet uppdaterar inställningarna från ett lokalt slut punkts objekt.
Du kan ange ett slut punkts objekt genom att använda parametern *TrafficManagerEndpoint* eller genom att använda pipeline.

Du kan hämta ett lokalt objekt som representerar en slut punkt med hjälp av Get-AzureRmTrafficManagerEndpoint cmdlet.
Ändra objektet lokalt och Använd sedan **set-AzureRmTrafficManagerEndpoint** för att bekräfta dina ändringar.

## BESKRIVS

### Exempel 1: uppdatera en slut punkt
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Det första kommandot får en slut punkt för Azure Traffic Manager genom att använda cmdleten **Get-AzureRmTrafficManagerEndpoint** .
Kommandot lagrar slut punkten lokalt i $TrafficManagerEndpoint variabel.

Det andra kommandot ändrar slut punkten lokalt.
Det här kommandot ändrar slut punkts vikten till 20.

Det tredje kommandot uppdaterar slut punkten i Traffic Manager för att matcha det lokala värdet i $TrafficManagerEndpoint.

## MALLPARAMETRAR

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

### Microsoft. Azure. commands. Network. TrafficManagerEndpoint
Denna cmdlet accepterar ett **TrafficManagerEndpoint** -objekt.

## VÄRDEN

### Microsoft. Azure. commands. Network. TrafficManagerEndpoint
Denna cmdlet returnerar ett **TrafficManagerEndpoint** -objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

