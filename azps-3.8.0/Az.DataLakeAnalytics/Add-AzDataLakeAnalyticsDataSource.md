---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: ddb291a72d3c35c79321ddefa0832d46c489998f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090529"
---
# <span data-ttu-id="f104e-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="f104e-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="f104e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f104e-102">SYNOPSIS</span></span>
<span data-ttu-id="f104e-103">Lägger till en data källa i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="f104e-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f104e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f104e-104">SYNTAX</span></span>

### <span data-ttu-id="f104e-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f104e-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f104e-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f104e-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f104e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f104e-107">DESCRIPTION</span></span>
<span data-ttu-id="f104e-108">Cmdleten **Add-AzDataLakeAnalyticsDataSource** lägger till en data källa i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="f104e-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f104e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f104e-109">EXAMPLES</span></span>

### <span data-ttu-id="f104e-110">Exempel 1: lägga till en data källa till ett konto</span><span class="sxs-lookup"><span data-stu-id="f104e-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="f104e-111">Det här kommandot lägger till data källor för data Lake Store i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="f104e-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f104e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f104e-112">PARAMETERS</span></span>

### <span data-ttu-id="f104e-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="f104e-113">-AccessKey</span></span>
<span data-ttu-id="f104e-114">Anger åtkomst tangenten för det Azure Blob Storage-konto som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f104e-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

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

### <span data-ttu-id="f104e-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="f104e-115">-Account</span></span>
<span data-ttu-id="f104e-116">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="f104e-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f104e-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="f104e-117">-Blob</span></span>
<span data-ttu-id="f104e-118">Anger namnet på det Azure Blob Storage-konto som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f104e-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

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

### <span data-ttu-id="f104e-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f104e-119">-DataLakeStore</span></span>
<span data-ttu-id="f104e-120">Anger namnet på Azure Data Lake Store-kontot som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="f104e-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

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

### <span data-ttu-id="f104e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f104e-121">-DefaultProfile</span></span>
<span data-ttu-id="f104e-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f104e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f104e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f104e-123">-ResourceGroupName</span></span>
<span data-ttu-id="f104e-124">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="f104e-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="f104e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f104e-125">CommonParameters</span></span>
<span data-ttu-id="f104e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f104e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f104e-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f104e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f104e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f104e-128">INPUTS</span></span>

### <span data-ttu-id="f104e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f104e-129">System.String</span></span>

## <span data-ttu-id="f104e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f104e-130">OUTPUTS</span></span>

### <span data-ttu-id="f104e-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="f104e-131">System.Object</span></span>
## <span data-ttu-id="f104e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f104e-132">NOTES</span></span>

## <span data-ttu-id="f104e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f104e-133">RELATED LINKS</span></span>

[<span data-ttu-id="f104e-134">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="f104e-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="f104e-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="f104e-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


