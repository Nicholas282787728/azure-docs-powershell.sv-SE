---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 25340322c7d5f74eb8f277db9f7693c938007840
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757928"
---
# <span data-ttu-id="65cc5-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65cc5-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="65cc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="65cc5-103">Tar bort en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="65cc5-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65cc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65cc5-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65cc5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65cc5-105">DESCRIPTION</span></span>
<span data-ttu-id="65cc5-106">Cmdleten **Remove-AzureRmLoadBalancerRuleConfig** tar bort en regel konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="65cc5-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="65cc5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65cc5-107">EXAMPLES</span></span>

### <span data-ttu-id="65cc5-108">Exempel 1: ta bort en regel konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="65cc5-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="65cc5-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="65cc5-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="65cc5-110">Det andra kommandot tar bort regel konfigurationen med namnet MyLBruleName från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="65cc5-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="65cc5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65cc5-111">PARAMETERS</span></span>

### <span data-ttu-id="65cc5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65cc5-112">-DefaultProfile</span></span>
<span data-ttu-id="65cc5-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65cc5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65cc5-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65cc5-114">-LoadBalancer</span></span>
<span data-ttu-id="65cc5-115">Anger det **Loadbalancer** -objekt som innehåller regel konfigurationen som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65cc5-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65cc5-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="65cc5-116">-Name</span></span>
<span data-ttu-id="65cc5-117">Anger namnet på den regel för belastnings utjämning som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="65cc5-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65cc5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65cc5-118">CommonParameters</span></span>
<span data-ttu-id="65cc5-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65cc5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65cc5-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65cc5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65cc5-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65cc5-121">INPUTS</span></span>

### <span data-ttu-id="65cc5-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65cc5-122">PSLoadBalancer</span></span>
<span data-ttu-id="65cc5-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="65cc5-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="65cc5-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65cc5-124">OUTPUTS</span></span>

### <span data-ttu-id="65cc5-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65cc5-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="65cc5-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65cc5-126">NOTES</span></span>

## <span data-ttu-id="65cc5-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65cc5-127">RELATED LINKS</span></span>

[<span data-ttu-id="65cc5-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65cc5-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="65cc5-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65cc5-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="65cc5-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65cc5-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="65cc5-131">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65cc5-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="65cc5-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65cc5-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


