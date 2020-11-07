---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 89106b6474e52863514c65614d334cf5d8382f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758155"
---
# New-AzureRmVpnClientIpsecParameter

## Sammanfattning
Med det här kommandot kan användarna skapa IPsec-parametrar-objekt med ett eller alla värden, till exempel IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, som ska anges på den befintliga VPN-gatewayen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Med det här kommandot kan användarna skapa IPsec-parametrar-objekt med ett eller alla värden, till exempel IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, som ska anges på den befintliga VPN-gatewayen.

## BESKRIVS

### Exempel 1
```
PS C:\> $vpnclientipsecparams1 = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

New-AzureRmVpnClientIpsecParameter cmdlet används för att skapa IPsec-parametrar-objektet för att använda en eller alla parametrar-värden som användaren kan ange för en befintlig virtuell nätverksgateway i ResourceGroup.
Det här skapade VpnClientIPsecParameters-objektet skickas till Set-AzureRmVpnClientIpsecParameter kommandot för att ange den angivna anpassade VPN-principen för IPSec på en virtuell nätverksgateway enligt exemplet ovan. Det här kommandot returnerar ett objekt med VpnClientIPsecParameters som visar inställda parametrar.

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

### -DhGroup
Vpnclient DH-grupper som används i IKE fas 1 för initial SA.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeEncryption
Vpnclient IKE-krypteringsalgoritm (IKE fas 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeIntegrity
Vpnclient IKE-integritetsalgoritm (IKE Phase 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecEncryption
Vpnclient IPSec-krypteringsalgoritm (IKE-fas 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecIntegrity
IPSec-integritetsalgoritmen Vpnclient (IKE-fas 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfsGroup
Vpnclient PFS-grupper som används i IKE fas 2 för ny underordnad SA

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SADataSize
Vpnclient säkerhets Association för IPSec (kallas även för en nytto Last storlek i KB för snabb läge eller fas 2)

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SALifeTime
Vpnclient säkerhets Association för IPSec (kallas även för snabb läge eller fas 2 SA) i sekunder

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSVpnClientIPsecParameters

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
