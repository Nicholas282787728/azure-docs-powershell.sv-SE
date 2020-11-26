---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262889"
---
# <span data-ttu-id="56418-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="56418-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="56418-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56418-102">SYNOPSIS</span></span>
<span data-ttu-id="56418-103">Avbryter en Synapse för SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="56418-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="56418-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56418-104">SYNTAX</span></span>

### <span data-ttu-id="56418-105">SuspendByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="56418-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56418-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56418-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56418-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56418-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56418-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56418-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56418-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56418-109">DESCRIPTION</span></span>
<span data-ttu-id="56418-110">Cmdleten **suspend-AzSynapseSqlPool** inaktive ras en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="56418-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="56418-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56418-111">EXAMPLES</span></span>

### <span data-ttu-id="56418-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="56418-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="56418-113">Det här kommandot gör att en aktiv Azure Synapse-BA-pool stoppas.</span><span class="sxs-lookup"><span data-stu-id="56418-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="56418-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56418-114">PARAMETERS</span></span>

### <span data-ttu-id="56418-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56418-115">-AsJob</span></span>
<span data-ttu-id="56418-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="56418-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56418-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56418-117">-DefaultProfile</span></span>
<span data-ttu-id="56418-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56418-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56418-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56418-119">-InputObject</span></span>
<span data-ttu-id="56418-120">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="56418-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56418-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="56418-121">-Name</span></span>
<span data-ttu-id="56418-122">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="56418-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56418-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56418-123">-PassThru</span></span>
<span data-ttu-id="56418-124">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="56418-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="56418-125">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="56418-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="56418-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56418-126">-ResourceGroupName</span></span>
<span data-ttu-id="56418-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="56418-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56418-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56418-128">-ResourceId</span></span>
<span data-ttu-id="56418-129">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="56418-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56418-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="56418-130">-WorkspaceName</span></span>
<span data-ttu-id="56418-131">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="56418-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56418-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="56418-132">-WorkspaceObject</span></span>
<span data-ttu-id="56418-133">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="56418-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56418-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56418-134">-Confirm</span></span>
<span data-ttu-id="56418-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56418-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56418-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56418-136">-WhatIf</span></span>
<span data-ttu-id="56418-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56418-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56418-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56418-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56418-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56418-139">CommonParameters</span></span>
<span data-ttu-id="56418-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56418-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56418-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56418-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56418-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56418-142">INPUTS</span></span>

### <span data-ttu-id="56418-143">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="56418-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="56418-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="56418-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="56418-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56418-145">OUTPUTS</span></span>

### <span data-ttu-id="56418-146">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="56418-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="56418-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56418-147">NOTES</span></span>

## <span data-ttu-id="56418-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56418-148">RELATED LINKS</span></span>