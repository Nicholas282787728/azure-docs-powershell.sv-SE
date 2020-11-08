---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262400"
---
# <span data-ttu-id="43e4c-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="43e4c-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="43e4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="43e4c-103">Skapar en Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="43e4c-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="43e4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43e4c-104">SYNTAX</span></span>

### <span data-ttu-id="43e4c-105">CreateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="43e4c-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e4c-106">CreateFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-106">CreateFromBackupIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e4c-107">CreateFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-107">CreateFromBackupIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e4c-108">CreateFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-108">CreateFromBackupNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43e4c-109">CreateFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-109">CreateFromBackupNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43e4c-110">CreateFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-110">CreateFromBackupInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e4c-111">CreateFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-111">CreateFromRestorePointIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43e4c-112">CreateFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-112">CreateFromRestorePointIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43e4c-113">CreateFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-113">CreateFromRestorePointNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e4c-114">CreateFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-114">CreateFromRestorePointNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43e4c-115">CreateFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-115">CreateFromRestorePointInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43e4c-116">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43e4c-116">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43e4c-117">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43e4c-117">DESCRIPTION</span></span>
<span data-ttu-id="43e4c-118">Cmdleten **New-AzSynapseSqlPool** skapar en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="43e4c-118">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="43e4c-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43e4c-119">EXAMPLES</span></span>

### <span data-ttu-id="43e4c-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="43e4c-120">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="43e4c-121">Det här kommandot skapar en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="43e4c-121">This command creates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="43e4c-122">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="43e4c-122">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="43e4c-123">Det här kommandot skapar en Azure Synapse-SQL-pool genom att återställa den senaste säkerhets kopian av en SQL-pool i det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="43e4c-123">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="43e4c-124">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="43e4c-124">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="43e4c-125">Det här kommandot skapar en Azure Synapse SQL-pool genom att utnyttja en återställnings punkt från vilken SQL-pool som helst i det här abonnemanget för att återställa eller kopiera från ett tidigare tillstånd.</span><span class="sxs-lookup"><span data-stu-id="43e4c-125">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="43e4c-126">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="43e4c-126">Example 4</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="43e4c-127">Det här kommandot skapar en Azure Synapse SQL-pool genom att återställa den senaste säkerhets kopian av en SQL-pool i den här prenumerationen med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="43e4c-127">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="43e4c-128">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="43e4c-128">Example 5</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="43e4c-129">Det här kommandot skapar en Azure Synapse SQL-pool genom att utnyttja en återställnings punkt från en SQL-pool i det här abonnemanget för att återställa eller kopiera från ett tidigare tillstånd med resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="43e4c-129">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="43e4c-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43e4c-130">PARAMETERS</span></span>

