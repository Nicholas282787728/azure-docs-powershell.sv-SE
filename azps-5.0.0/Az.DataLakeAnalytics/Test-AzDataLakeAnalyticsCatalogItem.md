---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320651"
---
# <span data-ttu-id="dc3c9-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="dc3c9-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="dc3c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3c9-103">Kontrollerar om det finns ett katalog objekt.</span><span class="sxs-lookup"><span data-stu-id="dc3c9-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="dc3c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc3c9-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc3c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc3c9-105">DESCRIPTION</span></span>
<span data-ttu-id="dc3c9-106">**Testet AzDataLakeAnalyticsCatalogItem** söker efter en Azure Data Lake Analytics-katalog.</span><span class="sxs-lookup"><span data-stu-id="dc3c9-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="dc3c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc3c9-107">EXAMPLES</span></span>

### <span data-ttu-id="dc3c9-108">Exempel 1: testa om en katalog artikel finns</span><span class="sxs-lookup"><span data-stu-id="dc3c9-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="dc3c9-109">Det här kommandot testar om ett angivet schema objekt finns.</span><span class="sxs-lookup"><span data-stu-id="dc3c9-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="dc3c9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc3c9-110">PARAMETERS</span></span>

### <span data-ttu-id="dc3c9-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="dc3c9-111">-Account</span></span>
<span data-ttu-id="dc3c9-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="dc3c9-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="dc3c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3c9-113">-DefaultProfile</span></span>
<span data-ttu-id="dc3c9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dc3c9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc3c9-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="dc3c9-115">-ItemType</span></span>
<span data-ttu-id="dc3c9-116">Anger katalog objekt typen för artikeln som ska kontrol leras.</span><span class="sxs-lookup"><span data-stu-id="dc3c9-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="dc3c9-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dc3c9-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dc3c9-118">Databas</span><span class="sxs-lookup"><span data-stu-id="dc3c9-118">Database</span></span>
- <span data-ttu-id="dc3c9-119">Schemafiler</span><span class="sxs-lookup"><span data-stu-id="dc3c9-119">Schema</span></span>
- <span data-ttu-id="dc3c9-120">Sammansättningscachen</span><span class="sxs-lookup"><span data-stu-id="dc3c9-120">Assembly</span></span>
- <span data-ttu-id="dc3c9-121">Tabell</span><span class="sxs-lookup"><span data-stu-id="dc3c9-121">Table</span></span>
- <span data-ttu-id="dc3c9-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="dc3c9-122">TablePartition</span></span>
- <span data-ttu-id="dc3c9-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="dc3c9-123">TableValuedFunction</span></span>
- <span data-ttu-id="dc3c9-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="dc3c9-124">TableStatistics</span></span>
- <span data-ttu-id="dc3c9-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="dc3c9-125">ExternalDataSource</span></span>
- <span data-ttu-id="dc3c9-126">Dokumentvy</span><span class="sxs-lookup"><span data-stu-id="dc3c9-126">View</span></span>
- <span data-ttu-id="dc3c9-127">Steg</span><span class="sxs-lookup"><span data-stu-id="dc3c9-127">Procedure</span></span>
- <span data-ttu-id="dc3c9-128">Svaret</span><span class="sxs-lookup"><span data-stu-id="dc3c9-128">Secret</span></span>
- <span data-ttu-id="dc3c9-129">Inloggning</span><span class="sxs-lookup"><span data-stu-id="dc3c9-129">Credential</span></span>
- <span data-ttu-id="dc3c9-130">Ramtyper</span><span class="sxs-lookup"><span data-stu-id="dc3c9-130">Types</span></span>

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

### <span data-ttu-id="dc3c9-131">-Path</span><span class="sxs-lookup"><span data-stu-id="dc3c9-131">-Path</span></span>
<span data-ttu-id="dc3c9-132">Anger sökvägen till objektet som ska hämtas, eller sökvägen till den överordnade posten för de objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="dc3c9-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc3c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3c9-133">CommonParameters</span></span>
<span data-ttu-id="dc3c9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc3c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3c9-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3c9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3c9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc3c9-136">INPUTS</span></span>

### <span data-ttu-id="dc3c9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dc3c9-137">System.String</span></span>

### <span data-ttu-id="dc3c9-138">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="dc3c9-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="dc3c9-139">Microsoft. Azure. commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="dc3c9-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="dc3c9-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc3c9-140">OUTPUTS</span></span>

### <span data-ttu-id="dc3c9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc3c9-141">System.Boolean</span></span>

## <span data-ttu-id="dc3c9-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc3c9-142">NOTES</span></span>

## <span data-ttu-id="dc3c9-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc3c9-143">RELATED LINKS</span></span>

[<span data-ttu-id="dc3c9-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="dc3c9-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)

