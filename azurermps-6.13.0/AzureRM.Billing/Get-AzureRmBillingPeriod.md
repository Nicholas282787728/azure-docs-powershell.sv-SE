---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 66c9a0bb9ba4aa2f17c48ffb737f1c8d72034f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581776"
---
# <span data-ttu-id="fb7e0-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="fb7e0-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="fb7e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7e0-103">Få fakturerings perioder för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fb7e0-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb7e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb7e0-104">SYNTAX</span></span>

### <span data-ttu-id="fb7e0-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="fb7e0-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb7e0-106">Enda</span><span class="sxs-lookup"><span data-stu-id="fb7e0-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb7e0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb7e0-107">DESCRIPTION</span></span>
<span data-ttu-id="fb7e0-108">Cmdleten **Get-AzureRmBillingPeriod** erhåller abonnemangets fakturerings period.</span><span class="sxs-lookup"><span data-stu-id="fb7e0-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="fb7e0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb7e0-109">EXAMPLES</span></span>

### <span data-ttu-id="fb7e0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fb7e0-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="fb7e0-111">Få alla tillgängliga fakturerings perioder för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fb7e0-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="fb7e0-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fb7e0-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="fb7e0-113">Skaffa fakturerings perioden för abonnemanget med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="fb7e0-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="fb7e0-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="fb7e0-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="fb7e0-115">Få maximalt 2 fakturerings perioder för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fb7e0-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="fb7e0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb7e0-116">PARAMETERS</span></span>

### <span data-ttu-id="fb7e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7e0-117">-DefaultProfile</span></span>
<span data-ttu-id="fb7e0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fb7e0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb7e0-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fb7e0-119">-MaxCount</span></span>
<span data-ttu-id="fb7e0-120">Ange det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="fb7e0-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="fb7e0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb7e0-121">-Name</span></span>
<span data-ttu-id="fb7e0-122">Namnet på en viss fakturerings period att få.</span><span class="sxs-lookup"><span data-stu-id="fb7e0-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="fb7e0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7e0-123">CommonParameters</span></span>
<span data-ttu-id="fb7e0-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7e0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7e0-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7e0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7e0-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb7e0-126">INPUTS</span></span>

### <span data-ttu-id="fb7e0-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="fb7e0-127">None</span></span>

## <span data-ttu-id="fb7e0-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb7e0-128">OUTPUTS</span></span>

### <span data-ttu-id="fb7e0-129">Microsoft. Azure. commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="fb7e0-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="fb7e0-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb7e0-130">NOTES</span></span>

## <span data-ttu-id="fb7e0-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb7e0-131">RELATED LINKS</span></span>
