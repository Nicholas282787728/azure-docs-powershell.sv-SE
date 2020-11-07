---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 62b0a959e632c3e54b07e9238ae4ea9034a7408b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744452"
---
# <span data-ttu-id="52c99-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="52c99-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="52c99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52c99-102">SYNOPSIS</span></span>
<span data-ttu-id="52c99-103">Hämtar information om synkronisering körs i dela prenumeration.</span><span class="sxs-lookup"><span data-stu-id="52c99-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="52c99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52c99-104">SYNTAX</span></span>

### <span data-ttu-id="52c99-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="52c99-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52c99-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52c99-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52c99-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52c99-107">DESCRIPTION</span></span>
<span data-ttu-id="52c99-108">Cmdleten **Get-AzDataShareSubscriptionSynchronization** innehåller informaiton om all synkronisering körs i en resurs prenumeration under ett data delnings konto på konsumenten.</span><span class="sxs-lookup"><span data-stu-id="52c99-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="52c99-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52c99-109">EXAMPLES</span></span>

### <span data-ttu-id="52c99-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52c99-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="52c99-111">Det här kommandot innehåller information om all synkronisering körs för en AdsShareSubscription för Share-prenumeration under WikiAds för data delning.</span><span class="sxs-lookup"><span data-stu-id="52c99-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="52c99-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52c99-112">PARAMETERS</span></span>

### <span data-ttu-id="52c99-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52c99-113">-AccountName</span></span>
<span data-ttu-id="52c99-114">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="52c99-114">Azure data share account name</span></span>

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

### <span data-ttu-id="52c99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c99-115">-DefaultProfile</span></span>
<span data-ttu-id="52c99-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52c99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52c99-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52c99-117">-ResourceGroupName</span></span>
<span data-ttu-id="52c99-118">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="52c99-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="52c99-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52c99-119">-ResourceId</span></span>
<span data-ttu-id="52c99-120">Resurs-ID för Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="52c99-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="52c99-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="52c99-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="52c99-122">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="52c99-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="52c99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c99-123">CommonParameters</span></span>
<span data-ttu-id="52c99-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52c99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c99-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52c99-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c99-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52c99-126">INPUTS</span></span>

### <span data-ttu-id="52c99-127">System. String</span><span class="sxs-lookup"><span data-stu-id="52c99-127">System.String</span></span>

## <span data-ttu-id="52c99-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52c99-128">OUTPUTS</span></span>

### <span data-ttu-id="52c99-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="52c99-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="52c99-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52c99-130">NOTES</span></span>

## <span data-ttu-id="52c99-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52c99-131">RELATED LINKS</span></span>
