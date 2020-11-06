---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
ms.openlocfilehash: fc94bb7de5663995e75f0c4f1fed05fb36b35f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576226"
---
# Get-AzureRmVpnClientPackage

## Sammanfattning
Hämtar information om ett VPN-klient paket.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmVpnClientPackage** hämtar information om de VPN-klient paket som är tillgängliga från en virtuell nätverksgateway.
Klient paket innehåller konfigurations data som gör att en klient dator kan göra en VPN-anslutning till ett virtuellt Azure-nätverk. klient datorerna måste ha rätt konfigurations paket installerat för att kunna ringa en VPN-anslutning.
Olika konfigurations paket finns tillgängliga baserat på klient datorns version av Windows (till exempel Windows 7 eller Windows 10) och på klient datorns processor arkitektur (AMD64 eller x86).
Du måste ange arkitektur typen när du kör **Get-AzureRmVpnClientPackage**.

## BESKRIVS

### Exempel 1: Hämta information om ett processor arkitektur för VPN-klienter
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Med det här kommandot får du information om de AMD64 VPN-klient paket som lagras på den virtuella Nätverksgatewayen med namnet ContosoVirtualNetworkGateway.
Om du vill ha information om x86-klient paketen ställer du in värdet på *processorArchitecture* -parametern till x86.

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

### -ProcessorArchitecture
Anger vilken typ av CPU-arkitektur som klient paketet är avsett för.
Giltiga värden är amd64 och x86.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.
Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Anger namnet på den virtuella nätverksgateway där klient paket informationen lagras.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String
Parametrar: ResourceGroupName (ByValue), VirtualNetworkGatewayName (ByValue)

## VÄRDEN

### System. String

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Ändra storlek – AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


