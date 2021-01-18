---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524690"
---
# <span data-ttu-id="8ebfd-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="8ebfd-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="8ebfd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ebfd-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebfd-103">Få faktura avsnitt.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-103">Get invoice sections.</span></span>

## <span data-ttu-id="8ebfd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ebfd-104">SYNTAX</span></span>

### <span data-ttu-id="8ebfd-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8ebfd-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ebfd-106">Enda</span><span class="sxs-lookup"><span data-stu-id="8ebfd-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ebfd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ebfd-107">DESCRIPTION</span></span>
<span data-ttu-id="8ebfd-108">Cmdleten **Get-AzInvoiceSection** hämtar faktura avsnitt under den angivna fakturerings profilen.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="8ebfd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ebfd-109">EXAMPLES</span></span>

### <span data-ttu-id="8ebfd-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8ebfd-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="8ebfd-111">Hämta alla faktura avsnitt under den angivna fakturerings profilen.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="8ebfd-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8ebfd-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="8ebfd-113">Gå till avsnittet faktura med angivet namn.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="8ebfd-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ebfd-114">PARAMETERS</span></span>

### <span data-ttu-id="8ebfd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebfd-115">-DefaultProfile</span></span>
<span data-ttu-id="8ebfd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8ebfd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ebfd-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="8ebfd-117">-BillingAccountName</span></span>
<span data-ttu-id="8ebfd-118">Namn på det specifika fakturerings kontot.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="8ebfd-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="8ebfd-119">-BillingProfileName</span></span>
<span data-ttu-id="8ebfd-120">Namnet på den specifika fakturerings profilen.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="8ebfd-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8ebfd-121">-Name</span></span>
<span data-ttu-id="8ebfd-122">Namn på ett specifikt faktura avsnitt.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="8ebfd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebfd-123">CommonParameters</span></span>
<span data-ttu-id="8ebfd-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebfd-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ebfd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebfd-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ebfd-126">INPUTS</span></span>

### <span data-ttu-id="8ebfd-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="8ebfd-127">None</span></span>

## <span data-ttu-id="8ebfd-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ebfd-128">OUTPUTS</span></span>

### <span data-ttu-id="8ebfd-129">Microsoft. Azure. commands. Billing. Models. PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="8ebfd-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="8ebfd-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ebfd-130">NOTES</span></span>

## <span data-ttu-id="8ebfd-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ebfd-131">RELATED LINKS</span></span>
