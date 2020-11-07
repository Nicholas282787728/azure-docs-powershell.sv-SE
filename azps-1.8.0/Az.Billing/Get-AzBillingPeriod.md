---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: b4e85f85d0e7b7724b2a09f3c78af03dfd489014
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917618"
---
# <span data-ttu-id="12bde-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="12bde-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="12bde-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12bde-102">SYNOPSIS</span></span>
<span data-ttu-id="12bde-103">Få fakturerings perioder för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="12bde-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="12bde-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12bde-104">SYNTAX</span></span>

### <span data-ttu-id="12bde-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="12bde-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12bde-106">Enda</span><span class="sxs-lookup"><span data-stu-id="12bde-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12bde-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12bde-107">DESCRIPTION</span></span>
<span data-ttu-id="12bde-108">Cmdleten **Get-AzBillingPeriod** erhåller abonnemangets fakturerings period.</span><span class="sxs-lookup"><span data-stu-id="12bde-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="12bde-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12bde-109">EXAMPLES</span></span>

### <span data-ttu-id="12bde-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="12bde-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="12bde-111">Få alla tillgängliga fakturerings perioder för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="12bde-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="12bde-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="12bde-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="12bde-113">Skaffa fakturerings perioden för abonnemanget med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="12bde-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="12bde-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="12bde-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="12bde-115">Få maximalt 2 fakturerings perioder för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="12bde-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="12bde-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12bde-116">PARAMETERS</span></span>

### <span data-ttu-id="12bde-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12bde-117">-DefaultProfile</span></span>
<span data-ttu-id="12bde-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="12bde-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12bde-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="12bde-119">-MaxCount</span></span>
<span data-ttu-id="12bde-120">Ange det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="12bde-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="12bde-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="12bde-121">-Name</span></span>
<span data-ttu-id="12bde-122">Namnet på en viss fakturerings period att få.</span><span class="sxs-lookup"><span data-stu-id="12bde-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="12bde-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12bde-123">CommonParameters</span></span>
<span data-ttu-id="12bde-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12bde-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12bde-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12bde-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12bde-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12bde-126">INPUTS</span></span>

### <span data-ttu-id="12bde-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="12bde-127">None</span></span>

## <span data-ttu-id="12bde-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12bde-128">OUTPUTS</span></span>

### <span data-ttu-id="12bde-129">Microsoft. Azure. commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="12bde-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="12bde-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12bde-130">NOTES</span></span>

## <span data-ttu-id="12bde-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12bde-131">RELATED LINKS</span></span>
