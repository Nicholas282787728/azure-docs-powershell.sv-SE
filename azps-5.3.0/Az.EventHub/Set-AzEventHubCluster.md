---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523670"
---
# <span data-ttu-id="8a9c5-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="8a9c5-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="8a9c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a9c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9c5-103">Uppdaterar taggen för det angivna klustret</span><span class="sxs-lookup"><span data-stu-id="8a9c5-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="8a9c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a9c5-104">SYNTAX</span></span>

### <span data-ttu-id="8a9c5-105">ClusterPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8a9c5-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a9c5-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a9c5-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a9c5-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8a9c5-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a9c5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a9c5-108">DESCRIPTION</span></span>
<span data-ttu-id="8a9c5-109">Set-AzEventHubCluster cmdlet uppdaterar taggar för det angivna klustret</span><span class="sxs-lookup"><span data-stu-id="8a9c5-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="8a9c5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a9c5-110">EXAMPLES</span></span>

### <span data-ttu-id="8a9c5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a9c5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="8a9c5-112">Uppdaterar taggar för det angivna klustret.</span><span class="sxs-lookup"><span data-stu-id="8a9c5-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="8a9c5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a9c5-113">PARAMETERS</span></span>

### <span data-ttu-id="8a9c5-114">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="8a9c5-114">-Capacity</span></span>
<span data-ttu-id="8a9c5-115">Kluster kapacitet (CU), curerntrly, tillåtet värde = 1</span><span class="sxs-lookup"><span data-stu-id="8a9c5-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9c5-116">-DefaultProfile</span></span>
<span data-ttu-id="8a9c5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a9c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a9c5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a9c5-118">-InputObject</span></span>
<span data-ttu-id="8a9c5-119">Kluster namn</span><span class="sxs-lookup"><span data-stu-id="8a9c5-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c5-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="8a9c5-120">-Location</span></span>
<span data-ttu-id="8a9c5-121">Kluster plats</span><span class="sxs-lookup"><span data-stu-id="8a9c5-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a9c5-122">-Name</span></span>
<span data-ttu-id="8a9c5-123">Kluster namn</span><span class="sxs-lookup"><span data-stu-id="8a9c5-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a9c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="8a9c5-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8a9c5-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a9c5-126">-ResourceId</span></span>
<span data-ttu-id="8a9c5-127">Resurs-ID för kluster</span><span class="sxs-lookup"><span data-stu-id="8a9c5-127">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c5-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8a9c5-128">-Tag</span></span>
<span data-ttu-id="8a9c5-129">Hashtables som representerar resurs tag gen för kluster</span><span class="sxs-lookup"><span data-stu-id="8a9c5-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a9c5-130">-Confirm</span></span>
<span data-ttu-id="8a9c5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a9c5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a9c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a9c5-132">-WhatIf</span></span>
<span data-ttu-id="8a9c5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a9c5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a9c5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a9c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a9c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9c5-135">CommonParameters</span></span>
<span data-ttu-id="8a9c5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a9c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9c5-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a9c5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9c5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a9c5-138">INPUTS</span></span>

### <span data-ttu-id="8a9c5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8a9c5-139">System.String</span></span>

### <span data-ttu-id="8a9c5-140">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8a9c5-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="8a9c5-141">Microsoft. Azure. commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="8a9c5-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="8a9c5-142">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="8a9c5-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8a9c5-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a9c5-143">OUTPUTS</span></span>

### <span data-ttu-id="8a9c5-144">Microsoft. Azure. commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="8a9c5-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="8a9c5-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a9c5-145">NOTES</span></span>

## <span data-ttu-id="8a9c5-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a9c5-146">RELATED LINKS</span></span>
