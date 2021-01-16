---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408787"
---
# <span data-ttu-id="d3f34-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="d3f34-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="d3f34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3f34-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f34-103">Skapar en ny återställnings punkt i en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="d3f34-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d3f34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3f34-104">SYNTAX</span></span>

### <span data-ttu-id="d3f34-105">CreateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d3f34-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3f34-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f34-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3f34-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f34-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f34-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f34-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f34-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3f34-109">DESCRIPTION</span></span>
<span data-ttu-id="d3f34-110">Cmdleten **New-AzSynapseSqlPoolRestorePoint** skapar en ny återställnings punkt som en Azure SYNAPSE Analytics SQL-pool kan återställas från.</span><span class="sxs-lookup"><span data-stu-id="d3f34-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="d3f34-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3f34-111">EXAMPLES</span></span>

### <span data-ttu-id="d3f34-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d3f34-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="d3f34-113">Det här kommandot skapar en återställnings punkt för SQL-poolen med namnet ContosoSqlPool i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d3f34-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="d3f34-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3f34-114">PARAMETERS</span></span>

### <span data-ttu-id="d3f34-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3f34-115">-AsJob</span></span>
<span data-ttu-id="d3f34-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d3f34-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3f34-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f34-117">-DefaultProfile</span></span>
<span data-ttu-id="d3f34-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f34-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3f34-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3f34-119">-InputObject</span></span>
<span data-ttu-id="d3f34-120">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3f34-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f34-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3f34-121">-Name</span></span>
<span data-ttu-id="d3f34-122">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="d3f34-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f34-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f34-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3f34-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d3f34-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f34-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f34-125">-ResourceId</span></span>
<span data-ttu-id="d3f34-126">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="d3f34-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f34-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="d3f34-127">-RestorePointLabel</span></span>
<span data-ttu-id="d3f34-128">Etiketten vi associerar en återställnings punkt med är kanske inte unik.</span><span class="sxs-lookup"><span data-stu-id="d3f34-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="d3f34-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d3f34-129">-WorkspaceName</span></span>
<span data-ttu-id="d3f34-130">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d3f34-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f34-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d3f34-131">-WorkspaceObject</span></span>
<span data-ttu-id="d3f34-132">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d3f34-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f34-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3f34-133">-Confirm</span></span>
<span data-ttu-id="d3f34-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3f34-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f34-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f34-135">-WhatIf</span></span>
<span data-ttu-id="d3f34-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3f34-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f34-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3f34-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f34-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f34-138">CommonParameters</span></span>
<span data-ttu-id="d3f34-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f34-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f34-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3f34-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f34-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3f34-141">INPUTS</span></span>

### <span data-ttu-id="d3f34-142">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d3f34-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d3f34-143">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d3f34-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d3f34-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3f34-144">OUTPUTS</span></span>

### <span data-ttu-id="d3f34-145">Microsoft. Azure. commands. Synapse. Models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="d3f34-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="d3f34-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3f34-146">NOTES</span></span>

## <span data-ttu-id="d3f34-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3f34-147">RELATED LINKS</span></span>
