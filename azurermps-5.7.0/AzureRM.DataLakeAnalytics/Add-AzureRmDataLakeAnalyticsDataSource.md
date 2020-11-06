---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 1f2fe13567bd17170fd73854ce5554a693210c7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575693"
---
# <span data-ttu-id="879fb-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="879fb-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="879fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="879fb-102">SYNOPSIS</span></span>
<span data-ttu-id="879fb-103">Lägger till en data källa i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="879fb-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="879fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="879fb-104">SYNTAX</span></span>

### <span data-ttu-id="879fb-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="879fb-105">AddDataLakeStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="879fb-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="879fb-106">AddBlobStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="879fb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="879fb-107">DESCRIPTION</span></span>
<span data-ttu-id="879fb-108">Cmdleten **Add-AzureRmDataLakeAnalyticsDataSource** lägger till en data källa i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="879fb-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="879fb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="879fb-109">EXAMPLES</span></span>

### <span data-ttu-id="879fb-110">Exempel 1: lägga till en data källa till ett konto</span><span class="sxs-lookup"><span data-stu-id="879fb-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="879fb-111">Det här kommandot lägger till data källor för data Lake Store i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="879fb-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="879fb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="879fb-112">PARAMETERS</span></span>

### <span data-ttu-id="879fb-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="879fb-113">-AccessKey</span></span>
<span data-ttu-id="879fb-114">Anger åtkomst tangenten för det Azure Blob Storage-konto som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="879fb-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="879fb-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="879fb-115">-Account</span></span>
<span data-ttu-id="879fb-116">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="879fb-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="879fb-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="879fb-117">-Blob</span></span>
<span data-ttu-id="879fb-118">Anger namnet på det Azure Blob Storage-konto som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="879fb-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="879fb-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="879fb-119">-DataLakeStore</span></span>
<span data-ttu-id="879fb-120">Anger namnet på Azure Data Lake Store-kontot som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="879fb-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="879fb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="879fb-121">-DefaultProfile</span></span>
<span data-ttu-id="879fb-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="879fb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="879fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="879fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="879fb-124">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="879fb-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="879fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="879fb-125">CommonParameters</span></span>
<span data-ttu-id="879fb-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="879fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="879fb-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="879fb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="879fb-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="879fb-128">INPUTS</span></span>

### <span data-ttu-id="879fb-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="879fb-129">None</span></span>
<span data-ttu-id="879fb-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="879fb-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="879fb-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="879fb-131">OUTPUTS</span></span>

### <span data-ttu-id="879fb-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="879fb-132">None</span></span>

## <span data-ttu-id="879fb-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="879fb-133">NOTES</span></span>

## <span data-ttu-id="879fb-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="879fb-134">RELATED LINKS</span></span>

[<span data-ttu-id="879fb-135">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="879fb-135">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="879fb-136">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="879fb-136">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


