---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220919"
---
# Set-AzNetworkInterface

## SYNOPSIS
Uppdaterar ett nätverksgränssnitt.

## SYNTAX

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Set-AzNetworkInterface uppdaterar** ett nätverksgränssnitt.

## EXEMPEL

### Exempel 1: Konfigurera ett nätverksgränssnitt
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

I det här exemplet konfigureras ett nätverksgränssnitt.
Det första kommandot får ett nätverksgränssnitt med namnet NetworkInterface1 i resursgruppen ResourceGroup1.
Det andra kommandot anger IP-adressen för IP-konfigurationen.
Det tredje kommandot anger statisk för den privata IP-metoden för tilldelning.
Det fjärde kommandot anger en tagg i nätverksgränssnittet.
Det femte kommandot använder informationen som lagras i $Nic för att ställa in nätverksgränssnittet.

### Exempel 2: Ändra DNS-inställningarna i ett nätverksgränssnitt
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

Det första kommandot får ett nätverksgränssnitt med namnet NetworkInterface1 som finns i resursgruppen ResourceGroup1. Med det andra kommandot läggs DNS-servern 192.168.1.100 till i det här gränssnittet. Det tredje kommandot tillämpar dessa ändringar på nätverksgränssnittet. Om du vill ta bort en DNS-server följer du kommandona som anges ovan, men ersätter ". Lägg till" med ". Ta bort" i det andra kommandot.

### Exempel 3: Aktivera IP-vidarebefordran i ett nätverksgränssnitt
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

Det första kommandot får ett befintligt nätverksgränssnitt som kallas NetworkInterface1 och lagrar det i variabeln $nic variabeln. Det andra kommandot ändrar IP-vidare vidarebefordransvärdet till sant. Slutligen gäller det tredje kommandot ändringarna för nätverksgränssnittet. Om du vill inaktivera IP-vidarebefordran i ett nätverksgränssnitt följer du exemplet, men se till att ändra det andra kommandot till "$nic. EnableIPForwarding = 0".

### Exempel 4: Ändra undernätet i ett nätverksgränssnitt
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

Det första kommandot får nätverksgränssnittet NetworkInterface1 och lagrar det i $nic variabeln. Det andra kommandot hämtar det virtuella nätverket som är kopplat till det undernät som nätverksgränssnittet ska associeras med. Det andra kommandot hämtar undernätet och lagrar det i variabeln $subnet 2. Det tredje kommandot kopplade den primära privata IP-adressen för nätverksgränssnittet till det nya undernätet. Slutligen tillämpade det senaste kommandot dessa ändringar i nätverksgränssnittet.
>[!NOTE] 
>IP-konfigurationerna måste vara dynamiska innan du kan ändra undernätet. Om du har statiska IP-konfigurationer ändrar du till dynamisk innan du fortsätter. 
>[!NOTE]
>Om nätverksgränssnittet har flera IP-konfigurationer måste det fjärde kommandot utföras för alla dessa IP-konfigurationer innan det slutliga ipSet-AzNetworkInterface kommandot körs. Det kan göras som i det fjärde kommandot, men genom att ersätta "0" med rätt nummer. Om ett nätverksgränssnitt har N IP-konfigurationer måste N-1 av dessa kommandon finnas.

### Exempel 5: Koppla/avaktivera en nätverkssäkerhetsgrupp till ett nätverksgränssnitt
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

Det första kommandot får ett befintligt nätverksgränssnitt som kallas NetworkInterface1 och lagrar det i variabeln $nic variabeln. Det andra kommandot får en befintlig nätverkssäkerhetsgrupp som kallas MyNSG och lagrar den $nsg variabeln. Det tredje kommandot tilldelar $nsg till $nic. Slutligen gäller det fjärde kommandot ändringarna för nätverksgränssnittet. Om du vill inaktivera nätverkssäkerhetsgrupper från ett nätverksgränssnitt ersätter du $nsg i det tredje kommandot med $null.

## PARAMETERS

### -As Ent
Kör cmdleten i bakgrunden

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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

### -NetworkInterface
Anger ett nätverksgränssnittsobjekt som representerar den status som nätverksgränssnittet ska ställas in för.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## UTDATA

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
