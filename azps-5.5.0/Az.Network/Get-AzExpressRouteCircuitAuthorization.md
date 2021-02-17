---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218814"
---
# Get-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Hämtar information om ExpressRoute-kretsauktoriseringar.

## SYNTAX

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzExpressRouteCircuitAuthorization** får information om auktoriseringarna för en ExpressRoute-krets. ExpressRoute-kretsar ansluter ditt lokala nätverk till Microsoft-molnet med hjälp av en anslutningsleverantör i stället för det offentliga Internet. Ägaren av en ExpressRoute-krets kan skapa upp till 10 auktoriseringar för varje krets. dessa auktoriseringar genererar en auktoriseringsnyckel som kan användas av en virtuell nätverksägare för att ansluta sitt nätverk till kretsen (en auktorisering per virtuellt nätverk). Auktoriseringsnycklar, liksom annan information om auktoriseringen, kan visas när som helst genom att köra **Get-AzExpressRouteCircuitAuthorization.**

## EXEMPEL

### Exempel 1: Hämta alla ExpressRoute-auktoriseringar
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Dessa kommandon returnerar information om alla ExpressRoute-auktoriseringar som är associerade med en ExpressRoute-krets. Det första kommandot använder cmdleten **Get-AzExpressRouteCircuit** för att skapa en objektreferens för en krets med namnet ContosoCircuit. objektreferensen lagras i den variabla $Circuit. Det andra kommandot använder sedan objektreferensen och cmdleten **Get-AzExpressRouteCircuitAuthorization** för att returnera information om auktoriseringarna som associeras med ContosoCircuit.

### Exempel 2: Hämta alla ExpressRoute-auktoriseringar med hjälp Where-Object cmdlet
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Dessa kommandon representerar en variant av kommandona som används i exempel 1. I det här fallet returneras dock endast information för de auktoriseringar som är tillgängliga för användning (d.v.s. för auktoriseringar som inte har tilldelats till ett virtuellt nätverk). För att göra detta returneras kretsauktoriseringsinformationen i kommando 2 och ledas till cmdleten **Where-Object.**
**Där objektet sedan** hämtar endast de auktoriseringar där *egenskapen AuthorizationUseStatus* är inställd på Tillgänglig. Om du bara vill visa de auktoriseringar som inte är tillgängliga använder du följande syntax för Where-satsen: `{$_.AuthorizationUseStatus -ne "Available"}`

## PARAMETERS

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

### -ExpressRouteCircuit
Anger ExpressRoute-kretsauktoriseringen.

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

### -Name
Anger namnet på ExpressRoute-kretsauktoriseringen som denna cmdlet får.
-Name "ContosoCircuitAuthorization"

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)
