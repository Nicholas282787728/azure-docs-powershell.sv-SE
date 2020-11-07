---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757689"
---
# <span data-ttu-id="315ca-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="315ca-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="315ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="315ca-102">SYNOPSIS</span></span>
<span data-ttu-id="315ca-103">Skapar DatabaseInfo-objektet för Azure Database migration-tjänsten som anger databas källan för migrering.</span><span class="sxs-lookup"><span data-stu-id="315ca-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="315ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="315ca-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="315ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="315ca-105">DESCRIPTION</span></span>
<span data-ttu-id="315ca-106">New-AzureRmDataMigrationDatabaseInfo-cmdleten skapar ett DatabaseInfo-objekt som anger vilken käll databas instans som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="315ca-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="315ca-107">Databas namnet tas med som indataparameter.</span><span class="sxs-lookup"><span data-stu-id="315ca-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="315ca-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="315ca-108">EXAMPLES</span></span>

### <span data-ttu-id="315ca-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="315ca-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="315ca-110">I det föregående exemplet skapas ett nytt DatabaseInfo-objekt för käll databasen **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="315ca-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>

<span data-ttu-id="315ca-111">Det här skriptet förutsätter att du redan är inloggad på ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="315ca-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="315ca-112">Du kan bekräfta din inloggnings status genom att använda Get-AzureSubscription cmdlet.</span><span class="sxs-lookup"><span data-stu-id="315ca-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="315ca-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="315ca-113">PARAMETERS</span></span>

### <span data-ttu-id="315ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315ca-114">-DefaultProfile</span></span>
<span data-ttu-id="315ca-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="315ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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
### <span data-ttu-id="315ca-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="315ca-116">-Confirm</span></span>
<span data-ttu-id="315ca-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="315ca-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="315ca-118">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="315ca-118">-SourceDatabaseName</span></span>
<span data-ttu-id="315ca-119">Käll databasens namn.</span><span class="sxs-lookup"><span data-stu-id="315ca-119">Source Database Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="315ca-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="315ca-120">-WhatIf</span></span>
<span data-ttu-id="315ca-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="315ca-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="315ca-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="315ca-122">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="315ca-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="315ca-123">INPUTS</span></span>

### <span data-ttu-id="315ca-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="315ca-124">None</span></span>


## <span data-ttu-id="315ca-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="315ca-125">OUTPUTS</span></span>

### <span data-ttu-id="315ca-126">Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="315ca-126">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>


## <span data-ttu-id="315ca-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="315ca-127">NOTES</span></span>

## <span data-ttu-id="315ca-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="315ca-128">RELATED LINKS</span></span>


