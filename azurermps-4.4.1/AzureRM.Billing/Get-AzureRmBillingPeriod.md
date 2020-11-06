---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: f6b75a1c161515ee45571ba3db6d2f84b95af967
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575012"
---
# <span data-ttu-id="096b4-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="096b4-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="096b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="096b4-102">SYNOPSIS</span></span>
<span data-ttu-id="096b4-103">Få fakturerings perioder för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="096b4-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="096b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="096b4-104">SYNTAX</span></span>

### <span data-ttu-id="096b4-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="096b4-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="096b4-106">Enda</span><span class="sxs-lookup"><span data-stu-id="096b4-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="096b4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="096b4-107">DESCRIPTION</span></span>
<span data-ttu-id="096b4-108">Cmdleten **Get-AzureRmBillingPeriod** erhåller abonnemangets fakturerings period.</span><span class="sxs-lookup"><span data-stu-id="096b4-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="096b4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="096b4-109">EXAMPLES</span></span>

### <span data-ttu-id="096b4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="096b4-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="096b4-111">Få alla tillgängliga fakturerings perioder för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="096b4-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="096b4-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="096b4-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="096b4-113">Skaffa fakturerings perioden för abonnemanget med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="096b4-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="096b4-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="096b4-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="096b4-115">Få maximalt 2 fakturerings perioder för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="096b4-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="096b4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="096b4-116">PARAMETERS</span></span>

### <span data-ttu-id="096b4-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="096b4-117">-MaxCount</span></span>
<span data-ttu-id="096b4-118">Ange det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="096b4-118">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="096b4-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="096b4-119">-Name</span></span>
<span data-ttu-id="096b4-120">Namnet på en viss fakturerings period att få.</span><span class="sxs-lookup"><span data-stu-id="096b4-120">Name of a specific billing period to get.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="096b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096b4-121">-DefaultProfile</span></span>
<span data-ttu-id="096b4-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="096b4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="096b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096b4-123">CommonParameters</span></span>
<span data-ttu-id="096b4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096b4-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096b4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096b4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="096b4-126">INPUTS</span></span>

### <span data-ttu-id="096b4-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="096b4-127">None</span></span>

## <span data-ttu-id="096b4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="096b4-128">OUTPUTS</span></span>

### <span data-ttu-id="096b4-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Billing. Models. PSBillingPeriod, Microsoft. Azure. commands. fakturering, version = 0.12.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="096b4-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod, Microsoft.Azure.Commands.Billing, Version=0.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="096b4-130">Microsoft. Azure. commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="096b4-130">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="096b4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="096b4-131">NOTES</span></span>

## <span data-ttu-id="096b4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="096b4-132">RELATED LINKS</span></span>

