---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227607"
---
# New-AzVpnClientRevokedCertificate

## SYNOPSIS
Skapar ett nytt VPN-klientåterkallningscertifikat.

## SYNTAX

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzVpnClientRevokedCertificate** skapar ett nytt virtuellt privat nätverkscertifikat (VPN) för användning i en virtuell nätverksgateway.
Klientåterkallningscertifikat hindrar klientdatorer från att använda det angivna certifikatet för autentisering.
Den här cmdleten skapar ett fristående certifikat som inte har tilldelats till en virtuell gateway.
I stället används certifikatet som skapas av **New-AzVpnClientRevokedCertificate** tillsammans med cmdleten New-AzVirtualNetworkGateway när den skapar en ny gateway.
Anta att du skapar ett nytt certifikat och sparar det i en variabel med namnet $Certificate.
Du kan sedan använda certifikatobjektet när du skapar en ny virtuell gateway.
Exempel: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
Mer information finns i dokumentationen för cmdleten New-AzVirtualNetworkGateway.

## EXEMPEL

### Exempel 1: Skapa ett nytt klient återkallat certifikat
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Det här kommandot skapar ett nytt klient återkallat certifikat och lagrar certifikatobjektet i en variabel med namnet $Certificate.
Den här variabeln kan sedan användas av cmdleten **New-AzVirtualNetworkGateway** för att lägga till certifikatet i en ny virtuell nätverksgateway.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -Name
Anger ett unikt namn för det nya klientåterkallningscertifikatet.

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

### -Thumbprint
Anger unik identifierare för certifikatet som läggs till.
Du kan returnera tumutskriftsinformation för dina certifikat genom att använda ett Windows PowerShell-kommando som liknar det här: `Get-ChildItem -Path Cert:\LocalMachine\Root`
Med föregående kommando returneras information för alla lokala datorcertifikat som finns i rotcertifikatarkivet.

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

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


