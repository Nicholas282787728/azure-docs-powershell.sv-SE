---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420856"
---
# <span data-ttu-id="4418c-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="4418c-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="4418c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4418c-102">SYNOPSIS</span></span>
<span data-ttu-id="4418c-103">Skapar en databas information som är specifik för det synkroniseringsförsök som ska användas för en migrering.</span><span class="sxs-lookup"><span data-stu-id="4418c-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="4418c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4418c-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4418c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4418c-105">DESCRIPTION</span></span>

<span data-ttu-id="4418c-106">New-AzDataMigrationSyncSelectedDB-cmdleten skapar ett specifikt databas informations objekt för det synkroniseringsförsök som innehåller information om käll-och mål databaser.</span><span class="sxs-lookup"><span data-stu-id="4418c-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="4418c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4418c-107">EXAMPLES</span></span>

### <span data-ttu-id="4418c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4418c-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="4418c-109">I det här exemplet skapas ett metadataobjekt för databas som beskriver migrerade inställningar för $DatabaseName till databas $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="4418c-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="4418c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4418c-110">PARAMETERS</span></span>

### <span data-ttu-id="4418c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4418c-111">-DefaultProfile</span></span>
<span data-ttu-id="4418c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4418c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4418c-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="4418c-113">-MigrationSetting</span></span>
<span data-ttu-id="4418c-114">Inställningar för migrering som styr migreringens beteende</span><span class="sxs-lookup"><span data-stu-id="4418c-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="4418c-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4418c-115">-SchemaName</span></span>
<span data-ttu-id="4418c-116">Schema namn som ska migreras</span><span class="sxs-lookup"><span data-stu-id="4418c-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="4418c-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4418c-117">-SourceDatabaseName</span></span>
<span data-ttu-id="4418c-118">Namnet på käll databasen.</span><span class="sxs-lookup"><span data-stu-id="4418c-118">The name of the source database.</span></span>

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

### <span data-ttu-id="4418c-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="4418c-119">-SourceSetting</span></span>
<span data-ttu-id="4418c-120">Käll inställningar för att justera källa för slut punkts migrering</span><span class="sxs-lookup"><span data-stu-id="4418c-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="4418c-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="4418c-121">-TableMap</span></span>
<span data-ttu-id="4418c-122">Mappning av källa till mål tabeller</span><span class="sxs-lookup"><span data-stu-id="4418c-122">Mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4418c-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4418c-123">-TargetDatabaseName</span></span>
<span data-ttu-id="4418c-124">Namnet på mål databasen</span><span class="sxs-lookup"><span data-stu-id="4418c-124">The name of the target database</span></span>

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

### <span data-ttu-id="4418c-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="4418c-125">-TargetSetting</span></span>
<span data-ttu-id="4418c-126">Mål inställningar för att finjustera beteendet för migrering av mål slut punkter</span><span class="sxs-lookup"><span data-stu-id="4418c-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="4418c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4418c-127">CommonParameters</span></span>
<span data-ttu-id="4418c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4418c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4418c-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4418c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4418c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4418c-130">INPUTS</span></span>

### <span data-ttu-id="4418c-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="4418c-131">None</span></span>

## <span data-ttu-id="4418c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4418c-132">OUTPUTS</span></span>

### <span data-ttu-id="4418c-133">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="4418c-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="4418c-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4418c-134">NOTES</span></span>

## <span data-ttu-id="4418c-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4418c-135">RELATED LINKS</span></span>
