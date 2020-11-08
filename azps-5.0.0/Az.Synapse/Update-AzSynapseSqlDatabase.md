---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269389"
---
# <span data-ttu-id="91c98-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91c98-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="91c98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91c98-102">SYNOPSIS</span></span>
<span data-ttu-id="91c98-103">Uppdaterar en Synapse Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="91c98-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="91c98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91c98-104">SYNTAX</span></span>

### <span data-ttu-id="91c98-105">UpdateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="91c98-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91c98-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91c98-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91c98-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91c98-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91c98-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91c98-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91c98-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91c98-109">DESCRIPTION</span></span>
<span data-ttu-id="91c98-110">Cmdleten **Update-AzSynapseSqlDatabase** uppdaterar en Azure SYNAPSE Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="91c98-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="91c98-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91c98-111">EXAMPLES</span></span>

### <span data-ttu-id="91c98-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="91c98-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="91c98-113">Det här kommandot uppdaterar en Azure Synapse Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="91c98-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="91c98-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91c98-114">PARAMETERS</span></span>

### <span data-ttu-id="91c98-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91c98-115">-AsJob</span></span>
<span data-ttu-id="91c98-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="91c98-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91c98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c98-117">-DefaultProfile</span></span>
<span data-ttu-id="91c98-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91c98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91c98-119">-InputObject</span></span>
<span data-ttu-id="91c98-120">SQL-databasens indatavärde, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="91c98-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91c98-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="91c98-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="91c98-122">Anger den maximala storleken på databasen i byte.</span><span class="sxs-lookup"><span data-stu-id="91c98-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c98-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="91c98-123">-Name</span></span>
<span data-ttu-id="91c98-124">Namn på Synapse SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="91c98-124">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91c98-125">-PassThru</span></span>
<span data-ttu-id="91c98-126">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="91c98-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="91c98-127">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="91c98-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="91c98-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c98-128">-ResourceGroupName</span></span>
<span data-ttu-id="91c98-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="91c98-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c98-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91c98-130">-ResourceId</span></span>
<span data-ttu-id="91c98-131">Resource-ID för Synapse SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="91c98-131">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c98-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="91c98-132">-Tag</span></span>
<span data-ttu-id="91c98-133">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="91c98-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="91c98-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="91c98-134">-WorkspaceName</span></span>
<span data-ttu-id="91c98-135">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="91c98-135">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c98-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="91c98-136">-WorkspaceObject</span></span>
<span data-ttu-id="91c98-137">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="91c98-137">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91c98-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="91c98-138">-Confirm</span></span>
<span data-ttu-id="91c98-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="91c98-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c98-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c98-140">-WhatIf</span></span>
<span data-ttu-id="91c98-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="91c98-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91c98-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="91c98-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c98-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c98-143">CommonParameters</span></span>
<span data-ttu-id="91c98-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c98-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c98-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91c98-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c98-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91c98-146">INPUTS</span></span>

### <span data-ttu-id="91c98-147">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="91c98-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="91c98-148">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91c98-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="91c98-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91c98-149">OUTPUTS</span></span>

### <span data-ttu-id="91c98-150">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="91c98-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="91c98-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91c98-151">NOTES</span></span>

## <span data-ttu-id="91c98-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91c98-152">RELATED LINKS</span></span>
