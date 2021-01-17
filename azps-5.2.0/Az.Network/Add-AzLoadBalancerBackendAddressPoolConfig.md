---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 39e388fbdb809f136942749a0d0585189155e32b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417251"
---
# <span data-ttu-id="f8c0a-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8c0a-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f8c0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c0a-103">Lägger till en konfiguration för en server dels adresspool i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="f8c0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8c0a-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8c0a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="f8c0a-106">Cmdleten **Add-AzLoadBalancerBackend** lägger till en server dels adress i en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="f8c0a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8c0a-107">EXAMPLES</span></span>

### <span data-ttu-id="f8c0a-108">Exempel 1: lägga till en konfiguration för en server dels adresspool i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="f8c0a-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="f8c0a-109">Det här kommandot får belastningsutjämnaren med namnet MyLoadBalancer, lägger till backend-adresspoolen med namnet BackendAddressPool02 i MyLoadBalancer och använder sedan cmdleten **set-AzLoadBalancer** för att uppdatera MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="f8c0a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8c0a-110">PARAMETERS</span></span>

### <span data-ttu-id="f8c0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c0a-111">-DefaultProfile</span></span>
<span data-ttu-id="f8c0a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8c0a-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8c0a-113">-LoadBalancer</span></span>
<span data-ttu-id="f8c0a-114">Anger ett **Loadbalancer** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="f8c0a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8c0a-115">-Name</span></span>
<span data-ttu-id="f8c0a-116">Anger namnet på Server delens adresspool som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c0a-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8c0a-117">-Confirm</span></span>
<span data-ttu-id="f8c0a-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c0a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8c0a-119">-WhatIf</span></span>
<span data-ttu-id="f8c0a-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8c0a-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c0a-122">CommonParameters</span></span>
<span data-ttu-id="f8c0a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c0a-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8c0a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c0a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8c0a-125">INPUTS</span></span>

### <span data-ttu-id="f8c0a-126">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8c0a-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f8c0a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8c0a-127">OUTPUTS</span></span>

### <span data-ttu-id="f8c0a-128">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8c0a-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f8c0a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8c0a-129">NOTES</span></span>

## <span data-ttu-id="f8c0a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8c0a-130">RELATED LINKS</span></span>

[<span data-ttu-id="f8c0a-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8c0a-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f8c0a-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f8c0a-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="f8c0a-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8c0a-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f8c0a-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8c0a-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f8c0a-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8c0a-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


