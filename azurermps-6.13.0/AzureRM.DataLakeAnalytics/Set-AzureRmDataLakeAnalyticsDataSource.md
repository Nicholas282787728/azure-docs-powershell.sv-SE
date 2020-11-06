---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 8aae62ccbf79f2b3c59f6009aa5233daf00853fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580180"
---
# <span data-ttu-id="d7a8d-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="d7a8d-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="d7a8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a8d-103">Ändrar informationen för en data källa för ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="d7a8d-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7a8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7a8d-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7a8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7a8d-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a8d-106">Cmdleten **set-AzureRmDataLakeAnalyticsDataSource** ändrar informationen för en data källa för ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="d7a8d-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d7a8d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7a8d-107">EXAMPLES</span></span>

### <span data-ttu-id="d7a8d-108">Exempel 1: ändra åtkomst tangenten för en data Källa</span><span class="sxs-lookup"><span data-stu-id="d7a8d-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="d7a8d-109">Det här kommandot ändrar åtkomst-tangenten som är lagrad för en Azure Blob Storage-datakälla.</span><span class="sxs-lookup"><span data-stu-id="d7a8d-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="d7a8d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7a8d-110">PARAMETERS</span></span>

### <span data-ttu-id="d7a8d-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="d7a8d-111">-AccessKey</span></span>
<span data-ttu-id="d7a8d-112">Anger den nya åtkomst knappen för data källan för Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="d7a8d-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="d7a8d-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="d7a8d-113">-Account</span></span>
<span data-ttu-id="d7a8d-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="d7a8d-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d7a8d-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="d7a8d-115">-Blob</span></span>
<span data-ttu-id="d7a8d-116">Anger namnet på din källa för Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="d7a8d-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="d7a8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a8d-117">-DefaultProfile</span></span>
<span data-ttu-id="d7a8d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d7a8d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7a8d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7a8d-119">-ResourceGroupName</span></span>
<span data-ttu-id="d7a8d-120">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="d7a8d-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="d7a8d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a8d-121">CommonParameters</span></span>
<span data-ttu-id="d7a8d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a8d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a8d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a8d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a8d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7a8d-124">INPUTS</span></span>

### <span data-ttu-id="d7a8d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d7a8d-125">System.String</span></span>

## <span data-ttu-id="d7a8d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7a8d-126">OUTPUTS</span></span>

### <span data-ttu-id="d7a8d-127">System. Void</span><span class="sxs-lookup"><span data-stu-id="d7a8d-127">System.Void</span></span>

## <span data-ttu-id="d7a8d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7a8d-128">NOTES</span></span>

## <span data-ttu-id="d7a8d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7a8d-129">RELATED LINKS</span></span>

[<span data-ttu-id="d7a8d-130">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="d7a8d-130">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="d7a8d-131">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="d7a8d-131">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


