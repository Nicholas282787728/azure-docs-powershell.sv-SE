---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 9840476e64c78293b747f96d1a689a3ce5099bff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574257"
---
# <span data-ttu-id="e69d4-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e69d4-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e69d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e69d4-102">SYNOPSIS</span></span>
<span data-ttu-id="e69d4-103">Tar bort en PROBE-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="e69d4-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e69d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e69d4-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e69d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e69d4-105">DESCRIPTION</span></span>
<span data-ttu-id="e69d4-106">Cmdleten **Remove-AzureRmLoadBalancerProbeConfig** tar bort en PROBE-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="e69d4-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="e69d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e69d4-107">EXAMPLES</span></span>

### <span data-ttu-id="e69d4-108">Exempel 1: ta bort en PROBE-konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="e69d4-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="e69d4-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="e69d4-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="e69d4-110">Det andra kommandot tar bort konfigurationen med namnet ' Avsök från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="e69d4-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="e69d4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e69d4-111">PARAMETERS</span></span>

### <span data-ttu-id="e69d4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e69d4-112">-DefaultProfile</span></span>
<span data-ttu-id="e69d4-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e69d4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e69d4-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e69d4-114">-LoadBalancer</span></span>
<span data-ttu-id="e69d4-115">Anger belastningsutjämnaren som innehåller den avsöknings konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e69d4-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e69d4-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e69d4-116">-Name</span></span>
<span data-ttu-id="e69d4-117">Anger namnet på den avsöknings konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e69d4-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e69d4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e69d4-118">CommonParameters</span></span>
<span data-ttu-id="e69d4-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e69d4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e69d4-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e69d4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e69d4-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e69d4-121">INPUTS</span></span>

### <span data-ttu-id="e69d4-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e69d4-122">PSLoadBalancer</span></span>
<span data-ttu-id="e69d4-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e69d4-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e69d4-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e69d4-124">OUTPUTS</span></span>

### <span data-ttu-id="e69d4-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e69d4-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e69d4-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e69d4-126">NOTES</span></span>

## <span data-ttu-id="e69d4-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e69d4-127">RELATED LINKS</span></span>

[<span data-ttu-id="e69d4-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e69d4-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e69d4-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e69d4-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e69d4-130">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e69d4-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e69d4-131">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e69d4-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="e69d4-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e69d4-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


