---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: ffa9de86a7ebbb70361752b8c7733129eb024845
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926874"
---
# <span data-ttu-id="139b6-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="139b6-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="139b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="139b6-102">SYNOPSIS</span></span>
<span data-ttu-id="139b6-103">Hämtar information om synkronisering uppgifter för Share-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="139b6-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="139b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="139b6-104">SYNTAX</span></span>

### <span data-ttu-id="139b6-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="139b6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="139b6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="139b6-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="139b6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="139b6-107">DESCRIPTION</span></span>
<span data-ttu-id="139b6-108">Cmdleten **Get-AzDataShareSubscriptionSynchronizationDetail** innehåller information om synkroniseringen som initierats för en resurs prenumeration.</span><span class="sxs-lookup"><span data-stu-id="139b6-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="139b6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="139b6-109">EXAMPLES</span></span>

### <span data-ttu-id="139b6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="139b6-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId "a6ee5c8d-0ce0-485e-b2f2-966b187dc6c7"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="139b6-111">Det här kommandot innehåller information om synkronisering initierat för AdsShareSubscription Share prenumeration under data Share Account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="139b6-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="139b6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="139b6-112">PARAMETERS</span></span>

### <span data-ttu-id="139b6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="139b6-113">-AccountName</span></span>
<span data-ttu-id="139b6-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="139b6-114">Azure data share account name</span></span>

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

### <span data-ttu-id="139b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="139b6-115">-DefaultProfile</span></span>
<span data-ttu-id="139b6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="139b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="139b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="139b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="139b6-118">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="139b6-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="139b6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="139b6-119">-ResourceId</span></span>
<span data-ttu-id="139b6-120">Resurs-ID för Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="139b6-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="139b6-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="139b6-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="139b6-122">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="139b6-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="139b6-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="139b6-123">-SynchronizationId</span></span>
<span data-ttu-id="139b6-124">Synkroniserings-ID för synkronisering av delade abonnemang</span><span class="sxs-lookup"><span data-stu-id="139b6-124">Synchronization id of share subscription synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="139b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139b6-125">CommonParameters</span></span>
<span data-ttu-id="139b6-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="139b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139b6-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="139b6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139b6-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="139b6-128">INPUTS</span></span>

### <span data-ttu-id="139b6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="139b6-129">System.String</span></span>

## <span data-ttu-id="139b6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="139b6-130">OUTPUTS</span></span>

### <span data-ttu-id="139b6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="139b6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="139b6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="139b6-132">NOTES</span></span>

## <span data-ttu-id="139b6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="139b6-133">RELATED LINKS</span></span>
