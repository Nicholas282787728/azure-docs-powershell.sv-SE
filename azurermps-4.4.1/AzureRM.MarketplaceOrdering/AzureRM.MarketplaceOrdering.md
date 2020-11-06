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
# Modulen AzureRM. MarketplaceOrdering
## Problembeskrivning
I det här avsnittet beskrivs Azure PowerShell cmdlets för Azure MarketplaceOrdering i ramverket Azure Resource Manager (ARM). Det finns cmdlets i Microsoft. Azure. commands. MarketplaceOrdering-namnrymd. De här cmdletarna gör att Azure-användare kan acceptera de juridiska villkoren för en marknads plats som möjliggör en programmtic-distribution för dessa lösningar. Användare kan också avvisa en uppsättning juridiska villkor som redan har accepterats.

## AzureRM. MarketplaceOrdering-cmdletar
### [Get-AzureRmMarketplaceTerms](Get-AzureRmMarketplaceTerms.md)
Skaffa avtals villkoren för ett angivet utgivare-ID (Publisher), och ge ID (produkt) och abonnemangs-ID (namn). Villkors objekt som returneras av det här kommandot ska överföras till Set-AzureRmMarketplaceTerms för att acceptera de juridiska villkoren.

### [Set-AzureRmMarketplaceTerms](Set-AzureRmMarketplaceTerms.md)
Acceptera eller avvisa de juridiska villkoren för ett utgivar-ID (Publisher), kan du ge ID (Product) och plan-ID (namn). Använd Get-AzureRmMarketplaceTerms för att få avtals villkoren.

