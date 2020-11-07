---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 0c68886906957204ee0885a00bfc07740fb6ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755862"
---
# Get-AzureRmVirtualNetworkPeering

## Sammanfattning
Hämtar virtuell nätverks-peering.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmVirtualNetworkPeering** hämtar det virtuella nätverkets peering.

## BESKRIVS

### Exempel 1: skapa en peering mellan två virtuella nätverk
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

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
Anger det virtuella nätverkets peering-namn.

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

### -ResourceGroupName
Anger namnet på den resurs grupp som det virtuella nätverks peer-datorn tillhör.

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

### -VirtualNetworkName
Anger det virtuella nätverks namnet som denna cmdlet får.

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

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkPeering

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmVirtualNetworkPeering](./Add-AzureRmVirtualNetworkPeering.md)

[Remove-AzureRmVirtualNetworkPeering](./Remove-AzureRmVirtualNetworkPeering.md)

[Set-AzureRmVirtualNetworkPeering](./Set-AzureRmVirtualNetworkPeering.md)


