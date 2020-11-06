---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 1f21022294b1bcf5c75a7cf49dcc009600dc4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581775"
---
# <span data-ttu-id="4567f-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="4567f-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="4567f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4567f-102">SYNOPSIS</span></span>
<span data-ttu-id="4567f-103">Skaffa faktura fakturor för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4567f-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4567f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4567f-104">SYNTAX</span></span>

### <span data-ttu-id="4567f-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="4567f-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4567f-106">RelatesTo</span><span class="sxs-lookup"><span data-stu-id="4567f-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4567f-107">Enda</span><span class="sxs-lookup"><span data-stu-id="4567f-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4567f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4567f-108">DESCRIPTION</span></span>
<span data-ttu-id="4567f-109">Cmdleten **Get-AzureRmBillingInvoice** får fakturerings fakturor för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4567f-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="4567f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4567f-110">EXAMPLES</span></span>

### <span data-ttu-id="4567f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4567f-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="4567f-112">Få den senaste fakturan för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4567f-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="4567f-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4567f-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="4567f-114">Hämta prenumerationen för abonnemanget med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="4567f-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="4567f-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="4567f-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="4567f-116">Hämta alla tillgängliga fakturor för abonnemanget i omvänd kronologisk ordning med början med den senaste fakturan utan nedladdnings-URL.</span><span class="sxs-lookup"><span data-stu-id="4567f-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="4567f-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="4567f-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="4567f-118">Få de senaste 10 fakturorna för abonnemanget och inkludera nedladdnings-URL: en i resultatet.</span><span class="sxs-lookup"><span data-stu-id="4567f-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="4567f-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4567f-119">PARAMETERS</span></span>

### <span data-ttu-id="4567f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4567f-120">-DefaultProfile</span></span>
<span data-ttu-id="4567f-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4567f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4567f-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="4567f-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="4567f-123">Generera nedladdnings-URL: en för fakturorna.</span><span class="sxs-lookup"><span data-stu-id="4567f-123">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567f-124">-Senaste</span><span class="sxs-lookup"><span data-stu-id="4567f-124">-Latest</span></span>
<span data-ttu-id="4567f-125">Skaffa den senaste fakturan.</span><span class="sxs-lookup"><span data-stu-id="4567f-125">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4567f-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4567f-126">-MaxCount</span></span>
<span data-ttu-id="4567f-127">Avgör det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="4567f-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="4567f-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="4567f-128">-Name</span></span>
<span data-ttu-id="4567f-129">Namnet på en specifik faktura för att få eller den senaste om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="4567f-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="4567f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4567f-130">CommonParameters</span></span>
<span data-ttu-id="4567f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4567f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4567f-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4567f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4567f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4567f-133">INPUTS</span></span>

### <span data-ttu-id="4567f-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="4567f-134">None</span></span>

## <span data-ttu-id="4567f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4567f-135">OUTPUTS</span></span>

### <span data-ttu-id="4567f-136">Microsoft. Azure. commands. Billing. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="4567f-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="4567f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4567f-137">NOTES</span></span>

## <span data-ttu-id="4567f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4567f-138">RELATED LINKS</span></span>
