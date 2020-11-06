---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 070680c1dc1c9fd091b311888867cda3f844ce4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576904"
---
# <span data-ttu-id="956ef-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="956ef-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="956ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="956ef-102">SYNOPSIS</span></span>
<span data-ttu-id="956ef-103">Hämtar en klient-IP-konfiguration i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="956ef-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="956ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="956ef-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="956ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="956ef-105">DESCRIPTION</span></span>
<span data-ttu-id="956ef-106">Cmdleten **Get-AzureRmLoadBalancerFrontendIpConfig** har en front-IP-konfiguration eller en lista över front-IP-konfigurationer i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="956ef-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="956ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="956ef-107">EXAMPLES</span></span>

### <span data-ttu-id="956ef-108">Exempel 1: Hämta en front-IP-konfiguration i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="956ef-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="956ef-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="956ef-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="956ef-110">Det andra kommandot får den klient konfiguration för front end som är kopplad till den belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="956ef-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="956ef-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="956ef-111">PARAMETERS</span></span>

### <span data-ttu-id="956ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956ef-112">-DefaultProfile</span></span>
<span data-ttu-id="956ef-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="956ef-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="956ef-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="956ef-114">-LoadBalancer</span></span>
<span data-ttu-id="956ef-115">Anger den belastningsutjämnare som är kopplad till den frontend-IP-konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="956ef-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="956ef-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="956ef-116">-Name</span></span>
<span data-ttu-id="956ef-117">Anger namnet på belastningsutjämnaren som innehåller den frontend-IP-konfiguration som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="956ef-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="956ef-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956ef-118">CommonParameters</span></span>
<span data-ttu-id="956ef-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="956ef-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956ef-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="956ef-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956ef-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="956ef-121">INPUTS</span></span>

### <span data-ttu-id="956ef-122">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="956ef-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="956ef-123">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="956ef-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="956ef-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="956ef-124">OUTPUTS</span></span>

### <span data-ttu-id="956ef-125">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="956ef-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="956ef-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="956ef-126">NOTES</span></span>

## <span data-ttu-id="956ef-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="956ef-127">RELATED LINKS</span></span>

[<span data-ttu-id="956ef-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="956ef-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="956ef-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="956ef-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="956ef-130">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="956ef-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="956ef-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="956ef-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="956ef-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="956ef-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


