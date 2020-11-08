---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271659"
---
# <span data-ttu-id="2f7b5-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="2f7b5-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="2f7b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7b5-103">Skaffa faktura fakturor för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="2f7b5-104">Få fakturerings fakturor för ett fakturerings konto och en fakturerings profil</span><span class="sxs-lookup"><span data-stu-id="2f7b5-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="2f7b5-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f7b5-105">SYNTAX</span></span>

### <span data-ttu-id="2f7b5-106">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="2f7b5-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="2f7b5-107">RelatesTo</span><span class="sxs-lookup"><span data-stu-id="2f7b5-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="2f7b5-108">Enda</span><span class="sxs-lookup"><span data-stu-id="2f7b5-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f7b5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f7b5-109">DESCRIPTION</span></span>
<span data-ttu-id="2f7b5-110">Cmdleten **Get-AzBillingInvoice** får fakturerings fakturor för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="2f7b5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f7b5-111">EXAMPLES</span></span>

### <span data-ttu-id="2f7b5-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2f7b5-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="2f7b5-113">Få den senaste fakturan för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="2f7b5-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2f7b5-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="2f7b5-115">Hämta prenumerationen för abonnemanget med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="2f7b5-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="2f7b5-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="2f7b5-117">Hämta alla tillgängliga fakturor för abonnemanget i omvänd kronologisk ordning med början med den senaste fakturan utan nedladdnings-URL.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="2f7b5-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="2f7b5-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="2f7b5-119">Få de senaste 10 fakturorna för abonnemanget och inkludera nedladdnings-URL: en i resultatet.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="2f7b5-120">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="2f7b5-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="2f7b5-121">Hämta den specifika fakturan efter namn och ta med nedladdnings-URL i resultatet.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="2f7b5-122">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="2f7b5-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="2f7b5-123">Skaffa fakturor efter namn på fakturerings konto och ta med nedladdnings-URL för varje faktura i resultatet.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="2f7b5-124">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="2f7b5-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="2f7b5-125">Hämta specifika fakturor efter faktura namn och fakturerings konto namn och inkludera URL-adressen för varje faktura i resultatet.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="2f7b5-126">Exempel 8</span><span class="sxs-lookup"><span data-stu-id="2f7b5-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="2f7b5-127">Hämta senaste faktura efter namn på fakturerings konto och inkludera URL-adressen för en faktura i resultatet.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="2f7b5-128">Exempel 9</span><span class="sxs-lookup"><span data-stu-id="2f7b5-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="2f7b5-129">Skaffa de senaste 10 fakturorna till det specifika fakturerings kontot och en viss fakturerings profil och inkludera URL-adressen för nedladdning i resultatet.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="2f7b5-130">Exempel 10</span><span class="sxs-lookup"><span data-stu-id="2f7b5-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="2f7b5-131">Hämta den senaste fakturan med namn på fakturerings kontot och namnet på fakturerings profilen och ta med URL-adressen till nedladdning i resultatet.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="2f7b5-132">Exempel 10</span><span class="sxs-lookup"><span data-stu-id="2f7b5-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="2f7b5-133">Skaffa fakturor efter namn på fakturerings konto och profil namn för en fakturerings period som anges med perioStart datum och periodEnd datum.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="2f7b5-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f7b5-134">PARAMETERS</span></span>

### <span data-ttu-id="2f7b5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7b5-135">-DefaultProfile</span></span>
<span data-ttu-id="2f7b5-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2f7b5-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f7b5-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="2f7b5-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="2f7b5-138">Generera nedladdnings-URL: en för fakturorna.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="2f7b5-139">-Senaste</span><span class="sxs-lookup"><span data-stu-id="2f7b5-139">-Latest</span></span>
<span data-ttu-id="2f7b5-140">Skaffa den senaste fakturan.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="2f7b5-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2f7b5-141">-MaxCount</span></span>
<span data-ttu-id="2f7b5-142">Avgör det maximala antalet poster som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="2f7b5-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f7b5-143">-Name</span></span>
<span data-ttu-id="2f7b5-144">Namnet på en specifik faktura för att få eller den senaste om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="2f7b5-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="2f7b5-145">-BillingAccountName</span></span>
<span data-ttu-id="2f7b5-146">Namnet på ett specifikt fakturerings konto för att få fakturor för.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7b5-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="2f7b5-147">-BillingProfileName</span></span>
<span data-ttu-id="2f7b5-148">Namnet på en viss fakturerings profil för att få fakturor för.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7b5-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="2f7b5-149">-PeriodStartDate</span></span>
<span data-ttu-id="2f7b5-150">Start datum för faktura.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7b5-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="2f7b5-151">-PeriodEndDate</span></span>
<span data-ttu-id="2f7b5-152">Slutdatum för faktura.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="2f7b5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7b5-153">CommonParameters</span></span>
<span data-ttu-id="2f7b5-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7b5-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f7b5-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7b5-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f7b5-156">INPUTS</span></span>

### <span data-ttu-id="2f7b5-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="2f7b5-157">None</span></span>

## <span data-ttu-id="2f7b5-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f7b5-158">OUTPUTS</span></span>

### <span data-ttu-id="2f7b5-159">Microsoft. Azure. commands. Billing. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="2f7b5-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="2f7b5-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f7b5-160">NOTES</span></span>

## <span data-ttu-id="2f7b5-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f7b5-161">RELATED LINKS</span></span>
