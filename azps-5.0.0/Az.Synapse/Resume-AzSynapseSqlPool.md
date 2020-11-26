---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ea27b23174d9555e4153dc5ef8c4d053ef5a49b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323519"
---
# <span data-ttu-id="03bdb-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="03bdb-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="03bdb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="03bdb-103">Återupptar en Synapse för SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="03bdb-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="03bdb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03bdb-104">SYNTAX</span></span>

### <span data-ttu-id="03bdb-105">ResumeByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="03bdb-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03bdb-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03bdb-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03bdb-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03bdb-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03bdb-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03bdb-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03bdb-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03bdb-109">DESCRIPTION</span></span>
<span data-ttu-id="03bdb-110">Cmdleten **Resume-AzSynapseSqlPool** återupptar en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="03bdb-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="03bdb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03bdb-111">EXAMPLES</span></span>

### <span data-ttu-id="03bdb-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="03bdb-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="03bdb-113">Det här kommandot återupptar en inaktiverad Azure Synapse Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="03bdb-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="03bdb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03bdb-114">PARAMETERS</span></span>

### <span data-ttu-id="03bdb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03bdb-115">-AsJob</span></span>
<span data-ttu-id="03bdb-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="03bdb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03bdb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bdb-117">-DefaultProfile</span></span>
<span data-ttu-id="03bdb-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03bdb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03bdb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03bdb-119">-InputObject</span></span>
<span data-ttu-id="03bdb-120">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="03bdb-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03bdb-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="03bdb-121">-Name</span></span>
<span data-ttu-id="03bdb-122">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="03bdb-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03bdb-123">-PassThru</span></span>
<span data-ttu-id="03bdb-124">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="03bdb-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="03bdb-125">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="03bdb-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="03bdb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03bdb-126">-ResourceGroupName</span></span>
<span data-ttu-id="03bdb-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="03bdb-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03bdb-128">-ResourceId</span></span>
<span data-ttu-id="03bdb-129">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="03bdb-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdb-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="03bdb-130">-WorkspaceName</span></span>
<span data-ttu-id="03bdb-131">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="03bdb-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdb-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="03bdb-132">-WorkspaceObject</span></span>
<span data-ttu-id="03bdb-133">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="03bdb-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03bdb-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="03bdb-134">-Confirm</span></span>
<span data-ttu-id="03bdb-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03bdb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03bdb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03bdb-136">-WhatIf</span></span>
<span data-ttu-id="03bdb-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="03bdb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03bdb-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="03bdb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03bdb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bdb-139">CommonParameters</span></span>
<span data-ttu-id="03bdb-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03bdb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bdb-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03bdb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bdb-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03bdb-142">INPUTS</span></span>

### <span data-ttu-id="03bdb-143">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="03bdb-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="03bdb-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="03bdb-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="03bdb-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03bdb-145">OUTPUTS</span></span>

### <span data-ttu-id="03bdb-146">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="03bdb-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="03bdb-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03bdb-147">NOTES</span></span>

## <span data-ttu-id="03bdb-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03bdb-148">RELATED LINKS</span></span>