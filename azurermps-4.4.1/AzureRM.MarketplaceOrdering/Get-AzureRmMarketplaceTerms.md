---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 29f3d645791dfa0b4f70ed936ccfcb4f72671038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585464"
---
# <span data-ttu-id="90d07-101">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="90d07-101">Get-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="90d07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90d07-102">SYNOPSIS</span></span>
<span data-ttu-id="90d07-103">Skaffa avtals villkoren för ett angivet utgivare-ID (Publisher), och ge ID (produkt) och abonnemangs-ID (namn).</span><span class="sxs-lookup"><span data-stu-id="90d07-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="90d07-104">Villkors objekt som returneras av det här kommandot ska överföras till Set-AzureRmMarketplaceTerms för att acceptera de juridiska villkoren.</span><span class="sxs-lookup"><span data-stu-id="90d07-104">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90d07-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90d07-105">SYNTAX</span></span>

```
Get-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90d07-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90d07-106">DESCRIPTION</span></span>
<span data-ttu-id="90d07-107">Cmdleten **Get-AzureRmMarketplaceTerms** returnerar villkoren för angivet utgivare-ID (Publisher), och ger ID-nummer (Product) och ID-nummer (Name).</span><span class="sxs-lookup"><span data-stu-id="90d07-107">The **Get-AzureRmMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="90d07-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90d07-108">EXAMPLES</span></span>

### <span data-ttu-id="90d07-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="90d07-109">Example 1</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="90d07-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90d07-110">PARAMETERS</span></span>

### <span data-ttu-id="90d07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d07-111">-DefaultProfile</span></span>
<span data-ttu-id="90d07-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90d07-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90d07-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="90d07-113">-Name</span></span>
<span data-ttu-id="90d07-114">Plan identifierare för bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="90d07-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d07-115">-Produkt</span><span class="sxs-lookup"><span data-stu-id="90d07-115">-Product</span></span>
<span data-ttu-id="90d07-116">ID för den bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="90d07-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d07-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="90d07-117">-Publisher</span></span>
<span data-ttu-id="90d07-118">Publisher-identifierare för den bild som distribueras.</span><span class="sxs-lookup"><span data-stu-id="90d07-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d07-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d07-119">CommonParameters</span></span>
<span data-ttu-id="90d07-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d07-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d07-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d07-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d07-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90d07-122">INPUTS</span></span>

### <span data-ttu-id="90d07-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="90d07-123">None</span></span>

## <span data-ttu-id="90d07-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90d07-124">OUTPUTS</span></span>

### <span data-ttu-id="90d07-125">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="90d07-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="90d07-126">Microsoft. Azure. commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="90d07-126">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="90d07-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90d07-127">NOTES</span></span>

## <span data-ttu-id="90d07-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90d07-128">RELATED LINKS</span></span>

