---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: 767f725633560d79cb19e1caad61c08772107b42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261863"
---
# <span data-ttu-id="778ef-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="778ef-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="778ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="778ef-102">SYNOPSIS</span></span>
<span data-ttu-id="778ef-103">Får en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="778ef-103">Gets a load balancer.</span></span>

## <span data-ttu-id="778ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="778ef-104">SYNTAX</span></span>

### <span data-ttu-id="778ef-105">Noexpandering (standard)</span><span class="sxs-lookup"><span data-stu-id="778ef-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="778ef-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="778ef-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="778ef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="778ef-107">DESCRIPTION</span></span>
<span data-ttu-id="778ef-108">Cmdleten **Get-AzLoadBalancer** har en eller flera Azure belastningsutjämnare som ingår i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="778ef-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="778ef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="778ef-109">EXAMPLES</span></span>

### <span data-ttu-id="778ef-110">Exempel 1: skaffa en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="778ef-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }
```

<span data-ttu-id="778ef-111">Det här kommandot får belastningsutjämnaren med namnet MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="778ef-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="778ef-112">Det måste finnas en belastningsutjämnare innan du kan köra denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="778ef-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="778ef-113">Exempel 2: list belastnings utjämning med filtrering</span><span class="sxs-lookup"><span data-stu-id="778ef-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic"
                           }
```

<span data-ttu-id="778ef-114">Det här kommandot får alla belastningsutjämnare med ett namn som börjar med "MyLoadBalancer"</span><span class="sxs-lookup"><span data-stu-id="778ef-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="778ef-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="778ef-115">PARAMETERS</span></span>

### <span data-ttu-id="778ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778ef-116">-DefaultProfile</span></span>
<span data-ttu-id="778ef-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="778ef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="778ef-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="778ef-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="778ef-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="778ef-119">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="778ef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="778ef-120">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="778ef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778ef-121">CommonParameters</span></span>
<span data-ttu-id="778ef-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="778ef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778ef-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="778ef-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778ef-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="778ef-124">INPUTS</span></span>

### <span data-ttu-id="778ef-125">System. String</span><span class="sxs-lookup"><span data-stu-id="778ef-125">System.String</span></span>

## <span data-ttu-id="778ef-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="778ef-126">OUTPUTS</span></span>

### <span data-ttu-id="778ef-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="778ef-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="778ef-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="778ef-128">NOTES</span></span>

## <span data-ttu-id="778ef-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="778ef-129">RELATED LINKS</span></span>

[<span data-ttu-id="778ef-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="778ef-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="778ef-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="778ef-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="778ef-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="778ef-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


