---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 5cb4a57994ad8b15048bfc22dadefbbee031aaf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213471"
---
# Remove-AzVpnClientRootCertificate

## SYNOPSIS
Tar bort ett befintligt VPN-klientrotcertifikat.

## SYNTAX

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzVpnClientRootCertificate** tar bort det angivna rotcertifikatet från en virtuell nätverksgateway.
Rotcertifikat är X.509-certifikat som identifierar rotcertifikatutfärdaren: alla andra certifikat som används på gatewayen litar på rotcertifikatet.
Om du tar bort rotcertifikatdatorer som använder certifikatet för autentisering kommer de inte längre att kunna ansluta till gatewayen.
När du använder **Remove-AzVpnClientRootCertificate** måste du ange både certifikatnamnet och en textrepresentation av certifikatdata.
Mer information om ett certifikats textrepresentation finns i parameterbeskrivningen *PublicCertData.*

## EXEMPEL

### Exempel 1: Ta bort ett klientrotcertifikat från en virtuell nätverksgateway
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

I det här exemplet tas ett klientrotcertifikat med namnet ContosoRootCertificate bort från den virtuella nätverksgatewayen ContosoVirtualGateway.
Det första kommandot använder **cmdleten Get-Content** för att få en tidigare exporterad textrepresentation av certifikatet. den här textrepresentationen lagras i en variabel $Text.
Det andra kommandot använder sedan en loop för att extrahera all text i $Text förutom den första och sista raden.
Denna extraherade text lagras i en variabel med namnet $CertificateText.
Det tredje kommandot använder informationen som lagras i $CertificateText-variabeln tillsammans med cmdleten **Remove-AzVpnClientRootCertificate** för att ta bort certifikatet från gatewayen.

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
Anger textrepresentationen för rotcertifikatet som ska tas bort.
För att få textrepresentationen exporterar du ditt certifikat i CER-format (med base64-kodning) och öppnar sedan den resulterande filen i en textredigerare.
Du bör se utdata som liknar följande (observera att de faktiska utdata kommer att innehålla många fler rader med text än det förkortade exemplet som visas här): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData består av alla rader mellan den första raden (----- BEGIN CERTIFICATE -----) och den sista raden (----- END CERTIFICATE -----) i filen.
Du kan hämta PublicCertData med windows PowerShell-kommandon ungefär så här: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = för ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

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
Anger namnet på resursgruppen som den virtuella nätverksgatewayen är tilldelad till.
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
Anger namnet på klientrotcertifikatet som cmdleten tar bort.

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

### System.Boolean

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


