---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: ceeb33615748b7cf11c13441399bbae6a934a56f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424128"
---
# <span data-ttu-id="59c72-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="59c72-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="59c72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59c72-102">SYNOPSIS</span></span>
<span data-ttu-id="59c72-103">Tar bort en återställnings punkt för Synapse Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="59c72-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="59c72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59c72-104">SYNTAX</span></span>

### <span data-ttu-id="59c72-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="59c72-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59c72-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59c72-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59c72-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59c72-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59c72-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59c72-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59c72-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59c72-109">DESCRIPTION</span></span>
<span data-ttu-id="59c72-110">Cmdleten **Remove-AzSynapseSqlPoolRestorePoint** tar bort en återställnings punkt för Azure SYNAPSE Analytics SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="59c72-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="59c72-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59c72-111">EXAMPLES</span></span>

### <span data-ttu-id="59c72-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59c72-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="59c72-113">Det här kommandot tar bort en återställnings punkt för Azure Synapse Analytics SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="59c72-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="59c72-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="59c72-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="59c72-115">Det här kommandot tar bort en återställnings punkt för Azure Synapse Analytics SQL-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="59c72-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="59c72-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="59c72-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="59c72-117">Det här kommandot tar bort en återställnings punkt för Azure Synapse Analytics SQL-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="59c72-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="59c72-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="59c72-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="59c72-119">Det här kommandot tar bort en återställnings punkt för Azure Synapse Analytics SQL-pool med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="59c72-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="59c72-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59c72-120">PARAMETERS</span></span>

### <span data-ttu-id="59c72-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59c72-121">-AsJob</span></span>
<span data-ttu-id="59c72-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="59c72-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59c72-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c72-123">-DefaultProfile</span></span>
<span data-ttu-id="59c72-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59c72-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c72-125">-Force</span><span class="sxs-lookup"><span data-stu-id="59c72-125">-Force</span></span>
<span data-ttu-id="59c72-126">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="59c72-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="59c72-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59c72-127">-InputObject</span></span>
<span data-ttu-id="59c72-128">Tids objekt för återställning av återställnings punkter för SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="59c72-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59c72-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59c72-129">-PassThru</span></span>
<span data-ttu-id="59c72-130">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="59c72-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="59c72-131">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="59c72-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="59c72-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c72-132">-ResourceGroupName</span></span>
<span data-ttu-id="59c72-133">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="59c72-133">Resource group name.</span></span>

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

### <span data-ttu-id="59c72-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59c72-134">-ResourceId</span></span>
<span data-ttu-id="59c72-135">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="59c72-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="59c72-136">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="59c72-136">-RestorePointCreationDate</span></span>
<span data-ttu-id="59c72-137">Namn på Synapse SQL återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="59c72-137">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c72-138">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="59c72-138">-SqlPoolName</span></span>
<span data-ttu-id="59c72-139">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="59c72-139">Name of Synapse Sql pool.</span></span>

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

### <span data-ttu-id="59c72-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="59c72-140">-SqlPoolObject</span></span>
<span data-ttu-id="59c72-141">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="59c72-141">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59c72-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="59c72-142">-WorkspaceName</span></span>
<span data-ttu-id="59c72-143">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="59c72-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="59c72-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59c72-144">-Confirm</span></span>
<span data-ttu-id="59c72-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59c72-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59c72-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59c72-146">-WhatIf</span></span>
<span data-ttu-id="59c72-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59c72-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59c72-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59c72-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59c72-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c72-149">CommonParameters</span></span>
<span data-ttu-id="59c72-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c72-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c72-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59c72-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c72-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59c72-152">INPUTS</span></span>

### <span data-ttu-id="59c72-153">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="59c72-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="59c72-154">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="59c72-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="59c72-155">Microsoft. Azure. commands. Synapse. Models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="59c72-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="59c72-156">System. String</span><span class="sxs-lookup"><span data-stu-id="59c72-156">System.String</span></span>

## <span data-ttu-id="59c72-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59c72-157">OUTPUTS</span></span>

### <span data-ttu-id="59c72-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59c72-158">System.Boolean</span></span>

## <span data-ttu-id="59c72-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59c72-159">NOTES</span></span>

## <span data-ttu-id="59c72-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59c72-160">RELATED LINKS</span></span>
