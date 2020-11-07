---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: b1c802425576679da2238afffc0b40b77fc64193
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928710"
---
# New-AzureRmVpnClientRevokedCertificate

## Sammanfattning
Skapar en ny VPN-klient-åter kallelse intyg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmVpnClientRevokedCertificate** skapar ett nytt virtuellt privat nätverk (VPN)-certifikat för åter kallelse för användning på en virtuell nätverksgateway.
Certifikat för klient åter kallelse gör att klient datorer inte använder det angivna certifikatet för att verifiera.

Denna cmdlet skapar ett fristående certifikat som inte är kopplat till en virtuell gateway.
I stället används certifikatet som skapas av **New-AzureRmVpnClientRevokedCertificate** tillsammans med New-AzureRmVirtualNetworkGateway cmdlet när en ny Gateway skapas.
Antag till exempel att du skapar ett nytt certifikat och lagrar det i en variabel som heter $Certificate.
Du kan sedan använda detta certifikat objekt när du skapar en ny virtuell gateway.
Till exempel:

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

Mer information finns i dokumentationen för New-AzureRmVirtualNetworkGateway-cmdleten.

## BESKRIVS

### Exempel 1: skapa ett nytt klient-återkallat certifikat
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Det här kommandot skapar ett nytt klient-återkallat certifikat och lagrar certifikat-objektet i en variabel som heter $Certificate.
Denna variabel kan sedan användas av **New-AzureRmVirtualNetworkGateway-** cmdleten för att lägga till certifikatet till en ny virtuell nätverksgateway.

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

### -Namn
Anger ett unikt namn för det nya klient certifikat för åter kallelse.

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

### -Tumavtryck
Anger unikt ID för det certifikat som läggs till.

Du kan returnera tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det här:

`Get-ChildItem -Path Cert:\LocalMachine\Root`

Föregående kommando returnerar information för alla lokala dator certifikat i rot certifikat arkivet.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

###  
Denna cmdlet accepterar inte förloppet.

## VÄRDEN

###  
Denna cmdlet skapar nya instanser av **Microsoft. Azure. commands. Network. Models. PSVpnClientRevokedCertificate** -objektet.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmVpnClientRevokedCertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[Get-AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[Remove-AzureRmVpnClientRevokedCertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


