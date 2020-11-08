---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260008"
---
# <span data-ttu-id="f98f1-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f98f1-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="f98f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f98f1-102">SYNOPSIS</span></span>
<span data-ttu-id="f98f1-103">Skapar DatabaseInfo-objektet för Azure Database migration-tjänsten som anger databas källan för migrering.</span><span class="sxs-lookup"><span data-stu-id="f98f1-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="f98f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f98f1-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f98f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f98f1-105">DESCRIPTION</span></span>
<span data-ttu-id="f98f1-106">New-AzDataMigrationDatabaseInfo-cmdleten skapar ett DatabaseInfo-objekt som anger vilken käll databas instans som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="f98f1-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="f98f1-107">Databas namnet tas med som indataparameter.</span><span class="sxs-lookup"><span data-stu-id="f98f1-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="f98f1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f98f1-108">EXAMPLES</span></span>

### <span data-ttu-id="f98f1-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f98f1-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="f98f1-110">I det föregående exemplet skapas ett nytt DatabaseInfo-objekt för käll databasen **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="f98f1-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="f98f1-111">Det här skriptet förutsätter att du redan är inloggad på ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="f98f1-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="f98f1-112">Du kan bekräfta din inloggnings status genom att använda Get-AzSubscription cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f98f1-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="f98f1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f98f1-113">PARAMETERS</span></span>

### <span data-ttu-id="f98f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98f1-114">-DefaultProfile</span></span>
<span data-ttu-id="f98f1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f98f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f98f1-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f98f1-116">-SourceDatabaseName</span></span>
<span data-ttu-id="f98f1-117">Käll databasens namn.</span><span class="sxs-lookup"><span data-stu-id="f98f1-117">Source Database Name.</span></span>

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

### <span data-ttu-id="f98f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98f1-118">CommonParameters</span></span>
<span data-ttu-id="f98f1-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f98f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98f1-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f98f1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98f1-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f98f1-121">INPUTS</span></span>

### <span data-ttu-id="f98f1-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="f98f1-122">None</span></span>

## <span data-ttu-id="f98f1-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f98f1-123">OUTPUTS</span></span>

### <span data-ttu-id="f98f1-124">Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f98f1-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="f98f1-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f98f1-125">NOTES</span></span>

## <span data-ttu-id="f98f1-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f98f1-126">RELATED LINKS</span></span>
