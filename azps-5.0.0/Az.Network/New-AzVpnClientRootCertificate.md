---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271477"
---
# New-AzVpnClientRootCertificate

## Sammanfattning
Skapar ett nytt rot certifikat för en VPN-klient.

## FRÅGESYNTAXEN

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzVpnClientRootCertificate** skapar ett nytt VPN-rotcertifikat för användning på en virtuell nätverksgateway.
Rot certifikat är 509 certifikat som identifierar rot certifikat utfärdaren: alla andra certifikat som används på gatewayen har rot certifikatet.
Denna cmdlet skapar ett fristående certifikat som inte är kopplat till en virtuell gateway.
I stället används certifikatet som skapas av **New-AzVpnClientRootCertificate** tillsammans med New-AzVirtualNetworkGateway cmdlet när du skapar en ny Gateway.
Anta till exempel att du skapar ett nytt certifikat och lagrar det i en variabel som heter $Certificate.
Du kan sedan använda detta certifikat objekt när du skapar en ny virtuell gateway.
Till exempel: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
Mer information finns i dokumentationen för New-AzVirtualNetworkGateway-cmdleten.

## BESKRIVS

### Exempel 1: skapa ett klient rot certifikat
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

I det här exemplet skapas ett klient rot certifikat och ett certifikat objekt sparas i en variabel som heter $Certificate.
Denna variabel kan sedan användas av **New-AzVirtualNetworkGateway-** cmdleten för att lägga till ett rot certifikat till en ny virtuell nätverksgateway.
I det första kommandot används cmdleten **Get-Content** för att få en tidigare exporterad text representation av rot certifikatet. att text data lagras i en variabel som heter $Text.
Det andra kommandot använder sedan en for-slinga för att extrahera all text förutom den första raden och den sista raden, och sedan spara den extraherade texten i en variabel som heter $CertificateText.
I det tredje kommandot används cmdleten **New-AzVpnClientRootCertificate** för att skapa certifikatet, vilket sparar det skapade objektet i en variabel som heter $Certificate.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -Namn
Anger ett namn för det nya klient rot certifikatet.

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
Anger en text representation av rot certifikatet som ska läggas till.
För att få text presentationen exporterar du certifikatet i CER-format (med base64-kodning) och öppnar sedan den resulterande filen i en text redigerare.
Utdata ser ut ungefär så här (Observera att den faktiska utmatningen innehåller många fler text rader än det förkortade provet som visas här):-----starta certifikatet-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----avsluta certifikat-----PublicCertData är upptaget av alla linjer mellan den första raden (-----BEGIN CERTIFICATe-----) och den sista raden (-----slut certifikat-----) i filen.
Du kan hämta PublicCertData med hjälp av Windows PowerShell-kommandon som liknar detta: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = för ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSVpnClientRootCertificate

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


