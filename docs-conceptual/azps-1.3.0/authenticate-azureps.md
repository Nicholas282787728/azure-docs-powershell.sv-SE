---
title: Logga in med Azure PowerShell
description: Så här loggar du in med Azure PowerShell som användare, med tjänstens huvudnamn eller med hanterade identiteter för Azure-resurser.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/12/2019
ms.locfileid: "56145267"
---
# <a name="sign-in-with-azure-powershell"></a>Logga in med Azure PowerShell

Azure PowerShell har stöd för flera autentiseringsmetoder. Det enklaste sättet att komma igång är med [Azure Cloud Shell](/azure/cloud-shell/overview), som automatiskt loggar in dig. Med en lokal installation kan du logga in interaktivt via webbläsaren. När du skriver skript för automatisering är den rekommenderade metoden att använda ett [tjänsthuvudnamn](create-azure-service-principal-azureps.md) med de nödvändiga behörigheterna. Du kan skydda dina Azure-resurser genom att begränsa behörigheterna för inloggning så mycket som möjligt.

När du har loggat in körs kommandon mot standardprenumerationen. Använd cmdleten [Set-AzContext](/powershell/module/az.accounts/set-azcontext) för att ändra din aktiva prenumeration för en session. Använd [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) för att ändra standardprenumerationen som används när du loggar in med Azure PowerShell.

> [!IMPORTANT]
>
> Dina autentiseringsuppgifter delas mellan flera PowerShell-sessioner så länge du är inloggad.
> Mer information finns i artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).

## <a name="sign-in-interactively"></a>Logga in interaktivt

Använd cmdleten [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) för att logga in interaktivt.

```azurepowershell-interactive
Connect-AzAccount
```

När du kör cmdleten visas en tokensträng. Kopiera den här strängen och klistra in den i https://microsoft.com/devicelogin i en webbläsare för att logga in. PowerShell-sessionen autentiseras därefter för anslutning till Azure.

## <a name="sign-in-with-credentials"></a>Logga in med autentiseringsuppgifter

Du kan även logga in med ett `PSCredential`-objekt som har behörighet för att ansluta till Azure.
Det enklaste sättet att hämta ett autentiseringsuppgiftsobjekt är med en [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential)-cmdlet. När den körs uppmanas du att ange ett användarnamn och ett lösenord.

> [!Note]
> Den här metoden fungerar inte med Microsoft-konton eller konton som har tvåfaktorsautentisering aktiverad.

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a>Logga in med ett huvudnamn för tjänsten

Tjänstens huvudnamn är icke-interaktiva Azure-konton. Precis som med andra användarkonton hanteras deras behörigheter med Azure Active Directory. Genom att endast bevilja de behörigheter som krävs för tjänstens huvudnamn skyddas dina automatiseringsskript.

I [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) finns information om hur du skapar ett huvudnamn för tjänsten som ska användas med Azure PowerShell.

Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzAccount` för att logga in med ett huvudnamn för tjänsten. Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn. Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn. Cmdleten visar en uppmaning om att ange användar-ID och lösenord för tjänstens huvudnamn.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a>Logga in med en hanterad identitet 

Hanterade identiteter är en funktion i Azure Active Directory. Hanterade identiteter är tjänsthuvudnamn som tilldelats till resurser som körs i Azure. Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser. Hanterade identiteter är endast tillgängliga på resurser som körs i ett Azure-moln.

Om du vill lära dig mer om hanterade identiteter för Azure-resurser kan du läsa [Använda hanterade identiteter för Azure-resurser på en virtuell Azure-dator för att hämta en åtkomsttoken](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Logga in med en klientorganisation som inte är standard eller som molnlösningsleverantör (CSP)

Om ditt konto är associerat med fler än en klientorganisation måste du använda parametern `-TenantId` när du ansluter för att logga in. Den här parametern fungerar med alla andra inloggningsmetoder. När du loggar in kan det här parametervärdet antingen vara klientorganisationens objekt-ID för Azure (klient-ID) eller det fullständigt kvalificerade domännamnet för klientorganisationen.

Om du är [molnlösningsleverantör (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) **måste** värdet `-TenantId` vara ett klient-ID.

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Logga in på ett annat moln

Azures molntjänster erbjuder miljöer som följer regionala lagar för datahantering.
För konton i ett regionalt moln anger du miljön när du loggar in med argumentet `-Environment`.
Om ditt konto till exempel finns i Kina-molnet:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Följande kommando hämtar en lista över tillgängliga miljöer:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```