---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: bb653669ff15dad78ce3cec10f406aa099808e55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424251"
---
# <span data-ttu-id="e9bc3-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e9bc3-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e9bc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bc3-103">Skapar en Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e9bc3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9bc3-104">SYNTAX</span></span>

### <span data-ttu-id="e9bc3-105">CreateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e9bc3-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9bc3-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9bc3-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9bc3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9bc3-107">DESCRIPTION</span></span>
<span data-ttu-id="e9bc3-108">Cmdleten **New-AzSynapseSqlPool** skapar en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e9bc3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9bc3-109">EXAMPLES</span></span>

### <span data-ttu-id="e9bc3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e9bc3-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="e9bc3-111">Det här kommandot skapar en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e9bc3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9bc3-112">PARAMETERS</span></span>

### <span data-ttu-id="e9bc3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9bc3-113">-AsJob</span></span>
<span data-ttu-id="e9bc3-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e9bc3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9bc3-115">-Sortering</span><span class="sxs-lookup"><span data-stu-id="e9bc3-115">-Collation</span></span>
<span data-ttu-id="e9bc3-116">Sortering definierar regler som sorterar och jämför data och kan inte ändras efter att SQL-poolen har skapats.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="e9bc3-117">Standard sorteringen är SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bc3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bc3-118">-DefaultProfile</span></span>
<span data-ttu-id="e9bc3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9bc3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9bc3-120">-Name</span></span>
<span data-ttu-id="e9bc3-121">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bc3-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="e9bc3-122">-PerformanceLevel</span></span>
<span data-ttu-id="e9bc3-123">SQL Service Tier och prestanda nivå som ska kopplas till SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="e9bc3-124">Till exempel DW2000c.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="e9bc3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9bc3-125">-ResourceGroupName</span></span>
<span data-ttu-id="e9bc3-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-126">Resource group name.</span></span>

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

### <span data-ttu-id="e9bc3-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e9bc3-127">-Tag</span></span>
<span data-ttu-id="e9bc3-128">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-128">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bc3-129">-Version</span><span class="sxs-lookup"><span data-stu-id="e9bc3-129">-Version</span></span>
<span data-ttu-id="e9bc3-130">Version av Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="e9bc3-131">Till exempel 2 eller 3.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-131">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bc3-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9bc3-132">-WorkspaceName</span></span>
<span data-ttu-id="e9bc3-133">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9bc3-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e9bc3-134">-WorkspaceObject</span></span>
<span data-ttu-id="e9bc3-135">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9bc3-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9bc3-136">-Confirm</span></span>
<span data-ttu-id="e9bc3-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9bc3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9bc3-138">-WhatIf</span></span>
<span data-ttu-id="e9bc3-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9bc3-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9bc3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bc3-141">CommonParameters</span></span>
<span data-ttu-id="e9bc3-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bc3-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9bc3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bc3-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9bc3-144">INPUTS</span></span>

### <span data-ttu-id="e9bc3-145">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e9bc3-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e9bc3-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9bc3-146">OUTPUTS</span></span>

### <span data-ttu-id="e9bc3-147">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e9bc3-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e9bc3-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9bc3-148">NOTES</span></span>

## <span data-ttu-id="e9bc3-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9bc3-149">RELATED LINKS</span></span>
