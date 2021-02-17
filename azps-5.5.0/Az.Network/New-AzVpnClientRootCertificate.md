---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225902"
---
# New-AzVpnClientRootCertificate

## SYNOPSIS
Skapar ett nytt VPN-klientrotcertifikat.

## SYNTAX

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzVpnClientRootCertificate** skapar ett nytt VPN-rotcertifikat för användning i en virtuell nätverksgateway.
Rotcertifikat är X.509-certifikat som identifierar rotcertifikatutfärdaren: alla andra certifikat som används på gatewayen litar på rotcertifikatet.
Den här cmdleten skapar ett fristående certifikat som inte har tilldelats till en virtuell gateway.
I stället används certifikatet som skapas av **New-AzVpnClientRootCertificate** tillsammans med cmdleten New-AzVirtualNetworkGateway när du skapar en ny gateway.
Anta till exempel att du skapar ett nytt certifikat och lagrar det i en variabel med namnet $Certificate.
Du kan sedan använda certifikatobjektet när du skapar en ny virtuell gateway.
Exempel: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
Mer information finns i dokumentationen för cmdleten New-AzVirtualNetworkGateway.

## EXEMPEL

### Exempel 1: Skapa ett rotcertifikat för klienten
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

I det här exemplet skapas ett klientrotcertifikat och certifikatobjektet lagras i en variabel med namnet $Certificate.
Den här variabeln kan sedan användas av cmdleten **New-AzVirtualNetworkGateway** för att lägga till ett rotcertifikat i en ny virtuell nätverksgateway.
Det första kommandot använder **cmdleten Get-Content** för att få en tidigare exporterad textrepresentation av rotcertifikatet. att textdata lagras i en variabel med namnet $Text.
Det andra kommandot använder sedan en loop för att extrahera all text förutom den första och den sista raden, och lagra den extraherade texten i en variabel med namnet $CertificateText.
Det tredje kommandot använder cmdleten **New-AzVpnClientRootCertificate** för att skapa certifikatet och lagra det skapade objektet i en variabel med namnet $Certificate.

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
Anger ett namn för det nya rotcertifikatet för klienten.

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

### -PublicCertData
Anger en textrepresentation av rotcertifikatet som ska läggas till.
För att få textrepresentationen exporterar du ditt certifikat i CER-format (med Base64-kodning) och öppnar sedan den resulterande filen i en textredigerare.
Du bör se utdata som liknar detta (observera att de faktiska utdata kommer att innehålla många fler rader med text än det förkortade exemplet som visas här): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData består av alla rader mellan den första raden (----- BEGIN CERTIFICATE -----) och den sista raden (----- END CERTIFICATE -----) i filen.
Du kan hämta PublicCertData med hjälp av Windows PowerShell-kommandon ungefär så här: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = för ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


