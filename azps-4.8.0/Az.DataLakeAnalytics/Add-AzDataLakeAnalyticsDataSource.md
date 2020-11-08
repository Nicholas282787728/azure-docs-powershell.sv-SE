---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: ddb291a72d3c35c79321ddefa0832d46c489998f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102941"
---
# <span data-ttu-id="60af7-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="60af7-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="60af7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60af7-102">SYNOPSIS</span></span>
<span data-ttu-id="60af7-103">Lägger till en data källa i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="60af7-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="60af7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60af7-104">SYNTAX</span></span>

### <span data-ttu-id="60af7-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60af7-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60af7-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60af7-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60af7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60af7-107">DESCRIPTION</span></span>
<span data-ttu-id="60af7-108">Cmdleten **Add-AzDataLakeAnalyticsDataSource** lägger till en data källa i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="60af7-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="60af7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60af7-109">EXAMPLES</span></span>

### <span data-ttu-id="60af7-110">Exempel 1: lägga till en data källa till ett konto</span><span class="sxs-lookup"><span data-stu-id="60af7-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="60af7-111">Det här kommandot lägger till data källor för data Lake Store i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="60af7-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="60af7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60af7-112">PARAMETERS</span></span>

### <span data-ttu-id="60af7-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="60af7-113">-AccessKey</span></span>
<span data-ttu-id="60af7-114">Anger åtkomst tangenten för det Azure Blob Storage-konto som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="60af7-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="60af7-115">-Account</span></span>
<span data-ttu-id="60af7-116">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="60af7-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="60af7-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="60af7-117">-Blob</span></span>
<span data-ttu-id="60af7-118">Anger namnet på det Azure Blob Storage-konto som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="60af7-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60af7-119">-DataLakeStore</span></span>
<span data-ttu-id="60af7-120">Anger namnet på Azure Data Lake Store-kontot som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="60af7-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60af7-121">-DefaultProfile</span></span>
<span data-ttu-id="60af7-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="60af7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60af7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60af7-123">-ResourceGroupName</span></span>
<span data-ttu-id="60af7-124">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="60af7-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60af7-125">CommonParameters</span></span>
<span data-ttu-id="60af7-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60af7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60af7-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60af7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60af7-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60af7-128">INPUTS</span></span>

### <span data-ttu-id="60af7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="60af7-129">System.String</span></span>

## <span data-ttu-id="60af7-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60af7-130">OUTPUTS</span></span>

### <span data-ttu-id="60af7-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="60af7-131">System.Object</span></span>
## <span data-ttu-id="60af7-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60af7-132">NOTES</span></span>

## <span data-ttu-id="60af7-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60af7-133">RELATED LINKS</span></span>

[<span data-ttu-id="60af7-134">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="60af7-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="60af7-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="60af7-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


