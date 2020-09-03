---
title: Azure-kontexter och autentiseringsuppgifter
description: Lär dig hur du återanvänder Azure-autentiseringsuppgifter och annan information över flera PowerShell-sessioner.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b6ac8b821f2d88431be67fd5fe1d50fc640d2b8f
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239799"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="2e8b0-103">Azure PowerShell-kontextobjekt</span><span class="sxs-lookup"><span data-stu-id="2e8b0-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="2e8b0-104">Azure PowerShell använder _Azure PowerShell-kontextobjekt_ (Azure-kontexter) för att lagra information om prenumeration och autentisering.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="2e8b0-105">Om du har mer än en prenumeration kan du använda Azure-kontexter för att välja den prenumeration som du vill köra Azure PowerShell-cmdletar på.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="2e8b0-106">Azure-kontexter används också för att lagra inloggningsinformation över flera PowerShell-sessioner och köra bakgrundsaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="2e8b0-107">Den här artikeln beskriver hur du hanterar Azure-kontexter, inte hantering av prenumerationer eller konton.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="2e8b0-108">Om du vill hantera användare, prenumerationer, klientorganisationer eller annan kontoinformation, se [Azure Active Directory](/azure/active-directory)-dokumentationen.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="2e8b0-109">När du har fått grepp om Azure-kontexter finns det information om hur du använder kontexter för att köra bakgrundsaktiviteter eller parallella uppgifter finns i [Använda Azure PowerShell-cmdletar i PowerShell-jobb](using-psjobs.md).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="2e8b0-110">Översikt över Azure-kontextobjekt</span><span class="sxs-lookup"><span data-stu-id="2e8b0-110">Overview of Azure context objects</span></span>

<span data-ttu-id="2e8b0-111">Azure-kontexter är PowerShell-objekt som representerar din aktiva prenumeration för att köra kommandon och den autentiseringsinformation som krävs för att ansluta till ett Azure-moln.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="2e8b0-112">Med Azure-kontexter behöver Azure PowerShell inte autentisera ditt konto varje gången du byter prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="2e8b0-113">En Azure-kontext består av följande:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-113">An Azure context consists of:</span></span>

