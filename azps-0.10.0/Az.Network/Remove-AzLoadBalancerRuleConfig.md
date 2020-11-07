---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922023"
---
# <span data-ttu-id="dcc00-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcc00-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="dcc00-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dcc00-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc00-103">Tar bort en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="dcc00-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="dcc00-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dcc00-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcc00-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dcc00-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc00-106">Cmdleten **Remove-AzLoadBalancerRuleConfig** tar bort en regel konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="dcc00-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="dcc00-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dcc00-107">EXAMPLES</span></span>

### <span data-ttu-id="dcc00-108">Exempel 1: ta bort en regel konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="dcc00-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="dcc00-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="dcc00-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="dcc00-110">Det andra kommandot tar bort regel konfigurationen med namnet MyLBruleName från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="dcc00-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="dcc00-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dcc00-111">PARAMETERS</span></span>

### <span data-ttu-id="dcc00-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc00-112">-DefaultProfile</span></span>
<span data-ttu-id="dcc00-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc00-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcc00-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcc00-114">-LoadBalancer</span></span>
<span data-ttu-id="dcc00-115">Anger det **Loadbalancer** -objekt som innehåller regel konfigurationen som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dcc00-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dcc00-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="dcc00-116">-Name</span></span>
<span data-ttu-id="dcc00-117">Anger namnet på den regel för belastnings utjämning som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="dcc00-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dcc00-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc00-118">CommonParameters</span></span>
<span data-ttu-id="dcc00-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcc00-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc00-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc00-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc00-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dcc00-121">INPUTS</span></span>

### <span data-ttu-id="dcc00-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcc00-122">PSLoadBalancer</span></span>
<span data-ttu-id="dcc00-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="dcc00-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="dcc00-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dcc00-124">OUTPUTS</span></span>

### <span data-ttu-id="dcc00-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcc00-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dcc00-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dcc00-126">NOTES</span></span>

## <span data-ttu-id="dcc00-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dcc00-127">RELATED LINKS</span></span>

[<span data-ttu-id="dcc00-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcc00-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="dcc00-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcc00-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="dcc00-130">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcc00-130">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="dcc00-131">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcc00-131">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="dcc00-132">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcc00-132">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


