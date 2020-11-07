---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: c04a79a54e42c64fe897a419565e4816964879b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758198"
---
# <span data-ttu-id="92314-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="92314-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="92314-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92314-102">SYNOPSIS</span></span>
<span data-ttu-id="92314-103">Skapar DatabaseInfo-objektet för Azure Database migration-tjänsten som anger databas källan för migrering.</span><span class="sxs-lookup"><span data-stu-id="92314-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92314-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92314-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92314-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92314-105">DESCRIPTION</span></span>
<span data-ttu-id="92314-106">New-AzureRmDataMigrationDatabaseInfo-cmdleten skapar ett DatabaseInfo-objekt som anger vilken käll databas instans som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="92314-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="92314-107">Databas namnet tas med som indataparameter.</span><span class="sxs-lookup"><span data-stu-id="92314-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="92314-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92314-108">EXAMPLES</span></span>

### <span data-ttu-id="92314-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="92314-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="92314-110">I det föregående exemplet skapas ett nytt DatabaseInfo-objekt för käll databasen **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="92314-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="92314-111">Det här skriptet förutsätter att du redan är inloggad på ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="92314-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="92314-112">Du kan bekräfta din inloggnings status genom att använda Get-AzureSubscription cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92314-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="92314-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92314-113">PARAMETERS</span></span>

### <span data-ttu-id="92314-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92314-114">-DefaultProfile</span></span>
<span data-ttu-id="92314-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92314-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92314-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="92314-116">-SourceDatabaseName</span></span>
<span data-ttu-id="92314-117">Käll databasens namn.</span><span class="sxs-lookup"><span data-stu-id="92314-117">Source Database Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92314-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92314-118">CommonParameters</span></span>
<span data-ttu-id="92314-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92314-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92314-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92314-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92314-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92314-121">INPUTS</span></span>

### <span data-ttu-id="92314-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="92314-122">None</span></span>

## <span data-ttu-id="92314-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92314-123">OUTPUTS</span></span>

### <span data-ttu-id="92314-124">Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="92314-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="92314-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92314-125">NOTES</span></span>

## <span data-ttu-id="92314-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92314-126">RELATED LINKS</span></span>
