---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 144d70318463b7c5ffebfa6b7d942ec2a351fc24
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929310"
---
# Remove-AzureRmExpressRouteCircuitAuthorization

## Sammanfattning
Tar bort en befintlig ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmExpressRouteCircuitAuthorization** tar bort ett godkännande som tilldelats en ExpressRoute-krets. ExpressRoute kretsar Anslut ditt lokala nätverk till Azure med hjälp av en anslutnings tjänst i stället för det offentliga Internet. Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta sitt nätverk till kretsen. Det kan bara finnas en auktorisering per virtuellt nätverk. Du kan när som helst använda **Remove-AzureRmExpressRouteCircuitAuthorization** för att ta bort auktoriseringen som tilldelats ett virtuellt nätverk. När det gäller det motsvarande virtuella nätverket kan du inte längre använda ExpressRoute-kretsen för att ansluta till Azure.

## BESKRIVS

### Exempel 1: ta bort en krets godkännande från en ExpressRoute-krets
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

I det här exemplet tas en krets bort från en ExpressRoute-krets. I det första kommandot används cmdleten **Get-AzureRmExpressRouteCircuit** för att skapa en objekt referens till en ExpressRoute-krets som heter ContosoCircuit och lagrar resultatet i variabeln som heter $Circuit.

Det andra kommandot markerar det ContosoCircuitAuthorization som ska tas bort.

Det tredje kommandot använder cmdleten Set-AzureRmExpressRouteCircuit för att bekräfta borttagningen av ExpressRoute-kretsen som lagras i $Circuit-variabeln.

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

### -ExpressRouteCircuit
Anger det ExpressRouteCircuit-objekt som denna cmdlet tar bort.

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den krets verifiering som tas bort av denna cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### PSExpressRouteCircuit
Denna cmdlet accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuit** -objektet.

## VÄRDEN

### PSExpressRouteCircuit
Denna cmdlet ändrar befintliga instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuit** -objektet.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[New-AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
