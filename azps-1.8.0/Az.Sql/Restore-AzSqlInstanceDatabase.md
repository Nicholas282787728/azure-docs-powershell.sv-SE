---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: d513c186f621329510582c9cd69a64461f9e068f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746538"
---
# <span data-ttu-id="e63d2-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e63d2-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="e63d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e63d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e63d2-103">Återställer en Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="e63d2-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="e63d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e63d2-104">SYNTAX</span></span>

### <span data-ttu-id="e63d2-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="e63d2-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e63d2-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e63d2-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e63d2-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e63d2-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e63d2-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="e63d2-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e63d2-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="e63d2-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e63d2-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e63d2-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e63d2-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e63d2-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e63d2-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e63d2-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e63d2-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e63d2-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e63d2-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e63d2-114">DESCRIPTION</span></span>
<span data-ttu-id="e63d2-115">Cmdleten **restore-AzSqlInstanceDatabase** återställer en instans databas från en Geo-redundant säkerhets kopiering eller en tidpunkt i en Live-databas.</span><span class="sxs-lookup"><span data-stu-id="e63d2-115">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup or a point in time in a live database.</span></span>
<span data-ttu-id="e63d2-116">Den återställda databasen skapas som en ny instans databas.</span><span class="sxs-lookup"><span data-stu-id="e63d2-116">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="e63d2-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e63d2-117">EXAMPLES</span></span>

### <span data-ttu-id="e63d2-118">Exempel 1: Återställ en instans databas från en tidpunkt</span><span class="sxs-lookup"><span data-stu-id="e63d2-118">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="e63d2-119">Kommandot återställer instans databasens Database01 från den angivna säkerhets kopian under tiden till instans databasen med namnet Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="e63d2-119">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="e63d2-120">Exempel 2: återställa en instans databas från en tidpunkt till en annan instans i en annan resurs grupp</span><span class="sxs-lookup"><span data-stu-id="e63d2-120">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="e63d2-121">Kommandot återställer instans databasen Database01 på instans managedInstance1 i resurs grupp ResourceGroup01 från den angivna säkerhets kopian under tiden till instans databasen med namnet Database01_restored på instans managedInstance2 på resurs grupp ResourceGroup02.</span><span class="sxs-lookup"><span data-stu-id="e63d2-121">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="e63d2-122">Exempel 3: Geo-Restore en instans databas</span><span class="sxs-lookup"><span data-stu-id="e63d2-122">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="e63d2-123">Det första kommandot får den geo-redundanta säkerhets kopieringen för databasen som heter Database01 och lagrar den sedan i $GeoBackup variabel.</span><span class="sxs-lookup"><span data-stu-id="e63d2-123">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="e63d2-124">Det andra kommandot återställer säkerhets kopian i $GeoBackup till instans databasen med namnet Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="e63d2-124">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

## <span data-ttu-id="e63d2-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e63d2-125">PARAMETERS</span></span>

### <span data-ttu-id="e63d2-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e63d2-126">-AsJob</span></span>
<span data-ttu-id="e63d2-127">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e63d2-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e63d2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e63d2-128">-DefaultProfile</span></span>
<span data-ttu-id="e63d2-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e63d2-129">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="e63d2-130">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="e63d2-130">-FromGeoBackup</span></span>
<span data-ttu-id="e63d2-131">Återställ från en geo-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="e63d2-131">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-132">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="e63d2-132">-FromPointInTimeBackup</span></span>
<span data-ttu-id="e63d2-133">Återställ från en säkerhets kopia under tiden.</span><span class="sxs-lookup"><span data-stu-id="e63d2-133">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-134">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="e63d2-134">-GeoBackupObject</span></span>
<span data-ttu-id="e63d2-135">Det återställnings bara instans databas objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="e63d2-135">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e63d2-136">-InputObject</span></span>
<span data-ttu-id="e63d2-137">Instans databas objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="e63d2-137">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-138">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e63d2-138">-InstanceName</span></span>
<span data-ttu-id="e63d2-139">Instans namnet.</span><span class="sxs-lookup"><span data-stu-id="e63d2-139">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="e63d2-140">-Name</span></span>
<span data-ttu-id="e63d2-141">Instans databas namn som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="e63d2-141">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-142">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="e63d2-142">-PointInTime</span></span>
<span data-ttu-id="e63d2-143">Tidpunkten då databasen återställs till.</span><span class="sxs-lookup"><span data-stu-id="e63d2-143">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e63d2-144">-ResourceGroupName</span></span>
<span data-ttu-id="e63d2-145">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e63d2-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e63d2-146">-ResourceId</span></span>
<span data-ttu-id="e63d2-147">Resurs-ID för instans databas objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="e63d2-147">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-148">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e63d2-148">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="e63d2-149">Namnet på mål instans databasen som ska återställas till.</span><span class="sxs-lookup"><span data-stu-id="e63d2-149">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="e63d2-150">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="e63d2-150">-TargetInstanceName</span></span>
<span data-ttu-id="e63d2-151">Namnet på mål instansen som ska återställas till.</span><span class="sxs-lookup"><span data-stu-id="e63d2-151">The name of the target instance to restore to.</span></span>
<span data-ttu-id="e63d2-152">Om det inte anges är mål förekomsten samma som käll instansen.</span><span class="sxs-lookup"><span data-stu-id="e63d2-152">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-153">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e63d2-153">-TargetResourceGroupName</span></span>
<span data-ttu-id="e63d2-154">Namnet på mål resurs gruppen som du vill återställa till.</span><span class="sxs-lookup"><span data-stu-id="e63d2-154">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="e63d2-155">Om det inte anges är mål resurs gruppen samma som käll resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e63d2-155">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63d2-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e63d2-156">-Confirm</span></span>
<span data-ttu-id="e63d2-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e63d2-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e63d2-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e63d2-158">-WhatIf</span></span>
<span data-ttu-id="e63d2-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e63d2-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e63d2-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e63d2-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e63d2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e63d2-161">CommonParameters</span></span>
<span data-ttu-id="e63d2-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e63d2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e63d2-163">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e63d2-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e63d2-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e63d2-164">INPUTS</span></span>

### <span data-ttu-id="e63d2-165">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e63d2-165">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="e63d2-166">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e63d2-166">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="e63d2-167">System. String</span><span class="sxs-lookup"><span data-stu-id="e63d2-167">System.String</span></span>

## <span data-ttu-id="e63d2-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e63d2-168">OUTPUTS</span></span>

### <span data-ttu-id="e63d2-169">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e63d2-169">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e63d2-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e63d2-170">NOTES</span></span>

## <span data-ttu-id="e63d2-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e63d2-171">RELATED LINKS</span></span>
