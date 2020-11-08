---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101125"
---
# <span data-ttu-id="0daac-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="0daac-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="0daac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0daac-102">SYNOPSIS</span></span>
<span data-ttu-id="0daac-103">Ta bort en skiss tilldelning från ett abonnemang eller en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="0daac-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="0daac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0daac-104">SYNTAX</span></span>

### <span data-ttu-id="0daac-105">BySubscriptionAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="0daac-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0daac-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="0daac-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0daac-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="0daac-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0daac-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0daac-108">DESCRIPTION</span></span>
<span data-ttu-id="0daac-109">Ta bort en skiss som har tilldelats till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="0daac-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="0daac-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0daac-110">EXAMPLES</span></span>

### <span data-ttu-id="0daac-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0daac-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="0daac-112">Ta bort den skiss tilldelning som anges av namnet från det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="0daac-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="0daac-113">Cmdleten uppmanas att bekräfta innan kommandot körs.</span><span class="sxs-lookup"><span data-stu-id="0daac-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="0daac-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0daac-114">PARAMETERS</span></span>

### <span data-ttu-id="0daac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0daac-115">-DefaultProfile</span></span>
<span data-ttu-id="0daac-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0daac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0daac-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0daac-117">-InputObject</span></span>
<span data-ttu-id="0daac-118">Objekt för skiss.</span><span class="sxs-lookup"><span data-stu-id="0daac-118">Blueprint assignment object.</span></span>

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

### <span data-ttu-id="0daac-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0daac-119">-ManagementGroupId</span></span>
<span data-ttu-id="0daac-120">ID för hanterings gruppen där skiss tilldelningen har sparats.</span><span class="sxs-lookup"><span data-stu-id="0daac-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="0daac-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0daac-121">-Name</span></span>
<span data-ttu-id="0daac-122">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="0daac-122">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="0daac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0daac-123">-PassThru</span></span>
<span data-ttu-id="0daac-124">När den är aktive rad returnerar cmdleten ett objekt som representerar den borttagna skiss uppgiften.</span><span class="sxs-lookup"><span data-stu-id="0daac-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="0daac-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0daac-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0daac-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0daac-126">-SubscriptionId</span></span>
<span data-ttu-id="0daac-127">Abonnemangs-ID som skiss uppgiften distribueras till.</span><span class="sxs-lookup"><span data-stu-id="0daac-127">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="0daac-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0daac-128">-Confirm</span></span>
<span data-ttu-id="0daac-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0daac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0daac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0daac-130">-WhatIf</span></span>
<span data-ttu-id="0daac-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0daac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0daac-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0daac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0daac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0daac-133">CommonParameters</span></span>
<span data-ttu-id="0daac-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0daac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0daac-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0daac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0daac-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0daac-136">INPUTS</span></span>

### <span data-ttu-id="0daac-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0daac-137">System.String</span></span>

### <span data-ttu-id="0daac-138">Microsoft. Azure. commands. skissa. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="0daac-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="0daac-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0daac-139">OUTPUTS</span></span>

### <span data-ttu-id="0daac-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="0daac-140">System.Object</span></span>
## <span data-ttu-id="0daac-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0daac-141">NOTES</span></span>

## <span data-ttu-id="0daac-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0daac-142">RELATED LINKS</span></span>
