---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6a1e5f4de5ec98030cc9bd3300d9e9fd447f6f02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918069"
---
# <span data-ttu-id="16e07-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16e07-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="16e07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16e07-102">SYNOPSIS</span></span>
<span data-ttu-id="16e07-103">Tar bort en PROBE-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="16e07-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="16e07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16e07-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e07-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16e07-105">DESCRIPTION</span></span>
<span data-ttu-id="16e07-106">Cmdleten **Remove-AzLoadBalancerProbeConfig** tar bort en PROBE-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="16e07-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="16e07-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16e07-107">EXAMPLES</span></span>

### <span data-ttu-id="16e07-108">Exempel 1: ta bort en PROBE-konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="16e07-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="16e07-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="16e07-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="16e07-110">Det andra kommandot tar bort konfigurationen med namnet ' Avsök från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="16e07-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="16e07-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16e07-111">PARAMETERS</span></span>

### <span data-ttu-id="16e07-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e07-112">-DefaultProfile</span></span>
<span data-ttu-id="16e07-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16e07-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16e07-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16e07-114">-LoadBalancer</span></span>
<span data-ttu-id="16e07-115">Anger belastningsutjämnaren som innehåller den avsöknings konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="16e07-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="16e07-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="16e07-116">-Name</span></span>
<span data-ttu-id="16e07-117">Anger namnet på den avsöknings konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="16e07-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="16e07-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16e07-118">-Confirm</span></span>
<span data-ttu-id="16e07-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16e07-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e07-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e07-120">-WhatIf</span></span>
<span data-ttu-id="16e07-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16e07-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16e07-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16e07-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e07-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e07-123">CommonParameters</span></span>
<span data-ttu-id="16e07-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e07-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e07-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e07-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e07-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16e07-126">INPUTS</span></span>

### <span data-ttu-id="16e07-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16e07-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="16e07-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16e07-128">OUTPUTS</span></span>

### <span data-ttu-id="16e07-129">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16e07-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="16e07-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16e07-130">NOTES</span></span>

## <span data-ttu-id="16e07-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16e07-131">RELATED LINKS</span></span>

[<span data-ttu-id="16e07-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16e07-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="16e07-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="16e07-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="16e07-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16e07-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="16e07-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16e07-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="16e07-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16e07-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)

