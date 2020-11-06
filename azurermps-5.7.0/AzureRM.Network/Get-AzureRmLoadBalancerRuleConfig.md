---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 3a11b6435c263b5460258a63adb9b72d7ac9f02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586055"
---
# <span data-ttu-id="fc494-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fc494-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="fc494-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc494-102">SYNOPSIS</span></span>
<span data-ttu-id="fc494-103">Hämtar regel konfigurationen för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="fc494-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc494-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc494-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc494-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc494-105">DESCRIPTION</span></span>
<span data-ttu-id="fc494-106">Cmdleten **Get-AzureRmLoadBalancerRuleConfig** hämtar en eller flera regler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="fc494-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="fc494-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc494-107">EXAMPLES</span></span>

### <span data-ttu-id="fc494-108">Exempel 1: Hämta regel konfigurationen för en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="fc494-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="fc494-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="fc494-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="fc494-110">Det andra kommandot hämtar den associerade regel konfigurationen med namnet MyLBrulename från belastningsutjämnaren i $slb.</span><span class="sxs-lookup"><span data-stu-id="fc494-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="fc494-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc494-111">PARAMETERS</span></span>

### <span data-ttu-id="fc494-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc494-112">-DefaultProfile</span></span>
<span data-ttu-id="fc494-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc494-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc494-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fc494-114">-LoadBalancer</span></span>
<span data-ttu-id="fc494-115">Anger den belastningsutjämnare som är associerad med den regel konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="fc494-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="fc494-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc494-116">-Name</span></span>
<span data-ttu-id="fc494-117">Anger namnet på den regel konfiguration som ska visas.</span><span class="sxs-lookup"><span data-stu-id="fc494-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="fc494-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc494-118">CommonParameters</span></span>
<span data-ttu-id="fc494-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc494-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc494-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc494-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc494-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc494-121">INPUTS</span></span>

### <span data-ttu-id="fc494-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fc494-122">PSLoadBalancer</span></span>
<span data-ttu-id="fc494-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="fc494-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="fc494-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc494-124">OUTPUTS</span></span>

### <span data-ttu-id="fc494-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="fc494-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="fc494-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc494-126">NOTES</span></span>

## <span data-ttu-id="fc494-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc494-127">RELATED LINKS</span></span>

[<span data-ttu-id="fc494-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fc494-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fc494-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fc494-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="fc494-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fc494-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fc494-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fc494-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


