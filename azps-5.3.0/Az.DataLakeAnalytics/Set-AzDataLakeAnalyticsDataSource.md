---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526160"
---
# <span data-ttu-id="df582-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="df582-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="df582-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df582-102">SYNOPSIS</span></span>
<span data-ttu-id="df582-103">Ändrar informationen för en data källa för ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="df582-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="df582-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df582-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df582-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df582-105">DESCRIPTION</span></span>
<span data-ttu-id="df582-106">Cmdleten **set-AzDataLakeAnalyticsDataSource** ändrar informationen för en data källa för ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="df582-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="df582-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df582-107">EXAMPLES</span></span>

### <span data-ttu-id="df582-108">Exempel 1: ändra åtkomst tangenten för en data Källa</span><span class="sxs-lookup"><span data-stu-id="df582-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="df582-109">Det här kommandot ändrar åtkomst-tangenten som är lagrad för en Azure Blob Storage-datakälla.</span><span class="sxs-lookup"><span data-stu-id="df582-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="df582-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df582-110">PARAMETERS</span></span>

### <span data-ttu-id="df582-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="df582-111">-AccessKey</span></span>
<span data-ttu-id="df582-112">Anger den nya åtkomst knappen för data källan för Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="df582-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="df582-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="df582-113">-Account</span></span>
<span data-ttu-id="df582-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="df582-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="df582-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="df582-115">-Blob</span></span>
<span data-ttu-id="df582-116">Anger namnet på din källa för Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="df582-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="df582-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df582-117">-DefaultProfile</span></span>
<span data-ttu-id="df582-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="df582-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df582-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df582-119">-ResourceGroupName</span></span>
<span data-ttu-id="df582-120">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="df582-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="df582-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df582-121">CommonParameters</span></span>
<span data-ttu-id="df582-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df582-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df582-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df582-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df582-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df582-124">INPUTS</span></span>

### <span data-ttu-id="df582-125">System. String</span><span class="sxs-lookup"><span data-stu-id="df582-125">System.String</span></span>

## <span data-ttu-id="df582-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df582-126">OUTPUTS</span></span>

### <span data-ttu-id="df582-127">System. Void</span><span class="sxs-lookup"><span data-stu-id="df582-127">System.Void</span></span>

## <span data-ttu-id="df582-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df582-128">NOTES</span></span>

## <span data-ttu-id="df582-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df582-129">RELATED LINKS</span></span>

[<span data-ttu-id="df582-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="df582-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="df582-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="df582-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


