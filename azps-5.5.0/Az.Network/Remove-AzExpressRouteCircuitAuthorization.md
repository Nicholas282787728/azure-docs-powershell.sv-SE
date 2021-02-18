---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225846"
---
# Remove-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Tar bort en befintlig ExpressRoute-konfigurationsauktorisering.

## SYNTAX

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Remove-AzExpressRouteCircuitAuthorization** tar bort en auktorisering som tilldelats en ExpressRoute-krets. ExpressRoute-kretsar ansluter ditt lokala nätverk till Azure med hjälp av en anslutningsleverantör i stället för det offentliga Internet. Ägaren av en ExpressRoute-krets kan skapa upp till 10 auktoriseringar för varje krets. Dessa auktoriseringar genererar en auktoriseringsnyckel som kan användas av en virtuell nätverksägare för att ansluta sitt nätverk till kretsen. Det kan bara finnas en auktorisering per virtuellt nätverk. När som helst kan kretsägaren däremot använda **Remove-AzExpressRouteCircuitAuthorization** för att ta bort auktoriseringen som tilldelats ett virtuellt nätverk. När det händer kan motsvarande virtuella nätverk inte längre använda ExpressRoute-kretsen för att ansluta till Azure.

## EXEMPEL

### Exempel 1: Ta bort en kretsauktorisering från en ExpressRoute-krets
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

I det här exemplet tas en kretsauktorisering bort från en ExpressRoute-krets. Det första kommandot använder cmdleten **Get-AzExpressRouteCircuit** för att skapa en objektreferens till en ExpressRoute-krets med namnet ContosoCircuit och lagrar resultatet i variabeln $Circuit.
Det andra kommandot markerar kretsauktoriseringen ContosoCircuitAuthorization för borttagning.
Det tredje kommandot använder cmdleten Set-AzExpressRouteCircuit för att bekräfta borttagningen av ExpressRoute-kretsen som $Circuit variabeln.

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

### -ExpressRouteCircuit
Anger ExpressRouteCircuit-objektet som cmdleten tar bort.

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
Anger namnet på kretsauktoriseringen som denna cmdlet tar bort.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
