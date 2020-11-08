---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261239"
---
# <span data-ttu-id="4ed4a-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="4ed4a-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="4ed4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ed4a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed4a-103">Acceptera eller avvisa villkor för ett angivet utgivare-ID (Publisher), kan du ge ID (Product) och plan-ID (namn).</span><span class="sxs-lookup"><span data-stu-id="4ed4a-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="4ed4a-104">Använd Get-AzMarketplaceTerms för att få avtals villkoren.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="4ed4a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ed4a-105">SYNTAX</span></span>

### <span data-ttu-id="4ed4a-106">AgreementAcceptParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4ed4a-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ed4a-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ed4a-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ed4a-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ed4a-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ed4a-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ed4a-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed4a-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ed4a-110">DESCRIPTION</span></span>
<span data-ttu-id="4ed4a-111">Cmdleten **set-AzMarketplaceTerms** sparar villkors objekt för angivet utgivare-ID (Publisher), och ger ID-nummer (Product) och ID-nummer för plan.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="4ed4a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ed4a-112">EXAMPLES</span></span>

### <span data-ttu-id="4ed4a-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4ed4a-113">Example 1</span></span>
<span data-ttu-id="4ed4a-114">Skaffa ett marknads avtal för Marketplace</span><span class="sxs-lookup"><span data-stu-id="4ed4a-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="4ed4a-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4ed4a-115">Example 2</span></span>
<span data-ttu-id="4ed4a-116">Ställ in utgivarens avtal för "Accept".</span><span class="sxs-lookup"><span data-stu-id="4ed4a-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="4ed4a-117">Hämta värdet för "villkor"-parametern från cmdleten Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="4ed4a-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="4ed4a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ed4a-118">PARAMETERS</span></span>

### <span data-ttu-id="4ed4a-119">-Acceptera</span><span class="sxs-lookup"><span data-stu-id="4ed4a-119">-Accept</span></span>
<span data-ttu-id="4ed4a-120">Godkänn detta för att acceptera de juridiska villkoren.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed4a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed4a-121">-DefaultProfile</span></span>
<span data-ttu-id="4ed4a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed4a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ed4a-123">-InputObject</span></span>
<span data-ttu-id="4ed4a-124">Termer-objekt som returneras i Get-AzMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="4ed4a-125">Det här är en obligatorisk parameter om Accepted parameter är true.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed4a-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ed4a-126">-Name</span></span>
<span data-ttu-id="4ed4a-127">Plan identifierare för bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-127">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed4a-128">-Produkt</span><span class="sxs-lookup"><span data-stu-id="4ed4a-128">-Product</span></span>
<span data-ttu-id="4ed4a-129">ID för den bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-129">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed4a-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4ed4a-130">-Publisher</span></span>
<span data-ttu-id="4ed4a-131">Publisher-identifierare för den bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-131">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed4a-132">-Avvisa</span><span class="sxs-lookup"><span data-stu-id="4ed4a-132">-Reject</span></span>
<span data-ttu-id="4ed4a-133">Godkänn detta för att avvisa de juridiska villkoren.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed4a-134">-Villkor</span><span class="sxs-lookup"><span data-stu-id="4ed4a-134">-Terms</span></span>
<span data-ttu-id="4ed4a-135">Termer-objekt som returneras i Get-AzMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="4ed4a-136">Det här är en obligatorisk parameter om Accepted parameter är true.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed4a-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ed4a-137">-Confirm</span></span>
<span data-ttu-id="4ed4a-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed4a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed4a-139">-WhatIf</span></span>
<span data-ttu-id="4ed4a-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ed4a-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed4a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed4a-142">CommonParameters</span></span>
<span data-ttu-id="4ed4a-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed4a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed4a-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed4a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed4a-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ed4a-145">INPUTS</span></span>

### <span data-ttu-id="4ed4a-146">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="4ed4a-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="4ed4a-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ed4a-147">OUTPUTS</span></span>

### <span data-ttu-id="4ed4a-148">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="4ed4a-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="4ed4a-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ed4a-149">NOTES</span></span>

## <span data-ttu-id="4ed4a-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ed4a-150">RELATED LINKS</span></span>
