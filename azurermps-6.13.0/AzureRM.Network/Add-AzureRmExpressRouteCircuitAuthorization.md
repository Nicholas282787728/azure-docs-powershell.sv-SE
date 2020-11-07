---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 108ea2b0262c34e38ffd7ed2961e3cba9a8d59ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755830"
---
# Add-AzureRmExpressRouteCircuitAuthorization

## Sammanfattning
Lägger till en ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmExpressRouteCircuitAuthorization** lägger till ett godkännande till en ExpressRoute-krets. ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet. Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta sitt nätverk till kretsen (en auktorisering per virtuellt nätverk). **Add-AzureRmExpressRouteCircuitAuthorization** lägger till ett nytt tillstånd för en krets och på samma gång genererar motsvarande auktoriseringspost. Dessa nycklar kan visas när som helst genom att köra Get-AzureRmExpressRouteCircuitAuthorization cmdlet och, om det behövs, och sedan kopieras och vidarebefordras till en lämplig nätverks ägare.
Observera att när du har kört **Add-AzureRmExpressRouteCircuitAuthorization** måste du anropa Set-AzureRmExpressRouteCircuit cmdlet för att aktivera den. Om du inte anropar **set-AzureRmExpressRouteCircuit** kommer tillståndet att läggas till i kretsen men inte aktive ras för användning.

## BESKRIVS

### Exempel 1: lägga till ett godkännande för den angivna ExpressRoute-kretsen
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Kommandona i det här exemplet lägger till ett nytt godkännande i en befintlig ExpressRoute-krets. Det första kommandot använder funktionen **Get-AzureRmExpressRouteCircuit** för att skapa en objekt referens till en krets med namnet ContosoCircuit. Objekt referensen lagras i en variabel som heter $Circuit.
I det andra kommandot används cmdleten **Add-AzureRmExpressRouteCircuitAuthorization** för att lägga till en ny auktorisering (ContosoCircuitAuthorization) i ExpressRoute-kretsen. Det här kommandot lägger till auktoriseringen men aktiverar inte den auktoriseringen. Om du aktiverar ett godkännande krävs **set-AzureRmExpressRouteCircuit** som visas i det sista kommandot i exemplet.

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

### -ExpressRouteCircuit
Anger den ExpressRoute-krets som den här cmdleten lägger till för auktoriseringen.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den krets som ska läggas till.

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

### Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit
Parametrar: ExpressRouteCircuit (ByValue)

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSExpressRouteCircuit

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[New-AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
