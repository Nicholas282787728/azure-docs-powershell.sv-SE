---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524694"
---
# <span data-ttu-id="11cfe-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="11cfe-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="11cfe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="11cfe-103">Skaffa fakturerings profiler.</span><span class="sxs-lookup"><span data-stu-id="11cfe-103">Get billing profiles.</span></span>

## <span data-ttu-id="11cfe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11cfe-104">SYNTAX</span></span>

### <span data-ttu-id="11cfe-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="11cfe-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11cfe-106">Enda</span><span class="sxs-lookup"><span data-stu-id="11cfe-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11cfe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11cfe-107">DESCRIPTION</span></span>
<span data-ttu-id="11cfe-108">Cmdleten **Get-AzBillingProfile** har fakturerings profiler under det angivna fakturerings kontot.</span><span class="sxs-lookup"><span data-stu-id="11cfe-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="11cfe-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11cfe-109">EXAMPLES</span></span>

### <span data-ttu-id="11cfe-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="11cfe-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="11cfe-111">Få alla fakturerings profiler under det angivna fakturerings kontot.</span><span class="sxs-lookup"><span data-stu-id="11cfe-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="11cfe-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="11cfe-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="11cfe-113">Skaffa fakturerings profilen med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="11cfe-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="11cfe-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="11cfe-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="11cfe-115">Hämta alla fakturerings profiler under angivet fakturerings konto och inkludera faktura avsnitten i resultatet.</span><span class="sxs-lookup"><span data-stu-id="11cfe-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="11cfe-116">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="11cfe-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="11cfe-117">Skaffa fakturerings profilen med det angivna namnet och inkludera faktura avsnitten i resultatet.</span><span class="sxs-lookup"><span data-stu-id="11cfe-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="11cfe-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11cfe-118">PARAMETERS</span></span>

### <span data-ttu-id="11cfe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11cfe-119">-DefaultProfile</span></span>
<span data-ttu-id="11cfe-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="11cfe-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11cfe-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="11cfe-121">-BillingAccountName</span></span>
<span data-ttu-id="11cfe-122">Namn på det specifika fakturerings kontot.</span><span class="sxs-lookup"><span data-stu-id="11cfe-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="11cfe-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="11cfe-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="11cfe-124">Inkludera avsnitten fakturor under fakturerings profil.</span><span class="sxs-lookup"><span data-stu-id="11cfe-124">Include the invoices sections under billing profile.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11cfe-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="11cfe-125">-Name</span></span>
<span data-ttu-id="11cfe-126">Namn på en specifik fakturerings profil.</span><span class="sxs-lookup"><span data-stu-id="11cfe-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="11cfe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11cfe-127">CommonParameters</span></span>
<span data-ttu-id="11cfe-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11cfe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11cfe-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11cfe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11cfe-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11cfe-130">INPUTS</span></span>

### <span data-ttu-id="11cfe-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="11cfe-131">None</span></span>

## <span data-ttu-id="11cfe-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11cfe-132">OUTPUTS</span></span>

### <span data-ttu-id="11cfe-133">Microsoft. Azure. commands. Billing. Models. PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="11cfe-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="11cfe-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11cfe-134">NOTES</span></span>

## <span data-ttu-id="11cfe-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11cfe-135">RELATED LINKS</span></span>
