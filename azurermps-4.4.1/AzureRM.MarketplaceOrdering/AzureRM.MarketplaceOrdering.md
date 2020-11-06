---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: f1446494d4eb68195ec0cefba248f519039a91ce
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93570711"
---
# <span data-ttu-id="8bf66-101">Modulen AzureRM. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8bf66-101">AzureRM.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="8bf66-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="8bf66-102">Description</span></span>
<span data-ttu-id="8bf66-103">I det här avsnittet beskrivs Azure PowerShell cmdlets för Azure MarketplaceOrdering i ramverket Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="8bf66-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="8bf66-104">Det finns cmdlets i Microsoft. Azure. commands. MarketplaceOrdering-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="8bf66-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="8bf66-105">De här cmdletarna gör att Azure-användare kan acceptera de juridiska villkoren för en marknads plats som möjliggör en programmtic-distribution för dessa lösningar.</span><span class="sxs-lookup"><span data-stu-id="8bf66-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmtic deployment for these solutions.</span></span> <span data-ttu-id="8bf66-106">Användare kan också avvisa en uppsättning juridiska villkor som redan har accepterats.</span><span class="sxs-lookup"><span data-stu-id="8bf66-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="8bf66-107">AzureRM. MarketplaceOrdering-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8bf66-107">AzureRM.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="8bf66-108">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="8bf66-108">Get-AzureRmMarketplaceTerms</span></span>](Get-AzureRmMarketplaceTerms.md)
<span data-ttu-id="8bf66-109">Skaffa avtals villkoren för ett angivet utgivare-ID (Publisher), och ge ID (produkt) och abonnemangs-ID (namn).</span><span class="sxs-lookup"><span data-stu-id="8bf66-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="8bf66-110">Villkors objekt som returneras av det här kommandot ska överföras till Set-AzureRmMarketplaceTerms för att acceptera de juridiska villkoren.</span><span class="sxs-lookup"><span data-stu-id="8bf66-110">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="8bf66-111">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="8bf66-111">Set-AzureRmMarketplaceTerms</span></span>](Set-AzureRmMarketplaceTerms.md)
<span data-ttu-id="8bf66-112">Acceptera eller avvisa de juridiska villkoren för ett utgivar-ID (Publisher), kan du ge ID (Product) och plan-ID (namn).</span><span class="sxs-lookup"><span data-stu-id="8bf66-112">Accept or reject the legal terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="8bf66-113">Använd Get-AzureRmMarketplaceTerms för att få avtals villkoren.</span><span class="sxs-lookup"><span data-stu-id="8bf66-113">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

