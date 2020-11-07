---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 2a3f4a6d386f37334908efde31332ed6137ecb74
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745038"
---
# <span data-ttu-id="25146-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="25146-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="25146-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25146-102">SYNOPSIS</span></span>
<span data-ttu-id="25146-103">Ta bort resursen för närhets placering.</span><span class="sxs-lookup"><span data-stu-id="25146-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="25146-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25146-104">SYNTAX</span></span>

### <span data-ttu-id="25146-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="25146-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25146-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="25146-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25146-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="25146-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25146-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25146-108">DESCRIPTION</span></span>
<span data-ttu-id="25146-109">Denna cmdlet tar bort gruppen närhet till placering.</span><span class="sxs-lookup"><span data-stu-id="25146-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="25146-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25146-110">EXAMPLES</span></span>

### <span data-ttu-id="25146-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25146-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="25146-112">Det här kommandot tar bort gruppen närhets placering.</span><span class="sxs-lookup"><span data-stu-id="25146-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="25146-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25146-113">PARAMETERS</span></span>

### <span data-ttu-id="25146-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25146-114">-AsJob</span></span>
<span data-ttu-id="25146-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="25146-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25146-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25146-116">-DefaultProfile</span></span>
<span data-ttu-id="25146-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25146-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25146-118">-Force</span><span class="sxs-lookup"><span data-stu-id="25146-118">-Force</span></span>
<span data-ttu-id="25146-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="25146-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25146-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25146-120">-InputObject</span></span>
<span data-ttu-id="25146-121">Grupp objekt med PS-närhet</span><span class="sxs-lookup"><span data-stu-id="25146-121">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25146-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="25146-122">-Name</span></span>
<span data-ttu-id="25146-123">Namnet på närhets placerings gruppen.</span><span class="sxs-lookup"><span data-stu-id="25146-123">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25146-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25146-124">-ResourceGroupName</span></span>
<span data-ttu-id="25146-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="25146-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25146-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25146-126">-ResourceId</span></span>
<span data-ttu-id="25146-127">Resurs-ID för placering av närhet.</span><span class="sxs-lookup"><span data-stu-id="25146-127">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25146-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="25146-128">-Confirm</span></span>
<span data-ttu-id="25146-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="25146-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25146-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25146-130">-WhatIf</span></span>
<span data-ttu-id="25146-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="25146-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25146-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="25146-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25146-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25146-133">CommonParameters</span></span>
<span data-ttu-id="25146-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25146-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25146-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25146-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25146-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25146-136">INPUTS</span></span>

### <span data-ttu-id="25146-137">System. String</span><span class="sxs-lookup"><span data-stu-id="25146-137">System.String</span></span>

### <span data-ttu-id="25146-138">Microsoft. Azure. commands. Compute. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="25146-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="25146-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25146-139">OUTPUTS</span></span>

### <span data-ttu-id="25146-140">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="25146-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="25146-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25146-141">NOTES</span></span>

## <span data-ttu-id="25146-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25146-142">RELATED LINKS</span></span>
