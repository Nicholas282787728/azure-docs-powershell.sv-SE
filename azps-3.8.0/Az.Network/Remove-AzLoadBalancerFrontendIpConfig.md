---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091764"
---
# <span data-ttu-id="afd4a-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="afd4a-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="afd4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afd4a-102">SYNOPSIS</span></span>
<span data-ttu-id="afd4a-103">Tar bort en front-IP-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="afd4a-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="afd4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afd4a-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd4a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afd4a-105">DESCRIPTION</span></span>
<span data-ttu-id="afd4a-106">Cmdleten **Remove-AzLoadBalancerFrontendIpConfig** tar bort en front-IP-konfiguration från en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="afd4a-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="afd4a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afd4a-107">EXAMPLES</span></span>

### <span data-ttu-id="afd4a-108">Exempel 1: ta bort en klient-IP-konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="afd4a-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="afd4a-109">Det första kommandot får den belastnings utjämning som är kopplad till den frontend-IP-konfiguration du vill ta bort och lagrar sedan den i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="afd4a-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="afd4a-110">Med det andra kommandot tas den tillhör ande IP-konfigurationen för klient delen bort från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="afd4a-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="afd4a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afd4a-111">PARAMETERS</span></span>

### <span data-ttu-id="afd4a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd4a-112">-DefaultProfile</span></span>
<span data-ttu-id="afd4a-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afd4a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afd4a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="afd4a-114">-LoadBalancer</span></span>
<span data-ttu-id="afd4a-115">Anger den belastningsutjämnare som innehåller den frontend-IP-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="afd4a-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="afd4a-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="afd4a-116">-Name</span></span>
<span data-ttu-id="afd4a-117">Anger namnet på den frontend-IP-adresskonfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="afd4a-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="afd4a-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="afd4a-118">-Confirm</span></span>
<span data-ttu-id="afd4a-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="afd4a-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd4a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd4a-120">-WhatIf</span></span>
<span data-ttu-id="afd4a-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="afd4a-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afd4a-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="afd4a-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd4a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd4a-123">CommonParameters</span></span>
<span data-ttu-id="afd4a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd4a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd4a-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd4a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd4a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afd4a-126">INPUTS</span></span>

### <span data-ttu-id="afd4a-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="afd4a-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="afd4a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afd4a-128">OUTPUTS</span></span>

### <span data-ttu-id="afd4a-129">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="afd4a-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="afd4a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afd4a-130">NOTES</span></span>

## <span data-ttu-id="afd4a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afd4a-131">RELATED LINKS</span></span>

[<span data-ttu-id="afd4a-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="afd4a-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="afd4a-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="afd4a-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="afd4a-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="afd4a-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="afd4a-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="afd4a-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="afd4a-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="afd4a-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

