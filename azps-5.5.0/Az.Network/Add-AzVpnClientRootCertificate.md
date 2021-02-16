---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252480"
---
# Add-AzVpnClientRootCertificate

## SYNOPSIS
Lägger till ett VPN-klientrotcertifikat.

## SYNTAX

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzVpnClientRootCertificate** lägger till ett rotcertifikat i en virtuell nätverksgateway.
Rotcertifikat är X.509-certifikat som identifierar din rotcertifikatutfärdare.
Som standard litar alla certifikat som används på gatewayen på rotcertifikatet.
Den här cmdleten tilldelar ett befintligt certifikat som ett gatewayrotcertifikat.
Om du inte har något tillgängligt X.509-certifikat kan du generera ett genom den offentliga nyckelinfrastrukturen eller använda en certifikatgenerator som makecert.exe.
Om du vill lägga till ett rotcertifikat måste du ange certifikatnamnet och tillhandahålla en endast textrepresentation av certifikatet (mer information finns i *PublicCertData-parametern).*
Med Azure kan du tilldela mer än ett rotcertifikat till en gateway.
Flera rotcertifikat distribueras ofta av organisationer som inkluderar användare från fler än ett företag.

## EXEMPEL

### Exempel 1: Lägga till ett klientrotcertifikat i en virtuell gateway
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

I det här exemplet läggs ett klientrotcertifikat till i en virtuell gateway med namnet ContosoVirtualGateway.
Det första kommandot använder cmdleten **Get-Content** för att få en tidigare exporterad textrepresentation av rotcertifikatet och lagrar som textdata för variabeln $Text.
Det andra kommandot använder sedan en loop för att extrahera all text förutom den första och sista raden.
Den extraherade texten lagras i en variabel med namnet $CertificateText.
Det tredje kommandot använder sedan texten som lagras i $CertificateText med cmdleten **Add-AzVpnClientRootCertificate** för att lägga till rotcertifikatet i gatewayen.

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

### -PublicCertData
Anger textrepresentationen av rotcertifikatet som ska läggas till.
För att få textrepresentationen exporterar du ditt certifikat i CER-format (med Base64-kodning) och öppnar sedan den resulterande filen i en textredigerare.
När du gör det ser du följande utdata (observera att de faktiska utdata kommer att innehålla många fler rader med text än det förkortade exemplet som visas här): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HGUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData består av alla rader mellan den första raden (----- BEGIN CERTIFICATE -----) och den sista raden (----- END CERTIFICATE -----) i filen.
Du kan hämta dessa data med hjälp av Windows PowerShell-kommandon ungefär så här: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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
Anger namnet på resursgruppen som rotcertifikatet tilldelas till.
Resursgrupper kategoriserar objekt för att förenkla lagerhantering och allmän Azure-administration.

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
Anger namnet på den virtuella nätverksgatewayen där certifikatet läggs till.

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
Anger namnet på klientrotcertifikatet som denna cmdlet lägger till.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


