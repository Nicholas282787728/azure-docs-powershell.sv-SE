---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 34f8b99ef4c8958415780fecb98c291d2845209d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088715"
---
# <span data-ttu-id="3cb93-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="3cb93-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="3cb93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3cb93-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb93-103">Ta bort en skiss tilldelning från ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="3cb93-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="3cb93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3cb93-104">SYNTAX</span></span>

### <span data-ttu-id="3cb93-105">DeleteBlueprintAssignmentByName (standard)</span><span class="sxs-lookup"><span data-stu-id="3cb93-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cb93-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="3cb93-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cb93-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3cb93-107">DESCRIPTION</span></span>
<span data-ttu-id="3cb93-108">Ta bort en skiss som har tilldelats till ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="3cb93-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="3cb93-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3cb93-109">EXAMPLES</span></span>

### <span data-ttu-id="3cb93-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3cb93-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="3cb93-111">Ta bort den skiss tilldelning som anges av namnet från det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3cb93-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="3cb93-112">Cmdleten uppmanas att bekräfta innan kommandot körs.</span><span class="sxs-lookup"><span data-stu-id="3cb93-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="3cb93-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3cb93-113">PARAMETERS</span></span>

### <span data-ttu-id="3cb93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb93-114">-DefaultProfile</span></span>
<span data-ttu-id="3cb93-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3cb93-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cb93-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cb93-116">-InputObject</span></span>
<span data-ttu-id="3cb93-117">Objekt för skiss.</span><span class="sxs-lookup"><span data-stu-id="3cb93-117">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3cb93-118">-Name</span></span>
<span data-ttu-id="3cb93-119">Namn på skiss tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="3cb93-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cb93-120">-PassThru</span></span>
<span data-ttu-id="3cb93-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3cb93-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3cb93-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3cb93-122">-SubscriptionId</span></span>
<span data-ttu-id="3cb93-123">Abonnemangs-ID som skiss uppgiften distribueras till.</span><span class="sxs-lookup"><span data-stu-id="3cb93-123">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb93-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3cb93-124">-Confirm</span></span>
<span data-ttu-id="3cb93-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3cb93-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb93-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb93-126">-WhatIf</span></span>
<span data-ttu-id="3cb93-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3cb93-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb93-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3cb93-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cb93-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb93-129">CommonParameters</span></span>
<span data-ttu-id="3cb93-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb93-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb93-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cb93-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb93-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3cb93-132">INPUTS</span></span>

### <span data-ttu-id="3cb93-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3cb93-133">System.String</span></span>

### <span data-ttu-id="3cb93-134">Microsoft. Azure. commands. skissa. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="3cb93-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="3cb93-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3cb93-135">OUTPUTS</span></span>

### <span data-ttu-id="3cb93-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="3cb93-136">System.Object</span></span>
## <span data-ttu-id="3cb93-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3cb93-137">NOTES</span></span>

## <span data-ttu-id="3cb93-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3cb93-138">RELATED LINKS</span></span>
