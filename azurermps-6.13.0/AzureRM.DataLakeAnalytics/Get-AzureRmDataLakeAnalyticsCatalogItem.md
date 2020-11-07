---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: bac4e3e2cc4471b8cf015f2f3ebeab421097f81c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757101"
---
# <span data-ttu-id="7a636-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="7a636-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="7a636-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a636-102">SYNOPSIS</span></span>
<span data-ttu-id="7a636-103">Hämtar ett katalog objekt för data Lake Analytics eller typer av objekt.</span><span class="sxs-lookup"><span data-stu-id="7a636-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a636-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a636-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a636-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a636-105">DESCRIPTION</span></span>
<span data-ttu-id="7a636-106">**Get-AzureRmDataLakeAnalyticsCatalogItem** får ett angivet Azure Data Lake Analytics-katalog objekt eller hämtar katalog objekt av en angiven typ.</span><span class="sxs-lookup"><span data-stu-id="7a636-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="7a636-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a636-107">EXAMPLES</span></span>

### <span data-ttu-id="7a636-108">Exempel 1: Hämta en angiven databas</span><span class="sxs-lookup"><span data-stu-id="7a636-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="7a636-109">Det här kommandot hämtar den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="7a636-109">This command gets the specified database.</span></span>

### <span data-ttu-id="7a636-110">Exempel 2: Hämta tabeller i en angiven databas och ett angivet schema</span><span class="sxs-lookup"><span data-stu-id="7a636-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="7a636-111">Det här kommandot får en lista med tabeller i den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="7a636-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="7a636-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a636-112">PARAMETERS</span></span>

### <span data-ttu-id="7a636-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="7a636-113">-Account</span></span>
<span data-ttu-id="7a636-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="7a636-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a636-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a636-115">-DefaultProfile</span></span>
<span data-ttu-id="7a636-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7a636-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a636-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="7a636-117">-ItemType</span></span>
<span data-ttu-id="7a636-118">Anger katalog objekt typen för de objekt som hämtas eller listas.</span><span class="sxs-lookup"><span data-stu-id="7a636-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="7a636-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7a636-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7a636-120">Databas</span><span class="sxs-lookup"><span data-stu-id="7a636-120">Database</span></span>
- <span data-ttu-id="7a636-121">Schemafiler</span><span class="sxs-lookup"><span data-stu-id="7a636-121">Schema</span></span>
- <span data-ttu-id="7a636-122">Sammansättningscachen</span><span class="sxs-lookup"><span data-stu-id="7a636-122">Assembly</span></span>
- <span data-ttu-id="7a636-123">Tabell</span><span class="sxs-lookup"><span data-stu-id="7a636-123">Table</span></span>
- <span data-ttu-id="7a636-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="7a636-124">TableValuedFunction</span></span>
- <span data-ttu-id="7a636-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="7a636-125">TableStatistics</span></span>
- <span data-ttu-id="7a636-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="7a636-126">ExternalDataSource</span></span>
- <span data-ttu-id="7a636-127">Dokumentvy</span><span class="sxs-lookup"><span data-stu-id="7a636-127">View</span></span>
- <span data-ttu-id="7a636-128">Steg</span><span class="sxs-lookup"><span data-stu-id="7a636-128">Procedure</span></span>
- <span data-ttu-id="7a636-129">Svaret</span><span class="sxs-lookup"><span data-stu-id="7a636-129">Secret</span></span>
- <span data-ttu-id="7a636-130">Inloggning</span><span class="sxs-lookup"><span data-stu-id="7a636-130">Credential</span></span>
- <span data-ttu-id="7a636-131">Ramtyper</span><span class="sxs-lookup"><span data-stu-id="7a636-131">Types</span></span>
- <span data-ttu-id="7a636-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="7a636-132">TablePartition</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a636-133">-Path</span><span class="sxs-lookup"><span data-stu-id="7a636-133">-Path</span></span>
<span data-ttu-id="7a636-134">Anger multi-part-sökvägen till objektet som ska hämtas, eller till den överordnade posten för de objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="7a636-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="7a636-135">Delar av sökvägen ska avgränsas med en punkt (.).</span><span class="sxs-lookup"><span data-stu-id="7a636-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a636-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a636-136">CommonParameters</span></span>
<span data-ttu-id="7a636-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a636-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a636-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a636-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a636-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a636-139">INPUTS</span></span>

### <span data-ttu-id="7a636-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7a636-140">System.String</span></span>

### <span data-ttu-id="7a636-141">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="7a636-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="7a636-142">Microsoft. Azure. commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="7a636-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="7a636-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a636-143">OUTPUTS</span></span>

### <span data-ttu-id="7a636-144">Microsoft. Azure. Management. DataLake. Analytics. Models. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="7a636-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="7a636-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a636-145">NOTES</span></span>

## <span data-ttu-id="7a636-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a636-146">RELATED LINKS</span></span>

[<span data-ttu-id="7a636-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="7a636-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


