---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228046"
---
# Add-AzExpressRouteCircuitAuthorization

## SYNOPSIS
Lägger till en ExpressRoute-kretsauktorisering.

## SYNTAX

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Add-AzExpressRouteCircuitAuthorization** lägger till en auktorisering till en ExpressRoute-krets. ExpressRoute-kretsar ansluter ditt lokala nätverk till Microsoft-molnet med hjälp av en anslutningsleverantör i stället för det offentliga Internet. Ägaren av en ExpressRoute-krets kan skapa upp till 10 auktoriseringar för varje krets. dessa auktoriseringar genererar en auktoriseringsnyckel som kan användas av en virtuell nätverksägare för att ansluta sitt nätverk till kretsen (en auktorisering per virtuellt nätverk). **Add-AzExpressRouteCircuitAuthorization** lägger till en ny auktorisering till en krets och genererar samtidigt motsvarande auktoriseringsnyckel. Du kan visa dessa nycklar när som helst genom att köra cmdleten Get-AzExpressRouteCircuitAuthorization och vid behov kopieras och vidarebefordras till rätt nätverksägare.
Observera att när du har **kört Add-AzExpressRouteCircuitAuthorization** måste du anropa cmdleten Set-AzExpressRouteCircuit för att aktivera nyckeln. Om du inte **anropar Set-AzExpressRouteCircuit** läggs auktoriseringen till i kretsen men aktiveras inte för användning.

## EXEMPEL

### Exempel 1: Lägg till en auktorisering till den angivna ExpressRoute-kretsen
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Med kommandona i det här exemplet lägger du till en ny auktorisering till en befintlig ExpressRoute-krets. Med det första kommandot **används Get-AzExpressRouteCircuit** för att skapa en objektreferens till en krets med namnet ContosoCircuit. Objektreferensen lagras i en variabel med namnet $Circuit.
I det andra kommandot används cmdleten **Add-AzExpressRouteCircuitAuthorization** till att lägga till en ny auktorisering (ContosoCircuitAuthorization) till ExpressRoute-kretsen. Det här kommandot lägger till auktoriseringen men aktiverar inte auktoriseringen. Om du vill aktivera en auktorisering **krävs den Set-AzExpressRouteCircuit** som visas i det sista kommandot i exemplet.

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
Anger ExpressRoute-kretsen som denna cmdlet lägger till auktoriseringen till.

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
Anger namnet på kretsauktoriseringen som ska läggas till.

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

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzExpressRouteCircuit](./Get-AzExpressRouteCircuit.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[New-AzExpressRouteCircuitAuthorization](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-AzExpressRouteCircuit](./Set-AzExpressRouteCircuit.md)
