---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 2dae942470dba8a36258ffb8c813e08c664f2e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323532"
---
# <span data-ttu-id="b1c13-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b1c13-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="b1c13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1c13-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c13-103">Återställer en Synapse för SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="b1c13-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b1c13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1c13-104">SYNTAX</span></span>

### <span data-ttu-id="b1c13-105">RestoreFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c13-105">RestoreFromBackupIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c13-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c13-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1c13-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c13-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1c13-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c13-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c13-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c13-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c13-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c13-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1c13-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c13-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c13-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c13-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1c13-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c13-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1c13-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1c13-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1c13-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1c13-115">DESCRIPTION</span></span>
<span data-ttu-id="b1c13-116">Med cmdleten **restore-AzSynapseSqlPool** återställs en Azure SYNAPSE-SQL-adresspool från en säkerhets kopia eller en återställnings punkt för en SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="b1c13-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="b1c13-117">Den återställda SQL-poolen skapas som en ny SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="b1c13-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="b1c13-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1c13-118">EXAMPLES</span></span>

### <span data-ttu-id="b1c13-119">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b1c13-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="b1c13-120">Det här kommandot skapar en Azure Synapse-SQL-pool genom att återställa den senaste säkerhets kopian av en SQL-pool i det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b1c13-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="b1c13-121">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b1c13-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="b1c13-122">Det här kommandot skapar en Azure Synapse SQL-pool genom att utnyttja en återställnings punkt från vilken SQL-pool som helst i det här abonnemanget för att återställa eller kopiera från ett tidigare tillstånd.</span><span class="sxs-lookup"><span data-stu-id="b1c13-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="b1c13-123">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="b1c13-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="b1c13-124">Det här kommandot skapar en Azure Synapse SQL-pool genom att återställa den senaste säkerhets kopian av en SQL-pool i den här prenumerationen med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b1c13-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="b1c13-125">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="b1c13-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="b1c13-126">Det här kommandot skapar en Azure Synapse SQL-pool genom att utnyttja en återställnings punkt från en SQL-pool i det här abonnemanget för att återställa eller kopiera från ett tidigare tillstånd med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b1c13-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="b1c13-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1c13-127">PARAMETERS</span></span>

### <span data-ttu-id="b1c13-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1c13-128">-AsJob</span></span>
<span data-ttu-id="b1c13-129">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b1c13-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1c13-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c13-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="b1c13-131">Namnet på den resurs grupp som bakcup SQL-poolnamn ska skapa från.</span><span class="sxs-lookup"><span data-stu-id="b1c13-131">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="b1c13-132">-BackupResourceId</span></span>
<span data-ttu-id="b1c13-133">Resurs-ID för säkerhets kopia av SQL-gruppobjekt som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="b1c13-133">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="b1c13-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="b1c13-135">Namnet på SQL-bakcup som du vill skapa från.</span><span class="sxs-lookup"><span data-stu-id="b1c13-135">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="b1c13-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="b1c13-137">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1c13-137">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b1c13-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="b1c13-139">Synapse arbets ytans namn för bakcup SQL-poolnamn att skapa från.</span><span class="sxs-lookup"><span data-stu-id="b1c13-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c13-140">-DefaultProfile</span></span>
<span data-ttu-id="b1c13-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c13-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1c13-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="b1c13-142">-FromBackup</span></span>
<span data-ttu-id="b1c13-143">Indikerar att återställa från den senaste säkerhets kopian av en SQL-pool i det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b1c13-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="b1c13-144">-FromRestorePoint</span></span>
<span data-ttu-id="b1c13-145">Visar att en återställnings punkt från en SQL-pool i det här abonnemanget återskapas eller kopieras från ett tidigare tillstånd.</span><span class="sxs-lookup"><span data-stu-id="b1c13-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="b1c13-146">-Name</span></span>
<span data-ttu-id="b1c13-147">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="b1c13-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="b1c13-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="b1c13-148">-PerformanceLevel</span></span>
<span data-ttu-id="b1c13-149">SQL Service Tier och prestanda nivå som ska kopplas till SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="b1c13-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="b1c13-150">Till exempel DW2000c.</span><span class="sxs-lookup"><span data-stu-id="b1c13-150">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c13-151">-ResourceGroupName</span></span>
<span data-ttu-id="b1c13-152">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b1c13-152">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="b1c13-153">-RestorePoint</span></span>
<span data-ttu-id="b1c13-154">Ögonblicks bild för återställning.</span><span class="sxs-lookup"><span data-stu-id="b1c13-154">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c13-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="b1c13-156">Namnet på den resurs grupp som du vill skapa från.</span><span class="sxs-lookup"><span data-stu-id="b1c13-156">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b1c13-157">-SourceResourceId</span></span>
<span data-ttu-id="b1c13-158">Resurs-ID för käll-SQL-poolnamn att skapa från.</span><span class="sxs-lookup"><span data-stu-id="b1c13-158">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="b1c13-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="b1c13-160">Namnet på käll-SQL-adresspoolen att skapa från.</span><span class="sxs-lookup"><span data-stu-id="b1c13-160">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="b1c13-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="b1c13-162">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1c13-162">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b1c13-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="b1c13-164">Synapse arbets ytans namn för källan för SQL-pooler att skapa från.</span><span class="sxs-lookup"><span data-stu-id="b1c13-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-165">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b1c13-165">-Tag</span></span>
<span data-ttu-id="b1c13-166">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="b1c13-166">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="b1c13-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b1c13-167">-WorkspaceName</span></span>
<span data-ttu-id="b1c13-168">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="b1c13-168">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-169">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b1c13-169">-WorkspaceObject</span></span>
<span data-ttu-id="b1c13-170">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1c13-170">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c13-171">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b1c13-171">-Confirm</span></span>
<span data-ttu-id="b1c13-172">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b1c13-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1c13-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c13-173">-WhatIf</span></span>
<span data-ttu-id="b1c13-174">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b1c13-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c13-175">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b1c13-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1c13-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c13-176">CommonParameters</span></span>
<span data-ttu-id="b1c13-177">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c13-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c13-178">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1c13-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c13-179">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1c13-179">INPUTS</span></span>

### <span data-ttu-id="b1c13-180">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b1c13-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b1c13-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1c13-181">OUTPUTS</span></span>

### <span data-ttu-id="b1c13-182">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b1c13-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="b1c13-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1c13-183">NOTES</span></span>

## <span data-ttu-id="b1c13-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1c13-184">RELATED LINKS</span></span>