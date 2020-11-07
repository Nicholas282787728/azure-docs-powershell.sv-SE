---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: e2a2153ca9d75447603ce87c896720ece0f83a18
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931354"
---
# Add-AzureRmVpnClientRevokedCertificate

## Sammanfattning
Lägger till en VPN-klient-åter kallelse intyg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmVpnClientRevokedCertificate** tilldelar ett certifikat för klient åter kallelse till en virtuell nätverksgateway.
Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.
Du måste ange både certifikat namnet och tumavtrycket för att använda denna cmdlet.

## BESKRIVS

### Exempel 1: lägga till ett nytt klient certifikat för åter kallelse till en virtuell nätverksgateway
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Det här kommandot lägger till ett nytt klient åter kallelse certifikat till den virtuella Nätverksgatewayen med namnet ContosoVirtualNetwork.
För att lägga till certifikatet måste du ange både certifikatets namn och tumavtryck för certifikatet.

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

### -ResourceGroupName
Anger namnet på den resurs grupp som den virtuella Nätverksgatewayen är tilldelad till.

Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tumavtryck
Anger unikt ID för det certifikat som läggs till.
Till exempel:

-Tumavtryck "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"

Du kan få information om tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det `Get-ChildItem -Path Cert:\LocalMachine\Root` här:

Med föregående kommando hämtas information för alla lokala dator certifikat i rot certifikat arkivet.

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

### -VirtualNetworkGatewayName
Anger namnet på den virtuella nätverksgateway där certifikatet ska läggas till.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRevokedCertificateName
Anger namnet på det VPN-klientcertifikat som ska läggas till.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSVpnClientRevokedCertificate

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[New-AzureRmVpnClientRevokedCertificate](./New-AzureRmVpnClientRevokedCertificate.md)

[Remove-AzureRmVpnClientRevokedCertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


