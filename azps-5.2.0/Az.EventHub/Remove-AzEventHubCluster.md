---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406552"
---
# <span data-ttu-id="de7d8-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="de7d8-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="de7d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de7d8-102">SYNOPSIS</span></span>
<span data-ttu-id="de7d8-103">Tar bort angivet dedikerat Eventhub-kluster från ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de7d8-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="de7d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de7d8-104">SYNTAX</span></span>

### <span data-ttu-id="de7d8-105">ClusterPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="de7d8-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de7d8-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="de7d8-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de7d8-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de7d8-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de7d8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de7d8-108">DESCRIPTION</span></span>
<span data-ttu-id="de7d8-109">Remove-AzEventHubCluster cmdlet tar bort angivet dedikerade eventhub-kluster namn från angiven resourcegroup</span><span class="sxs-lookup"><span data-stu-id="de7d8-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="de7d8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de7d8-110">EXAMPLES</span></span>

### <span data-ttu-id="de7d8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="de7d8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="de7d8-112">Tar bort Eventhub-kluster-5557-kluster från RSG-Cluster27651 resourcegroup</span><span class="sxs-lookup"><span data-stu-id="de7d8-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="de7d8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de7d8-113">PARAMETERS</span></span>

### <span data-ttu-id="de7d8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de7d8-114">-AsJob</span></span>
<span data-ttu-id="de7d8-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="de7d8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de7d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de7d8-116">-DefaultProfile</span></span>
<span data-ttu-id="de7d8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de7d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de7d8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de7d8-118">-InputObject</span></span>
<span data-ttu-id="de7d8-119">Kluster objekt</span><span class="sxs-lookup"><span data-stu-id="de7d8-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de7d8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="de7d8-120">-Name</span></span>
<span data-ttu-id="de7d8-121">Kluster namn</span><span class="sxs-lookup"><span data-stu-id="de7d8-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de7d8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de7d8-122">-PassThru</span></span>
<span data-ttu-id="de7d8-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="de7d8-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="de7d8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de7d8-124">-ResourceGroupName</span></span>
<span data-ttu-id="de7d8-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="de7d8-125">Resource Group Name</span></span>

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

### <span data-ttu-id="de7d8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de7d8-126">-ResourceId</span></span>
<span data-ttu-id="de7d8-127">Kluster resurs-ID</span><span class="sxs-lookup"><span data-stu-id="de7d8-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de7d8-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de7d8-128">-Confirm</span></span>
<span data-ttu-id="de7d8-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de7d8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de7d8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de7d8-130">-WhatIf</span></span>
<span data-ttu-id="de7d8-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de7d8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de7d8-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de7d8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de7d8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de7d8-133">CommonParameters</span></span>
<span data-ttu-id="de7d8-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de7d8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de7d8-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de7d8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de7d8-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de7d8-136">INPUTS</span></span>

### <span data-ttu-id="de7d8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="de7d8-137">System.String</span></span>

### <span data-ttu-id="de7d8-138">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="de7d8-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="de7d8-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de7d8-139">OUTPUTS</span></span>

### <span data-ttu-id="de7d8-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de7d8-140">System.Boolean</span></span>

## <span data-ttu-id="de7d8-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de7d8-141">NOTES</span></span>

## <span data-ttu-id="de7d8-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de7d8-142">RELATED LINKS</span></span>
