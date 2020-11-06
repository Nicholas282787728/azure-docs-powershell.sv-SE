---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: c52546ba0477a2911ac34533060d7a47df0b0698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574787"
---
# <span data-ttu-id="9b36b-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9b36b-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="9b36b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b36b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b36b-103">Tar bort en PROBE-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="9b36b-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b36b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b36b-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b36b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b36b-105">DESCRIPTION</span></span>
<span data-ttu-id="9b36b-106">Cmdleten **Remove-AzureRmLoadBalancerProbeConfig** tar bort en PROBE-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="9b36b-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="9b36b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b36b-107">EXAMPLES</span></span>

### <span data-ttu-id="9b36b-108">Exempel 1: ta bort en PROBE-konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="9b36b-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="9b36b-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="9b36b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="9b36b-110">Det andra kommandot tar bort konfigurationen med namnet ' Avsök från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="9b36b-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="9b36b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b36b-111">PARAMETERS</span></span>

### <span data-ttu-id="9b36b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b36b-112">-DefaultProfile</span></span>
<span data-ttu-id="9b36b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b36b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b36b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b36b-114">-LoadBalancer</span></span>
<span data-ttu-id="9b36b-115">Anger belastningsutjämnaren som innehåller den avsöknings konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="9b36b-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9b36b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b36b-116">-Name</span></span>
<span data-ttu-id="9b36b-117">Anger namnet på den avsöknings konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="9b36b-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9b36b-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b36b-118">-Confirm</span></span>
<span data-ttu-id="9b36b-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b36b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b36b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b36b-120">-WhatIf</span></span>
<span data-ttu-id="9b36b-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b36b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b36b-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b36b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b36b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b36b-123">CommonParameters</span></span>
<span data-ttu-id="9b36b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b36b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b36b-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b36b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b36b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b36b-126">INPUTS</span></span>

### <span data-ttu-id="9b36b-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b36b-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="9b36b-128">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b36b-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="9b36b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b36b-129">OUTPUTS</span></span>

### <span data-ttu-id="9b36b-130">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b36b-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9b36b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b36b-131">NOTES</span></span>

## <span data-ttu-id="9b36b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b36b-132">RELATED LINKS</span></span>

[<span data-ttu-id="9b36b-133">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9b36b-133">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="9b36b-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9b36b-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="9b36b-135">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9b36b-135">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="9b36b-136">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9b36b-136">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="9b36b-137">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9b36b-137">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


