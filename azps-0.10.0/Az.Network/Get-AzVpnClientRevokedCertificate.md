---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 3151ffb45064d1cb85b69d11a1ccbd49d4c045e8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922185"
---
# Get-AzVpnClientRevokedCertificate

## Sammanfattning
Hämtar information om certifikat för återkallade klienter.

## FRÅGESYNTAXEN

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzVpnClientRevokedCertificate** returnerar information om återkallade klient certifikat som har tilldelats till en virtuell nätverksgateway.
Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.
**Get-AzVpnClientRevokedCertificate** gör att du kan returnera information om alla klient återkallnings certifikat på gatewayen eller genom att använda parametern *VpnClientRevokedCertificateName* för att få information om ett enda certifikat.

## BESKRIVS

### Exempel 1: få information om alla certifikat för återkallning från klient
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

Det här kommandot får information om alla klient återkallnings certifikat som är kopplade till den virtuella Nätverksgatewayen med namnet ContosoVirtualNetworkGateway.

### Exempel 2: få information om specifika certifikat för åter kallelse av klient
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

Det här kommandot är en variant av kommandot som visas i exempel 1.
I det här fallet används *VpnClientRevokedCertificateName* -parametern för att begränsa den returnerade informationen till ett specifikt klient-återkallat certifikat: certifikatet med namnet ContosoRevokedClientCertificate.

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

### -VirtualNetworkGatewayName
Anger namnet på den virtuella nätverksgateway där den återkallade certifikat informationen är tilldelad.

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
Anger namnet på det VPN-klient certifikat som den här cmdleten får.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

###  
**Get-AzVpnClientRevokedCertificate** returnerar instanser av **Microsoft. Azure. commands. Network. Models. PSVpnClientRevokedCertificate** .

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[New-AzVpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


