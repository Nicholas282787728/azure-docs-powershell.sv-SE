---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b7a608e4bed6e68f06660f10f2ef72effb6ad18b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755770"
---
# <span data-ttu-id="ddfda-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="ddfda-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="ddfda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddfda-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfda-103">Hämtar ett katalog objekt för data Lake Analytics eller typer av objekt.</span><span class="sxs-lookup"><span data-stu-id="ddfda-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddfda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddfda-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddfda-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddfda-105">DESCRIPTION</span></span>
<span data-ttu-id="ddfda-106">**Get-AzureRmDataLakeAnalyticsCatalogItem** får ett angivet Azure Data Lake Analytics-katalog objekt eller hämtar katalog objekt av en angiven typ.</span><span class="sxs-lookup"><span data-stu-id="ddfda-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="ddfda-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddfda-107">EXAMPLES</span></span>

### <span data-ttu-id="ddfda-108">Exempel 1: Hämta en angiven databas</span><span class="sxs-lookup"><span data-stu-id="ddfda-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="ddfda-109">Det här kommandot hämtar den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="ddfda-109">This command gets the specified database.</span></span>

### <span data-ttu-id="ddfda-110">Exempel 2: Hämta tabeller i en angiven databas och ett angivet schema</span><span class="sxs-lookup"><span data-stu-id="ddfda-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="ddfda-111">Det här kommandot får en lista med tabeller i den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="ddfda-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="ddfda-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddfda-112">PARAMETERS</span></span>

### <span data-ttu-id="ddfda-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="ddfda-113">-Account</span></span>
<span data-ttu-id="ddfda-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="ddfda-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddfda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddfda-115">-DefaultProfile</span></span>
<span data-ttu-id="ddfda-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ddfda-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddfda-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="ddfda-117">-ItemType</span></span>
<span data-ttu-id="ddfda-118">Anger katalog objekt typen för de objekt som hämtas eller listas.</span><span class="sxs-lookup"><span data-stu-id="ddfda-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="ddfda-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ddfda-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ddfda-120">Databas</span><span class="sxs-lookup"><span data-stu-id="ddfda-120">Database</span></span>
- <span data-ttu-id="ddfda-121">Schemafiler</span><span class="sxs-lookup"><span data-stu-id="ddfda-121">Schema</span></span>
- <span data-ttu-id="ddfda-122">Sammansättningscachen</span><span class="sxs-lookup"><span data-stu-id="ddfda-122">Assembly</span></span>
- <span data-ttu-id="ddfda-123">Tabell</span><span class="sxs-lookup"><span data-stu-id="ddfda-123">Table</span></span>
- <span data-ttu-id="ddfda-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="ddfda-124">TableValuedFunction</span></span>
- <span data-ttu-id="ddfda-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="ddfda-125">TableStatistics</span></span>
- <span data-ttu-id="ddfda-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="ddfda-126">ExternalDataSource</span></span>
- <span data-ttu-id="ddfda-127">Dokumentvy</span><span class="sxs-lookup"><span data-stu-id="ddfda-127">View</span></span>
- <span data-ttu-id="ddfda-128">Steg</span><span class="sxs-lookup"><span data-stu-id="ddfda-128">Procedure</span></span>
- <span data-ttu-id="ddfda-129">Svaret</span><span class="sxs-lookup"><span data-stu-id="ddfda-129">Secret</span></span>
- <span data-ttu-id="ddfda-130">Inloggning</span><span class="sxs-lookup"><span data-stu-id="ddfda-130">Credential</span></span>
- <span data-ttu-id="ddfda-131">Ramtyper</span><span class="sxs-lookup"><span data-stu-id="ddfda-131">Types</span></span>
- <span data-ttu-id="ddfda-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="ddfda-132">TablePartition</span></span>

```yaml
Type: CatalogItemType
Parameter Sets: (All)
Aliases: 
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddfda-133">-Path</span><span class="sxs-lookup"><span data-stu-id="ddfda-133">-Path</span></span>
<span data-ttu-id="ddfda-134">Anger multi-part-sökvägen till objektet som ska hämtas, eller till den överordnade posten för de objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ddfda-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="ddfda-135">Delar av sökvägen ska avgränsas med en punkt (.).</span><span class="sxs-lookup"><span data-stu-id="ddfda-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddfda-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfda-136">CommonParameters</span></span>
<span data-ttu-id="ddfda-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddfda-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfda-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddfda-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfda-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddfda-139">INPUTS</span></span>

### <span data-ttu-id="ddfda-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="ddfda-140">None</span></span>
<span data-ttu-id="ddfda-141">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ddfda-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ddfda-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddfda-142">OUTPUTS</span></span>

### <span data-ttu-id="ddfda-143">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="ddfda-143">CatalogItem</span></span>
<span data-ttu-id="ddfda-144">Det angivna katalogobjektet.</span><span class="sxs-lookup"><span data-stu-id="ddfda-144">The specified catalog item.</span></span>

### <span data-ttu-id="ddfda-145">Förteckning<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="ddfda-145">List<CatalogItem></span></span>
<span data-ttu-id="ddfda-146">Listan med angivna katalog objekt under motsvarande behållare.</span><span class="sxs-lookup"><span data-stu-id="ddfda-146">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="ddfda-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddfda-147">NOTES</span></span>

## <span data-ttu-id="ddfda-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddfda-148">RELATED LINKS</span></span>

[<span data-ttu-id="ddfda-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="ddfda-149">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


