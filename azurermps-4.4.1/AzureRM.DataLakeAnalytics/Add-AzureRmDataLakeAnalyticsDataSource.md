---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: a3eff47b688f2f426c4f255d400ce1ef73c3c027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574701"
---
# <span data-ttu-id="bf9d5-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bf9d5-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="bf9d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9d5-103">Lägger till en data källa i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="bf9d5-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf9d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf9d5-104">SYNTAX</span></span>

### <span data-ttu-id="bf9d5-105">Lägga till ett data Lake Storage-konto</span><span class="sxs-lookup"><span data-stu-id="bf9d5-105">Add a Data Lake storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf9d5-106">Lägga till ett BLOB-lagringsenhet</span><span class="sxs-lookup"><span data-stu-id="bf9d5-106">Add a Blob storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf9d5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf9d5-107">DESCRIPTION</span></span>
<span data-ttu-id="bf9d5-108">Cmdleten **Add-AzureRmDataLakeAnalyticsDataSource** lägger till en data källa i ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="bf9d5-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="bf9d5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf9d5-109">EXAMPLES</span></span>

### <span data-ttu-id="bf9d5-110">Exempel 1: lägga till en data källa till ett konto</span><span class="sxs-lookup"><span data-stu-id="bf9d5-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="bf9d5-111">Det här kommandot lägger till data källor för data Lake Store i ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="bf9d5-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="bf9d5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf9d5-112">PARAMETERS</span></span>

### <span data-ttu-id="bf9d5-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="bf9d5-113">-AccessKey</span></span>
<span data-ttu-id="bf9d5-114">Anger åtkomst tangenten för det Azure Blob Storage-konto som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="bf9d5-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9d5-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="bf9d5-115">-Account</span></span>
<span data-ttu-id="bf9d5-116">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="bf9d5-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="bf9d5-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="bf9d5-117">-Blob</span></span>
<span data-ttu-id="bf9d5-118">Anger namnet på det Azure Blob Storage-konto som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="bf9d5-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9d5-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bf9d5-119">-DataLakeStore</span></span>
<span data-ttu-id="bf9d5-120">Anger namnet på Azure Data Lake Store-kontot som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="bf9d5-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Data Lake storage account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="bf9d5-122">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="bf9d5-122">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="bf9d5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9d5-123">-DefaultProfile</span></span>
<span data-ttu-id="bf9d5-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf9d5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf9d5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9d5-125">CommonParameters</span></span>
<span data-ttu-id="bf9d5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf9d5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9d5-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf9d5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9d5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf9d5-128">INPUTS</span></span>

## <span data-ttu-id="bf9d5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf9d5-129">OUTPUTS</span></span>

### <span data-ttu-id="bf9d5-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="bf9d5-130">None</span></span>

## <span data-ttu-id="bf9d5-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf9d5-131">NOTES</span></span>

## <span data-ttu-id="bf9d5-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf9d5-132">RELATED LINKS</span></span>

[<span data-ttu-id="bf9d5-133">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bf9d5-133">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="bf9d5-134">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bf9d5-134">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


