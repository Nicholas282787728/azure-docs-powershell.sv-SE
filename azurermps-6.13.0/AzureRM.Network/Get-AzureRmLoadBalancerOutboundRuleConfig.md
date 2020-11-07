---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1bcaab526ac2fbb82d696db7197bbc8d69c0078f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758330"
---
# Get-AzureRmLoadBalancerOutboundRuleConfig

## Sammanfattning
Hämtar en regel för utgående trafik i en belastnings utjämning.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmLoadBalancerOutboundRuleConfig** hämtar en konfiguration för utgående regel eller en lista med konfigurationer för utgående trafik i en belastningsutjämnare.

## BESKRIVS

### Exempel 1: Hämta en konfiguration för utgående regel i en belastningsutjämnare
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.
Det andra kommandot hämtar regeln för utgående regel som heter min regel kopplad till den belastningsutjämnaren.

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

### -LoadBalancer
Referensen för belastnings Utjämnings resursen.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Namn
Namn på regeln för utgående trafik.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Networks. Models. PSLoadBalancer

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSOutboundRule

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
