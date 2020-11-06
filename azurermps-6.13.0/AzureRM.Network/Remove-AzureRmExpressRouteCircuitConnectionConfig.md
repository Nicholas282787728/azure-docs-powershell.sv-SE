---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 6524e69662f26a993bbc9cdf74eba71ff801f879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576181"
---
# Remove-AzureRmExpressRouteCircuitConnectionConfig

## Sammanfattning
Tar bort en ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String>
 [-ExpressRouteCircuit] <PSExpressRouteCircuit> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmExpressRouteCircuitConnectionConfig** tar bort en konfiguration för ExpressRoute-anslutning som är kopplad till en given ExpressRoute-krets.

## BESKRIVS

### Exempel 1: ta bort en kabel anslutnings konfiguration från en ExpressRoute-krets
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### Exempel 2: ta bort en anslutnings konfiguration för en krets med ledning från en ExpressRoute-krets
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzureRmExpressRouteCircuit
```

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
ExpressRoute-kretsen som innehåller peering-konfigurationen som ska tas bort.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Namnet på den krets som ska tas bort.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
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

[Get-AzureRmExpressRouteCircuit](Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitConnectionConfig](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[Add-AzureRmExpressRouteCircuitConnectionConfig](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[Set-AzureRmExpressRouteCircuitConnectionConfig](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[New-AzureRmExpressRouteCircuitConnectionConfig](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[Set-AzureRmExpressRouteCircuit](Set-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuit](Get-AzureRmExpressRouteCircuit.md)
