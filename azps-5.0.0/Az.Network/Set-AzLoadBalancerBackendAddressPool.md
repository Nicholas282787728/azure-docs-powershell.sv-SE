---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270824"
---
# <span data-ttu-id="82040-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82040-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="82040-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82040-102">SYNOPSIS</span></span>
<span data-ttu-id="82040-103">Uppdaterar backend-poolen på en Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="82040-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="82040-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82040-104">SYNTAX</span></span>

### <span data-ttu-id="82040-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="82040-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82040-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82040-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82040-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82040-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82040-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82040-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82040-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82040-109">DESCRIPTION</span></span>
<span data-ttu-id="82040-110">Uppdaterar backend-poolen på en Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="82040-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="82040-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82040-111">EXAMPLES</span></span>

### <span data-ttu-id="82040-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82040-112">Example 1</span></span>
```powershell
###Set by name and modified input object
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip3 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.7" -Name "TestVNetRef3" -VirtualNetworkId $virtualNetwork.id
PS C:\> $ips = @($ip1, $ip2)
PS C:\> $b2 = Get-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool1
PS C:\> $b2.LoadBalancerBackendAddresses.Add($ip3)

PS C:\> Set-AzLoadBalancerBackendAddressPool -InputObject $b2
```
### <span data-ttu-id="82040-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="82040-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="82040-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="82040-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="82040-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82040-115">PARAMETERS</span></span>

### <span data-ttu-id="82040-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82040-116">-DefaultProfile</span></span>
<span data-ttu-id="82040-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82040-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82040-118">-Force</span><span class="sxs-lookup"><span data-stu-id="82040-118">-Force</span></span>
<span data-ttu-id="82040-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="82040-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="82040-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82040-120">-InputObject</span></span>
<span data-ttu-id="82040-121">Backend-adresspoolen att ange</span><span class="sxs-lookup"><span data-stu-id="82040-121">The backend address pool to set</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82040-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="82040-122">-LoadBalancer</span></span>
<span data-ttu-id="82040-123">Resursen för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="82040-123">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82040-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="82040-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="82040-125">Server delens adresser.</span><span class="sxs-lookup"><span data-stu-id="82040-125">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82040-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="82040-126">-LoadBalancerName</span></span>
<span data-ttu-id="82040-127">Namnet på belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="82040-127">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82040-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="82040-128">-Name</span></span>
<span data-ttu-id="82040-129">Namnet på backend-poolen.</span><span class="sxs-lookup"><span data-stu-id="82040-129">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82040-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82040-130">-PassThru</span></span>
<span data-ttu-id="82040-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="82040-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="82040-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82040-132">-ResourceGroupName</span></span>
<span data-ttu-id="82040-133">Belastnings utjämningens resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="82040-133">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82040-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82040-134">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82040-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82040-135">-Confirm</span></span>
<span data-ttu-id="82040-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82040-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82040-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82040-137">-WhatIf</span></span>
<span data-ttu-id="82040-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82040-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82040-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82040-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82040-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82040-140">CommonParameters</span></span>
<span data-ttu-id="82040-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82040-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82040-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82040-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82040-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82040-143">INPUTS</span></span>

### <span data-ttu-id="82040-144">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="82040-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="82040-145">System. String</span><span class="sxs-lookup"><span data-stu-id="82040-145">System.String</span></span>

## <span data-ttu-id="82040-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82040-146">OUTPUTS</span></span>

### <span data-ttu-id="82040-147">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="82040-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="82040-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82040-148">NOTES</span></span>

## <span data-ttu-id="82040-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82040-149">RELATED LINKS</span></span>
