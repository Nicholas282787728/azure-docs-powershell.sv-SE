---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388452"
---
# <span data-ttu-id="5d71c-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="5d71c-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="5d71c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d71c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d71c-103">Skapar ett nytt dedikerat eventhub-kluster</span><span class="sxs-lookup"><span data-stu-id="5d71c-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="5d71c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d71c-104">SYNTAX</span></span>

### <span data-ttu-id="5d71c-105">ClusterPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5d71c-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d71c-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d71c-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d71c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d71c-107">DESCRIPTION</span></span>
<span data-ttu-id="5d71c-108">New-AzEventHubCluster-cmdleten skapar det dedikerade eventhub-klustret i den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5d71c-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="5d71c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d71c-109">EXAMPLES</span></span>

### <span data-ttu-id="5d71c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5d71c-110">Example 1</span></span>
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

<span data-ttu-id="5d71c-111">Skapar ett dedicerat kluster av typen Eventhub-Cluster-5557 i resourcegroup ' RSG-Cluster27651 ' med platsen southcentralus och Capacity as 1</span><span class="sxs-lookup"><span data-stu-id="5d71c-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="5d71c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d71c-112">PARAMETERS</span></span>

### <span data-ttu-id="5d71c-113">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="5d71c-113">-Capacity</span></span>
<span data-ttu-id="5d71c-114">Kluster kapacitet (CU), curerntrly, tillåtet värde = 1</span><span class="sxs-lookup"><span data-stu-id="5d71c-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="5d71c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d71c-115">-DefaultProfile</span></span>
<span data-ttu-id="5d71c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d71c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d71c-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="5d71c-117">-Location</span></span>
<span data-ttu-id="5d71c-118">Kluster plats</span><span class="sxs-lookup"><span data-stu-id="5d71c-118">Location of Cluster</span></span>

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

### <span data-ttu-id="5d71c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d71c-119">-Name</span></span>
<span data-ttu-id="5d71c-120">Kluster namn</span><span class="sxs-lookup"><span data-stu-id="5d71c-120">Cluster Name</span></span>

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

### <span data-ttu-id="5d71c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d71c-121">-ResourceGroupName</span></span>
<span data-ttu-id="5d71c-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5d71c-122">Resource Group Name</span></span>

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

### <span data-ttu-id="5d71c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d71c-123">-ResourceId</span></span>
<span data-ttu-id="5d71c-124">Resurs-ID för kluster</span><span class="sxs-lookup"><span data-stu-id="5d71c-124">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="5d71c-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5d71c-125">-Tag</span></span>
<span data-ttu-id="5d71c-126">Hashtables som representerar resurs märken för kluster</span><span class="sxs-lookup"><span data-stu-id="5d71c-126">Hashtables which represents resource Tags for Clusters</span></span>

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

### <span data-ttu-id="5d71c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5d71c-127">-Confirm</span></span>
<span data-ttu-id="5d71c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5d71c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d71c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d71c-129">-WhatIf</span></span>
<span data-ttu-id="5d71c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5d71c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d71c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5d71c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d71c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d71c-132">CommonParameters</span></span>
<span data-ttu-id="5d71c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d71c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d71c-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d71c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d71c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d71c-135">INPUTS</span></span>

### <span data-ttu-id="5d71c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5d71c-136">System.String</span></span>

### <span data-ttu-id="5d71c-137">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5d71c-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="5d71c-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5d71c-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5d71c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d71c-139">OUTPUTS</span></span>

### <span data-ttu-id="5d71c-140">Microsoft. Azure. commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="5d71c-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="5d71c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d71c-141">NOTES</span></span>

## <span data-ttu-id="5d71c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d71c-142">RELATED LINKS</span></span>
