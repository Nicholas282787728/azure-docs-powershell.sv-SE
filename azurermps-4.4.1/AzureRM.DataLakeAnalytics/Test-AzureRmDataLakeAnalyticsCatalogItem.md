---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 249ef7ae66436d4bf82b3b038aa8b1201f68110e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756353"
---
# <span data-ttu-id="b4aae-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="b4aae-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="b4aae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4aae-102">SYNOPSIS</span></span>
<span data-ttu-id="b4aae-103">Kontrollerar om det finns ett katalog objekt.</span><span class="sxs-lookup"><span data-stu-id="b4aae-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4aae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4aae-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4aae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4aae-105">DESCRIPTION</span></span>
<span data-ttu-id="b4aae-106">**Testet AzureRmDataLakeAnalyticsCatalogItem** söker efter en Azure Data Lake Analytics-katalog.</span><span class="sxs-lookup"><span data-stu-id="b4aae-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="b4aae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4aae-107">EXAMPLES</span></span>

### <span data-ttu-id="b4aae-108">Exempel 1: testa om en katalog artikel finns</span><span class="sxs-lookup"><span data-stu-id="b4aae-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="b4aae-109">Det här kommandot testar om ett angivet schema objekt finns.</span><span class="sxs-lookup"><span data-stu-id="b4aae-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="b4aae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4aae-110">PARAMETERS</span></span>

### <span data-ttu-id="b4aae-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="b4aae-111">-Account</span></span>
<span data-ttu-id="b4aae-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="b4aae-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b4aae-113">-ItemType</span><span class="sxs-lookup"><span data-stu-id="b4aae-113">-ItemType</span></span>
<span data-ttu-id="b4aae-114">Anger katalog objekt typen för artikeln som ska kontrol leras.</span><span class="sxs-lookup"><span data-stu-id="b4aae-114">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="b4aae-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b4aae-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4aae-116">Databas</span><span class="sxs-lookup"><span data-stu-id="b4aae-116">Database</span></span>
- <span data-ttu-id="b4aae-117">Schemafiler</span><span class="sxs-lookup"><span data-stu-id="b4aae-117">Schema</span></span>
- <span data-ttu-id="b4aae-118">Sammansättningscachen</span><span class="sxs-lookup"><span data-stu-id="b4aae-118">Assembly</span></span>
- <span data-ttu-id="b4aae-119">Tabell</span><span class="sxs-lookup"><span data-stu-id="b4aae-119">Table</span></span>
- <span data-ttu-id="b4aae-120">TablePartition</span><span class="sxs-lookup"><span data-stu-id="b4aae-120">TablePartition</span></span>
- <span data-ttu-id="b4aae-121">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="b4aae-121">TableValuedFunction</span></span>
- <span data-ttu-id="b4aae-122">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="b4aae-122">TableStatistics</span></span>
- <span data-ttu-id="b4aae-123">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="b4aae-123">ExternalDataSource</span></span>
- <span data-ttu-id="b4aae-124">Dokumentvy</span><span class="sxs-lookup"><span data-stu-id="b4aae-124">View</span></span>
- <span data-ttu-id="b4aae-125">Steg</span><span class="sxs-lookup"><span data-stu-id="b4aae-125">Procedure</span></span>
- <span data-ttu-id="b4aae-126">Svaret</span><span class="sxs-lookup"><span data-stu-id="b4aae-126">Secret</span></span>
- <span data-ttu-id="b4aae-127">Inloggning</span><span class="sxs-lookup"><span data-stu-id="b4aae-127">Credential</span></span>
- <span data-ttu-id="b4aae-128">Ramtyper</span><span class="sxs-lookup"><span data-stu-id="b4aae-128">Types</span></span>

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

### <span data-ttu-id="b4aae-129">-Path</span><span class="sxs-lookup"><span data-stu-id="b4aae-129">-Path</span></span>
<span data-ttu-id="b4aae-130">Anger sökvägen till objektet som ska hämtas, eller sökvägen till den överordnade posten för de objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="b4aae-130">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="b4aae-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4aae-131">-DefaultProfile</span></span>
<span data-ttu-id="b4aae-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4aae-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4aae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4aae-133">CommonParameters</span></span>
<span data-ttu-id="b4aae-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4aae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4aae-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4aae-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4aae-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4aae-136">INPUTS</span></span>

## <span data-ttu-id="b4aae-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4aae-137">OUTPUTS</span></span>

### <span data-ttu-id="b4aae-138">bool</span><span class="sxs-lookup"><span data-stu-id="b4aae-138">bool</span></span>
<span data-ttu-id="b4aae-139">Sant eller falskt anger om det angivna katalogobjektet finns eller inte.</span><span class="sxs-lookup"><span data-stu-id="b4aae-139">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="b4aae-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4aae-140">NOTES</span></span>

## <span data-ttu-id="b4aae-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4aae-141">RELATED LINKS</span></span>

[<span data-ttu-id="b4aae-142">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="b4aae-142">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


