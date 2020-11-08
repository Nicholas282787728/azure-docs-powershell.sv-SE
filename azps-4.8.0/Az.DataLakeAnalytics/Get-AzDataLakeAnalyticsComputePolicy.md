---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260555"
---
# <span data-ttu-id="b91c7-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="b91c7-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="b91c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b91c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b91c7-103">Hämtar en beräknings princip för data Lake Analytics eller en lista över beräknings principer.</span><span class="sxs-lookup"><span data-stu-id="b91c7-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="b91c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b91c7-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b91c7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b91c7-105">DESCRIPTION</span></span>
<span data-ttu-id="b91c7-106">Funktionen **Get-AzDataLakeAnalyticsComputePolicy** hämtar en beräknings princip för Azure Data Lake Analytics eller en lista med principer.</span><span class="sxs-lookup"><span data-stu-id="b91c7-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="b91c7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b91c7-107">EXAMPLES</span></span>

### <span data-ttu-id="b91c7-108">Exempel 1: Hämta en angiven beräknings princip</span><span class="sxs-lookup"><span data-stu-id="b91c7-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="b91c7-109">Det här kommandot hämtar den angivna beräknings principen med namnet "policy" i kontot ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="b91c7-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="b91c7-110">Exempel 2: Hämta en lista över alla beräknings principer i kontot</span><span class="sxs-lookup"><span data-stu-id="b91c7-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="b91c7-111">Det här kommandot får en lista över alla beräknings principer i kontot "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="b91c7-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="b91c7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b91c7-112">PARAMETERS</span></span>

### <span data-ttu-id="b91c7-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="b91c7-113">-Account</span></span>
<span data-ttu-id="b91c7-114">Namnet på kontot som du vill hämta en beräknings princip från.</span><span class="sxs-lookup"><span data-stu-id="b91c7-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="b91c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b91c7-115">-DefaultProfile</span></span>
<span data-ttu-id="b91c7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b91c7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b91c7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b91c7-117">-Name</span></span>
<span data-ttu-id="b91c7-118">Namnet på den beräknings princip som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="b91c7-118">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b91c7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b91c7-119">-ResourceGroupName</span></span>
<span data-ttu-id="b91c7-120">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="b91c7-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="b91c7-121">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="b91c7-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b91c7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b91c7-122">CommonParameters</span></span>
<span data-ttu-id="b91c7-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b91c7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b91c7-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b91c7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b91c7-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b91c7-125">INPUTS</span></span>

### <span data-ttu-id="b91c7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b91c7-126">System.String</span></span>

## <span data-ttu-id="b91c7-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b91c7-127">OUTPUTS</span></span>

### <span data-ttu-id="b91c7-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="b91c7-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="b91c7-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b91c7-129">NOTES</span></span>

## <span data-ttu-id="b91c7-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b91c7-130">RELATED LINKS</span></span>
