---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576544"
---
# <span data-ttu-id="8a8e3-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span><span class="sxs-lookup"><span data-stu-id="8a8e3-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span></span>

## <span data-ttu-id="8a8e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a8e3-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8e3-103">Skapar ett MigrateSqlServerSqlDbDatabaseInput-objekt som innehåller information om käll-och mål databaserna för migrering.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-103">Creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a8e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a8e3-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="8a8e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a8e3-105">DESCRIPTION</span></span>
<span data-ttu-id="8a8e3-106">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB-cmdleten skapar ett MigrateSqlServerSqlDbDatabaseInput-objekt som innehåller information om käll-och mål databaser samt tabell mappningar för migrering.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-106">The New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="8a8e3-107">Denna cmdlet kan användas som en parameter med New-AzureRmDataMigrationTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-107">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="8a8e3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a8e3-108">EXAMPLES</span></span>

### <span data-ttu-id="8a8e3-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a8e3-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

<span data-ttu-id="8a8e3-110">I exemplet ovan skapas MigrateSqlServerSqlDbDatabaseInput-objektet för att migrera **AdventureWorks2016** -databasen till en SQL Azure-databas med samma namn.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-110">The above example creates MigrateSqlServerSqlDbDatabaseInput object for migrating the **AdventureWorks2016** database to a SQL Azure database with the same name.</span></span>

## <span data-ttu-id="8a8e3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a8e3-111">PARAMETERS</span></span>

### <span data-ttu-id="8a8e3-112">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a8e3-112">-Confirm</span></span>
<span data-ttu-id="8a8e3-113">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a8e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8e3-114">-DefaultProfile</span></span>
<span data-ttu-id="8a8e3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a8e3-116">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="8a8e3-116">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="8a8e3-117">Ange databas till ReadOnly före migrering</span><span class="sxs-lookup"><span data-stu-id="8a8e3-117">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="8a8e3-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a8e3-118">-Name</span></span>
<span data-ttu-id="8a8e3-119">Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-119">The name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8e3-120">-TableMap</span><span class="sxs-lookup"><span data-stu-id="8a8e3-120">-TableMap</span></span>
<span data-ttu-id="8a8e3-121">Mappning av källa till mål tabeller</span><span class="sxs-lookup"><span data-stu-id="8a8e3-121">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a8e3-122">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a8e3-122">-TargetDatabaseName</span></span>
<span data-ttu-id="8a8e3-123">Namnet på mål databasen.</span><span class="sxs-lookup"><span data-stu-id="8a8e3-123">The name of the target Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="8a8e3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a8e3-124">INPUTS</span></span>

### <span data-ttu-id="8a8e3-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="8a8e3-125">None</span></span>


## <span data-ttu-id="8a8e3-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a8e3-126">OUTPUTS</span></span>

### <span data-ttu-id="8a8e3-127">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="8a8e3-127">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>


## <span data-ttu-id="8a8e3-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a8e3-128">NOTES</span></span>

## <span data-ttu-id="8a8e3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a8e3-129">RELATED LINKS</span></span>


