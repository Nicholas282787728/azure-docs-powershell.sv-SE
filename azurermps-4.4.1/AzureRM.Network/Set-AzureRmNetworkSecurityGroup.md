---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 9cb5a19adaf5c9d7371196a5ed917a557ef7c6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575966"
---
# Set-AzureRmNetworkSecurityGroup

## Sammanfattning
Anger mål tillståndet för en nätverks säkerhets grupp.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmNetworkSecurityGroup** anger mål tillståndet för en Azure Network Security-grupp.

## BESKRIVS

### Exempel 1: Ange mål tillstånd för en nätverks säkerhets grupp
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

Det här kommandot hämtar Azure nätverks säkerhets gruppen med namnet Nsg1 och lägger till en nätverks säkerhets regel med namnet Rdp-Rule för att tillåta Internet trafik på port 3389 till det hämtade objektet nätverks säkerhets grupp med hjälp av Add-AzureRmNetworkSecurityRuleConfig.
Kommandot behåller den ändrade Azure Network Security-gruppen med **set-AzureRmNetworkSecurityGroup**.

## MALLPARAMETRAR

### -NetworkSecurityGroup
Ett nätverks säkerhets grupp objekt som representerar mål tillståndet där cmdleten ställer in nätverks säkerhets gruppen.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
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

### PSNetworkSecurityGroup
Parametern ' NetworkSecurityGroup ' godkänner värdet av typen ' PSNetworkSecurityGroup ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmNetworkSecurityGroup](./Get-AzureRmNetworkSecurityGroup.md)

[New-AzureRmNetworkSecurityGroup](./New-AzureRmNetworkSecurityGroup.md)

[Remove-AzureRmNetworkSecurityGroup](./Remove-AzureRmNetworkSecurityGroup.md)