* <span data-ttu-id="2e8b0-114">Det _konto_ som användes för att logga in på Azure med [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="2e8b0-115">Azure-kontexter behandlar användare, program-ID:n och tjänsters huvudnamn från ett kontoperspektiv.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="2e8b0-116">Den aktiva _prenumerationen_, ett serviceavtal med Microsoft om att skapa och köra Azure-resurser som är kopplade till en _klientorganisation_.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-116">The active _subscription_, a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="2e8b0-117">Klientorganisationer kallas ofta _organisationer_ i dokumentationen eller när du arbetar med Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="2e8b0-118">En referens till en _tokencache_, en lagrad autentiseringstoken för åtkomst till ett Azure-moln.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-118">A reference to a _token cache_, a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="2e8b0-119">Var denna token lagras och hur länge bestäms av [inställningen för att spara kontext automatiskt](#save-azure-contexts-across-powershell-sessions).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="2e8b0-120">Mer information om de här villkoren finns i [Azure Active Directory-terminologi](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="2e8b0-121">Autentiseringstokens som används av Azure-kontexter är samma som andra lagrade tokens som ingår i en beständig session.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span> 

<span data-ttu-id="2e8b0-122">När du loggar in med `Connect-AzAccount` skapas minst en Azure-kontext för din standardprenumeration.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="2e8b0-123">Objektet som returneras av `Connect-AzAccount` är standardkontexten som används för resten av PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="2e8b0-124">Hämta Azure-kontexter</span><span class="sxs-lookup"><span data-stu-id="2e8b0-124">Get Azure contexts</span></span>

<span data-ttu-id="2e8b0-125">Tillgängliga Azure-kontexter hämtas med cmdleten [get-AzContext](/powershell/module/az.accounts/get-azcontext).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="2e8b0-126">Lista alla tillgängliga kontexter med `-ListAvailable`:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="2e8b0-127">Eller hämta en kontext efter namn:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

<span data-ttu-id="2e8b0-128">Kontextnamn får vara ett annat än namnet på den associerade prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e8b0-129">De tillgängliga Azure-kontexterna __är inte__ alltid dina tillgängliga prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="2e8b0-130">Azure-kontexter representerar endast lokalt lagrad information.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="2e8b0-131">Du kan hämta dina prenumerationer med cmdleten [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="2e8b0-132">Skapa en ny Azure-kontext från prenumerationsinformation</span><span class="sxs-lookup"><span data-stu-id="2e8b0-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="2e8b0-133">Cmdleten [set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) används både för att skapa nya Azure-kontexter och ange dem som aktiv kontext.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="2e8b0-134">Det enklaste sättet att skapa en ny Azure-kontext är att använda befintlig prenumerationsinformation.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="2e8b0-135">Cmdleten är utformad för att ta utdataobjektet från `Get-AzSubscription` som ett pipelinevärde och konfigurera en ny Azure-kontext:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="2e8b0-136">Eller ange prenumerationsnamnet eller -ID och klientorganisations-ID om det behövs:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="2e8b0-137">Om argumentet `-Name` utelämnas används prenumerationens namn och ID som kontextnamn i formatet `Subscription Name (subscription-id)`.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="2e8b0-138">Ändra den aktiva Azure-kontexten</span><span class="sxs-lookup"><span data-stu-id="2e8b0-138">Change the active Azure context</span></span>

<span data-ttu-id="2e8b0-139">Både `Set-AzContext` och [Select-AzContext](/powershell/module/az.accounts/set-azcontext) kan användas för att ändra den aktiva Azure-kontexten.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext) can be used to change the active Azure context.</span></span> <span data-ttu-id="2e8b0-140">Som vi beskriver i [Skapa en ny Azure-kontext](#create-a-new-azure-context-from-subscription-information) skapar `Set-AzContext` en ny Azure-kontext för en prenumeration om den inte finns, och växlar sedan till att använda den kontexten som den aktiva.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="2e8b0-141">`Select-AzContext` är avsedd att användas med befintliga Azure-kontexter och fungerar på liknande sätt som med `Set-AzContext -Context`, men är utformad för användning med pipeline:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="2e8b0-142">Precis som många andra konto- och kontexthanteringskommandon i Azure PowerShell, har `Set-AzContext` och `Select-AzContext` stöd för argumentet `-Scope` så att du kan styra hur länge kontexten är aktiv.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="2e8b0-143">`-Scope` gör att du kan ändra en enskild sessions aktiva kontext utan att ändra standardvärdet:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="2e8b0-144">För att undvika att växla kontext för en hel PowerShell-session kan alla Azure PowerShell-kommandon köras mot en specifik kontext med argumentet `-AzContext`:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="2e8b0-145">Den andra huvudsakliga användningen av kontexter med Azure PowerShell-cmdletar är att köra bakgrundskommandon.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="2e8b0-146">Mer information om hur du kör PowerShell-jobb med Azure PowerShell finns i [Köra Azure PowerShell-cmdletar i PowerShell-jobb](using-psjobs.md).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="2e8b0-147">Spara Azure-kontexter mellan PowerShell-sessioner</span><span class="sxs-lookup"><span data-stu-id="2e8b0-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="2e8b0-148">Som standard sparas Azure-kontexter för användning mellan PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="2e8b0-149">Du kan ändra det här beteendet på följande sätt:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="2e8b0-150">Logga in med `-Scope Process` och `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="2e8b0-151">Azure-kontexten som returneras som en del av den här inloggningen är _endast_ giltig för den aktuella sessionen bara och sparas inte automatiskt, oavsett Azure PowerShell-inställningen för att spara kontext automatiskt.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="2e8b0-152">Inaktivera Azure Powershell-inställningen spara kontext automatiskt med cmdleten [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="2e8b0-153">Att du inaktivera inställningen spara kontext automatiskt rensar __inte__ alla lagrade tokens.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="2e8b0-154">Information om hur du rensar lagrad information om Azure-kontext finns i [Ta bort Azure-kontexter och autentiseringsuppgifter](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="2e8b0-155">Aktivera explicit inställningen spara Azure-kontext automatiskt kan aktiveras med cmdleten [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="2e8b0-156">När spara automatiskt är aktiverat lagras alla användares kontexter lokalt för senare PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="2e8b0-157">Spara kontexter manuellt med [Save-AzContext](/powershell/module/az.accounts/save-azcontext) som ska användas i framtida PowerShell-sessioner, där de kan läsas in med [import-AzContext](/powershell/module/az.accounts/import-azcontext):</span><span class="sxs-lookup"><span data-stu-id="2e8b0-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="2e8b0-158">Om du inaktiverar spara kontext automatiskt rensas __inte__ eventuell lagrad kontextinformation som sparats.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="2e8b0-159">Om du vill ta bort lagrad information använder du cmdleten [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="2e8b0-160">Mer information om hur du tar bort sparade kontexter finns i [Ta bort kontexter och autentiseringsuppgifter](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="2e8b0-161">Vart och ett av dessa kommandon har stöd för parametern `-Scope`, som kan ta ett värde om `Process` för att endast appliceras på den processen som körs för närvarande.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="2e8b0-162">Om du till exempel vill se till att nyligen skapade kontexter inte sparas när du har avslutat en PowerShell-session:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="2e8b0-163">Kontextinformation och tokens lagras i `$env:USERPROFILE\.Azure`-katalogen i Windows och på `$HOME/.Azure` på andra plattformar.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="2e8b0-164">Känslig information, till exempel prenumerations-ID och klientorganisations-ID kan fortfarande visas i lagrad information, via loggar eller sparade kontexter.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="2e8b0-165">Information om hur du rensar lagrad information finns i avsnittet [Ta bort kontexter och autentiseringsuppgifter](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="2e8b0-166">Ta bort Azure-kontexter och lagrade autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="2e8b0-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="2e8b0-167">Så här rensar du Azure-kontexter och autentiseringsuppgifter:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="2e8b0-168">Logga ut från ett konto med [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="2e8b0-169">Du kan logga ut från ett konto antingen via konto eller kontext:</span><span class="sxs-lookup"><span data-stu-id="2e8b0-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="2e8b0-170">Vid frånkoppling tas alltid lagrade autentiseringstokens bort och alla sparade kontexter som är kopplade till den frånkopplade användaren eller kontexten tas bort.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="2e8b0-171">Använd [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="2e8b0-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="2e8b0-172">Den här cmdleten garanterar att lagrade kontexter och autentiseringstoken tas bort. Dessutom blir du utloggad.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="2e8b0-173">Ta bort en kontext med [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span><span class="sxs-lookup"><span data-stu-id="2e8b0-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="2e8b0-174">Om du tar bort den aktiva kontexten kopplas du bort från Azure och måste autentiseras igen med `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="2e8b0-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e8b0-175">Se även</span><span class="sxs-lookup"><span data-stu-id="2e8b0-175">See also</span></span>

* [<span data-ttu-id="2e8b0-176">Köra Azure PowerShell-cmdletar i PowerShell-jobb</span><span class="sxs-lookup"><span data-stu-id="2e8b0-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="2e8b0-177">Azure Active Directory-terminologi</span><span class="sxs-lookup"><span data-stu-id="2e8b0-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="2e8b0-178">Referens för Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2e8b0-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)
