---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 5f642892413b027d3eee4dec3c0264587dbb02a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584140"
---
# Add-AzureRmVpnClientRootCertificate

## Sammanfattning
Lägger till en VPN-klient rot certifikat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmVpnClientRootCertificate** lägger till ett rot certifikat till en virtuell nätverksgateway.
Rot certifikat är 509 certifikat som identifierar din rot certifikat utfärdare.
Efter design är rot certifikatet som används på gatewayen.
Denna cmdlet tilldelar ett befintligt certifikat som ett Gateway-rotcertifikat.
Om du inte har något 509-certifikat tillgängligt kan du skapa ett via din offentliga infrastruktur eller använda en certifikat generator, till exempel makecert.exe.
Om du vill lägga till ett rot certifikat måste du ange certifikat namnet och tillhandahålla en representation av certifikatet (se *PublicCertData* -parametern för mer information).
Med Azure kan du tilldela mer än ett rot certifikat till en gateway.
Flera rot certifikat distribueras ofta av organisationer som innehåller användare från mer än ett företag.

## BESKRIVS

### Exempel 1: lägga till ett klient rot certifikat till en virtuell gateway
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

Det här exemplet lägger till ett klient rot certifikat till en virtuell gateway med namnet ContosoVirtualGateway.
I det första kommandot används cmdleten **Get-Content** för att få en tidigare exporterad text av rot certifikatet och lagrar text data som variabeln $text.
Det andra kommandot använder sedan en for-slinga för att extrahera all text förutom den första raden och den sista raden.
Den extraherade texten lagras i en variabel som heter $CertificateText.
Det tredje kommandot använder sedan den text som lagras i $CertificateText med cmdleten **Add-AzureRmVpnClientRootCertificate** för att lägga till rot certifikatet till gatewayen.

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

### -PublicCertData
Anger text representationen för det rot certifikat som ska läggas till.
För att få text presentationen exporterar du certifikatet i CER-format (med base64-kodning) och öppnar sedan den resulterande filen i en text redigerare.
När du gör det ser du utdata som liknar följande (Observera att den faktiska utmatningen innehåller många fler text rader än det förkortade provet som visas här):-----starta certifikatet-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----avsluta certifikatet-----PublicCertData är upptaget av alla linjer mellan den första raden (-----BEGIN CERTIFICATe-----) på filen.
Du kan hämta dessa data genom att använda Windows PowerShell-kommandon som det här: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

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

### -ResourceGroupName
Anger namnet på resurs gruppen som rot certifikatet är tilldelat till.
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

### -VirtualNetworkGatewayName
Anger namnet på den virtuella nätverksgateway där certifikatet läggs till.

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

### -VpnClientRootCertificateName
Anger namnet på klient rot certifikatet som läggs till av denna cmdlet.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSVpnClientRootCertificate

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmVpnClientRootCertificate](./Get-AzureRmVpnClientRootCertificate.md)

[New-AzureRmVpnClientRootCertificate](./New-AzureRmVpnClientRootCertificate.md)

[Remove-AzureRmVpnClientRootCertificate](./Remove-AzureRmVpnClientRootCertificate.md)


