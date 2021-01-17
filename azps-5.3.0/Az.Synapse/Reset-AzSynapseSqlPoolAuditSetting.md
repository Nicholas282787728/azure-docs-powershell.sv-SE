---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 77299e9424f0a194776b1114146b76ef2be3329f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424075"
---
# <span data-ttu-id="dac5f-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="dac5f-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="dac5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dac5f-102">SYNOPSIS</span></span>
<span data-ttu-id="dac5f-103">Tar bort gransknings inställningar för en Azure Synapse-BA SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="dac5f-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="dac5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dac5f-104">SYNTAX</span></span>

### <span data-ttu-id="dac5f-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dac5f-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dac5f-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac5f-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dac5f-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac5f-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dac5f-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dac5f-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dac5f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dac5f-109">DESCRIPTION</span></span>
<span data-ttu-id="dac5f-110">Cmdleten **Reset-AzSynapseSqlPoolAuditSetting** tar bort gransknings inställningarna för en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="dac5f-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="dac5f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dac5f-111">EXAMPLES</span></span>

### <span data-ttu-id="dac5f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dac5f-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="dac5f-113">Det här kommandot tar bort gransknings inställningarna för en SQL-pool med namnet ContosoSqlPool i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="dac5f-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="dac5f-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="dac5f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="dac5f-115">Det här kommandot tar bort gransknings inställningarna för en SQL-pool som heter ContosoSqlPool i arbets ytans ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="dac5f-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="dac5f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dac5f-116">PARAMETERS</span></span>

### <span data-ttu-id="dac5f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dac5f-117">-AsJob</span></span>
<span data-ttu-id="dac5f-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="dac5f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dac5f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac5f-119">-DefaultProfile</span></span>
<span data-ttu-id="dac5f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dac5f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dac5f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dac5f-121">-InputObject</span></span>
<span data-ttu-id="dac5f-122">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="dac5f-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dac5f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="dac5f-123">-Name</span></span>
<span data-ttu-id="dac5f-124">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="dac5f-124">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac5f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dac5f-125">-PassThru</span></span>
<span data-ttu-id="dac5f-126">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="dac5f-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="dac5f-127">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="dac5f-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="dac5f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dac5f-128">-ResourceGroupName</span></span>
<span data-ttu-id="dac5f-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="dac5f-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac5f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dac5f-130">-ResourceId</span></span>
<span data-ttu-id="dac5f-131">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="dac5f-131">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac5f-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dac5f-132">-WorkspaceName</span></span>
<span data-ttu-id="dac5f-133">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="dac5f-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac5f-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dac5f-134">-WorkspaceObject</span></span>
<span data-ttu-id="dac5f-135">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="dac5f-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dac5f-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dac5f-136">-Confirm</span></span>
<span data-ttu-id="dac5f-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dac5f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dac5f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dac5f-138">-WhatIf</span></span>
<span data-ttu-id="dac5f-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dac5f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dac5f-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dac5f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dac5f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac5f-141">CommonParameters</span></span>
<span data-ttu-id="dac5f-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dac5f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac5f-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dac5f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac5f-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dac5f-144">INPUTS</span></span>

### <span data-ttu-id="dac5f-145">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dac5f-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dac5f-146">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="dac5f-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="dac5f-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dac5f-147">OUTPUTS</span></span>

### <span data-ttu-id="dac5f-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dac5f-148">System.Boolean</span></span>

## <span data-ttu-id="dac5f-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dac5f-149">NOTES</span></span>

## <span data-ttu-id="dac5f-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dac5f-150">RELATED LINKS</span></span>
