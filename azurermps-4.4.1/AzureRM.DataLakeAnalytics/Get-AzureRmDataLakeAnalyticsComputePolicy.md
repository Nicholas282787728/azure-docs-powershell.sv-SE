---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 59bc611d63d062d06b3b3bdebe9ac8b0f1349179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758097"
---
# <span data-ttu-id="9f41a-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="9f41a-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="9f41a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f41a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f41a-103">Hämtar en beräknings princip för data Lake Analytics eller en lista över beräknings principer.</span><span class="sxs-lookup"><span data-stu-id="9f41a-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f41a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f41a-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f41a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f41a-105">DESCRIPTION</span></span>
<span data-ttu-id="9f41a-106">Funktionen **Get-AzureRmDataLakeAnalyticsComputePolicy** hämtar en beräknings princip för Azure Data Lake Analytics eller en lista med principer.</span><span class="sxs-lookup"><span data-stu-id="9f41a-106">The **Get-AzureRmDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="9f41a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f41a-107">EXAMPLES</span></span>

### <span data-ttu-id="9f41a-108">Exempel 1: Hämta en angiven beräknings princip</span><span class="sxs-lookup"><span data-stu-id="9f41a-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="9f41a-109">Det här kommandot hämtar den angivna beräknings principen med namnet "policy" i kontot ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="9f41a-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="9f41a-110">Exempel 2: Hämta en lista över alla beräknings principer i kontot</span><span class="sxs-lookup"><span data-stu-id="9f41a-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="9f41a-111">Det här kommandot får en lista över alla beräknings principer i kontot "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="9f41a-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="9f41a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f41a-112">PARAMETERS</span></span>

### <span data-ttu-id="9f41a-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="9f41a-113">-Account</span></span>
<span data-ttu-id="9f41a-114">Namnet på kontot som du vill hämta en beräknings princip från.</span><span class="sxs-lookup"><span data-stu-id="9f41a-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="9f41a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f41a-115">-Name</span></span>
<span data-ttu-id="9f41a-116">Namnet på den beräknings princip som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="9f41a-116">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="9f41a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f41a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9f41a-118">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="9f41a-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="9f41a-119">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="9f41a-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="9f41a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f41a-120">-DefaultProfile</span></span>
<span data-ttu-id="9f41a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f41a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f41a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f41a-122">CommonParameters</span></span>
<span data-ttu-id="9f41a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f41a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f41a-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f41a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f41a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f41a-125">INPUTS</span></span>

### <span data-ttu-id="9f41a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9f41a-126">System.String</span></span>

## <span data-ttu-id="9f41a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f41a-127">OUTPUTS</span></span>

### <span data-ttu-id="9f41a-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="9f41a-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>
<span data-ttu-id="9f41a-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft. Azure. commands. DataLakeAnalytics, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9f41a-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft.Azure.Commands.DataLakeAnalytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9f41a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f41a-130">NOTES</span></span>

## <span data-ttu-id="9f41a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f41a-131">RELATED LINKS</span></span>

