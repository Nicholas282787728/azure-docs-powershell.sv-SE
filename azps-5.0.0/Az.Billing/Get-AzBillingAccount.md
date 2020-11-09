---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323952"
---
# <span data-ttu-id="9a4db-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="9a4db-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="9a4db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a4db-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4db-103">Skaffa fakturerings konton.</span><span class="sxs-lookup"><span data-stu-id="9a4db-103">Get billing accounts.</span></span>

## <span data-ttu-id="9a4db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a4db-104">SYNTAX</span></span>

### <span data-ttu-id="9a4db-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="9a4db-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a4db-106">Enda</span><span class="sxs-lookup"><span data-stu-id="9a4db-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a4db-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a4db-107">DESCRIPTION</span></span>
<span data-ttu-id="9a4db-108">Cmdleten **Get-AzBillingAccount** använder fakturerings konton, användaren har åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="9a4db-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="9a4db-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a4db-109">EXAMPLES</span></span>

### <span data-ttu-id="9a4db-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a4db-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="9a4db-111">Få alla fakturerings konton som användaren har åtkomst till.</span><span class="sxs-lookup"><span data-stu-id="9a4db-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="9a4db-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9a4db-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="9a4db-113">Skaffa fakturerings kontot med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="9a4db-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="9a4db-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9a4db-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="9a4db-115">Få alla fakturerings konton som användaren har åtkomst till och inkludera adressen i resultatet.</span><span class="sxs-lookup"><span data-stu-id="9a4db-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="9a4db-116">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="9a4db-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="9a4db-117">Skaffa alla fakturerings konton användare har till gång till och inkludera fakturerings profilerna i resultatet.</span><span class="sxs-lookup"><span data-stu-id="9a4db-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="9a4db-118">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="9a4db-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="9a4db-119">Få alla fakturerings konton som användaren har åtkomst till och inkludera avsnitten fakturerings profiler och faktura under dem i resultatet.</span><span class="sxs-lookup"><span data-stu-id="9a4db-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="9a4db-120">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="9a4db-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="9a4db-121">Skaffa fakturerings kontot med det angivna namnet och inkludera avsnitten adress, fakturering och faktura under dem i resultatet.</span><span class="sxs-lookup"><span data-stu-id="9a4db-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="9a4db-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a4db-122">PARAMETERS</span></span>

### <span data-ttu-id="9a4db-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4db-123">-DefaultProfile</span></span>
<span data-ttu-id="9a4db-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9a4db-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a4db-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="9a4db-125">-IncludeAddress</span></span>
<span data-ttu-id="9a4db-126">Ta med adressen till fakturerings kontot.</span><span class="sxs-lookup"><span data-stu-id="9a4db-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="9a4db-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="9a4db-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="9a4db-128">Ta med fakturerings profiler under fakturerings kontot.</span><span class="sxs-lookup"><span data-stu-id="9a4db-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="9a4db-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="9a4db-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="9a4db-130">Ta med fakturerings profilerna under fakturerings konto och fakturor under dem.</span><span class="sxs-lookup"><span data-stu-id="9a4db-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="9a4db-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a4db-131">-Name</span></span>
<span data-ttu-id="9a4db-132">Namn på ett specifikt fakturerings konto.</span><span class="sxs-lookup"><span data-stu-id="9a4db-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="9a4db-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="9a4db-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="9a4db-134">Visa en lista med fakturerings enheter under fakturerings konto som kan användas som indata för att skapa abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9a4db-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a4db-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4db-135">CommonParameters</span></span>
<span data-ttu-id="9a4db-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a4db-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4db-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a4db-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4db-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a4db-138">INPUTS</span></span>

### <span data-ttu-id="9a4db-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="9a4db-139">None</span></span>

## <span data-ttu-id="9a4db-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a4db-140">OUTPUTS</span></span>

### <span data-ttu-id="9a4db-141">Microsoft. Azure. commands. Billing. Models. PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="9a4db-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="9a4db-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a4db-142">NOTES</span></span>

## <span data-ttu-id="9a4db-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a4db-143">RELATED LINKS</span></span>
