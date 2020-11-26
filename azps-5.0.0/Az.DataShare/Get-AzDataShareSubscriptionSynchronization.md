---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: f1527cfcb947f802cb4a2710ab2f25a1d7b9bf75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320339"
---
# <span data-ttu-id="a462a-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="a462a-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="a462a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a462a-102">SYNOPSIS</span></span>
<span data-ttu-id="a462a-103">Hämtar information om synkronisering körs i dela prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a462a-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="a462a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a462a-104">SYNTAX</span></span>

### <span data-ttu-id="a462a-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a462a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a462a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a462a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a462a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a462a-107">DESCRIPTION</span></span>
<span data-ttu-id="a462a-108">Cmdleten **Get-AzDataShareSubscriptionSynchronization** innehåller informaiton om all synkronisering körs i en resurs prenumeration under ett data delnings konto på konsumenten.</span><span class="sxs-lookup"><span data-stu-id="a462a-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="a462a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a462a-109">EXAMPLES</span></span>

### <span data-ttu-id="a462a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a462a-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="a462a-111">Det här kommandot innehåller information om all synkronisering körs för en AdsShareSubscription för Share-prenumeration under WikiAds för data delning.</span><span class="sxs-lookup"><span data-stu-id="a462a-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="a462a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a462a-112">PARAMETERS</span></span>

### <span data-ttu-id="a462a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a462a-113">-AccountName</span></span>
<span data-ttu-id="a462a-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="a462a-114">Azure data share account name</span></span>

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

### <span data-ttu-id="a462a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a462a-115">-DefaultProfile</span></span>
<span data-ttu-id="a462a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a462a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a462a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a462a-117">-ResourceGroupName</span></span>
<span data-ttu-id="a462a-118">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="a462a-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a462a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a462a-119">-ResourceId</span></span>
<span data-ttu-id="a462a-120">Resurs-ID för Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="a462a-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="a462a-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a462a-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="a462a-122">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="a462a-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="a462a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a462a-123">CommonParameters</span></span>
<span data-ttu-id="a462a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a462a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a462a-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a462a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a462a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a462a-126">INPUTS</span></span>

### <span data-ttu-id="a462a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a462a-127">System.String</span></span>

## <span data-ttu-id="a462a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a462a-128">OUTPUTS</span></span>

### <span data-ttu-id="a462a-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="a462a-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="a462a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a462a-130">NOTES</span></span>

## <span data-ttu-id="a462a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a462a-131">RELATED LINKS</span></span>