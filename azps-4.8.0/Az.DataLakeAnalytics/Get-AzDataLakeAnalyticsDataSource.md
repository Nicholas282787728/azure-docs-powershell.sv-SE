---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e14e4c1b58b24cb8065681ae806789cd1252a0db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102929"
---
# <span data-ttu-id="9de8f-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9de8f-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="9de8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9de8f-102">SYNOPSIS</span></span>
<span data-ttu-id="9de8f-103">Hämtar data källan data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9de8f-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="9de8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9de8f-104">SYNTAX</span></span>

### <span data-ttu-id="9de8f-105">GetAllDataSources (standard)</span><span class="sxs-lookup"><span data-stu-id="9de8f-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9de8f-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9de8f-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9de8f-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9de8f-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9de8f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9de8f-108">DESCRIPTION</span></span>
<span data-ttu-id="9de8f-109">Cmdleten **Get-AzDataLakeAnalyticsDataSource** får en Azure Data Lake Analytics-datakälla.</span><span class="sxs-lookup"><span data-stu-id="9de8f-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="9de8f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9de8f-110">EXAMPLES</span></span>

### <span data-ttu-id="9de8f-111">Exempel 1: Hämta en data Källa från ett konto</span><span class="sxs-lookup"><span data-stu-id="9de8f-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="9de8f-112">Det här kommandot hämtar data källan för data Lake Store som heter ContosoAdls från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="9de8f-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="9de8f-113">Exempel 2: hämta listan över data Lake Store-konton i ett data Lake Analytics-konto</span><span class="sxs-lookup"><span data-stu-id="9de8f-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="9de8f-114">Det här kommandot får alla data Lake Store-konton från ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="9de8f-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="9de8f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9de8f-115">PARAMETERS</span></span>

### <span data-ttu-id="9de8f-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="9de8f-116">-Account</span></span>
<span data-ttu-id="9de8f-117">Anger det data Lake Analytics-konto som denna cmdlet hämtar data källor.</span><span class="sxs-lookup"><span data-stu-id="9de8f-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="9de8f-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="9de8f-118">-Blob</span></span>
<span data-ttu-id="9de8f-119">Anger namnet på din källa för Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="9de8f-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de8f-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9de8f-120">-DataLakeStore</span></span>
<span data-ttu-id="9de8f-121">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="9de8f-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de8f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de8f-122">-DefaultProfile</span></span>
<span data-ttu-id="9de8f-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9de8f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9de8f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de8f-124">-ResourceGroupName</span></span>
<span data-ttu-id="9de8f-125">Anger namnet på resurs gruppen som innehåller data källan.</span><span class="sxs-lookup"><span data-stu-id="9de8f-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="9de8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de8f-126">CommonParameters</span></span>
<span data-ttu-id="9de8f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de8f-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de8f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de8f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9de8f-129">INPUTS</span></span>

### <span data-ttu-id="9de8f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9de8f-130">System.String</span></span>

## <span data-ttu-id="9de8f-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9de8f-131">OUTPUTS</span></span>

### <span data-ttu-id="9de8f-132">Microsoft. Azure. commands. DataLakeAnalytics. Models. PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="9de8f-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="9de8f-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="9de8f-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="9de8f-134">Microsoft. Azure. commands. DataLakeAnalytics. Models. AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="9de8f-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="9de8f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9de8f-135">NOTES</span></span>

## <span data-ttu-id="9de8f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9de8f-136">RELATED LINKS</span></span>

[<span data-ttu-id="9de8f-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9de8f-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="9de8f-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9de8f-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="9de8f-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9de8f-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)

