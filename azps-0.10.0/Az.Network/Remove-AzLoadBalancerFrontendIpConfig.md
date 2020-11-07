---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b9782d56fb18f0f00c52e9ff37ef0d62a609f980
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922035"
---
# <span data-ttu-id="89624-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89624-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="89624-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89624-102">SYNOPSIS</span></span>
<span data-ttu-id="89624-103">Tar bort en front-IP-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="89624-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="89624-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89624-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89624-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89624-105">DESCRIPTION</span></span>
<span data-ttu-id="89624-106">Cmdleten **Remove-AzLoadBalancerFrontendIpConfig** tar bort en front-IP-konfiguration från en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="89624-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="89624-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89624-107">EXAMPLES</span></span>

### <span data-ttu-id="89624-108">Exempel 1: ta bort en klient-IP-konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="89624-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="89624-109">Det första kommandot får den belastnings utjämning som är kopplad till den frontend-IP-konfiguration du vill ta bort och lagrar sedan den i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="89624-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="89624-110">Med det andra kommandot tas den tillhör ande IP-konfigurationen för klient delen bort från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="89624-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="89624-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89624-111">PARAMETERS</span></span>

### <span data-ttu-id="89624-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89624-112">-DefaultProfile</span></span>
<span data-ttu-id="89624-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89624-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89624-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89624-114">-LoadBalancer</span></span>
<span data-ttu-id="89624-115">Anger den belastningsutjämnare som innehåller den frontend-IP-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="89624-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="89624-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="89624-116">-Name</span></span>
<span data-ttu-id="89624-117">Anger namnet på den frontend-IP-adresskonfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="89624-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="89624-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89624-118">CommonParameters</span></span>
<span data-ttu-id="89624-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89624-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89624-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89624-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89624-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89624-121">INPUTS</span></span>

### <span data-ttu-id="89624-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89624-122">PSLoadBalancer</span></span>
<span data-ttu-id="89624-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="89624-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="89624-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89624-124">OUTPUTS</span></span>

### <span data-ttu-id="89624-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89624-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="89624-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89624-126">NOTES</span></span>

## <span data-ttu-id="89624-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89624-127">RELATED LINKS</span></span>

[<span data-ttu-id="89624-128">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89624-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="89624-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89624-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="89624-130">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89624-130">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="89624-131">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89624-131">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="89624-132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="89624-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


