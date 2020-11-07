---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 3d8d80f8f8de0c1a0dedd50e7f4c6a93ce414b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756492"
---
# <span data-ttu-id="eb1ad-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eb1ad-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="eb1ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1ad-103">Hämtar en PROBE-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb1ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb1ad-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb1ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb1ad-105">DESCRIPTION</span></span>
<span data-ttu-id="eb1ad-106">Cmdleten **Get-AzureRmLoadBalancerProbeConfig** hämtar en eller flera PROBE-konfigurationer för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="eb1ad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb1ad-107">EXAMPLES</span></span>

### <span data-ttu-id="eb1ad-108">Exempel 1: Hämta avsöknings konfigurationen för en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="eb1ad-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="eb1ad-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="eb1ad-110">Det andra kommandot får den associerade avsöknings konfigurationen som heter ' Avsök från belastningsutjämnaren i $slb.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="eb1ad-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb1ad-111">PARAMETERS</span></span>

### <span data-ttu-id="eb1ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb1ad-112">-DefaultProfile</span></span>
<span data-ttu-id="eb1ad-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb1ad-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eb1ad-114">-LoadBalancer</span></span>
<span data-ttu-id="eb1ad-115">Anger den belastningsutjämnare som är kopplad till den avsöknings konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="eb1ad-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb1ad-116">-Name</span></span>
<span data-ttu-id="eb1ad-117">Anger namnet på den PROBE-konfiguration som ska visas.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="eb1ad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1ad-118">CommonParameters</span></span>
<span data-ttu-id="eb1ad-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb1ad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1ad-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb1ad-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1ad-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb1ad-121">INPUTS</span></span>

### <span data-ttu-id="eb1ad-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eb1ad-122">PSLoadBalancer</span></span>
<span data-ttu-id="eb1ad-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="eb1ad-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="eb1ad-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb1ad-124">OUTPUTS</span></span>

### <span data-ttu-id="eb1ad-125">Microsoft. Azure. commands. Networks. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="eb1ad-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="eb1ad-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb1ad-126">NOTES</span></span>

## <span data-ttu-id="eb1ad-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb1ad-127">RELATED LINKS</span></span>

[<span data-ttu-id="eb1ad-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eb1ad-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="eb1ad-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eb1ad-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="eb1ad-130">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eb1ad-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="eb1ad-131">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eb1ad-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="eb1ad-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="eb1ad-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


