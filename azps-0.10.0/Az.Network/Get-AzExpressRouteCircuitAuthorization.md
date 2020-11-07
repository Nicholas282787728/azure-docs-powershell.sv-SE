---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3b51a16d6ff2de8292b1bbb66f7f5ab24cc17b93
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922284"
---
# Get-AzExpressRouteCircuitAuthorization

## Sammanfattning
Hämtar information om ExpressRoute.

## FRÅGESYNTAXEN

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzExpressRouteCircuitAuthorization** hämtar information om de godkännanden som tilldelats en ExpressRoute-krets. ExpressRoute kretsar Anslut det lokala nätverket till Microsoft Cloud genom att använda en anslutnings leverantör i stället för det offentliga Internet. Ägaren till en ExpressRoute-krets kan skapa upp till 10 godkännanden för varje krets; dessa godkännanden genererar en auktoriseringsregel som kan användas av en virtuell nätverks ägare för att ansluta sitt nätverk till kretsen (en auktorisering per virtuellt nätverk). Auktoriseringsregler, samt annan information om auktoriseringen, kan visas när som helst genom att köra **Get-AzExpressRouteCircuitAuthorization**.

## BESKRIVS

### Exempel 1: skaffa alla ExpressRoute-godkännanden
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

De här kommandona returnerar information om alla ExpressRoute-godkännanden som är associerade med en ExpressRoute-krets. I det första kommandot används cmdleten **Get-AzExpressRouteCircuit** för att skapa en objekt referens med en krets som heter ContosoCircuit; objekt referensen lagras i variabeln $Circuit. Det andra kommandot använder då objekt referensen och cmdleten **Get-AzExpressRouteCircuitAuthorization** för att returnera information om godkännanden som är associerade med ContosoCircuit.

### Exempel 2: Hämta alla ExpressRoute-tillstånd med Where-Object cmdlet
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

De här kommandona representerar en variant av kommandona som används i exempel 1. I det här fallet returneras informationen endast för de godkännanden som är tillgängliga för användning (det vill säga för godkännanden som inte har tilldelats ett virtuellt nätverk). För att göra det här returneras information om kretsen i kommando 2 och är piped till cmdleten **Where-Object** .
**WHERE-objekt** gör sedan endast för de godkännanden där egenskapen *AuthorizationUseStatus* är tillgänglig. Om du bara vill lista de godkännanden som inte är tillgängliga använder du denna syntax för WHERE-satsen:

`{$_.AuthorizationUseStatus -ne "Available"}`

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
Anger ExpressRoute.

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
Anger namnet på den ExpressRoute som den här cmdleten får.

-Name "ContosoCircuitAuthorization"

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### PSExpressRouteCircuit
**Get-AzExpressRouteCircuitAuthorization** accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuit.**

## VÄRDEN

### PSExpressRouteCircuitAuthorization
**Get-AzExpressRouteCircuitAuthorization** returnerar instanser av **Microsoft. Azure. commands. Network. Models. PSExpressRouteCircuitAuthorization** .

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
