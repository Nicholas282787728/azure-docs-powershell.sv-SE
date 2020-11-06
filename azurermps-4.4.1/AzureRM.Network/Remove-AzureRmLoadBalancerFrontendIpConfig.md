---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: c4809371792a2add8510b1bf7f4db39dd344b037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573632"
---
# <span data-ttu-id="0c540-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0c540-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="0c540-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c540-102">SYNOPSIS</span></span>
<span data-ttu-id="0c540-103">Tar bort en front-IP-konfiguration från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="0c540-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c540-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c540-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c540-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c540-105">DESCRIPTION</span></span>
<span data-ttu-id="0c540-106">Cmdleten **Remove-AzureRmLoadBalancerFrontendIpConfig** tar bort en front-IP-konfiguration från en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="0c540-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="0c540-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c540-107">EXAMPLES</span></span>

### <span data-ttu-id="0c540-108">Exempel 1: ta bort en klient-IP-konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="0c540-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="0c540-109">Det första kommandot får den belastnings utjämning som är kopplad till den frontend-IP-konfiguration du vill ta bort och lagrar sedan den i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="0c540-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="0c540-110">Med det andra kommandot tas den tillhör ande IP-konfigurationen för klient delen bort från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0c540-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="0c540-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c540-111">PARAMETERS</span></span>

### <span data-ttu-id="0c540-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c540-112">-LoadBalancer</span></span>
<span data-ttu-id="0c540-113">Anger den belastningsutjämnare som innehåller den frontend-IP-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0c540-113">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c540-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c540-114">-Name</span></span>
<span data-ttu-id="0c540-115">Anger namnet på den frontend-IP-adresskonfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0c540-115">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="0c540-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c540-116">-DefaultProfile</span></span>
<span data-ttu-id="0c540-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c540-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c540-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c540-118">CommonParameters</span></span>
<span data-ttu-id="0c540-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c540-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c540-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c540-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c540-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c540-121">INPUTS</span></span>

### <span data-ttu-id="0c540-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c540-122">PSLoadBalancer</span></span>
<span data-ttu-id="0c540-123">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0c540-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0c540-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c540-124">OUTPUTS</span></span>

### <span data-ttu-id="0c540-125">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c540-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0c540-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c540-126">NOTES</span></span>

## <span data-ttu-id="0c540-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c540-127">RELATED LINKS</span></span>

[<span data-ttu-id="0c540-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0c540-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0c540-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c540-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="0c540-130">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0c540-130">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0c540-131">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0c540-131">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0c540-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0c540-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


