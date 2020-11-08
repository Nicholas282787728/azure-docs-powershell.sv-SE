---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271908"
---
# <span data-ttu-id="22ab1-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="22ab1-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="22ab1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="22ab1-103">Skapar ett nytt dedikerat eventhub-kluster</span><span class="sxs-lookup"><span data-stu-id="22ab1-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="22ab1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22ab1-104">SYNTAX</span></span>

### <span data-ttu-id="22ab1-105">ClusterPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="22ab1-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22ab1-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22ab1-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22ab1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22ab1-107">DESCRIPTION</span></span>
<span data-ttu-id="22ab1-108">New-AzEventHubCluster-cmdleten skapar det dedikerade eventhub-klustret i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="22ab1-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="22ab1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22ab1-109">EXAMPLES</span></span>

### <span data-ttu-id="22ab1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="22ab1-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="22ab1-111">Skapar ett dedicerat kluster av typen Eventhub-Cluster-5557 i resourcegroup ' RSG-Cluster27651 ' med platsen southcentralus och Capacity as 1</span><span class="sxs-lookup"><span data-stu-id="22ab1-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="22ab1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22ab1-112">PARAMETERS</span></span>

### <span data-ttu-id="22ab1-113">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="22ab1-113">-Capacity</span></span>
<span data-ttu-id="22ab1-114">Kluster kapacitet (CU), curerntrly, tillåtet värde = 1</span><span class="sxs-lookup"><span data-stu-id="22ab1-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="22ab1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ab1-115">-DefaultProfile</span></span>
<span data-ttu-id="22ab1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22ab1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22ab1-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="22ab1-117">-Location</span></span>
<span data-ttu-id="22ab1-118">Kluster plats</span><span class="sxs-lookup"><span data-stu-id="22ab1-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ab1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="22ab1-119">-Name</span></span>
<span data-ttu-id="22ab1-120">Kluster namn</span><span class="sxs-lookup"><span data-stu-id="22ab1-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ab1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ab1-121">-ResourceGroupName</span></span>
<span data-ttu-id="22ab1-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="22ab1-122">Resource Group Name</span></span>

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

### <span data-ttu-id="22ab1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22ab1-123">-ResourceId</span></span>
<span data-ttu-id="22ab1-124">Resurs-ID för kluster</span><span class="sxs-lookup"><span data-stu-id="22ab1-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="22ab1-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="22ab1-125">-Tag</span></span>
<span data-ttu-id="22ab1-126">Hashtables som representerar resurs märken för kluster</span><span class="sxs-lookup"><span data-stu-id="22ab1-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ab1-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22ab1-127">-Confirm</span></span>
<span data-ttu-id="22ab1-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22ab1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ab1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ab1-129">-WhatIf</span></span>
<span data-ttu-id="22ab1-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22ab1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22ab1-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22ab1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ab1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ab1-132">CommonParameters</span></span>
<span data-ttu-id="22ab1-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ab1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ab1-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22ab1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ab1-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22ab1-135">INPUTS</span></span>

### <span data-ttu-id="22ab1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="22ab1-136">System.String</span></span>

### <span data-ttu-id="22ab1-137">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="22ab1-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="22ab1-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="22ab1-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22ab1-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22ab1-139">OUTPUTS</span></span>

### <span data-ttu-id="22ab1-140">Microsoft. Azure. commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="22ab1-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="22ab1-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22ab1-141">NOTES</span></span>

## <span data-ttu-id="22ab1-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22ab1-142">RELATED LINKS</span></span>
