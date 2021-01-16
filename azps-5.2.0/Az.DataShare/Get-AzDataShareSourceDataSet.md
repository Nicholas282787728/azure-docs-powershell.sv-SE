---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409427"
---
# <span data-ttu-id="0c98a-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="0c98a-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="0c98a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c98a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c98a-103">Hämtar information om käll data uppsättningar i dela prenumeration.</span><span class="sxs-lookup"><span data-stu-id="0c98a-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="0c98a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c98a-104">SYNTAX</span></span>

### <span data-ttu-id="0c98a-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0c98a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c98a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c98a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c98a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c98a-107">DESCRIPTION</span></span>
<span data-ttu-id="0c98a-108">Cmdleten **Get-AzDataShareSourceDataSet** innehåller information om käll data uppsättningarna i Share-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0c98a-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="0c98a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c98a-109">EXAMPLES</span></span>

### <span data-ttu-id="0c98a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0c98a-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="0c98a-111">Hämtar data mängder i käll resursen</span><span class="sxs-lookup"><span data-stu-id="0c98a-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="0c98a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c98a-112">PARAMETERS</span></span>

### <span data-ttu-id="0c98a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c98a-113">-AccountName</span></span>
<span data-ttu-id="0c98a-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="0c98a-114">Azure data share account name</span></span>

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

### <span data-ttu-id="0c98a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c98a-115">-DefaultProfile</span></span>
<span data-ttu-id="0c98a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c98a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c98a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c98a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0c98a-118">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="0c98a-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="0c98a-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0c98a-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="0c98a-120">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="0c98a-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="0c98a-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="0c98a-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="0c98a-122">Resurs-ID för Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="0c98a-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="0c98a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c98a-123">CommonParameters</span></span>
<span data-ttu-id="0c98a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c98a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c98a-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c98a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c98a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c98a-126">INPUTS</span></span>

### <span data-ttu-id="0c98a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0c98a-127">System.String</span></span>

## <span data-ttu-id="0c98a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c98a-128">OUTPUTS</span></span>

### <span data-ttu-id="0c98a-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="0c98a-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="0c98a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c98a-130">NOTES</span></span>

## <span data-ttu-id="0c98a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c98a-131">RELATED LINKS</span></span>
