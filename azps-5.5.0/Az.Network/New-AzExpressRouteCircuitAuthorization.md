---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223759"
---
# New-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Skapar en ExpressRoute-kretsauktorisering.

## SYNTAX

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzExpressRouteCircuitAuthorization** skapar en kretsauktorisering som kan läggas till i en ExpressRoute-krets. ExpressRoute-kretsar ansluter ditt lokala nätverk till Microsoft-molnet med hjälp av en anslutningsleverantör i stället för det offentliga Internet. Ägaren av en ExpressRoute-krets kan skapa upp till 10 auktoriseringar för varje krets. dessa auktoriseringar genererar en auktoriseringsnyckel som kan användas av en virtuell nätverksägare för att ansluta ett nätverk till kretsen. Det kan bara finnas en auktorisering per virtuellt nätverk.
När du har skapat en ExpressRoute-krets kan du lägga till en auktorisering för kretsen med **add-AzExpressRouteCircuitAuthorization.**
Alternativt kan du använda **New AzExpressRouteCircuitAuthorization** för att skapa en auktorisering som kan läggas till i en ny krets samtidigt som kretsen skapas.

## EXEMPEL

### Exempel 1: Skapa en ny kretsauktorisering
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Det här kommandot skapar en ny kretsauktorisering med namnet ContosoCircuitAuthorization och lagrar sedan objektet i en variabel med namnet $Authorization. Att spara objektet till en variabel är viktigt: även om **new-AzExpressRouteCircuitAuthorization** kan skapa en kretsauktorisering kan det inte lägga till den auktoriseringen till en kretsroute. Istället används de $Authorization vid skapande New-AzExpressRouteCircuit helt nya ExpressRoute-krets.
Mer information finns i dokumentationen för cmdleten New-AzExpressRouteCircuit.

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

### -Name
Anger ett unikt namn för den nya ExpressRoute-kretsauktoriseringen.

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

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

