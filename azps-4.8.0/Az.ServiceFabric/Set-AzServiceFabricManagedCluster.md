---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261674"
---
# <span data-ttu-id="7125a-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7125a-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="7125a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7125a-102">SYNOPSIS</span></span>
<span data-ttu-id="7125a-103">Ange egenskaper för en kluster resurs.</span><span class="sxs-lookup"><span data-stu-id="7125a-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="7125a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7125a-104">SYNTAX</span></span>

### <span data-ttu-id="7125a-105">ByObj (standard)</span><span class="sxs-lookup"><span data-stu-id="7125a-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7125a-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="7125a-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7125a-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="7125a-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7125a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7125a-108">DESCRIPTION</span></span>
<span data-ttu-id="7125a-109">Ange egenskaper för en kluster resurs.</span><span class="sxs-lookup"><span data-stu-id="7125a-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="7125a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7125a-110">EXAMPLES</span></span>

### <span data-ttu-id="7125a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7125a-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="7125a-112">Uppdatera DNS-namn och klient anslutnings port för klustret.</span><span class="sxs-lookup"><span data-stu-id="7125a-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="7125a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7125a-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="7125a-114">Uppdatera DNS-namn och klient anslutnings portar för klustret med rör dragning.</span><span class="sxs-lookup"><span data-stu-id="7125a-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="7125a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7125a-115">PARAMETERS</span></span>

### <span data-ttu-id="7125a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7125a-116">-AsJob</span></span>
<span data-ttu-id="7125a-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="7125a-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="7125a-118">-ClientConnectionPort</span></span>
<span data-ttu-id="7125a-119">Port som används för klient anslutningar till klustret.</span><span class="sxs-lookup"><span data-stu-id="7125a-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="7125a-120">Standard: 19000.</span><span class="sxs-lookup"><span data-stu-id="7125a-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="7125a-121">-CodeVersion</span></span>
<span data-ttu-id="7125a-122">Kluster kod version.</span><span class="sxs-lookup"><span data-stu-id="7125a-122">Cluster code version.</span></span> <span data-ttu-id="7125a-123">Använd endast om uppgraderings läget är manuell.</span><span class="sxs-lookup"><span data-stu-id="7125a-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7125a-124">-DefaultProfile</span></span>
<span data-ttu-id="7125a-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7125a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7125a-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="7125a-126">-DnsName</span></span>
<span data-ttu-id="7125a-127">Klustrets DNS-namn.</span><span class="sxs-lookup"><span data-stu-id="7125a-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="7125a-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="7125a-129">Port som används för HTTP-anslutningar till klustret.</span><span class="sxs-lookup"><span data-stu-id="7125a-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="7125a-130">Standard: 19080.</span><span class="sxs-lookup"><span data-stu-id="7125a-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7125a-131">-InputObject</span></span>
<span data-ttu-id="7125a-132">Hanterad kluster resurs</span><span class="sxs-lookup"><span data-stu-id="7125a-132">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="7125a-133">-Name</span></span>
<span data-ttu-id="7125a-134">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="7125a-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7125a-135">-ResourceGroupName</span></span>
<span data-ttu-id="7125a-136">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7125a-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7125a-137">-ResourceId</span></span>
<span data-ttu-id="7125a-138">Hanterat kluster resurs-ID</span><span class="sxs-lookup"><span data-stu-id="7125a-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="7125a-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="7125a-140">Slut punkt som används av omvänd proxy.</span><span class="sxs-lookup"><span data-stu-id="7125a-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="7125a-141">-UpgradeMode</span></span>
<span data-ttu-id="7125a-142">Uppgraderings läge för kluster kod version.</span><span class="sxs-lookup"><span data-stu-id="7125a-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="7125a-143">Automatisk eller manuell.</span><span class="sxs-lookup"><span data-stu-id="7125a-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125a-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7125a-144">-Confirm</span></span>
<span data-ttu-id="7125a-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7125a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7125a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7125a-146">-WhatIf</span></span>
<span data-ttu-id="7125a-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7125a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7125a-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7125a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7125a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7125a-149">CommonParameters</span></span>
<span data-ttu-id="7125a-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7125a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7125a-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7125a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7125a-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7125a-152">INPUTS</span></span>

### <span data-ttu-id="7125a-153">System. String</span><span class="sxs-lookup"><span data-stu-id="7125a-153">System.String</span></span>

## <span data-ttu-id="7125a-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7125a-154">OUTPUTS</span></span>

### <span data-ttu-id="7125a-155">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7125a-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="7125a-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7125a-156">NOTES</span></span>

## <span data-ttu-id="7125a-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7125a-157">RELATED LINKS</span></span>
