---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: f19c4f9d39837534ea5ddd5b16daa055ee54aef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576565"
---
# <span data-ttu-id="1ae5c-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1ae5c-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="1ae5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ae5c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae5c-103">Hämtar en beräknings princip för data Lake Analytics eller en lista över beräknings principer.</span><span class="sxs-lookup"><span data-stu-id="1ae5c-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ae5c-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae5c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ae5c-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae5c-106">Funktionen **Get-AzureRmDataLakeAnalyticsComputePolicy** hämtar en beräknings princip för Azure Data Lake Analytics eller en lista med principer.</span><span class="sxs-lookup"><span data-stu-id="1ae5c-106">The **Get-AzureRmDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="1ae5c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ae5c-107">EXAMPLES</span></span>

### <span data-ttu-id="1ae5c-108">Exempel 1: Hämta en angiven beräknings princip</span><span class="sxs-lookup"><span data-stu-id="1ae5c-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="1ae5c-109">Det här kommandot hämtar den angivna beräknings principen med namnet "policy" i kontot ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="1ae5c-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="1ae5c-110">Exempel 2: Hämta en lista över alla beräknings principer i kontot</span><span class="sxs-lookup"><span data-stu-id="1ae5c-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="1ae5c-111">Det här kommandot får en lista över alla beräknings principer i kontot "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="1ae5c-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="1ae5c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ae5c-112">PARAMETERS</span></span>

### <span data-ttu-id="1ae5c-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="1ae5c-113">-Account</span></span>
<span data-ttu-id="1ae5c-114">Namnet på kontot som du vill hämta en beräknings princip från.</span><span class="sxs-lookup"><span data-stu-id="1ae5c-114">Name of the account to get the compute policy or policies from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae5c-115">-DefaultProfile</span></span>
<span data-ttu-id="1ae5c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1ae5c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ae5c-117">-Name</span></span>
<span data-ttu-id="1ae5c-118">Namnet på den beräknings princip som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="1ae5c-118">Name of the compute policy to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae5c-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ae5c-120">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="1ae5c-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="1ae5c-121">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="1ae5c-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae5c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae5c-122">CommonParameters</span></span>
<span data-ttu-id="1ae5c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae5c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae5c-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae5c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae5c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ae5c-125">INPUTS</span></span>

### <span data-ttu-id="1ae5c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1ae5c-126">System.String</span></span>

## <span data-ttu-id="1ae5c-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ae5c-127">OUTPUTS</span></span>

### <span data-ttu-id="1ae5c-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1ae5c-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>
<span data-ttu-id="1ae5c-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft. Azure. commands. DataLakeAnalytics, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1ae5c-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft.Azure.Commands.DataLakeAnalytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1ae5c-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ae5c-130">NOTES</span></span>

## <span data-ttu-id="1ae5c-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ae5c-131">RELATED LINKS</span></span>

