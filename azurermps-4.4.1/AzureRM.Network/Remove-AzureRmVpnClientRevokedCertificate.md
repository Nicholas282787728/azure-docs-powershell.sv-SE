---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 7c6457e30140e10c5e6746c69a213f5ac4932cc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582300"
---
# Remove-AzureRmVpnClientRevokedCertificate

## Sammanfattning
Tar bort en VPN-klient-åter kallelse intyg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmVpnClientRevokedCertificate** tar bort ett certifikat för klient åter kallelse från en virtuell nätverksgateway.
Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.
Om du tar bort klient datorer för klient åter kallelse kan du använda det tidigare blockerade certifikatet för att skapa en anslutning till ett virtuellt privat nätverk (VPN).

## BESKRIVS

### Exempel 1: ta bort ett certifikat för klient åter kallelse från en virtuell nätverksgateway
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Det här kommandot tar bort ett certifikat för klient åter kallelse från en virtuell nätverksgateway som heter ContosoVirtualNetwork.
Om du vill ta bort ett certifikat för klient åter kallelse måste du ange både certifikatets namn och tumavtryck för certifikatet.

## MALLPARAMETRAR

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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tumavtryck
Anger unik identifierare för det certifikat som tas bort.

Du kan returnera tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det här:

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

Föregående kommando returnerar information för alla lokala dator certifikat i rot certifikat arkivet.

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

### -VirtualNetworkGatewayName
Anger namnet på den virtuella nätverksgateway som certifikatet har tilldelats till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRevokedCertificateName
Anger namnet på det VPN-klientcertifikat som tas bort.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmVpnClientRevokedCertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[Get-AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[New-AzureRmVpnClientRevokedCertificate](./New-AzureRmVpnClientRevokedCertificate.md)


