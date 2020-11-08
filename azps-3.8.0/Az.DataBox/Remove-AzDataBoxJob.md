---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 545b99168d421fd9839d42bc8eb0af198dc48042
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089890"
---
# <span data-ttu-id="a8875-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="a8875-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="a8875-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8875-102">SYNOPSIS</span></span>
<span data-ttu-id="a8875-103">Tar bort datamappen</span><span class="sxs-lookup"><span data-stu-id="a8875-103">Deletes the databox job</span></span>

## <span data-ttu-id="a8875-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8875-104">SYNTAX</span></span>

### <span data-ttu-id="a8875-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a8875-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8875-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8875-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8875-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8875-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8875-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8875-108">DESCRIPTION</span></span>
<span data-ttu-id="a8875-109">Cmdleten **Remove-AzDataBoxJob** används för att ta bort ett slutfört data-jobb från listan över datavyer.</span><span class="sxs-lookup"><span data-stu-id="a8875-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="a8875-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8875-110">EXAMPLES</span></span>

### <span data-ttu-id="a8875-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a8875-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="a8875-112">Tar bort det angivna datamappen</span><span class="sxs-lookup"><span data-stu-id="a8875-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="a8875-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a8875-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="a8875-114">Tar bort det angivna inmatnings jobbet för data</span><span class="sxs-lookup"><span data-stu-id="a8875-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="a8875-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a8875-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="a8875-116">Tar bort det angivna datamappen</span><span class="sxs-lookup"><span data-stu-id="a8875-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="a8875-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8875-117">PARAMETERS</span></span>

### <span data-ttu-id="a8875-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8875-118">-DefaultProfile</span></span>
<span data-ttu-id="a8875-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8875-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8875-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a8875-120">-Force</span></span>
<span data-ttu-id="a8875-121">Tvinga borttagning utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="a8875-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="a8875-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8875-122">-InputObject</span></span>
<span data-ttu-id="a8875-123">InputObject av typen PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="a8875-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8875-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8875-124">-Name</span></span>
<span data-ttu-id="a8875-125">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="a8875-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8875-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8875-126">-PassThru</span></span>
<span data-ttu-id="a8875-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="a8875-127">PassThru</span></span>

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

### <span data-ttu-id="a8875-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8875-128">-ResourceGroupName</span></span>
<span data-ttu-id="a8875-129">Namn på jobb i en datastapel</span><span class="sxs-lookup"><span data-stu-id="a8875-129">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8875-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8875-130">-ResourceId</span></span>
<span data-ttu-id="a8875-131">Resurs-ID för datastapel</span><span class="sxs-lookup"><span data-stu-id="a8875-131">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8875-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8875-132">-Confirm</span></span>
<span data-ttu-id="a8875-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8875-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8875-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8875-134">-WhatIf</span></span>
<span data-ttu-id="a8875-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8875-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8875-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8875-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8875-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8875-137">CommonParameters</span></span>
<span data-ttu-id="a8875-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8875-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8875-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8875-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8875-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8875-140">INPUTS</span></span>

### <span data-ttu-id="a8875-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a8875-141">System.String</span></span>

## <span data-ttu-id="a8875-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8875-142">OUTPUTS</span></span>

### <span data-ttu-id="a8875-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="a8875-143">System.Void</span></span>

## <span data-ttu-id="a8875-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8875-144">NOTES</span></span>

## <span data-ttu-id="a8875-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8875-145">RELATED LINKS</span></span>
