---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102920"
---
# <span data-ttu-id="81cb1-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="81cb1-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="81cb1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="81cb1-103">Skapar en samlings inställning för migrering enligt mongoDb migration</span><span class="sxs-lookup"><span data-stu-id="81cb1-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="81cb1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81cb1-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="81cb1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="81cb1-106">New-AzDataMigrationMongoDbCollectionSetting-cmdleten skapar objektet för migrering som anger beteendet för genomflöde och borttagning.</span><span class="sxs-lookup"><span data-stu-id="81cb1-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="81cb1-107">Utdata till cmdleten består av nyckel värde par med namnet på samlingen och värdet för inställningen.</span><span class="sxs-lookup"><span data-stu-id="81cb1-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="81cb1-108">Utdata används för att samla inställningar för databas nivå för migrering.</span><span class="sxs-lookup"><span data-stu-id="81cb1-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="81cb1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81cb1-109">EXAMPLES</span></span>

### <span data-ttu-id="81cb1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="81cb1-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="81cb1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81cb1-111">PARAMETERS</span></span>

### <span data-ttu-id="81cb1-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="81cb1-112">-Name</span></span>
<span data-ttu-id="81cb1-113">Namn på samlingen</span><span class="sxs-lookup"><span data-stu-id="81cb1-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cb1-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="81cb1-114">-ShardKey</span></span>
<span data-ttu-id="81cb1-115">Den kommaseparerade listan med Shard-tangenter.</span><span class="sxs-lookup"><span data-stu-id="81cb1-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="81cb1-116">För mongoDb Target kan du ange Shard-tangenten för "ShardKeyName: order", där order är 1,-1 eller tom för hash, till exempel "_id, e-post:-1".</span><span class="sxs-lookup"><span data-stu-id="81cb1-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81cb1-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="81cb1-117">-TargetRequestUnit</span></span>
<span data-ttu-id="81cb1-118">Beställnings enhet svärdet för dedikerad insamling.</span><span class="sxs-lookup"><span data-stu-id="81cb1-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="81cb1-119">Om den inte är inställd används den delade databasen RU.</span><span class="sxs-lookup"><span data-stu-id="81cb1-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="81cb1-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="81cb1-120">-CanDelete</span></span>
<span data-ttu-id="81cb1-121">Om mål data ska tas bort om växeln är inställd rensas den vid migreringen</span><span class="sxs-lookup"><span data-stu-id="81cb1-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="81cb1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cb1-122">CommonParameters</span></span>
<span data-ttu-id="81cb1-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81cb1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cb1-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81cb1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cb1-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81cb1-125">INPUTS</span></span>

### <span data-ttu-id="81cb1-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="81cb1-126">None</span></span>

## <span data-ttu-id="81cb1-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81cb1-127">OUTPUTS</span></span>

### <span data-ttu-id="81cb1-128">Microsoft. Azure. commands. DataMigration. Models. MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="81cb1-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="81cb1-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81cb1-129">NOTES</span></span>

## <span data-ttu-id="81cb1-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81cb1-130">RELATED LINKS</span></span>
