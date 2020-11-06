---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582616"
---
# Add-AzureRmDelegation

## Sammanfattning
Lägger till en delegering till ett undernät.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureRmDelegation** lägger till en tjänst delegering till ett Azure-undernät.

## BESKRIVS

### 1: lägga till en delegering
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

Det första kommandot hämtar det virtuella nätverk som under nätet. Det andra kommandot isolerar det intressanta under nätet-det du vill delegera. Det tredje kommandot lägger till en delegering till under nätet. Det här exemplet är användbart när du vill aktivera SQL för att skapa gränssnitts slut punkter i det här under nätet. Det sista kommandot skickar det uppdaterade under nätet till servern som faktiskt uppdaterar ditt undernät.

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
Ombudets namn

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

### -ServiceName
Namnet på tjänsten som under nätet ska delegeras till

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

### -Undernät
Under nätet

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.
Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. Networks. Models. PSSubnet

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSSubnet

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)
