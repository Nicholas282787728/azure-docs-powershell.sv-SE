---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: fbdca80b33dd15e34a958cb63a41377b400d03ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523923"
---
# <span data-ttu-id="efe85-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="efe85-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="efe85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="efe85-102">SYNOPSIS</span></span>
<span data-ttu-id="efe85-103">Tar bort en Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="efe85-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="efe85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="efe85-104">SYNTAX</span></span>

### <span data-ttu-id="efe85-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="efe85-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe85-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe85-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efe85-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efe85-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efe85-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="efe85-108">DESCRIPTION</span></span>
<span data-ttu-id="efe85-109">Cmdleten **Remove-AzSynapseWorkspace** tar bort en Azure Synapse Analytics-arbetsyta permanent.</span><span class="sxs-lookup"><span data-stu-id="efe85-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="efe85-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="efe85-110">EXAMPLES</span></span>

### <span data-ttu-id="efe85-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="efe85-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="efe85-112">Det här kommandot tar bort en Azure Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="efe85-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="efe85-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="efe85-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="efe85-114">Det här kommandot tar bort en Azure Synapse-arbetsyta via pipeline.</span><span class="sxs-lookup"><span data-stu-id="efe85-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="efe85-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="efe85-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="efe85-116">Det här kommandot tar bort en Azure Synapse-arbetsyta via pipeline med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="efe85-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="efe85-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="efe85-117">PARAMETERS</span></span>

### <span data-ttu-id="efe85-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efe85-118">-AsJob</span></span>
<span data-ttu-id="efe85-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="efe85-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efe85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe85-120">-DefaultProfile</span></span>
<span data-ttu-id="efe85-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="efe85-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efe85-122">-Force</span><span class="sxs-lookup"><span data-stu-id="efe85-122">-Force</span></span>
<span data-ttu-id="efe85-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="efe85-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="efe85-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efe85-124">-InputObject</span></span>
<span data-ttu-id="efe85-125">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="efe85-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efe85-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="efe85-126">-Name</span></span>
<span data-ttu-id="efe85-127">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="efe85-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe85-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efe85-128">-PassThru</span></span>
<span data-ttu-id="efe85-129">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="efe85-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="efe85-130">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="efe85-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="efe85-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efe85-131">-ResourceGroupName</span></span>
<span data-ttu-id="efe85-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="efe85-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe85-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efe85-133">-ResourceId</span></span>
<span data-ttu-id="efe85-134">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="efe85-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe85-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="efe85-135">-Confirm</span></span>
<span data-ttu-id="efe85-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="efe85-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efe85-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efe85-137">-WhatIf</span></span>
<span data-ttu-id="efe85-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="efe85-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efe85-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="efe85-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efe85-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe85-140">CommonParameters</span></span>
<span data-ttu-id="efe85-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe85-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe85-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efe85-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe85-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="efe85-143">INPUTS</span></span>

### <span data-ttu-id="efe85-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="efe85-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="efe85-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="efe85-145">OUTPUTS</span></span>

### <span data-ttu-id="efe85-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="efe85-146">System.Boolean</span></span>

## <span data-ttu-id="efe85-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="efe85-147">NOTES</span></span>

## <span data-ttu-id="efe85-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="efe85-148">RELATED LINKS</span></span>
