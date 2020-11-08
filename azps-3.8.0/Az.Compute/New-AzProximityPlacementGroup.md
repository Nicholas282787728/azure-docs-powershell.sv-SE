---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: cf8c4867fcc623065cce73fa392cb78d513200fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089178"
---
# <span data-ttu-id="623d3-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="623d3-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="623d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="623d3-102">SYNOPSIS</span></span>
<span data-ttu-id="623d3-103">Skapa en grupp resurs för närhets placering.</span><span class="sxs-lookup"><span data-stu-id="623d3-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="623d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="623d3-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="623d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="623d3-105">DESCRIPTION</span></span>
<span data-ttu-id="623d3-106">Denna cmdlet kommer att skapa grupp resursen närhets placering.</span><span class="sxs-lookup"><span data-stu-id="623d3-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="623d3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="623d3-107">EXAMPLES</span></span>

### <span data-ttu-id="623d3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="623d3-108">Example 1</span></span>
```
PS C:\> New-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = "val1"}

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {"key1":"val1"}
```

<span data-ttu-id="623d3-109">Det här kommandot skapar en närhets plats grupp på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="623d3-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="623d3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="623d3-110">PARAMETERS</span></span>

### <span data-ttu-id="623d3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="623d3-111">-AsJob</span></span>
<span data-ttu-id="623d3-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="623d3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="623d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623d3-113">-DefaultProfile</span></span>
<span data-ttu-id="623d3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="623d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="623d3-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="623d3-115">-Location</span></span>
<span data-ttu-id="623d3-116">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="623d3-116">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623d3-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="623d3-117">-Name</span></span>
<span data-ttu-id="623d3-118">Namnet på närhets placerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="623d3-118">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623d3-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="623d3-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="623d3-120">Anger typen för närhets placerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="623d3-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="623d3-121">Möjliga värden är: standard eller Ultra</span><span class="sxs-lookup"><span data-stu-id="623d3-121">Possible values are: Standard or Ultra</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="623d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="623d3-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="623d3-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623d3-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="623d3-124">-Tag</span></span>
<span data-ttu-id="623d3-125">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="623d3-125">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623d3-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="623d3-126">-Confirm</span></span>
<span data-ttu-id="623d3-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="623d3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="623d3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="623d3-128">-WhatIf</span></span>
<span data-ttu-id="623d3-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="623d3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="623d3-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="623d3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="623d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623d3-131">CommonParameters</span></span>
<span data-ttu-id="623d3-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623d3-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="623d3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623d3-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="623d3-134">INPUTS</span></span>

### <span data-ttu-id="623d3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="623d3-135">System.String</span></span>

## <span data-ttu-id="623d3-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="623d3-136">OUTPUTS</span></span>

### <span data-ttu-id="623d3-137">Microsoft. Azure. commands. Compute. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="623d3-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="623d3-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="623d3-138">NOTES</span></span>

## <span data-ttu-id="623d3-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="623d3-139">RELATED LINKS</span></span>
