---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 93c4c5c1fa269414b80001f9fd24f1a79c5ed4de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101845"
---
# <span data-ttu-id="8c183-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8c183-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="8c183-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c183-102">SYNOPSIS</span></span>
<span data-ttu-id="8c183-103">Anger en säkerhets kopierings princip för kortvarigt bevarande.</span><span class="sxs-lookup"><span data-stu-id="8c183-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="8c183-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c183-104">SYNTAX</span></span>

### <span data-ttu-id="8c183-105">PolicyByResourceInstanceDatabaseSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8c183-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c183-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8c183-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c183-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8c183-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c183-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c183-108">DESCRIPTION</span></span>
<span data-ttu-id="8c183-109">Cmdleten **set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** hämtar den kortsiktiga bevarande principen som är registrerad för den här databasen.</span><span class="sxs-lookup"><span data-stu-id="8c183-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="8c183-110">Policyn är den bevarande period, i dagar, för säkerhets kopior för återställning vid tillfället.</span><span class="sxs-lookup"><span data-stu-id="8c183-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="8c183-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c183-111">EXAMPLES</span></span>

### <span data-ttu-id="8c183-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8c183-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="8c183-113">Det här kommandot anger den kortsiktiga bevarande principen för database01 till 35 dagar.</span><span class="sxs-lookup"><span data-stu-id="8c183-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="8c183-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8c183-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="8c183-115">Det här kommandot anger den kortsiktiga bevarande principen för database01 till 35 dagar via överföring i ett databas objekt.</span><span class="sxs-lookup"><span data-stu-id="8c183-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="8c183-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8c183-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="8c183-117">Det här kommandot anger den kortsiktiga bevarande principen för alla borttagna databaser med namnet DB1 via överföring i ett borttaget databas objekt.</span><span class="sxs-lookup"><span data-stu-id="8c183-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="8c183-118">Obs! Du kan bara minska bevarande perioden för borttagna databaser.</span><span class="sxs-lookup"><span data-stu-id="8c183-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="8c183-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c183-119">PARAMETERS</span></span>

### <span data-ttu-id="8c183-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8c183-120">-DatabaseName</span></span>
<span data-ttu-id="8c183-121">Namnet på den Azure SQL instance-databas som du vill hämta säkerhets kopior för.</span><span class="sxs-lookup"><span data-stu-id="8c183-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c183-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c183-122">-DefaultProfile</span></span>
<span data-ttu-id="8c183-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c183-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c183-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="8c183-124">-DeletionDate</span></span>
<span data-ttu-id="8c183-125">Borttagnings datumet för Azure SQL instance-databasen att hämta säkerhets kopior för, med millisekunder precision (till exempel 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="8c183-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c183-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c183-126">-InputObject</span></span>
<span data-ttu-id="8c183-127">Det levande eller borttagna databasobjektet för att hämta eller ange principen.</span><span class="sxs-lookup"><span data-stu-id="8c183-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c183-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8c183-128">-InstanceName</span></span>
<span data-ttu-id="8c183-129">Namnet på den SQL-hanterade instans i Azure som databasen finns i.</span><span class="sxs-lookup"><span data-stu-id="8c183-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c183-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c183-130">-ResourceGroupName</span></span>
<span data-ttu-id="8c183-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8c183-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c183-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c183-132">-ResourceId</span></span>
<span data-ttu-id="8c183-133">Den kortsiktiga resurs-ID för bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="8c183-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c183-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="8c183-134">-RetentionDays</span></span>
<span data-ttu-id="8c183-135">Dagars lagrings tid för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="8c183-135">Days of backup retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c183-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c183-136">-Confirm</span></span>
<span data-ttu-id="8c183-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c183-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c183-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c183-138">-WhatIf</span></span>
<span data-ttu-id="8c183-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c183-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c183-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c183-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c183-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c183-141">CommonParameters</span></span>
<span data-ttu-id="8c183-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c183-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c183-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c183-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c183-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c183-144">INPUTS</span></span>

### <span data-ttu-id="8c183-145">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="8c183-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="8c183-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8c183-146">System.String</span></span>

## <span data-ttu-id="8c183-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c183-147">OUTPUTS</span></span>

### <span data-ttu-id="8c183-148">Microsoft. Azure. commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="8c183-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="8c183-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c183-149">NOTES</span></span>

## <span data-ttu-id="8c183-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c183-150">RELATED LINKS</span></span>
