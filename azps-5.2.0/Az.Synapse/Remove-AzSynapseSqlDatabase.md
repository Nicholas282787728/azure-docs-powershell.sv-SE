---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 4951fbe707dbae8c1fdff34e828e468a2d3168bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395904"
---
# <span data-ttu-id="11d98-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="11d98-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="11d98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11d98-102">SYNOPSIS</span></span>
<span data-ttu-id="11d98-103">Tar bort en Synapse Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="11d98-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="11d98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11d98-104">SYNTAX</span></span>

### <span data-ttu-id="11d98-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="11d98-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d98-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d98-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d98-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d98-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d98-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d98-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11d98-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11d98-109">DESCRIPTION</span></span>
<span data-ttu-id="11d98-110">Cmdleten **Remove-AzSynapseSqlPool** tar bort en Azure SYNAPSE Analytics SQL-databas permanent.</span><span class="sxs-lookup"><span data-stu-id="11d98-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="11d98-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11d98-111">EXAMPLES</span></span>

### <span data-ttu-id="11d98-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="11d98-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="11d98-113">Det här kommandot tar bort en Azure Synapse Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="11d98-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="11d98-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="11d98-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="11d98-115">Det här kommandot tar bort en Azure Synapse Analytics SQL-databas via pipeline.</span><span class="sxs-lookup"><span data-stu-id="11d98-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="11d98-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="11d98-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="11d98-117">Det här kommandot tar bort en Azure Synapse Analytics SQL-databas via pipeline.</span><span class="sxs-lookup"><span data-stu-id="11d98-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="11d98-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="11d98-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="11d98-119">Det här kommandot tar bort en Azure Synapse-BA-databas med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="11d98-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="11d98-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11d98-120">PARAMETERS</span></span>

### <span data-ttu-id="11d98-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11d98-121">-AsJob</span></span>
<span data-ttu-id="11d98-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="11d98-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11d98-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d98-123">-DefaultProfile</span></span>
<span data-ttu-id="11d98-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11d98-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d98-125">-Force</span><span class="sxs-lookup"><span data-stu-id="11d98-125">-Force</span></span>
<span data-ttu-id="11d98-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="11d98-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="11d98-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11d98-127">-InputObject</span></span>
<span data-ttu-id="11d98-128">SQL-databasens indatavärde, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="11d98-128">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="11d98-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="11d98-129">-Name</span></span>
<span data-ttu-id="11d98-130">Namn på Synapse SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="11d98-130">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="11d98-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11d98-131">-PassThru</span></span>
<span data-ttu-id="11d98-132">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="11d98-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="11d98-133">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="11d98-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="11d98-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d98-134">-ResourceGroupName</span></span>
<span data-ttu-id="11d98-135">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="11d98-135">Resource group name.</span></span>

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

### <span data-ttu-id="11d98-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11d98-136">-ResourceId</span></span>
<span data-ttu-id="11d98-137">Resource-ID för Synapse SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="11d98-137">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="11d98-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11d98-138">-WorkspaceName</span></span>
<span data-ttu-id="11d98-139">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="11d98-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="11d98-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="11d98-140">-WorkspaceObject</span></span>
<span data-ttu-id="11d98-141">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="11d98-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="11d98-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11d98-142">-Confirm</span></span>
<span data-ttu-id="11d98-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11d98-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d98-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d98-144">-WhatIf</span></span>
<span data-ttu-id="11d98-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11d98-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11d98-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11d98-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11d98-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d98-147">CommonParameters</span></span>
<span data-ttu-id="11d98-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11d98-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d98-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11d98-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d98-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11d98-150">INPUTS</span></span>

### <span data-ttu-id="11d98-151">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="11d98-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="11d98-152">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="11d98-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="11d98-153">System. String</span><span class="sxs-lookup"><span data-stu-id="11d98-153">System.String</span></span>

## <span data-ttu-id="11d98-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11d98-154">OUTPUTS</span></span>

### <span data-ttu-id="11d98-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11d98-155">System.Boolean</span></span>

## <span data-ttu-id="11d98-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11d98-156">NOTES</span></span>

## <span data-ttu-id="11d98-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11d98-157">RELATED LINKS</span></span>
