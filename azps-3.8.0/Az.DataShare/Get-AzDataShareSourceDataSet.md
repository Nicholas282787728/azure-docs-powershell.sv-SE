---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: cda879a29d207a3e71d903c02e20129267124414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088891"
---
# <span data-ttu-id="07cdd-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="07cdd-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="07cdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="07cdd-103">Hämtar information om käll data uppsättningar i dela prenumeration.</span><span class="sxs-lookup"><span data-stu-id="07cdd-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="07cdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07cdd-104">SYNTAX</span></span>

### <span data-ttu-id="07cdd-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="07cdd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07cdd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07cdd-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07cdd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07cdd-107">DESCRIPTION</span></span>
<span data-ttu-id="07cdd-108">Cmdleten **Get-AzDataShareSourceDataSet** innehåller information om käll data uppsättningarna i Share-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="07cdd-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="07cdd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07cdd-109">EXAMPLES</span></span>

### <span data-ttu-id="07cdd-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="07cdd-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="07cdd-111">Hämtar data mängder i käll resursen</span><span class="sxs-lookup"><span data-stu-id="07cdd-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="07cdd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07cdd-112">PARAMETERS</span></span>

### <span data-ttu-id="07cdd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="07cdd-113">-AccountName</span></span>
<span data-ttu-id="07cdd-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="07cdd-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cdd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07cdd-115">-DefaultProfile</span></span>
<span data-ttu-id="07cdd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07cdd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07cdd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07cdd-117">-ResourceGroupName</span></span>
<span data-ttu-id="07cdd-118">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="07cdd-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cdd-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="07cdd-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="07cdd-120">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="07cdd-120">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cdd-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="07cdd-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="07cdd-122">Resurs-ID för Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="07cdd-122">Azure data share subscription resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07cdd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07cdd-123">CommonParameters</span></span>
<span data-ttu-id="07cdd-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07cdd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07cdd-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07cdd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07cdd-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07cdd-126">INPUTS</span></span>

### <span data-ttu-id="07cdd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="07cdd-127">System.String</span></span>

## <span data-ttu-id="07cdd-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07cdd-128">OUTPUTS</span></span>

### <span data-ttu-id="07cdd-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="07cdd-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="07cdd-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07cdd-130">NOTES</span></span>

## <span data-ttu-id="07cdd-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07cdd-131">RELATED LINKS</span></span>
