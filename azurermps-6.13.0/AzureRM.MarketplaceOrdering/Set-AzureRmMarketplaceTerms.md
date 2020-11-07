---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 7932a733fcd672d8ee92e6452765745281ee0a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755474"
---
# <span data-ttu-id="73683-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="73683-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="73683-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73683-102">SYNOPSIS</span></span>
<span data-ttu-id="73683-103">Acceptera eller avvisa villkor för ett angivet utgivare-ID (Publisher), kan du ge ID (Product) och plan-ID (namn).</span><span class="sxs-lookup"><span data-stu-id="73683-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="73683-104">Använd Get-AzureRmMarketplaceTerms för att få avtals villkoren.</span><span class="sxs-lookup"><span data-stu-id="73683-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73683-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73683-105">SYNTAX</span></span>

### <span data-ttu-id="73683-106">AgreementAcceptParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="73683-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73683-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73683-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73683-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="73683-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73683-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73683-109">InputObjectRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73683-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73683-110">DESCRIPTION</span></span>
<span data-ttu-id="73683-111">Cmdleten **set-AzureRmMarketplaceTerms** sparar villkors objekt för angivet utgivare-ID (Publisher), och ger ID-nummer (Product) och ID-nummer för plan.</span><span class="sxs-lookup"><span data-stu-id="73683-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="73683-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73683-112">EXAMPLES</span></span>

### <span data-ttu-id="73683-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73683-113">Example 1</span></span>
<span data-ttu-id="73683-114">Skaffa ett marknads avtal för Marketplace</span><span class="sxs-lookup"><span data-stu-id="73683-114">Get the marketplace publisher agreement</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

### <span data-ttu-id="73683-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="73683-115">Example 2</span></span>
<span data-ttu-id="73683-116">Ställ in utgivarens avtal för "Accept".</span><span class="sxs-lookup"><span data-stu-id="73683-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="73683-117">Hämta värdet för "villkor"-parametern från cmdleten Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="73683-117">Get the value for the 'Terms' parameter from the 'Get-AzureRmMarketplaceTerms' cmdlet</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```


## <span data-ttu-id="73683-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73683-118">PARAMETERS</span></span>

### <span data-ttu-id="73683-119">-Acceptera</span><span class="sxs-lookup"><span data-stu-id="73683-119">-Accept</span></span>
<span data-ttu-id="73683-120">Godkänn detta för att acceptera de juridiska villkoren.</span><span class="sxs-lookup"><span data-stu-id="73683-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73683-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73683-121">-DefaultProfile</span></span>
<span data-ttu-id="73683-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73683-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73683-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73683-123">-InputObject</span></span>
<span data-ttu-id="73683-124">Termer-objekt som returneras i Get-AzureRmMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73683-124">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="73683-125">Det här är en obligatorisk parameter om accepterad parameter är sant.</span><span class="sxs-lookup"><span data-stu-id="73683-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73683-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="73683-126">-Name</span></span>
<span data-ttu-id="73683-127">Plan identifierare för bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="73683-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="73683-128">-Produkt</span><span class="sxs-lookup"><span data-stu-id="73683-128">-Product</span></span>
<span data-ttu-id="73683-129">ID för den bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="73683-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="73683-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="73683-130">-Publisher</span></span>
<span data-ttu-id="73683-131">Publisher-identifierare för den bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="73683-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="73683-132">-Avvisa</span><span class="sxs-lookup"><span data-stu-id="73683-132">-Reject</span></span>
<span data-ttu-id="73683-133">Godkänn detta för att avvisa de juridiska villkoren.</span><span class="sxs-lookup"><span data-stu-id="73683-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73683-134">-Villkor</span><span class="sxs-lookup"><span data-stu-id="73683-134">-Terms</span></span>
<span data-ttu-id="73683-135">Termer-objekt som returneras i Get-AzureRmMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73683-135">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="73683-136">Det här är en obligatorisk parameter om accepterad parameter är sant.</span><span class="sxs-lookup"><span data-stu-id="73683-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="73683-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73683-137">-Confirm</span></span>
<span data-ttu-id="73683-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73683-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73683-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73683-139">-WhatIf</span></span>
<span data-ttu-id="73683-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73683-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73683-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73683-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73683-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73683-142">CommonParameters</span></span>
<span data-ttu-id="73683-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73683-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73683-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73683-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73683-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73683-145">INPUTS</span></span>

### <span data-ttu-id="73683-146">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="73683-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="73683-147">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="73683-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="73683-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73683-148">OUTPUTS</span></span>

### <span data-ttu-id="73683-149">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="73683-149">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="73683-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73683-150">NOTES</span></span>

## <span data-ttu-id="73683-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73683-151">RELATED LINKS</span></span>