### <span data-ttu-id="43e4c-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43e4c-131">-AsJob</span></span>
<span data-ttu-id="43e4c-132">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="43e4c-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43e4c-133">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e4c-133">-BackupResourceGroupName</span></span>
<span data-ttu-id="43e4c-134">Namnet på den resurs grupp som bakcup SQL-poolnamn ska skapa från.</span><span class="sxs-lookup"><span data-stu-id="43e4c-134">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-135">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="43e4c-135">-BackupResourceId</span></span>
<span data-ttu-id="43e4c-136">Resurs-ID för säkerhets kopia av SQL-gruppobjekt som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="43e4c-136">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-137">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="43e4c-137">-BackupSqlPoolName</span></span>
<span data-ttu-id="43e4c-138">Namnet på SQL-bakcup som du vill skapa från.</span><span class="sxs-lookup"><span data-stu-id="43e4c-138">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-139">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="43e4c-139">-BackupSqlPoolObject</span></span>
<span data-ttu-id="43e4c-140">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="43e4c-140">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-141">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="43e4c-141">-BackupWorkspaceName</span></span>
<span data-ttu-id="43e4c-142">Synapse arbets ytans namn för bakcup SQL-poolnamn att skapa från.</span><span class="sxs-lookup"><span data-stu-id="43e4c-142">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-143">-Sortering</span><span class="sxs-lookup"><span data-stu-id="43e4c-143">-Collation</span></span>
<span data-ttu-id="43e4c-144">Sortering definierar regler som sorterar och jämför data och kan inte ändras efter att SQL-poolen har skapats.</span><span class="sxs-lookup"><span data-stu-id="43e4c-144">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="43e4c-145">Standard sorteringen är SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="43e4c-145">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e4c-146">-DefaultProfile</span></span>
<span data-ttu-id="43e4c-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43e4c-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43e4c-148">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="43e4c-148">-FromBackup</span></span>
<span data-ttu-id="43e4c-149">Indikerar att återställa från den senaste säkerhets kopian av en SQL-pool i det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="43e4c-149">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-150">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="43e4c-150">-FromRestorePoint</span></span>
<span data-ttu-id="43e4c-151">Visar att en återställnings punkt från en SQL-pool i det här abonnemanget återskapas eller kopieras från ett tidigare tillstånd.</span><span class="sxs-lookup"><span data-stu-id="43e4c-151">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-152">-Namn</span><span class="sxs-lookup"><span data-stu-id="43e4c-152">-Name</span></span>
<span data-ttu-id="43e4c-153">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="43e4c-153">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="43e4c-154">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="43e4c-154">-PerformanceLevel</span></span>
<span data-ttu-id="43e4c-155">SQL Service Tier och prestanda nivå som ska kopplas till SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="43e4c-155">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="43e4c-156">Till exempel DW2000c.</span><span class="sxs-lookup"><span data-stu-id="43e4c-156">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e4c-157">-ResourceGroupName</span></span>
<span data-ttu-id="43e4c-158">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="43e4c-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-159">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="43e4c-159">-RestorePoint</span></span>
<span data-ttu-id="43e4c-160">Ögonblicks bild för återställning.</span><span class="sxs-lookup"><span data-stu-id="43e4c-160">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-161">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e4c-161">-SourceResourceGroupName</span></span>
<span data-ttu-id="43e4c-162">Namnet på den resurs grupp som du vill skapa från.</span><span class="sxs-lookup"><span data-stu-id="43e4c-162">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-163">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="43e4c-163">-SourceResourceId</span></span>
<span data-ttu-id="43e4c-164">Resurs-ID för käll-SQL-poolnamn att skapa från.</span><span class="sxs-lookup"><span data-stu-id="43e4c-164">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-165">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="43e4c-165">-SourceSqlPoolName</span></span>
<span data-ttu-id="43e4c-166">Namnet på käll-SQL-adresspoolen att skapa från.</span><span class="sxs-lookup"><span data-stu-id="43e4c-166">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-167">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="43e4c-167">-SourceSqlPoolObject</span></span>
<span data-ttu-id="43e4c-168">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="43e4c-168">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-169">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="43e4c-169">-SourceWorkspaceName</span></span>
<span data-ttu-id="43e4c-170">Synapse arbets ytans namn för källan för SQL-pooler att skapa från.</span><span class="sxs-lookup"><span data-stu-id="43e4c-170">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-171">-Tagg</span><span class="sxs-lookup"><span data-stu-id="43e4c-171">-Tag</span></span>
<span data-ttu-id="43e4c-172">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="43e4c-172">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="43e4c-173">-Version</span><span class="sxs-lookup"><span data-stu-id="43e4c-173">-Version</span></span>
<span data-ttu-id="43e4c-174">Version av Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="43e4c-174">Version of Synapse SQL pool.</span></span> <span data-ttu-id="43e4c-175">Till exempel 2 eller 3.</span><span class="sxs-lookup"><span data-stu-id="43e4c-175">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="43e4c-176">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="43e4c-176">-WorkspaceName</span></span>
<span data-ttu-id="43e4c-177">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="43e4c-177">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-178">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="43e4c-178">-WorkspaceObject</span></span>
<span data-ttu-id="43e4c-179">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="43e4c-179">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43e4c-180">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43e4c-180">-Confirm</span></span>
<span data-ttu-id="43e4c-181">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43e4c-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43e4c-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43e4c-182">-WhatIf</span></span>
<span data-ttu-id="43e4c-183">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43e4c-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43e4c-184">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43e4c-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43e4c-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e4c-185">CommonParameters</span></span>
<span data-ttu-id="43e4c-186">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43e4c-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e4c-187">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43e4c-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e4c-188">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43e4c-188">INPUTS</span></span>

### <span data-ttu-id="43e4c-189">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="43e4c-189">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="43e4c-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43e4c-190">OUTPUTS</span></span>

### <span data-ttu-id="43e4c-191">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="43e4c-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="43e4c-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43e4c-192">NOTES</span></span>

## <span data-ttu-id="43e4c-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43e4c-193">RELATED LINKS</span></span>
