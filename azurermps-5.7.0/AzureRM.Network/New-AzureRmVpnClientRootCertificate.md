---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: b83af7bc0242ddf1c1ed5c182cd0be7c2b7d8a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757658"
---
# New-AzureRmVpnClientRootCertificate

## Sammanfattning
Skapar ett nytt rot certifikat för en VPN-klient.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmVpnClientRootCertificate** skapar ett nytt VPN-rotcertifikat för användning på en virtuell nätverksgateway.
Rot certifikat är 509 certifikat som identifierar rot certifikat utfärdaren: alla andra certifikat som används på gatewayen har rot certifikatet.

Denna cmdlet skapar ett fristående certifikat som inte är kopplat till en virtuell gateway.
I stället används certifikatet som skapas av **New-AzureRmVpnClientRootCertificate** tillsammans med New-AzureRmVirtualNetworkGateway cmdlet när du skapar en ny Gateway.
Anta till exempel att du skapar ett nytt certifikat och lagrar det i en variabel som heter $Certificate.
Du kan sedan använda detta certifikat objekt när du skapar en ny virtuell gateway.
Till exempel:

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

Mer information finns i dokumentationen för New-AzureRmVirtualNetworkGateway-cmdleten.

## BESKRIVS

### Exempel 1: skapa aclient rot certifikat
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

I det här exemplet skapas ett klient rot certifikat och ett certifikat objekt sparas i en variabel som heter $Certificate.
Denna variabel kan sedan användas av **New-AzureRmVirtualNetworkGateway-** cmdleten för att lägga till ett rot certifikat till en ny virtuell nätverksgateway.

I det första kommandot används cmdleten **Get-Content** för att få en tidigare exporterad text representation av rot certifikatet. att text data lagras i en variabel som heter $Text.

Det andra kommandot använder sedan en for-slinga för att extrahera all text förutom den första raden och den sista raden, och sedan spara den extraherade texten i en variabel som heter $CertificateText.

I det tredje kommandot används cmdleten **New-AzureRmVpnClientRootCertificate** för att skapa certifikatet, vilket sparar det skapade objektet i en variabel som heter $Certificate.

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
Anger ett namn för det nya klient rot certifikatet.

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

### -PublicCertData
Anger en text representation av rot certifikatet som ska läggas till.
För att få text presentationen exporterar du certifikatet i CER-format (med base64-kodning) och öppnar sedan den resulterande filen i en text redigerare.
Utdata ser ut ungefär så här (Observera att den faktiska utmatningen innehåller många fler text rader än det förkortade provet här):

-----Starta certifikat----------avsluta certifikat-----

PublicCertData består av alla rader mellan den första raden (-----BEGIN CERTIFICATe-----) och den sista raden (-----slut certifikatet-----) i filen.
Du kan hämta PublicCertData genom att använda Windows PowerShell-kommandon som det här:

$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = för ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

###  
Denna cmdlet accepterar inte förloppet.

## VÄRDEN

###  
Denna cmdlet skapar nya instanser av **Microsoft. Azure. commands. Network. Models. PSVpnClientRootCertificate** -objektet.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmVpnClientRootCertificate](./Add-AzureRmVpnClientRootCertificate.md)

[Get-AzureRmVpnClientRootCertificate](./Get-AzureRmVpnClientRootCertificate.md)

[Remove-AzureRmVpnClientRootCertificate](./Remove-AzureRmVpnClientRootCertificate.md)


