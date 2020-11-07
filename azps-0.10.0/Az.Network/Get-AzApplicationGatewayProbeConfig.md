---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: b3e2b3ea03ca0bae0db1bea1606e4ae6b94a597e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922320"
---
# Get-AzApplicationGatewayProbeConfig

## Sammanfattning
Hämtar en befintlig Health PROBE-konfiguration från en Programgateway.

## FRÅGESYNTAXEN

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Den Get-AzApplicationGatewayProbeConfig cmdleten hämtar en befintlig Health PROBE-konfiguration från en Programgateway.

## BESKRIVS

### Exempel 1: Hämta en befintlig sond från en Programgateway
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

Det här kommandot får hälso avsökningen med namnet Probe02 från programgatewayen heter Gateway.

## MALLPARAMETRAR

### -ApplicationGateway
Anger den Programgateway som denna cmdlet ska ha en PROBE-konfiguration för.

```yaml
Type: PSApplicationGateway
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
Anger namnet på sonden.

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

### PSApplicationGateway
Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbe

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. Network. Models. PSApplicationGatewayProbe]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Lägga till en sond i en befintlig Application Gateway](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[Add-AzApplicationGatewayProbeConfig]()

[New-AzApplicationGatewayProbeConfig]()

[Remove-AzApplicationGatewayProbeConfig]()

[Set-AzApplicationGatewayProbeConfig]()

