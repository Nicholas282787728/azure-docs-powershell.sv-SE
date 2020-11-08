---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089800"
---
# <span data-ttu-id="1fd1e-101">Modulen AZ. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1fd1e-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="1fd1e-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="1fd1e-102">Description</span></span>
<span data-ttu-id="1fd1e-103">I det här avsnittet beskrivs Azure PowerShell cmdlets för Azure MarketplaceOrdering i ramverket Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="1fd1e-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="1fd1e-104">Det finns cmdlets i Microsoft. Azure. commands. MarketplaceOrdering-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="1fd1e-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="1fd1e-105">De här cmdletarna gör att Azure-användare kan acceptera de juridiska villkoren för en marknads plats som möjliggör program mässig distribution för dessa lösningar.</span><span class="sxs-lookup"><span data-stu-id="1fd1e-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="1fd1e-106">Användare kan också avvisa en uppsättning juridiska villkor som redan har accepterats.</span><span class="sxs-lookup"><span data-stu-id="1fd1e-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="1fd1e-107">AZ. MarketplaceOrdering-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1fd1e-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="1fd1e-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="1fd1e-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="1fd1e-109">Skaffa avtals villkoren för ett angivet utgivare-ID (Publisher), och ge ID (produkt) och abonnemangs-ID (namn).</span><span class="sxs-lookup"><span data-stu-id="1fd1e-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="1fd1e-110">Villkors objekt som returneras av det här kommandot ska överföras till Set-AzMarketplaceTerms för att acceptera de juridiska villkoren.</span><span class="sxs-lookup"><span data-stu-id="1fd1e-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="1fd1e-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="1fd1e-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="1fd1e-112">Acceptera eller avvisa villkor för ett angivet utgivare-ID (Publisher), kan du ge ID (Product) och plan-ID (namn).</span><span class="sxs-lookup"><span data-stu-id="1fd1e-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="1fd1e-113">Använd Get-AzMarketplaceTerms för att få avtals villkoren.</span><span class="sxs-lookup"><span data-stu-id="1fd1e-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>
