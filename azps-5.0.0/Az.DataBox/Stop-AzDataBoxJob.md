---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321256"
---
# <span data-ttu-id="81624-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="81624-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="81624-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81624-102">SYNOPSIS</span></span>
<span data-ttu-id="81624-103">Avbryter ett pågående data jobb om jobbet är avbrutet.</span><span class="sxs-lookup"><span data-stu-id="81624-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="81624-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81624-104">SYNTAX</span></span>

### <span data-ttu-id="81624-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="81624-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81624-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81624-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81624-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81624-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81624-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81624-108">DESCRIPTION</span></span>
<span data-ttu-id="81624-109">Cmdleten **Stop-AzDataBoxJob** används för att avbryta ett Datalist jobb.</span><span class="sxs-lookup"><span data-stu-id="81624-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="81624-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81624-110">EXAMPLES</span></span>

### <span data-ttu-id="81624-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="81624-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="81624-112">Avbryter det angivna datamappen</span><span class="sxs-lookup"><span data-stu-id="81624-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="81624-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="81624-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="81624-114">Avbryter framtvingad utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="81624-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="81624-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="81624-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="81624-116">Avbryter det angivna datamappen</span><span class="sxs-lookup"><span data-stu-id="81624-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="81624-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81624-117">PARAMETERS</span></span>

### <span data-ttu-id="81624-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81624-118">-DefaultProfile</span></span>
<span data-ttu-id="81624-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81624-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81624-120">-Force</span><span class="sxs-lookup"><span data-stu-id="81624-120">-Force</span></span>
<span data-ttu-id="81624-121">Tvinga stopp utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="81624-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="81624-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81624-122">-InputObject</span></span>
<span data-ttu-id="81624-123">InputObject av typen PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="81624-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="81624-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="81624-124">-Name</span></span>
<span data-ttu-id="81624-125">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="81624-125">Databox Job Name</span></span>

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

### <span data-ttu-id="81624-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81624-126">-PassThru</span></span>
<span data-ttu-id="81624-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="81624-127">PassThru</span></span>

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

### <span data-ttu-id="81624-128">-Orsak</span><span class="sxs-lookup"><span data-stu-id="81624-128">-Reason</span></span>
<span data-ttu-id="81624-129">Orsak till annullering</span><span class="sxs-lookup"><span data-stu-id="81624-129">Reason For Cancellation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81624-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81624-130">-ResourceGroupName</span></span>
<span data-ttu-id="81624-131">Namn på jobb i en datastapel</span><span class="sxs-lookup"><span data-stu-id="81624-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="81624-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81624-132">-ResourceId</span></span>
<span data-ttu-id="81624-133">Resurs-ID för datasamtal</span><span class="sxs-lookup"><span data-stu-id="81624-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="81624-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81624-134">-Confirm</span></span>
<span data-ttu-id="81624-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81624-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81624-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81624-136">-WhatIf</span></span>
<span data-ttu-id="81624-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81624-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81624-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81624-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81624-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81624-139">CommonParameters</span></span>
<span data-ttu-id="81624-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81624-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81624-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81624-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81624-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81624-142">INPUTS</span></span>

### <span data-ttu-id="81624-143">System. String</span><span class="sxs-lookup"><span data-stu-id="81624-143">System.String</span></span>

## <span data-ttu-id="81624-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81624-144">OUTPUTS</span></span>

### <span data-ttu-id="81624-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="81624-145">System.Void</span></span>

## <span data-ttu-id="81624-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81624-146">NOTES</span></span>

## <span data-ttu-id="81624-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81624-147">RELATED LINKS</span></span>