---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 61fe76eba8d1f8faf0ab45d0a24f56a8dabf3641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584844"
---
# <span data-ttu-id="8e776-101">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="8e776-101">Restore-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="8e776-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e776-102">SYNOPSIS</span></span>
<span data-ttu-id="8e776-103">Återställer en Azure SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="8e776-103">Restores an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e776-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e776-104">SYNTAX</span></span>

### <span data-ttu-id="8e776-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="8e776-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e776-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="8e776-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e776-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="8e776-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e776-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="8e776-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e776-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="8e776-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e776-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="8e776-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e776-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e776-111">DESCRIPTION</span></span>
<span data-ttu-id="8e776-112">Cmdleten **restore-AzureRmSqlInstanceDatabase** återställer en instans databas från en tidpunkt i en Live-databas.</span><span class="sxs-lookup"><span data-stu-id="8e776-112">The **Restore-AzureRmSqlInstanceDatabase** cmdlet restores an instance database from a point in time in a live database.</span></span>
<span data-ttu-id="8e776-113">Den återställda databasen skapas som en ny instans databas.</span><span class="sxs-lookup"><span data-stu-id="8e776-113">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="8e776-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e776-114">EXAMPLES</span></span>

### <span data-ttu-id="8e776-115">Exempel 1: återställa en instans databas från en tidpunkt</span><span class="sxs-lookup"><span data-stu-id="8e776-115">Example 1: Restore a instance database from a point in time</span></span>
```
PS C:\> Restore-AzureRmSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="8e776-116">Kommandot återställer instans databasens Database01 från den angivna säkerhets kopian under tiden till instans databasen med namnet Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="8e776-116">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="8e776-117">Exempel 2: återställa en instans databas från en tidpunkt till en annan instans i en annan resurs grupp</span><span class="sxs-lookup"><span data-stu-id="8e776-117">Example 2: Restore a instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="8e776-118">Kommandot återställer instans databasen Database01 på instans managedInstance1 i resurs grupp ResourceGroup01 från den angivna säkerhets kopian under tiden till instans databasen med namnet Database01_restored på instans managedInstance2 på resurs grupp ResourceGroup02.</span><span class="sxs-lookup"><span data-stu-id="8e776-118">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

## <span data-ttu-id="8e776-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e776-119">PARAMETERS</span></span>

### <span data-ttu-id="8e776-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e776-120">-AsJob</span></span>
<span data-ttu-id="8e776-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8e776-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e776-122">-DefaultProfile</span></span>
<span data-ttu-id="8e776-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e776-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-124">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="8e776-124">-FromPointInTimeBackup</span></span>
<span data-ttu-id="8e776-125">Återställ från en säkerhets kopia under tiden.</span><span class="sxs-lookup"><span data-stu-id="8e776-125">Restore from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e776-126">-InputObject</span></span>
<span data-ttu-id="8e776-127">Instans databas objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="8e776-127">The Instance Database object to restore</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8e776-128">-InstanceName</span></span>
<span data-ttu-id="8e776-129">Instans namnet.</span><span class="sxs-lookup"><span data-stu-id="8e776-129">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e776-130">-Name</span></span>
<span data-ttu-id="8e776-131">Instans databas namn som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="8e776-131">The instance database name to restore.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="8e776-132">-PointInTime</span></span>
<span data-ttu-id="8e776-133">Tidpunkten då databasen återställs till.</span><span class="sxs-lookup"><span data-stu-id="8e776-133">The point in time to restore the database to.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e776-134">-ResourceGroupName</span></span>
<span data-ttu-id="8e776-135">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8e776-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e776-136">-ResourceId</span></span>
<span data-ttu-id="8e776-137">Resurs-ID för instans databas objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="8e776-137">The resource id of Instance Database object to restore</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-138">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8e776-138">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="8e776-139">Namnet på mål instans databasen som ska återställas till.</span><span class="sxs-lookup"><span data-stu-id="8e776-139">The name of the target instance database to restore to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-140">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="8e776-140">-TargetInstanceName</span></span>
<span data-ttu-id="8e776-141">Namnet på mål instansen som ska återställas till.</span><span class="sxs-lookup"><span data-stu-id="8e776-141">The name of the target instance to restore to.</span></span>
<span data-ttu-id="8e776-142">Om det inte anges är mål förekomsten samma som käll instansen.</span><span class="sxs-lookup"><span data-stu-id="8e776-142">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-143">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e776-143">-TargetResourceGroupName</span></span>
<span data-ttu-id="8e776-144">Namnet på mål resurs gruppen som du vill återställa till.</span><span class="sxs-lookup"><span data-stu-id="8e776-144">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="8e776-145">Om det inte anges är mål resurs gruppen samma som käll resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8e776-145">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e776-146">-Confirm</span></span>
<span data-ttu-id="8e776-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e776-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e776-148">-WhatIf</span></span>
<span data-ttu-id="8e776-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e776-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e776-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e776-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e776-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e776-151">CommonParameters</span></span>
<span data-ttu-id="8e776-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e776-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e776-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e776-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e776-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e776-154">INPUTS</span></span>

### <span data-ttu-id="8e776-155">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8e776-155">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="8e776-156">System. String</span><span class="sxs-lookup"><span data-stu-id="8e776-156">System.String</span></span>

## <span data-ttu-id="8e776-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e776-157">OUTPUTS</span></span>

### <span data-ttu-id="8e776-158">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8e776-158">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="8e776-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e776-159">NOTES</span></span>

## <span data-ttu-id="8e776-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e776-160">RELATED LINKS</span></span>
