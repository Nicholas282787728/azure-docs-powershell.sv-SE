---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322200"
---
# <span data-ttu-id="0b689-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="0b689-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="0b689-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b689-102">SYNOPSIS</span></span>
<span data-ttu-id="0b689-103">Skapa kluster</span><span class="sxs-lookup"><span data-stu-id="0b689-103">Create cluster</span></span>

## <span data-ttu-id="0b689-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b689-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b689-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b689-105">DESCRIPTION</span></span>

<span data-ttu-id="0b689-106">Skapa kluster</span><span class="sxs-lookup"><span data-stu-id="0b689-106">Create cluster</span></span>

## <span data-ttu-id="0b689-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b689-107">EXAMPLES</span></span>

### <span data-ttu-id="0b689-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0b689-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="0b689-109">Skapa kluster</span><span class="sxs-lookup"><span data-stu-id="0b689-109">Create cluster</span></span>

## <span data-ttu-id="0b689-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b689-110">PARAMETERS</span></span>

### <span data-ttu-id="0b689-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b689-111">-AsJob</span></span>
<span data-ttu-id="0b689-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0b689-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b689-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="0b689-113">-ClusterName</span></span>
<span data-ttu-id="0b689-114">Kluster namnet.</span><span class="sxs-lookup"><span data-stu-id="0b689-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b689-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b689-115">-DefaultProfile</span></span>
<span data-ttu-id="0b689-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b689-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b689-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0b689-117">-IdentityType</span></span>
<span data-ttu-id="0b689-118">identitets typen och värdet kan vara ' SystemAssigned ', ' none '.</span><span class="sxs-lookup"><span data-stu-id="0b689-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b689-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="0b689-119">-Location</span></span>
<span data-ttu-id="0b689-120">Den geografiska region som klustret ska distribueras till.</span><span class="sxs-lookup"><span data-stu-id="0b689-120">The geographic region that the cluster will be deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b689-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b689-121">-ResourceGroupName</span></span>
<span data-ttu-id="0b689-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0b689-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b689-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="0b689-123">-SkuCapacity</span></span>
<span data-ttu-id="0b689-124">SKU-kapaciteten måste vara delbar med 100 och i intervallet 1000-2000.</span><span class="sxs-lookup"><span data-stu-id="0b689-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b689-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0b689-125">-SkuName</span></span>
<span data-ttu-id="0b689-126">SKU-namnet kan nu vara "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="0b689-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b689-127">-Taggar</span><span class="sxs-lookup"><span data-stu-id="0b689-127">-Tags</span></span>
<span data-ttu-id="0b689-128">Taggar i klustret</span><span class="sxs-lookup"><span data-stu-id="0b689-128">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b689-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b689-129">-Confirm</span></span>
<span data-ttu-id="0b689-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b689-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b689-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b689-131">-WhatIf</span></span>
<span data-ttu-id="0b689-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b689-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b689-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b689-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b689-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b689-134">CommonParameters</span></span>
<span data-ttu-id="0b689-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b689-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b689-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b689-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b689-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b689-137">INPUTS</span></span>

### <span data-ttu-id="0b689-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0b689-138">System.String</span></span>

## <span data-ttu-id="0b689-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b689-139">OUTPUTS</span></span>

### <span data-ttu-id="0b689-140">Microsoft. Azure. commands. OperationalInsights. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0b689-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="0b689-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b689-141">NOTES</span></span>

## <span data-ttu-id="0b689-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b689-142">RELATED LINKS</span></span>
