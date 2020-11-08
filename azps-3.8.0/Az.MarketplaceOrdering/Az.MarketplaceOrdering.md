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
# Modulen AZ. MarketplaceOrdering
## Problembeskrivning
I det här avsnittet beskrivs Azure PowerShell cmdlets för Azure MarketplaceOrdering i ramverket Azure Resource Manager (ARM). Det finns cmdlets i Microsoft. Azure. commands. MarketplaceOrdering-namnrymd. De här cmdletarna gör att Azure-användare kan acceptera de juridiska villkoren för en marknads plats som möjliggör program mässig distribution för dessa lösningar. Användare kan också avvisa en uppsättning juridiska villkor som redan har accepterats.

## AZ. MarketplaceOrdering-cmdletar
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Skaffa avtals villkoren för ett angivet utgivare-ID (Publisher), och ge ID (produkt) och abonnemangs-ID (namn). Villkors objekt som returneras av det här kommandot ska överföras till Set-AzMarketplaceTerms för att acceptera de juridiska villkoren.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Acceptera eller avvisa villkor för ett angivet utgivare-ID (Publisher), kan du ge ID (Product) och plan-ID (namn). Använd Get-AzMarketplaceTerms för att få avtals villkoren.

