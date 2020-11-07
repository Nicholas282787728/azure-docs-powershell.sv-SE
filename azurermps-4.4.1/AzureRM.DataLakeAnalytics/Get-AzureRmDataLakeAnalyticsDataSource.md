---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: b7f2c6f2077d0b7e9c7510f6984ada15a65d6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758096"
---
# <span data-ttu-id="ce2c9-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ce2c9-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="ce2c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce2c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ce2c9-103">Hämtar data källan data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce2c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce2c9-104">SYNTAX</span></span>

### <span data-ttu-id="ce2c9-105">Lista alla data källor (standard)</span><span class="sxs-lookup"><span data-stu-id="ce2c9-105">List all data sources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce2c9-106">Skaffa ett data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="ce2c9-106">Get a Data Lake Store account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce2c9-107">Skaffa ett Blob Storage-konto</span><span class="sxs-lookup"><span data-stu-id="ce2c9-107">Get a Blob storage account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce2c9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce2c9-108">DESCRIPTION</span></span>
<span data-ttu-id="ce2c9-109">Cmdleten **Get-AzureRmDataLakeAnalyticsDataSource** får en Azure Data Lake Analytics-datakälla.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="ce2c9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce2c9-110">EXAMPLES</span></span>

### <span data-ttu-id="ce2c9-111">Exempel 1: Hämta en data Källa från ett konto</span><span class="sxs-lookup"><span data-stu-id="ce2c9-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="ce2c9-112">Det här kommandot hämtar data källan för data Lake Store som heter ContosoAdls från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="ce2c9-113">Exempel 2: hämta listan över data Lake Store-konton i ett data Lake Analytics-konto</span><span class="sxs-lookup"><span data-stu-id="ce2c9-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="ce2c9-114">Det här kommandot får alla data Lake Store-konton från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ce2c9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce2c9-115">PARAMETERS</span></span>

### <span data-ttu-id="ce2c9-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="ce2c9-116">-Account</span></span>
<span data-ttu-id="ce2c9-117">Anger det data Lake Analytics-konto som denna cmdlet hämtar data källor.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="ce2c9-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="ce2c9-118">-Blob</span></span>
<span data-ttu-id="ce2c9-119">Anger namnet på din källa för Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce2c9-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce2c9-120">-DataLakeStore</span></span>
<span data-ttu-id="ce2c9-121">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Data Lake Store account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce2c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce2c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="ce2c9-123">Anger namnet på resurs gruppen som innehåller data källan.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-123">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce2c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce2c9-124">-DefaultProfile</span></span>
<span data-ttu-id="ce2c9-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce2c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce2c9-126">CommonParameters</span></span>
<span data-ttu-id="ce2c9-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce2c9-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce2c9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce2c9-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce2c9-129">INPUTS</span></span>

## <span data-ttu-id="ce2c9-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce2c9-130">OUTPUTS</span></span>

### <span data-ttu-id="ce2c9-131">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="ce2c9-131">PSStorageAccountInfo</span></span>
<span data-ttu-id="ce2c9-132">De angivna Azure Storage-konto uppgifterna.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-132">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="ce2c9-133">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="ce2c9-133">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="ce2c9-134">De angivna konto uppgifterna för data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ce2c9-134">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="ce2c9-135">Förteckning<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="ce2c9-135">List<AdlDataSource></span></span>
<span data-ttu-id="ce2c9-136">Listan över både Azure Storage-konton och data Lake Store-konton i det angivna data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="ce2c9-136">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="ce2c9-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce2c9-137">NOTES</span></span>

## <span data-ttu-id="ce2c9-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce2c9-138">RELATED LINKS</span></span>

[<span data-ttu-id="ce2c9-139">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ce2c9-139">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="ce2c9-140">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ce2c9-140">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="ce2c9-141">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ce2c9-141">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


