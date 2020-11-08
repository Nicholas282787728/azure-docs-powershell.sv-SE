---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258210"
---
# <span data-ttu-id="59eed-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="59eed-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="59eed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59eed-102">SYNOPSIS</span></span>
<span data-ttu-id="59eed-103">Tar bort en server del från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="59eed-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="59eed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59eed-104">SYNTAX</span></span>

### <span data-ttu-id="59eed-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="59eed-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59eed-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59eed-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59eed-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59eed-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59eed-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59eed-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59eed-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59eed-109">DESCRIPTION</span></span>
<span data-ttu-id="59eed-110">Tar bort en server del från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="59eed-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="59eed-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59eed-111">EXAMPLES</span></span>

### <span data-ttu-id="59eed-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59eed-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="59eed-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="59eed-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="59eed-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="59eed-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="59eed-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59eed-115">PARAMETERS</span></span>

### <span data-ttu-id="59eed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59eed-116">-DefaultProfile</span></span>
<span data-ttu-id="59eed-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59eed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eed-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59eed-118">-InputObject</span></span>
<span data-ttu-id="59eed-119">Backend-adresspoolen att ta bort</span><span class="sxs-lookup"><span data-stu-id="59eed-119">The backend address pool to remove</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eed-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59eed-120">-LoadBalancer</span></span>
<span data-ttu-id="59eed-121">Resursen för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="59eed-121">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59eed-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="59eed-122">-LoadBalancerName</span></span>
<span data-ttu-id="59eed-123">Namnet på belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="59eed-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="59eed-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="59eed-124">-Name</span></span>
<span data-ttu-id="59eed-125">Namnet på belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="59eed-125">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eed-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59eed-126">-PassThru</span></span>
<span data-ttu-id="59eed-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="59eed-127">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59eed-128">-ResourceGroupName</span></span>
<span data-ttu-id="59eed-129">Belastnings utjämningens resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="59eed-129">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eed-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59eed-130">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59eed-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59eed-131">-Confirm</span></span>
<span data-ttu-id="59eed-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59eed-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eed-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59eed-133">-WhatIf</span></span>
<span data-ttu-id="59eed-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59eed-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59eed-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59eed-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59eed-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59eed-136">CommonParameters</span></span>
<span data-ttu-id="59eed-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59eed-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59eed-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59eed-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59eed-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59eed-139">INPUTS</span></span>

### <span data-ttu-id="59eed-140">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="59eed-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="59eed-141">System. String</span><span class="sxs-lookup"><span data-stu-id="59eed-141">System.String</span></span>

## <span data-ttu-id="59eed-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59eed-142">OUTPUTS</span></span>

### <span data-ttu-id="59eed-143">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="59eed-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="59eed-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59eed-144">NOTES</span></span>

## <span data-ttu-id="59eed-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59eed-145">RELATED LINKS</span></span>
