---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: a80fa84beaaea0307447f25767d665c465e8c2aa
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928750"
---
# <span data-ttu-id="4c593-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c593-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="4c593-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c593-102">SYNOPSIS</span></span>
<span data-ttu-id="4c593-103">Hämtar en klient-IP-konfiguration i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="4c593-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c593-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c593-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c593-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c593-105">DESCRIPTION</span></span>
<span data-ttu-id="4c593-106">Cmdleten **Get-AzureRmLoadBalancerFrontendIpConfig** har en front-IP-konfiguration eller en lista över front-IP-konfigurationer i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="4c593-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="4c593-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c593-107">EXAMPLES</span></span>

### <span data-ttu-id="4c593-108">Exempel 1: Hämta en front-IP-konfiguration i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="4c593-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="4c593-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="4c593-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="4c593-110">Det andra kommandot får den klient konfiguration för front end som är kopplad till den belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="4c593-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="4c593-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c593-111">PARAMETERS</span></span>

### <span data-ttu-id="4c593-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c593-112">-DefaultProfile</span></span>
<span data-ttu-id="4c593-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c593-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c593-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4c593-114">-LoadBalancer</span></span>
<span data-ttu-id="4c593-115">Anger den belastningsutjämnare som är kopplad till den frontend-IP-konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="4c593-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="4c593-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c593-116">-Name</span></span>
<span data-ttu-id="4c593-117">Anger namnet på belastningsutjämnaren som innehåller den frontend-IP-konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="4c593-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="4c593-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c593-118">CommonParameters</span></span>
<span data-ttu-id="4c593-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c593-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c593-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c593-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c593-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c593-121">INPUTS</span></span>

### <span data-ttu-id="4c593-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4c593-122">PSLoadBalancer</span></span>
<span data-ttu-id="4c593-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4c593-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4c593-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c593-124">OUTPUTS</span></span>

### <span data-ttu-id="4c593-125">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c593-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="4c593-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c593-126">NOTES</span></span>

## <span data-ttu-id="4c593-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c593-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c593-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c593-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4c593-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4c593-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4c593-130">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c593-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4c593-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c593-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4c593-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c593-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


