---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757849"
---
# Get-AzureRmFirewall

## Sammanfattning
Får en Azure-brandvägg.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmFirewall** hämtar en eller flera brand väggar i en resurs grupp.

## BESKRIVS

### 1: Hämta alla brand väggar i en resurs grupp
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

I det här exemplet hämtas alla brand väggar i resurs gruppen "rgName".

### 2: Hämta en brand vägg efter namn
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

I det här exemplet hämtas brand väggen med namnet "azFw" i resurs gruppen "rgName".

### 3: Hämta en brand vägg och Lägg till en program regel samling i brand väggen
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

I det här exemplet hämtas en brand vägg och läggs sedan till i brand väggen genom att anropa metoden AddApplicationRuleCollection.

### 4: Hämta en brand vägg och Lägg sedan till en nätverks regel samling i brand väggen
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

I det här exemplet hämtas en brand vägg och en nätverks regel läggs till i brand väggen genom att anropa metoden AddNetworkRuleCollection.

### 5: Hämta en brand vägg och hämta en samling med program regler efter namn från brand väggen
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

I det här exemplet hämtas en brand vägg och sedan får regel samlingen ett namn som anropar metod GetApplicationRuleCollectionByName på brand Väggs objekt. Namnet på regel samlingen för metod GetApplicationRuleCollectionByName är Skift läges känsligt.

### 6: Hämta en brand vägg och hämta en nätverks regel samling efter namn från brand väggen
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

I det här exemplet hämtas en brand vägg och sedan får regel samlingen ett namn som anropar metod GetNetworkRuleCollectionByName på brand Väggs objekt. Namnet på regel samlingen för metod GetNetworkRuleCollectionByName är Skift läges känsligt.

### 7: Hämta en brand vägg och ta sedan bort en samling med program regler efter namn från brand väggen
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

I det här exemplet hämtas en brand vägg och sedan tas en regel samling bort från namn, metod RemoveApplicationRuleCollectionByName på brand Väggs objekt. Namnet på regel samlingen för metod RemoveApplicationRuleCollectionByName är Skift läges känsligt.

### 8: Hämta en brand vägg och ta sedan bort en nätverks regel samling efter namn från brand väggen
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

I det här exemplet hämtas en brand vägg och sedan tas en regel samling bort från namn, metod RemoveNetworkRuleCollectionByName på brand Väggs objekt. Namnet på regel samlingen för metod RemoveNetworkRuleCollectionByName är Skift läges känsligt.

### 9: Hämta en brand vägg och tilldela sedan brand väggen
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

I det här exemplet hämtas en brand vägg och samtal för att starta brand Väggs tjänsten med den konfiguration (program-och nätverks regel samlingar) som är kopplade till brand väggen.

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
Anger namnet på den brand vägg som den här cmdleten får.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som brand väggen tillhör.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSAzureFirewall

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)
