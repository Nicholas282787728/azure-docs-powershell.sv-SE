---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413496"
---
# <span data-ttu-id="001e7-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="001e7-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="001e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="001e7-102">SYNOPSIS</span></span>
<span data-ttu-id="001e7-103">Uppdatera kluster</span><span class="sxs-lookup"><span data-stu-id="001e7-103">update cluster</span></span>

## <span data-ttu-id="001e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="001e7-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="001e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="001e7-105">DESCRIPTION</span></span>
<span data-ttu-id="001e7-106">Uppdatera kluster</span><span class="sxs-lookup"><span data-stu-id="001e7-106">update cluster</span></span>

## <span data-ttu-id="001e7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="001e7-107">EXAMPLES</span></span>

### <span data-ttu-id="001e7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="001e7-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="001e7-109">Uppdatera kluster med egenskaper för viktiga valv och SKU</span><span class="sxs-lookup"><span data-stu-id="001e7-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="001e7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="001e7-110">PARAMETERS</span></span>

### <span data-ttu-id="001e7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="001e7-111">-AsJob</span></span>
<span data-ttu-id="001e7-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="001e7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="001e7-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="001e7-113">-ClusterName</span></span>
<span data-ttu-id="001e7-114">Kluster namnet.</span><span class="sxs-lookup"><span data-stu-id="001e7-114">The cluster name.</span></span>

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

### <span data-ttu-id="001e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="001e7-115">-DefaultProfile</span></span>
<span data-ttu-id="001e7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="001e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="001e7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="001e7-117">-KeyName</span></span>
<span data-ttu-id="001e7-118">Namn på knappen</span><span class="sxs-lookup"><span data-stu-id="001e7-118">Key Name</span></span>

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

### <span data-ttu-id="001e7-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="001e7-119">-KeyVaultUri</span></span>
<span data-ttu-id="001e7-120">Key valv URI, "rensnings skydd" och "mjuk borttagning" måste aktive ras för detta valv</span><span class="sxs-lookup"><span data-stu-id="001e7-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="001e7-121">-Version</span><span class="sxs-lookup"><span data-stu-id="001e7-121">-KeyVersion</span></span>
<span data-ttu-id="001e7-122">Viktig version</span><span class="sxs-lookup"><span data-stu-id="001e7-122">Key Version</span></span>

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

### <span data-ttu-id="001e7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="001e7-123">-ResourceGroupName</span></span>
<span data-ttu-id="001e7-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="001e7-124">The resource group name.</span></span>

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

### <span data-ttu-id="001e7-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="001e7-125">-SkuCapacity</span></span>
<span data-ttu-id="001e7-126">SKU-kapacitet</span><span class="sxs-lookup"><span data-stu-id="001e7-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="001e7-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="001e7-127">-SkuName</span></span>
<span data-ttu-id="001e7-128">SKU-namnet kan nu vara "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="001e7-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="001e7-129">-Taggar</span><span class="sxs-lookup"><span data-stu-id="001e7-129">-Tags</span></span>
<span data-ttu-id="001e7-130">Taggar i klustret</span><span class="sxs-lookup"><span data-stu-id="001e7-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="001e7-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="001e7-131">-Confirm</span></span>
<span data-ttu-id="001e7-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="001e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="001e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="001e7-133">-WhatIf</span></span>
<span data-ttu-id="001e7-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="001e7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="001e7-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="001e7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="001e7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001e7-136">CommonParameters</span></span>
<span data-ttu-id="001e7-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="001e7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001e7-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="001e7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001e7-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="001e7-139">INPUTS</span></span>

### <span data-ttu-id="001e7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="001e7-140">System.String</span></span>

## <span data-ttu-id="001e7-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="001e7-141">OUTPUTS</span></span>

### <span data-ttu-id="001e7-142">Microsoft. Azure. commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="001e7-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="001e7-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="001e7-143">NOTES</span></span>

## <span data-ttu-id="001e7-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="001e7-144">RELATED LINKS</span></span>
