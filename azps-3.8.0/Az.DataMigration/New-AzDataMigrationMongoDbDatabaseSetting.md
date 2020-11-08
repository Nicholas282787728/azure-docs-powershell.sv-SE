---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925917"
---
# <span data-ttu-id="3e84c-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="3e84c-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="3e84c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e84c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e84c-103">Skapar databas inställning för migrering för mongoDb-migreringen</span><span class="sxs-lookup"><span data-stu-id="3e84c-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="3e84c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e84c-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="3e84c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e84c-105">DESCRIPTION</span></span>
<span data-ttu-id="3e84c-106">New-AzDataMigrationMongoDbDatabaseSetting-cmdleten skapar objektet för migrering som anger beteendet för genomflöde och borttagning.</span><span class="sxs-lookup"><span data-stu-id="3e84c-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="3e84c-107">Utdata är ett nyckel värde par med namnet på samlingen och värdet för inställningen, som kan användas för att starta migreringen.</span><span class="sxs-lookup"><span data-stu-id="3e84c-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="3e84c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e84c-108">EXAMPLES</span></span>

### <span data-ttu-id="3e84c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e84c-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="3e84c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e84c-110">PARAMETERS</span></span>

### <span data-ttu-id="3e84c-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e84c-111">-Name</span></span>
<span data-ttu-id="3e84c-112">Namn på databasen</span><span class="sxs-lookup"><span data-stu-id="3e84c-112">Name of the database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="3e84c-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="3e84c-113">-TargetRequestUnit</span></span>
<span data-ttu-id="3e84c-114">Det dedikerade värdet på en begäran om databas nivå.</span><span class="sxs-lookup"><span data-stu-id="3e84c-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="3e84c-115">Om den inte är inställd används den delade databasen RU.</span><span class="sxs-lookup"><span data-stu-id="3e84c-115">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e84c-116">-Samlingar</span><span class="sxs-lookup"><span data-stu-id="3e84c-116">-Collections</span></span>
<span data-ttu-id="3e84c-117">Matrisen med MongoDb som returneras av New-AzureRmDmsMongoDbDatabaseSetting-samtal.</span><span class="sxs-lookup"><span data-stu-id="3e84c-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e84c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e84c-118">CommonParameters</span></span>
<span data-ttu-id="3e84c-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e84c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e84c-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e84c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e84c-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e84c-121">INPUTS</span></span>

### <span data-ttu-id="3e84c-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="3e84c-122">None</span></span>

## <span data-ttu-id="3e84c-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e84c-123">OUTPUTS</span></span>

### <span data-ttu-id="3e84c-124">Microsoft. Azure. commands. DataMigration. Models. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="3e84c-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="3e84c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e84c-125">NOTES</span></span>

## <span data-ttu-id="3e84c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e84c-126">RELATED LINKS</span></span>