---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 2525792f7696c69a03a926850eaea20267d14fbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103359"
---
# <span data-ttu-id="81985-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="81985-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="81985-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81985-102">SYNOPSIS</span></span>
<span data-ttu-id="81985-103">Tar bort en Synapse Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="81985-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="81985-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81985-104">SYNTAX</span></span>

### <span data-ttu-id="81985-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="81985-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81985-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81985-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81985-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81985-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81985-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81985-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81985-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81985-109">DESCRIPTION</span></span>
<span data-ttu-id="81985-110">Cmdleten **Remove-AzSynapseSqlPool** tar bort en Azure SYNAPSE Analytics SQL-databas permanent.</span><span class="sxs-lookup"><span data-stu-id="81985-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="81985-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81985-111">EXAMPLES</span></span>

### <span data-ttu-id="81985-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="81985-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="81985-113">Det här kommandot tar bort en Azure Synapse Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="81985-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="81985-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="81985-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="81985-115">Det här kommandot tar bort en Azure Synapse Analytics SQL-databas via pipeline.</span><span class="sxs-lookup"><span data-stu-id="81985-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="81985-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="81985-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="81985-117">Det här kommandot tar bort en Azure Synapse Analytics SQL-databas via pipeline.</span><span class="sxs-lookup"><span data-stu-id="81985-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="81985-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="81985-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="81985-119">Det här kommandot tar bort en Azure Synapse-BA-databas med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="81985-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="81985-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81985-120">PARAMETERS</span></span>

### <span data-ttu-id="81985-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81985-121">-AsJob</span></span>
<span data-ttu-id="81985-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="81985-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81985-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81985-123">-DefaultProfile</span></span>
<span data-ttu-id="81985-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81985-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81985-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81985-125">-InputObject</span></span>
<span data-ttu-id="81985-126">SQL-databasens indatavärde, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="81985-126">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81985-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="81985-127">-Name</span></span>
<span data-ttu-id="81985-128">Namn på Synapse SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="81985-128">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81985-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81985-129">-PassThru</span></span>
<span data-ttu-id="81985-130">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="81985-130">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="81985-131">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="81985-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="81985-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81985-132">-ResourceGroupName</span></span>
<span data-ttu-id="81985-133">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="81985-133">Resource group name.</span></span>

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

### <span data-ttu-id="81985-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81985-134">-ResourceId</span></span>
<span data-ttu-id="81985-135">Resource-ID för Synapse SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="81985-135">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81985-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="81985-136">-WorkspaceName</span></span>
<span data-ttu-id="81985-137">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="81985-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81985-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="81985-138">-WorkspaceObject</span></span>
<span data-ttu-id="81985-139">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="81985-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81985-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81985-140">-Confirm</span></span>
<span data-ttu-id="81985-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81985-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81985-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81985-142">-WhatIf</span></span>
<span data-ttu-id="81985-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81985-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81985-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81985-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81985-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81985-145">CommonParameters</span></span>
<span data-ttu-id="81985-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81985-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81985-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81985-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81985-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81985-148">INPUTS</span></span>

### <span data-ttu-id="81985-149">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="81985-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="81985-150">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="81985-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="81985-151">System. String</span><span class="sxs-lookup"><span data-stu-id="81985-151">System.String</span></span>

## <span data-ttu-id="81985-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81985-152">OUTPUTS</span></span>

### <span data-ttu-id="81985-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81985-153">System.Boolean</span></span>

## <span data-ttu-id="81985-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81985-154">NOTES</span></span>

## <span data-ttu-id="81985-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81985-155">RELATED LINKS</span></span>