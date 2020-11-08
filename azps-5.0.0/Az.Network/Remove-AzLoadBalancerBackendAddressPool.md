---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269307"
---
# <span data-ttu-id="17082-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="17082-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="17082-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17082-102">SYNOPSIS</span></span>
<span data-ttu-id="17082-103">Tar bort en server del från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="17082-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="17082-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17082-104">SYNTAX</span></span>

### <span data-ttu-id="17082-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="17082-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17082-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17082-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17082-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17082-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17082-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17082-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17082-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17082-109">DESCRIPTION</span></span>
<span data-ttu-id="17082-110">Tar bort en server del från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="17082-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="17082-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17082-111">EXAMPLES</span></span>

### <span data-ttu-id="17082-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17082-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="17082-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="17082-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="17082-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="17082-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="17082-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17082-115">PARAMETERS</span></span>

### <span data-ttu-id="17082-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17082-116">-DefaultProfile</span></span>
<span data-ttu-id="17082-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17082-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17082-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17082-118">-InputObject</span></span>
<span data-ttu-id="17082-119">Backend-adresspoolen att ta bort</span><span class="sxs-lookup"><span data-stu-id="17082-119">The backend address pool to remove</span></span>

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

### <span data-ttu-id="17082-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17082-120">-LoadBalancer</span></span>
<span data-ttu-id="17082-121">Resursen för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="17082-121">The load balancer resource.</span></span>

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

### <span data-ttu-id="17082-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="17082-122">-LoadBalancerName</span></span>
<span data-ttu-id="17082-123">Namnet på belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="17082-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="17082-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="17082-124">-Name</span></span>
<span data-ttu-id="17082-125">Namnet på belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="17082-125">The name of the load balancer.</span></span>

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

### <span data-ttu-id="17082-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17082-126">-PassThru</span></span>
<span data-ttu-id="17082-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="17082-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="17082-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17082-128">-ResourceGroupName</span></span>
<span data-ttu-id="17082-129">Belastnings utjämningens resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="17082-129">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="17082-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17082-130">-ResourceId</span></span>

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

### <span data-ttu-id="17082-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17082-131">-Confirm</span></span>
<span data-ttu-id="17082-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17082-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17082-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17082-133">-WhatIf</span></span>
<span data-ttu-id="17082-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="17082-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17082-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="17082-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17082-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17082-136">CommonParameters</span></span>
<span data-ttu-id="17082-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17082-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17082-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17082-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17082-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17082-139">INPUTS</span></span>

### <span data-ttu-id="17082-140">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17082-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="17082-141">System. String</span><span class="sxs-lookup"><span data-stu-id="17082-141">System.String</span></span>

## <span data-ttu-id="17082-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17082-142">OUTPUTS</span></span>

### <span data-ttu-id="17082-143">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="17082-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="17082-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17082-144">NOTES</span></span>

## <span data-ttu-id="17082-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17082-145">RELATED LINKS</span></span>
