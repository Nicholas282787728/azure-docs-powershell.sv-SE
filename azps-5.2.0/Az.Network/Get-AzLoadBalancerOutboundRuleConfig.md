---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401448"
---
# <span data-ttu-id="cfb88-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfb88-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="cfb88-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfb88-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb88-103">Hämtar en regel för utgående trafik i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="cfb88-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="cfb88-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfb88-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfb88-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfb88-105">DESCRIPTION</span></span>
<span data-ttu-id="cfb88-106">Cmdleten **Get-AzLoadBalancerOutboundRuleConfig** hämtar en konfiguration för utgående regel eller en lista med konfigurationer för utgående trafik i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="cfb88-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="cfb88-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfb88-107">EXAMPLES</span></span>

### <span data-ttu-id="cfb88-108">Exempel 1: Hämta en konfiguration för utgående regel i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="cfb88-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="cfb88-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="cfb88-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="cfb88-110">Det andra kommandot hämtar regeln för utgående regel som heter min regel kopplad till den belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="cfb88-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="cfb88-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfb88-111">PARAMETERS</span></span>

### <span data-ttu-id="cfb88-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb88-112">-DefaultProfile</span></span>
<span data-ttu-id="cfb88-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfb88-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfb88-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cfb88-114">-LoadBalancer</span></span>
<span data-ttu-id="cfb88-115">Referensen för belastnings Utjämnings resursen.</span><span class="sxs-lookup"><span data-stu-id="cfb88-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="cfb88-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfb88-116">-Name</span></span>
<span data-ttu-id="cfb88-117">Namn på regeln för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="cfb88-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="cfb88-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb88-118">CommonParameters</span></span>
<span data-ttu-id="cfb88-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfb88-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb88-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfb88-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb88-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfb88-121">INPUTS</span></span>

### <span data-ttu-id="cfb88-122">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cfb88-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cfb88-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfb88-123">OUTPUTS</span></span>

### <span data-ttu-id="cfb88-124">Microsoft. Azure. commands. Networks. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="cfb88-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="cfb88-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfb88-125">NOTES</span></span>

## <span data-ttu-id="cfb88-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfb88-126">RELATED LINKS</span></span>

[<span data-ttu-id="cfb88-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfb88-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="cfb88-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfb88-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="cfb88-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfb88-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="cfb88-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfb88-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
