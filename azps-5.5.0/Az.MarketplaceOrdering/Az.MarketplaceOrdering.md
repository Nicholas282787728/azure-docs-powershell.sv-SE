---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214334"
---
# Az.MarketplaceOrdering-modul
## Beskrivning
Avsnitten i det här avsnittet innehåller Azure PowerShell-cmdlets för Azure MarketplaceOrdering i Azure Resource Manager-ramverket (ARM). Cmdletarna finns i namnområdet Microsoft.Azure.Commands.MarketplaceOrdering. Med de här cmdletarna kan Azure-användare godkänna de juridiska villkoren för ett marknadsplatserbjudande som möjliggör programmatisk distribution för dessa lösningar. Användare kan också avvisa en uppsättning juridiska termer som redan har accepterats.

## Az.MarketplaceOrdering-cmdlets
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Hämta avtalsvillkoren för ett visst utgivar-ID(Publisher), erbjudande-ID(Produkt) och abonnemangs-ID(Namn). Termobjektet som returneras av det här kommandot bör skickas till Set-AzMarketplaceTerms godkänna juridiska villkor.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Acceptera eller avvisa villkor för ett visst utgivar-ID(Publisher), erbjudande-ID(Produkt) och abonnemangs-ID(Namn). Använd Get-AzMarketplaceTerms för att hämta avtalsvillkoren.

