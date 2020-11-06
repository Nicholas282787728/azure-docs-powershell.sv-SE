---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 93e64c4a64eecbe66fc3f9b2923ade65405a05a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573454"
---
# <span data-ttu-id="54a0c-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="54a0c-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="54a0c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="54a0c-103">Hämtar data källan data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="54a0c-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54a0c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54a0c-104">SYNTAX</span></span>

### <span data-ttu-id="54a0c-105">GetAllDataSources (standard)</span><span class="sxs-lookup"><span data-stu-id="54a0c-105">GetAllDataSources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a0c-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="54a0c-106">GetDataLakeStoreAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a0c-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54a0c-107">GetBlobStorageAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54a0c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54a0c-108">DESCRIPTION</span></span>
<span data-ttu-id="54a0c-109">Cmdleten **Get-AzureRmDataLakeAnalyticsDataSource** får en Azure Data Lake Analytics-datakälla.</span><span class="sxs-lookup"><span data-stu-id="54a0c-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="54a0c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54a0c-110">EXAMPLES</span></span>

### <span data-ttu-id="54a0c-111">Exempel 1: Hämta en data Källa från ett konto</span><span class="sxs-lookup"><span data-stu-id="54a0c-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="54a0c-112">Det här kommandot hämtar data källan för data Lake Store som heter ContosoAdls från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="54a0c-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="54a0c-113">Exempel 2: hämta listan över data Lake Store-konton i ett data Lake Analytics-konto</span><span class="sxs-lookup"><span data-stu-id="54a0c-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="54a0c-114">Det här kommandot får alla data Lake Store-konton från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="54a0c-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="54a0c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54a0c-115">PARAMETERS</span></span>

### <span data-ttu-id="54a0c-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="54a0c-116">-Account</span></span>
<span data-ttu-id="54a0c-117">Anger det data Lake Analytics-konto som denna cmdlet hämtar data källor.</span><span class="sxs-lookup"><span data-stu-id="54a0c-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="54a0c-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="54a0c-118">-Blob</span></span>
<span data-ttu-id="54a0c-119">Anger namnet på din källa för Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="54a0c-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54a0c-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="54a0c-120">-DataLakeStore</span></span>
<span data-ttu-id="54a0c-121">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="54a0c-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: GetDataLakeStoreAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54a0c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a0c-122">-DefaultProfile</span></span>
<span data-ttu-id="54a0c-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="54a0c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54a0c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a0c-124">-ResourceGroupName</span></span>
<span data-ttu-id="54a0c-125">Anger namnet på resurs gruppen som innehåller data källan.</span><span class="sxs-lookup"><span data-stu-id="54a0c-125">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54a0c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a0c-126">CommonParameters</span></span>
<span data-ttu-id="54a0c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54a0c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a0c-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54a0c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a0c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54a0c-129">INPUTS</span></span>

### <span data-ttu-id="54a0c-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="54a0c-130">None</span></span>
<span data-ttu-id="54a0c-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="54a0c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="54a0c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54a0c-132">OUTPUTS</span></span>

### <span data-ttu-id="54a0c-133">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="54a0c-133">PSStorageAccountInfo</span></span>
<span data-ttu-id="54a0c-134">De angivna Azure Storage-konto uppgifterna.</span><span class="sxs-lookup"><span data-stu-id="54a0c-134">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="54a0c-135">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="54a0c-135">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="54a0c-136">De angivna konto uppgifterna för data Lake Store</span><span class="sxs-lookup"><span data-stu-id="54a0c-136">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="54a0c-137">Förteckning<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="54a0c-137">List<AdlDataSource></span></span>
<span data-ttu-id="54a0c-138">Listan över både Azure Storage-konton och data Lake Store-konton i det angivna data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="54a0c-138">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="54a0c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54a0c-139">NOTES</span></span>

## <span data-ttu-id="54a0c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54a0c-140">RELATED LINKS</span></span>

[<span data-ttu-id="54a0c-141">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="54a0c-141">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="54a0c-142">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="54a0c-142">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="54a0c-143">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="54a0c-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


