---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269327"
---
# <span data-ttu-id="20e51-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="20e51-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="20e51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20e51-102">SYNOPSIS</span></span>
<span data-ttu-id="20e51-103">Ta bort en skiss tilldelning från ett abonnemang eller en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="20e51-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="20e51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20e51-104">SYNTAX</span></span>

### <span data-ttu-id="20e51-105">BySubscriptionAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="20e51-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20e51-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="20e51-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20e51-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="20e51-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20e51-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20e51-108">DESCRIPTION</span></span>
<span data-ttu-id="20e51-109">Ta bort en skiss som har tilldelats till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="20e51-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="20e51-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20e51-110">EXAMPLES</span></span>

### <span data-ttu-id="20e51-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20e51-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="20e51-112">Ta bort den skiss tilldelning som anges av namnet från det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="20e51-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="20e51-113">Cmdleten uppmanas att bekräfta innan kommandot körs.</span><span class="sxs-lookup"><span data-stu-id="20e51-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="20e51-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20e51-114">PARAMETERS</span></span>

### <span data-ttu-id="20e51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e51-115">-DefaultProfile</span></span>
<span data-ttu-id="20e51-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20e51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20e51-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20e51-117">-InputObject</span></span>
<span data-ttu-id="20e51-118">Objekt för skiss.</span><span class="sxs-lookup"><span data-stu-id="20e51-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20e51-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="20e51-119">-ManagementGroupId</span></span>
<span data-ttu-id="20e51-120">ID för hanterings gruppen där skiss tilldelningen har sparats.</span><span class="sxs-lookup"><span data-stu-id="20e51-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20e51-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="20e51-121">-Name</span></span>
<span data-ttu-id="20e51-122">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="20e51-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e51-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20e51-123">-PassThru</span></span>
<span data-ttu-id="20e51-124">När den är aktive rad returnerar cmdleten ett objekt som representerar den borttagna skiss uppgiften.</span><span class="sxs-lookup"><span data-stu-id="20e51-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="20e51-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="20e51-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20e51-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20e51-126">-SubscriptionId</span></span>
<span data-ttu-id="20e51-127">Abonnemangs-ID som skiss uppgiften distribueras till.</span><span class="sxs-lookup"><span data-stu-id="20e51-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20e51-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20e51-128">-Confirm</span></span>
<span data-ttu-id="20e51-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20e51-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20e51-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20e51-130">-WhatIf</span></span>
<span data-ttu-id="20e51-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20e51-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20e51-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20e51-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20e51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e51-133">CommonParameters</span></span>
<span data-ttu-id="20e51-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e51-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20e51-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e51-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20e51-136">INPUTS</span></span>

### <span data-ttu-id="20e51-137">System. String</span><span class="sxs-lookup"><span data-stu-id="20e51-137">System.String</span></span>

### <span data-ttu-id="20e51-138">Microsoft. Azure. commands. skissa. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="20e51-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="20e51-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20e51-139">OUTPUTS</span></span>

### <span data-ttu-id="20e51-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="20e51-140">System.Object</span></span>
## <span data-ttu-id="20e51-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20e51-141">NOTES</span></span>

## <span data-ttu-id="20e51-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20e51-142">RELATED LINKS</span></span>