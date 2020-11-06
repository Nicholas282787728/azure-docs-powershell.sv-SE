---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b12b09c686a2e0a5fcd85854551608b16cb43d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584768"
---
# <span data-ttu-id="1888a-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="1888a-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="1888a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1888a-102">SYNOPSIS</span></span>
<span data-ttu-id="1888a-103">Hämtar ett katalog objekt för data Lake Analytics eller typer av objekt.</span><span class="sxs-lookup"><span data-stu-id="1888a-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1888a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1888a-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1888a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1888a-105">DESCRIPTION</span></span>
<span data-ttu-id="1888a-106">**Get-AzureRmDataLakeAnalyticsCatalogItem** får ett angivet Azure Data Lake Analytics-katalog objekt eller hämtar katalog objekt av en angiven typ.</span><span class="sxs-lookup"><span data-stu-id="1888a-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="1888a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1888a-107">EXAMPLES</span></span>

### <span data-ttu-id="1888a-108">Exempel 1: Hämta en angiven databas</span><span class="sxs-lookup"><span data-stu-id="1888a-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="1888a-109">Det här kommandot hämtar den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="1888a-109">This command gets the specified database.</span></span>

### <span data-ttu-id="1888a-110">Exempel 2: Hämta tabeller i en angiven databas och ett angivet schema</span><span class="sxs-lookup"><span data-stu-id="1888a-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="1888a-111">Det här kommandot får en lista med tabeller i den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="1888a-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="1888a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1888a-112">PARAMETERS</span></span>

### <span data-ttu-id="1888a-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="1888a-113">-Account</span></span>
<span data-ttu-id="1888a-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="1888a-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1888a-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="1888a-115">-ItemType</span></span>
<span data-ttu-id="1888a-116">Anger katalog objekt typen för de objekt som hämtas eller listas.</span><span class="sxs-lookup"><span data-stu-id="1888a-116">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="1888a-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1888a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1888a-118">Databas</span><span class="sxs-lookup"><span data-stu-id="1888a-118">Database</span></span>
- <span data-ttu-id="1888a-119">Schemafiler</span><span class="sxs-lookup"><span data-stu-id="1888a-119">Schema</span></span>
- <span data-ttu-id="1888a-120">Sammansättningscachen</span><span class="sxs-lookup"><span data-stu-id="1888a-120">Assembly</span></span>
- <span data-ttu-id="1888a-121">Tabell</span><span class="sxs-lookup"><span data-stu-id="1888a-121">Table</span></span>
- <span data-ttu-id="1888a-122">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="1888a-122">TableValuedFunction</span></span>
- <span data-ttu-id="1888a-123">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="1888a-123">TableStatistics</span></span>
- <span data-ttu-id="1888a-124">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="1888a-124">ExternalDataSource</span></span>
- <span data-ttu-id="1888a-125">Dokumentvy</span><span class="sxs-lookup"><span data-stu-id="1888a-125">View</span></span>
- <span data-ttu-id="1888a-126">Steg</span><span class="sxs-lookup"><span data-stu-id="1888a-126">Procedure</span></span>
- <span data-ttu-id="1888a-127">Svaret</span><span class="sxs-lookup"><span data-stu-id="1888a-127">Secret</span></span>
- <span data-ttu-id="1888a-128">Inloggning</span><span class="sxs-lookup"><span data-stu-id="1888a-128">Credential</span></span>
- <span data-ttu-id="1888a-129">Ramtyper</span><span class="sxs-lookup"><span data-stu-id="1888a-129">Types</span></span>
- <span data-ttu-id="1888a-130">TablePartition</span><span class="sxs-lookup"><span data-stu-id="1888a-130">TablePartition</span></span>

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

### <span data-ttu-id="1888a-131">-Path</span><span class="sxs-lookup"><span data-stu-id="1888a-131">-Path</span></span>
<span data-ttu-id="1888a-132">Anger multi-part-sökvägen till objektet som ska hämtas, eller till den överordnade posten för de objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="1888a-132">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="1888a-133">Delar av sökvägen ska avgränsas med en punkt (.).</span><span class="sxs-lookup"><span data-stu-id="1888a-133">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="1888a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1888a-134">-DefaultProfile</span></span>
<span data-ttu-id="1888a-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1888a-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1888a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1888a-136">CommonParameters</span></span>
<span data-ttu-id="1888a-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1888a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1888a-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1888a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1888a-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1888a-139">INPUTS</span></span>

## <span data-ttu-id="1888a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1888a-140">OUTPUTS</span></span>

### <span data-ttu-id="1888a-141">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="1888a-141">CatalogItem</span></span>
<span data-ttu-id="1888a-142">Det angivna katalogobjektet.</span><span class="sxs-lookup"><span data-stu-id="1888a-142">The specified catalog item.</span></span>

### <span data-ttu-id="1888a-143">Förteckning<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="1888a-143">List<CatalogItem></span></span>
<span data-ttu-id="1888a-144">Listan med angivna katalog objekt under motsvarande behållare.</span><span class="sxs-lookup"><span data-stu-id="1888a-144">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="1888a-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1888a-145">NOTES</span></span>

## <span data-ttu-id="1888a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1888a-146">RELATED LINKS</span></span>

[<span data-ttu-id="1888a-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="1888a-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


