---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e97e8f3ed5769e4f81175b29f097aa4946d28881
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922414"
---
# <span data-ttu-id="4cd09-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4cd09-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="4cd09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cd09-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd09-103">Lägger till en konfiguration för en server dels adresspool i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="4cd09-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="4cd09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cd09-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cd09-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cd09-105">DESCRIPTION</span></span>
<span data-ttu-id="4cd09-106">Cmdleten **Add-AzLoadBalancerBackend** lägger till en server dels adress i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="4cd09-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="4cd09-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cd09-107">EXAMPLES</span></span>

### <span data-ttu-id="4cd09-108">Exempel 1 lägga till en konfiguration för en server dels adresspool i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="4cd09-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="4cd09-109">Det här kommandot får belastningsutjämnaren med namnet MyLoadBalancer, lägger till backend-adresspoolen med namnet BackendAddressPool02 i MyLoadBalancer och använder sedan cmdleten **set-AzLoadBalancer** för att uppdatera MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="4cd09-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="4cd09-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cd09-110">PARAMETERS</span></span>

### <span data-ttu-id="4cd09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd09-111">-DefaultProfile</span></span>
<span data-ttu-id="4cd09-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd09-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cd09-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cd09-113">-LoadBalancer</span></span>
<span data-ttu-id="4cd09-114">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4cd09-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="4cd09-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4cd09-115">-Name</span></span>
<span data-ttu-id="4cd09-116">Anger namnet på Server delens adresspool som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="4cd09-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd09-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd09-117">CommonParameters</span></span>
<span data-ttu-id="4cd09-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cd09-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd09-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd09-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd09-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cd09-120">INPUTS</span></span>

### <span data-ttu-id="4cd09-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cd09-121">PSLoadBalancer</span></span>
<span data-ttu-id="4cd09-122">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4cd09-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4cd09-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cd09-123">OUTPUTS</span></span>

### <span data-ttu-id="4cd09-124">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cd09-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4cd09-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cd09-125">NOTES</span></span>

## <span data-ttu-id="4cd09-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cd09-126">RELATED LINKS</span></span>

[<span data-ttu-id="4cd09-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cd09-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4cd09-128">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4cd09-128">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="4cd09-129">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4cd09-129">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4cd09-130">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4cd09-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4cd09-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4cd09-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


