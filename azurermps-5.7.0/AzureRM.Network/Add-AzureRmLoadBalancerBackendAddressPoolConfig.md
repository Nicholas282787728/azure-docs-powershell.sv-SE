---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 82775229bc368f80c03a886b10a631a4482341df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577162"
---
# <span data-ttu-id="99230-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="99230-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="99230-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99230-102">SYNOPSIS</span></span>
<span data-ttu-id="99230-103">Lägger till en konfiguration för en server dels adresspool i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="99230-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99230-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99230-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99230-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99230-105">DESCRIPTION</span></span>
<span data-ttu-id="99230-106">Cmdleten **Add-AzureRmLoadBalancerBackend** lägger till en server dels adress i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="99230-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="99230-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99230-107">EXAMPLES</span></span>

### <span data-ttu-id="99230-108">Exempel 1 lägga till en konfiguration för en server dels adresspool i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="99230-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="99230-109">Det här kommandot får belastningsutjämnaren med namnet MyLoadBalancer, lägger till backend-adresspoolen med namnet BackendAddressPool02 i MyLoadBalancer och använder sedan cmdleten **set-AzureRmLoadBalancer** för att uppdatera MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="99230-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="99230-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99230-110">PARAMETERS</span></span>

### <span data-ttu-id="99230-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99230-111">-DefaultProfile</span></span>
<span data-ttu-id="99230-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99230-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99230-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99230-113">-LoadBalancer</span></span>
<span data-ttu-id="99230-114">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="99230-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="99230-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="99230-115">-Name</span></span>
<span data-ttu-id="99230-116">Anger namnet på Server delens adresspool som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="99230-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="99230-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99230-117">CommonParameters</span></span>
<span data-ttu-id="99230-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99230-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99230-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99230-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99230-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99230-120">INPUTS</span></span>

### <span data-ttu-id="99230-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99230-121">PSLoadBalancer</span></span>
<span data-ttu-id="99230-122">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="99230-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="99230-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99230-123">OUTPUTS</span></span>

### <span data-ttu-id="99230-124">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99230-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="99230-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99230-125">NOTES</span></span>

## <span data-ttu-id="99230-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99230-126">RELATED LINKS</span></span>

[<span data-ttu-id="99230-127">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99230-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="99230-128">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="99230-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="99230-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="99230-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="99230-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="99230-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="99230-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="99230-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


