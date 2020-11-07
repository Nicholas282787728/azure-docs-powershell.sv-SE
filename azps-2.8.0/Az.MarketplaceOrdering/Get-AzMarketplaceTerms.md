---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 730861b055259fd0aee5490de2421abe96afc10b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743636"
---
# <span data-ttu-id="b0b4a-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="b0b4a-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="b0b4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b4a-103">Skaffa avtals villkoren för ett angivet utgivare-ID (Publisher), och ge ID (produkt) och abonnemangs-ID (namn).</span><span class="sxs-lookup"><span data-stu-id="b0b4a-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="b0b4a-104">Villkors objekt som returneras av det här kommandot ska överföras till Set-AzMarketplaceTerms för att acceptera de juridiska villkoren.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="b0b4a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0b4a-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0b4a-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0b4a-106">DESCRIPTION</span></span>
<span data-ttu-id="b0b4a-107">Cmdleten **Get-AzMarketplaceTerms** returnerar villkoren för angivet utgivare-ID (Publisher), och ger ID-nummer (Product) och ID-nummer (Name).</span><span class="sxs-lookup"><span data-stu-id="b0b4a-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="b0b4a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0b4a-108">EXAMPLES</span></span>

### <span data-ttu-id="b0b4a-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b0b4a-109">Example 1</span></span>
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="b0b4a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0b4a-110">PARAMETERS</span></span>

### <span data-ttu-id="b0b4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b4a-111">-DefaultProfile</span></span>
<span data-ttu-id="b0b4a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b4a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0b4a-113">-Name</span></span>
<span data-ttu-id="b0b4a-114">Plan identifierare för bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="b0b4a-115">-Produkt</span><span class="sxs-lookup"><span data-stu-id="b0b4a-115">-Product</span></span>
<span data-ttu-id="b0b4a-116">ID för den bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="b0b4a-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b0b4a-117">-Publisher</span></span>
<span data-ttu-id="b0b4a-118">Publisher-identifierare för den bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="b0b4a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b4a-119">CommonParameters</span></span>
<span data-ttu-id="b0b4a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b4a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b4a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0b4a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b4a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0b4a-122">INPUTS</span></span>

### <span data-ttu-id="b0b4a-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="b0b4a-123">None</span></span>

## <span data-ttu-id="b0b4a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0b4a-124">OUTPUTS</span></span>

### <span data-ttu-id="b0b4a-125">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="b0b4a-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="b0b4a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0b4a-126">NOTES</span></span>

## <span data-ttu-id="b0b4a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0b4a-127">RELATED LINKS</span></span>
