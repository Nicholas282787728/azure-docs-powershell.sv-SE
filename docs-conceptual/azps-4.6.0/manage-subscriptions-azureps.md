---
title: Hantera Azure-prenumerationer med Azure PowerShell
description: Hantera Azure-prenumerationer med Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 96b94ffcb5075764eb5d2dcaec7b13c5933b83da
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242196"
---
# <a name="use-multiple-azure-subscriptions"></a>Använda flera Azure-prenumerationer

De flesta Azure-användare har bara en enstaka prenumeration. Om du däremot är en del av mer än en organisation eller om din organisation har delat upp åtkomst till vissa resurser i grupper kan du ha flera prenumerationer i Azure. CLI har stöd för att välja en prenumeration både globalt och per kommando.

Detaljerad information om prenumerationer, fakturering och kostnadshantering finns i [dokumentationen om fakturering och kostnadshantering](/azure/billing/).

## <a name="tenants-users-and-subscriptions"></a>Klienter, användare och prenumerationer

Du kanske funderar över skillnaden mellan klienter, användare och prenumerationer i Azure. En _klient_ är den Azure Active Directory-enhet som omfattar hela organisationen. Klienten har minst en _prenumeration_ och _användare_. En användare är en person och är endast associerad till en klient, vilken är organisationen som användaren tillhör. Användare är de konton som loggar in på Azure för att skapa, hantera och använda resurser.
En användare kan ha åtkomst till flera _prenumerationer_, som är avtal med Microsoft för användning av molntjänster, inklusive Azure. Varje resurs är associerad med en prenumeration.

Om du vill veta mer om skillnaderna mellan klienter, användare och prenumerationer kan du läsa [ordlistan för molnterminologi i Azure](/azure/azure-glossary-cloud-terminology).  Om du vill lära dig att lägga till en ny prenumeration till din Azure Active Directory-klientorganisation läser du [Associera eller lägg till en Azure-prenumeration till din Azure Active Directory-klientorganisation](/azure/active-directory/active-directory-how-subscriptions-associated-directory).
Information om hur du loggar in på en specifik klient finns i [Logga in med Azure PowerShell](/powershell/azure/authenticate-azureps).

## <a name="change-the-active-subscription"></a>Ändra den aktiva prenumerationen

Du måste ändra prenumerationen som är associerad med den aktuella Azure-sessionen för att få tillgång till resurserna för en prenumeration i Azure PowerShell.
Du gör detta genom att ändra den aktiva sessionens kontext, det vill säga informationen om vilken klientorganisation, prenumeration, samt användar-cmdletar som ska köras.
Om du vill ändra prenumeration måste ett Azure PowerShell-kontextobjekt först hämtas med [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) och sedan måste den nuvarande kontexten ändras med [Set-AzContext](/powershell/module/az.accounts/set-azcontext).

Följande exempel visar hur du skaffar en prenumeration i den aktiva klientorganisationen och ställer in den som den aktiva sessionen:

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

Läs informationen om att [spara autentiseringsuppgifter med Azure PowerShell-kontexter](context-persistence.md) för att lära dig mer om Azure PowerShell-kontexter, inklusive hur du sparar dem och snabbt växlar mellan dem för att arbeta med flera prenumerationer på ett enkelt sätt.
