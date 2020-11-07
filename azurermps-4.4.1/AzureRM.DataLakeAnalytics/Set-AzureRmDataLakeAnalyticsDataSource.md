---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 258db8a7dc1d771b73ea4c4fa373b1861847b820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756998"
---
# <span data-ttu-id="4a522-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4a522-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="4a522-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a522-102">SYNOPSIS</span></span>
<span data-ttu-id="4a522-103">Ändrar informationen för en data källa för ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="4a522-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a522-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a522-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a522-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a522-105">DESCRIPTION</span></span>
<span data-ttu-id="4a522-106">Cmdleten **set-AzureRmDataLakeAnalyticsDataSource** ändrar informationen för en data källa för ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="4a522-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4a522-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a522-107">EXAMPLES</span></span>

### <span data-ttu-id="4a522-108">Exempel 1: ändra åtkomst tangenten för en data Källa</span><span class="sxs-lookup"><span data-stu-id="4a522-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="4a522-109">Det här kommandot ändrar åtkomst-tangenten som är lagrad för en Azure Blob Storage-datakälla.</span><span class="sxs-lookup"><span data-stu-id="4a522-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="4a522-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a522-110">PARAMETERS</span></span>

### <span data-ttu-id="4a522-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="4a522-111">-AccessKey</span></span>
<span data-ttu-id="4a522-112">Anger den nya åtkomst knappen för data källan för Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="4a522-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a522-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="4a522-113">-Account</span></span>
<span data-ttu-id="4a522-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="4a522-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4a522-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="4a522-115">-Blob</span></span>
<span data-ttu-id="4a522-116">Anger namnet på din källa för Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="4a522-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a522-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a522-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a522-118">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="4a522-118">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="4a522-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a522-119">-DefaultProfile</span></span>
<span data-ttu-id="4a522-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a522-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a522-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a522-121">CommonParameters</span></span>
<span data-ttu-id="4a522-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a522-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a522-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a522-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a522-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a522-124">INPUTS</span></span>

## <span data-ttu-id="4a522-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a522-125">OUTPUTS</span></span>

### <span data-ttu-id="4a522-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="4a522-126">None</span></span>

## <span data-ttu-id="4a522-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a522-127">NOTES</span></span>

## <span data-ttu-id="4a522-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a522-128">RELATED LINKS</span></span>

[<span data-ttu-id="4a522-129">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4a522-129">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="4a522-130">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4a522-130">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


