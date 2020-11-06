---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e1f85cbb90e1318c6eab595ef00929ceb1a5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574593"
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

### -Namn
Anger ett unikt namn för det nya klient certifikat för åter kallelse.

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

### -Tumavtryck
Anger unikt ID för det certifikat som läggs till.

Du kan returnera tumavtryck för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det här:

`Get-ChildItem -Path Cert:\LocalMachine\Root`

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


