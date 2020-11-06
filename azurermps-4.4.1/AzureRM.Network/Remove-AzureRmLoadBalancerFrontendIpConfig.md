---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: c4809371792a2add8510b1bf7f4db39dd344b037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573632"
---
# Remove-AzureRmLoadBalancerFrontendIpConfig

## Sammanfattning
Tar bort en front-IP-konfiguration från en belastningsutjämnare.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmLoadBalancerFrontendIpConfig** tar bort en front-IP-konfiguration från en Azure-belastningsutjämnare.

## BESKRIVS

### Exempel 1: ta bort en klient-IP-konfiguration från en belastningsutjämnare
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

Det första kommandot får den belastnings utjämning som är kopplad till den frontend-IP-konfiguration du vill ta bort och lagrar sedan den i $loadbalancer variabel.

Med det andra kommandot tas den tillhör ande IP-konfigurationen för klient delen bort från belastningsutjämnaren i $loadbalancer.

## MALLPARAMETRAR

### -LoadBalancer
Anger den belastningsutjämnare som innehåller den frontend-IP-konfiguration som ska tas bort.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den frontend-IP-adresskonfiguration som ska tas bort.

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

### PSLoadBalancer
Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSLoadBalancer

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmLoadBalancerFrontendIpConfig](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[Get-AzureRmLoadBalancer](./Get-AzureRmLoadBalancer.md)

[Get-AzureRmLoadBalancerFrontendIpConfig](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[New-AzureRmLoadBalancerFrontendIpConfig](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[Set-AzureRmLoadBalancerFrontendIpConfig](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


