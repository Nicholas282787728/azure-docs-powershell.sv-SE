---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: f0e66c1e601ab63eec6d2540edd3ba0235727e9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929721"
---
# New-AzureRmExpressRouteCircuitAuthorization

## Sammanfattning
Skapar en ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmExpressRouteCircuitAuthorization** skapar ett krets godkännande som kan läggas till i en ExpressRoute-krets. ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet. Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta ett nätverk till kretsen. Det kan bara finnas en auktorisering per virtuellt nätverk.

När du har skapat en ExpressRoute-krets kan du använda **Add-AzureRmExpressRouteCircuitAuthorization** för att lägga till ett godkännande till kretsen.
Alternativt kan du använda **New-AzureRmExpressRouteCircuitAuthorization** för att skapa ett godkännande som kan läggas till i en ny krets samtidigt som kretsen skapas.

## BESKRIVS

### Exempel 1: skapa en ny krets auktorisering
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Det här kommandot skapar en ny auktorisering av kretsen med namnet ContosoCircuitAuthorization och lagrar sedan objektet i en variabel som heter $Authorization. Det är viktigt att spara objektet till en variabel: även om det inte går att skapa en **AzureRmExpressRouteCircuitAuthorization** kan du inte lägga till auktorisationen i ett kretsar. I stället används variabel $Authorization New-AzureRmExpressRouteCircuit när du skapar en helt ny ExpressRoute-krets.

Mer information finns i dokumentationen för New-AzureRmExpressRouteCircuit-cmdleten.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger ett unikt namn för den nya ExpressRoute.

```yaml
Type: String
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

### Ingen
Denna cmdlet accepterar inte förloppet.

## VÄRDEN

### PSExpressRouteCircuitAuthorization
Denna cmdlet skapar instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuitAuthorization** -objektet.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

