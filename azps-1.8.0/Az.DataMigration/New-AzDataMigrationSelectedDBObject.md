---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 502e64ba553f20983bd437fea40d5247cf04548f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754259"
---
# <span data-ttu-id="6dd65-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="6dd65-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="6dd65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6dd65-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd65-103">Skapar ett databas objekt som innehåller information om käll-och mål databaserna för migrering.</span><span class="sxs-lookup"><span data-stu-id="6dd65-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="6dd65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6dd65-104">SYNTAX</span></span>

### <span data-ttu-id="6dd65-105">MigrateSqlServerSqlDb (standard)</span><span class="sxs-lookup"><span data-stu-id="6dd65-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dd65-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="6dd65-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dd65-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6dd65-107">DESCRIPTION</span></span>
<span data-ttu-id="6dd65-108">New-AzDataMigrationSelectedDB-cmdleten skapar ett databas informations objekt som innehåller information om käll-och mål databaser samt tabell mappningar för migrering.</span><span class="sxs-lookup"><span data-stu-id="6dd65-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="6dd65-109">Denna cmdlet kan användas som en parameter med New-AzDataMigrationTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd65-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="6dd65-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6dd65-110">EXAMPLES</span></span>

### <span data-ttu-id="6dd65-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6dd65-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="6dd65-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6dd65-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="6dd65-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6dd65-113">PARAMETERS</span></span>

### <span data-ttu-id="6dd65-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="6dd65-114">-BackupFileShare</span></span>
<span data-ttu-id="6dd65-115">Fil delning där käll serverns databasfiler för databasen ska säkerhets kopie ras.</span><span class="sxs-lookup"><span data-stu-id="6dd65-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="6dd65-116">Använd den här inställningen om du vill åsidosätta fil information för varje databas.</span><span class="sxs-lookup"><span data-stu-id="6dd65-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="6dd65-117">Använd fullkvalificerat domän namn för servern.</span><span class="sxs-lookup"><span data-stu-id="6dd65-117">Use fully qualified domain name for the server.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd65-118">-DefaultProfile</span></span>
<span data-ttu-id="6dd65-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd65-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dd65-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="6dd65-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="6dd65-121">Ange databas till ReadOnly före migrering</span><span class="sxs-lookup"><span data-stu-id="6dd65-121">Set Database to readonly before migration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd65-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="6dd65-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="6dd65-123">Ange typ av migrering till SQL Server till SQL DB migration.</span><span class="sxs-lookup"><span data-stu-id="6dd65-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd65-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="6dd65-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="6dd65-125">Ange migrering till SQL Server till MI-migrering för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="6dd65-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd65-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6dd65-126">-SourceDatabaseName</span></span>
<span data-ttu-id="6dd65-127">Namnet på käll databasen.</span><span class="sxs-lookup"><span data-stu-id="6dd65-127">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd65-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="6dd65-128">-TableMap</span></span>
<span data-ttu-id="6dd65-129">Mappning av källa till mål tabeller</span><span class="sxs-lookup"><span data-stu-id="6dd65-129">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd65-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6dd65-130">-TargetDatabaseName</span></span>
<span data-ttu-id="6dd65-131">Namnet på mål databasen.</span><span class="sxs-lookup"><span data-stu-id="6dd65-131">The name of the target database.</span></span>

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

### <span data-ttu-id="6dd65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd65-132">CommonParameters</span></span>
<span data-ttu-id="6dd65-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd65-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd65-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd65-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6dd65-135">INPUTS</span></span>

### <span data-ttu-id="6dd65-136">Microsoft. Azure. Management. DataMigration. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="6dd65-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="6dd65-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6dd65-137">OUTPUTS</span></span>

### <span data-ttu-id="6dd65-138">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="6dd65-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="6dd65-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6dd65-139">NOTES</span></span>

## <span data-ttu-id="6dd65-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6dd65-140">RELATED LINKS</span></span>
