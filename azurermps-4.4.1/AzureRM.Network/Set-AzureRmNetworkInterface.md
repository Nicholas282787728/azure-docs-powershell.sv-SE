---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
ms.openlocfilehash: 8403a2e26bbc149db35c9c20cdea3075adb88492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575967"
---
# Set-AzureRmNetworkInterface

## Sammanfattning
Anger mål tillstånd för ett nätverks gränssnitt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Set-AzureRmNetworkInterface** anger mål tillståndet för ett Azure-nätverkskort.

## BESKRIVS

### Exempel 1: Konfigurera ett nätverks gränssnitt
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

Det här exemplet konfigurerar ett nätverks gränssnitt.
Det första kommandot får ett nätverks gränssnitt som heter NetworkInterface1 i ResourceGroup1 för resurs grupp.
Med det andra kommandot anges IP-konfigurationens privata IP-adress.
Det tredje kommandot ställer in den privata IP-tilldelnings metoden till statisk.
Det fjärde kommandot anger en tagg i nätverks gränssnittet.
Det femte kommandot använder informationen som lagras i $Nic variabel för att ange nätverks gränssnittet.

### Exempel 2: ändra DNS-inställningar i ett nätverks gränssnitt
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

Det första kommandot får ett nätverks gränssnitt med namnet NetworkInterface1 som finns i resurs grupp ResourceGroup1. Det andra kommandot lägger till DNS-192.168.1.100 till det här gränssnittet. Det tredje kommandot tillämpar dessa ändringar i nätverks gränssnittet. Om du vill ta bort en DNS-Server följer du kommandona ovan, men Ersätt ". Lägg till "med". Ta bort "i det andra kommandot.

### Exempel 3: aktivera IP-forwading på ett nätverks gränssnitt
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

Det första kommandot får ett befintligt nätverks gränssnitt med namnet NetworkInterface1 och lagrar det i $nic variabeln. Det andra kommandot ändrar värdet för IP-vidarekoppling till sant. Dessutom tillämpar det tredje kommandot ändringarna i nätverks gränssnittet. Om du vill inaktivera IP-vidarebefordran i ett nätverks gränssnitt följer du exempel exempel på att ändra det andra kommandot till "$nic. EnableIPForwarding = 0 ".

### Exempel 4: ändra undernät för ett nätverks gränssnitt
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

Det första kommandot får nätverks gränssnittet NetworkInterface1 och lagrar det i $nic variabel. Det andra kommandot hämtar det virtuella nätverk som är kopplat till det undernät som nätverks gränssnittet ska kopplas till. Det andra kommandot hämtar under nätet och lagrar det i variabeln $subnet 2. Det tredje kommandot associerade den primära privata IP-adressen för nätverks gränssnittet med det nya under nätet. Slutligen användes de här ändringarna i nätverks gränssnittet.

>[!NOTE] 
>IP-konfigurationerna måste vara dynamiska innan du kan ändra under nätet. Om du har statiska IP-konfigurationer måste du ändra till dynamisk innan du fortsätter. 

>[!NOTE]
>Om nätverks gränssnittet har flera IP-konfigurationer måste kommandot tillbaka utföras för alla dessa IP-konfigurationer innan kommandot Set-AzureRmNetworkInterface körs. Det kan du göra på det sätt som gäller, men genom att ersätta "0" med rätt nummer. Om ett nätverks gränssnitt har N IP-konfigurationer måste N-1 av dessa kommandon finnas.

### Exempel 5: associera/koppla bort en nätverks säkerhets grupp till ett nätverks gränssnitt
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

Det första kommandot får ett befintligt nätverks gränssnitt med namnet NetworkInterface1 och lagrar det i $nic variabeln. Det andra kommandot får en befintlig nätverks säkerhets grupp som heter MyNSG och lagrar den i $nsg variabeln. Kommandot det här tilldelar $nsg till $nic. Slutligen tillämpar det femte kommandot ändringarna i nätverks gränssnittet. Om du vill koppla från nätverks säkerhets grupper från ett nätverks gränssnitt kan du enkelt ersätta $nsg i kommandot tillbaka med $null.

## MALLPARAMETRAR

### -NetworkInterface
Anger ett **NetworkInterface** -objekt som representerar mål tillståndet för ett nätverks gränssnitt.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### PSNetworkInterface
Parametern ' NetworkInterface ' godkänner värdet av typen ' PSNetworkInterface ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSNetworkInterface

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[Get-AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[New-AzureRmNetworkInterface](./New-AzureRmNetworkInterface.md)

[Remove-AzureRmNetworkInterface](./Remove-AzureRmNetworkInterface.md)
