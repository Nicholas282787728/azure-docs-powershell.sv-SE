---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 75d86c77b57511b5a3fefb9cc21a668a81446746
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755664"
---
# Remove-AzureRmVpnClientRootCertificate

## Sammanfattning
Tar bort ett befintligt rot certifikat för en VPN-klient.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmVpnClientRootCertificate** tar bort det angivna rot certifikatet från en virtuell nätverksgateway.
Rot certifikat är 509 certifikat som identifierar rot certifikat utfärdaren: alla andra certifikat som används på gatewayen har rot certifikatet.
Om du tar bort en rot certifikat dator som använder certifikatet för verifiering kommer inte längre att kunna ansluta till gatewayen.

När du använder **Remove-AzureRmVpnClientRootCertificate** måste du ange både certifikat namnet och en text representation av certifikat data.
Mer information om hur du visar text i ett certifikat finns i beskrivningen av *PublicCertData* -parametern.

## BESKRIVS

### Exempel 1: ta bort ett klient rot certifikat från en virtuell nätverksgateway
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

I det här exemplet tas klient rot certifikatet bort med namnet ContosoRootCertificate från den virtuella Nätverksgatewayen ContosoVirtualGateway.

I det första kommandot används cmdleten **Get-Content** för att få en tidigare exporterad text från certifikatet; den här text presentationen lagras i en variabel som heter $Text.

Det andra kommandot använder sedan en for-slinga för att extrahera all text i $Text förutom den första raden och den sista raden.
Den extraherade texten lagras i en variabel som heter $CertificateText.

Det tredje kommandot använder informationen som lagras i $CertificateText variabel tillsammans med cmdleten **Remove-AzureRmVpnClientRootCertificate** för att ta bort certifikatet från gatewayen.

## MALLPARAMETRAR

### -PublicCertData
Anger text åter givningen för det rot certifikat som ska tas bort.
För att få text presentationen exporterar du certifikatet i CER-format (med base64-kodning) och öppnar sedan den resulterande filen i en text redigerare.
Utdata ser ut ungefär så här (Observera att den faktiska utmatningen innehåller många fler text rader än det förkortade provet här):

-----Starta certifikat----------avsluta certifikat-----

PublicCertData består av alla rader mellan den första raden (-----BEGIN CERTIFICATe-----) och den sista raden (-----slut certifikatet-----) i filen.
Du kan hämta PublicCertData med hjälp av Windows PowerShell-kommandon som följande:

$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = för ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

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

### -VirtualNetworkGatewayName
Anger namnet på den virtuella nätverksgateway som certifikatet tas bort från.

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
Anger namnet på klient rot certifikatet som denna cmdlet tar bort.

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

[Add-AzureRmVpnClientRootCertificate](./Add-AzureRmVpnClientRootCertificate.md)

[Get-AzureRmVpnClientRootCertificate](./Get-AzureRmVpnClientRootCertificate.md)

[New-AzureRmVpnClientRootCertificate](./New-AzureRmVpnClientRootCertificate.md)


