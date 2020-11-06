---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 843bb68c5aebc18af60e1cc74915b269738059f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585467"
---
# <span data-ttu-id="2b3f5-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="2b3f5-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="2b3f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3f5-103">Acceptera eller avvisa villkor för ett angivet utgivare-ID (Publisher), kan du ge ID (Product) och plan-ID (namn).</span><span class="sxs-lookup"><span data-stu-id="2b3f5-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="2b3f5-104">Använd Get-AzureRmMarketplaceTerms för att få avtals villkoren.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b3f5-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b3f5-105">SYNTAX</span></span>

### <span data-ttu-id="2b3f5-106">AgreementAcceptParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2b3f5-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b3f5-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b3f5-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b3f5-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="2b3f5-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b3f5-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="2b3f5-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b3f5-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b3f5-110">DESCRIPTION</span></span>
<span data-ttu-id="2b3f5-111">Cmdleten **set-AzureRmMarketplaceTerms** sparar villkors objekt för angivet utgivare-ID (Publisher), och ger ID-nummer (Product) och ID-nummer för plan.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="2b3f5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b3f5-112">EXAMPLES</span></span>

### <span data-ttu-id="2b3f5-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2b3f5-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="2b3f5-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2b3f5-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="2b3f5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b3f5-115">PARAMETERS</span></span>

### <span data-ttu-id="2b3f5-116">-Acceptera</span><span class="sxs-lookup"><span data-stu-id="2b3f5-116">-Accept</span></span>
<span data-ttu-id="2b3f5-117">Godkänn detta för att acceptera de juridiska villkoren.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-117">Pass this to accept the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3f5-118">-DefaultProfile</span></span>
<span data-ttu-id="2b3f5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b3f5-120">-InputObject</span></span>
<span data-ttu-id="2b3f5-121">Termer-objekt som returneras i Get-AzureRmMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="2b3f5-122">Det här är en obligatorisk parameter om accepterad parameter är sant.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="2b3f5-123">-Name</span></span>
<span data-ttu-id="2b3f5-124">Plan identifierare för bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-124">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-125">-Produkt</span><span class="sxs-lookup"><span data-stu-id="2b3f5-125">-Product</span></span>
<span data-ttu-id="2b3f5-126">ID för den bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-126">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2b3f5-127">-Publisher</span></span>
<span data-ttu-id="2b3f5-128">Publisher-identifierare för den bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-128">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-129">-Avvisa</span><span class="sxs-lookup"><span data-stu-id="2b3f5-129">-Reject</span></span>
<span data-ttu-id="2b3f5-130">Godkänn detta för att avvisa de juridiska villkoren.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-130">Pass this to reject the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-131">-Villkor</span><span class="sxs-lookup"><span data-stu-id="2b3f5-131">-Terms</span></span>
<span data-ttu-id="2b3f5-132">Termer-objekt som returneras i Get-AzureRmMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="2b3f5-133">Det här är en obligatorisk parameter om accepterad parameter är sant.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2b3f5-134">-Confirm</span></span>
<span data-ttu-id="2b3f5-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b3f5-136">-WhatIf</span></span>
<span data-ttu-id="2b3f5-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b3f5-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3f5-139">CommonParameters</span></span>
<span data-ttu-id="2b3f5-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3f5-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b3f5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3f5-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b3f5-142">INPUTS</span></span>

### <span data-ttu-id="2b3f5-143">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="2b3f5-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="2b3f5-144">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="2b3f5-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="2b3f5-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b3f5-145">OUTPUTS</span></span>

### <span data-ttu-id="2b3f5-146">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="2b3f5-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="2b3f5-147">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="2b3f5-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="2b3f5-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b3f5-148">NOTES</span></span>

## <span data-ttu-id="2b3f5-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b3f5-149">RELATED LINKS</span></span>

