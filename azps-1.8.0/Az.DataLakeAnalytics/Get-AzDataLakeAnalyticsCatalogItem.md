---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2a69517a3b8a7624098a01e621e51b81dfaba835
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754333"
---
# <span data-ttu-id="895ca-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="895ca-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="895ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="895ca-102">SYNOPSIS</span></span>
<span data-ttu-id="895ca-103">Hämtar ett katalog objekt för data Lake Analytics eller typer av objekt.</span><span class="sxs-lookup"><span data-stu-id="895ca-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="895ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="895ca-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="895ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="895ca-105">DESCRIPTION</span></span>
<span data-ttu-id="895ca-106">**Get-AzDataLakeAnalyticsCatalogItem** får ett angivet Azure Data Lake Analytics-katalog objekt eller hämtar katalog objekt av en angiven typ.</span><span class="sxs-lookup"><span data-stu-id="895ca-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="895ca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="895ca-107">EXAMPLES</span></span>

### <span data-ttu-id="895ca-108">Exempel 1: Hämta en angiven databas</span><span class="sxs-lookup"><span data-stu-id="895ca-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="895ca-109">Det här kommandot hämtar den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="895ca-109">This command gets the specified database.</span></span>

### <span data-ttu-id="895ca-110">Exempel 2: Hämta tabeller i en angiven databas och ett angivet schema</span><span class="sxs-lookup"><span data-stu-id="895ca-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="895ca-111">Det här kommandot får en lista med tabeller i den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="895ca-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="895ca-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="895ca-112">PARAMETERS</span></span>

### <span data-ttu-id="895ca-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="895ca-113">-Account</span></span>
<span data-ttu-id="895ca-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="895ca-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="895ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="895ca-115">-DefaultProfile</span></span>
<span data-ttu-id="895ca-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="895ca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="895ca-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="895ca-117">-ItemType</span></span>
<span data-ttu-id="895ca-118">Anger katalog objekt typen för de objekt som hämtas eller listas.</span><span class="sxs-lookup"><span data-stu-id="895ca-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="895ca-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="895ca-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="895ca-120">Databas</span><span class="sxs-lookup"><span data-stu-id="895ca-120">Database</span></span>
- <span data-ttu-id="895ca-121">Schemafiler</span><span class="sxs-lookup"><span data-stu-id="895ca-121">Schema</span></span>
- <span data-ttu-id="895ca-122">Sammansättningscachen</span><span class="sxs-lookup"><span data-stu-id="895ca-122">Assembly</span></span>
- <span data-ttu-id="895ca-123">Tabell</span><span class="sxs-lookup"><span data-stu-id="895ca-123">Table</span></span>
- <span data-ttu-id="895ca-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="895ca-124">TableValuedFunction</span></span>
- <span data-ttu-id="895ca-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="895ca-125">TableStatistics</span></span>
- <span data-ttu-id="895ca-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="895ca-126">ExternalDataSource</span></span>
- <span data-ttu-id="895ca-127">Dokumentvy</span><span class="sxs-lookup"><span data-stu-id="895ca-127">View</span></span>
- <span data-ttu-id="895ca-128">Steg</span><span class="sxs-lookup"><span data-stu-id="895ca-128">Procedure</span></span>
- <span data-ttu-id="895ca-129">Svaret</span><span class="sxs-lookup"><span data-stu-id="895ca-129">Secret</span></span>
- <span data-ttu-id="895ca-130">Inloggning</span><span class="sxs-lookup"><span data-stu-id="895ca-130">Credential</span></span>
- <span data-ttu-id="895ca-131">Ramtyper</span><span class="sxs-lookup"><span data-stu-id="895ca-131">Types</span></span>
- <span data-ttu-id="895ca-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="895ca-132">TablePartition</span></span>

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

### <span data-ttu-id="895ca-133">-Path</span><span class="sxs-lookup"><span data-stu-id="895ca-133">-Path</span></span>
<span data-ttu-id="895ca-134">Anger multi-part-sökvägen till objektet som ska hämtas, eller till den överordnade posten för de objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="895ca-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="895ca-135">Delar av sökvägen ska avgränsas med en punkt (.).</span><span class="sxs-lookup"><span data-stu-id="895ca-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="895ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="895ca-136">CommonParameters</span></span>
<span data-ttu-id="895ca-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="895ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="895ca-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="895ca-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="895ca-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="895ca-139">INPUTS</span></span>

### <span data-ttu-id="895ca-140">System. String</span><span class="sxs-lookup"><span data-stu-id="895ca-140">System.String</span></span>

### <span data-ttu-id="895ca-141">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="895ca-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="895ca-142">Microsoft. Azure. commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="895ca-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="895ca-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="895ca-143">OUTPUTS</span></span>

### <span data-ttu-id="895ca-144">Microsoft. Azure. Management. DataLake. Analytics. Models. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="895ca-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="895ca-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="895ca-145">NOTES</span></span>

## <span data-ttu-id="895ca-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="895ca-146">RELATED LINKS</span></span>

[<span data-ttu-id="895ca-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="895ca-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


