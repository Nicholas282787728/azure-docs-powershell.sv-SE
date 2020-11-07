---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 11de4e8966b5e57e817b6c5d829536deacf229f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922026"
---
# <span data-ttu-id="19d7b-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="19d7b-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="19d7b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="19d7b-103">Tar bort en PROBE-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="19d7b-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="19d7b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19d7b-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19d7b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="19d7b-106">Cmdleten **Remove-AzLoadBalancerProbeConfig** tar bort en PROBE-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="19d7b-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="19d7b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19d7b-107">EXAMPLES</span></span>

### <span data-ttu-id="19d7b-108">Exempel 1: ta bort en PROBE-konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="19d7b-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="19d7b-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="19d7b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="19d7b-110">Det andra kommandot tar bort konfigurationen med namnet ' Avsök från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="19d7b-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="19d7b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19d7b-111">PARAMETERS</span></span>

### <span data-ttu-id="19d7b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d7b-112">-DefaultProfile</span></span>
<span data-ttu-id="19d7b-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19d7b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19d7b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19d7b-114">-LoadBalancer</span></span>
<span data-ttu-id="19d7b-115">Anger belastningsutjämnaren som innehåller den avsöknings konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="19d7b-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="19d7b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="19d7b-116">-Name</span></span>
<span data-ttu-id="19d7b-117">Anger namnet på den avsöknings konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="19d7b-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="19d7b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d7b-118">CommonParameters</span></span>
<span data-ttu-id="19d7b-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19d7b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d7b-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d7b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d7b-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19d7b-121">INPUTS</span></span>

### <span data-ttu-id="19d7b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19d7b-122">PSLoadBalancer</span></span>
<span data-ttu-id="19d7b-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="19d7b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="19d7b-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19d7b-124">OUTPUTS</span></span>

### <span data-ttu-id="19d7b-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19d7b-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="19d7b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19d7b-126">NOTES</span></span>

## <span data-ttu-id="19d7b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19d7b-127">RELATED LINKS</span></span>

[<span data-ttu-id="19d7b-128">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="19d7b-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="19d7b-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="19d7b-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="19d7b-130">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="19d7b-130">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="19d7b-131">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="19d7b-131">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="19d7b-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="19d7b-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


