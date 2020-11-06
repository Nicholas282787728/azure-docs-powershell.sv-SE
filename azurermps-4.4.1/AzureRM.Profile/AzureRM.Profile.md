---
Module Name: AzureRM.Profile
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
ms.openlocfilehash: bc3ccc2c2b0574eee40357fb0079fe22124ea3e6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571180"
---
# <span data-ttu-id="e85ee-101">AzureRM. Profile-modul</span><span class="sxs-lookup"><span data-stu-id="e85ee-101">AzureRM.Profile Module</span></span>
## <span data-ttu-id="e85ee-102">Problembeskrivning</span><span class="sxs-lookup"><span data-stu-id="e85ee-102">Description</span></span>
<span data-ttu-id="e85ee-103">Hanterar autentiseringsuppgifter och gemensam konfiguration för alla Azure-moduler.</span><span class="sxs-lookup"><span data-stu-id="e85ee-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="e85ee-104">AzureRM. profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e85ee-104">AzureRM.Profile Cmdlets</span></span>
### [<span data-ttu-id="e85ee-105">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="e85ee-105">Add-AzureRmAccount</span></span>](Add-AzureRmAccount.md)
<span data-ttu-id="e85ee-106">Lägger till ett autentiserat konto som ska användas för Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="e85ee-106">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="e85ee-107">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="e85ee-107">Add-AzureRmEnvironment</span></span>](Add-AzureRmEnvironment.md)
<span data-ttu-id="e85ee-108">Lägger till slut punkter och metadata för en instans av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e85ee-108">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="e85ee-109">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e85ee-109">Clear-AzureRmContext</span></span>](Clear-AzureRmContext.md)
<span data-ttu-id="e85ee-110">Ta bort all information om Azure-autentiseringsuppgifter,-konto och-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="e85ee-110">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="e85ee-111">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="e85ee-111">Disable-AzureRmContextAutosave</span></span>](Disable-AzureRmContextAutosave.md)
<span data-ttu-id="e85ee-112">Inaktivera Spara autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="e85ee-112">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="e85ee-113">Din inloggnings information blir glömt nästa gång du öppnar ett PowerShell-fönster</span><span class="sxs-lookup"><span data-stu-id="e85ee-113">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="e85ee-114">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="e85ee-114">Disable-AzureRmDataCollection</span></span>](Disable-AzureRmDataCollection.md)
<span data-ttu-id="e85ee-115">Det går inte att samla in data för att förbättra AzurePowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e85ee-115">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="e85ee-116">Data samlas in såvida du inte uttryckligen väljer.</span><span class="sxs-lookup"><span data-stu-id="e85ee-116">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="e85ee-117">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="e85ee-117">Enable-AzureRmContextAutosave</span></span>](Enable-AzureRmContextAutosave.md)
<span data-ttu-id="e85ee-118">Tillåt att Azure-autentiseringsuppgiften, konto-och prenumerations information sparas och läses in automatiskt när du öppnar ett PowerShell-fönster.</span><span class="sxs-lookup"><span data-stu-id="e85ee-118">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="e85ee-119">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="e85ee-119">Enable-AzureRmDataCollection</span></span>](Enable-AzureRmDataCollection.md)
<span data-ttu-id="e85ee-120">Gör att Azure PowerShell samlar in data för att förbättra användar upplevelsen med AzurePowerShell cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e85ee-120">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="e85ee-121">Kör den här cmdleten till data insamling för den aktuella användaren på den aktuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e85ee-121">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="e85ee-122">Inga data samlas in om du inte uttryckligen väljer.</span><span class="sxs-lookup"><span data-stu-id="e85ee-122">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="e85ee-123">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e85ee-123">Get-AzureRmContext</span></span>](Get-AzureRmContext.md)
<span data-ttu-id="e85ee-124">Hämtar de metadata som används för att autentisera Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="e85ee-124">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="e85ee-125">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="e85ee-125">Get-AzureRmContextAutosaveSetting</span></span>](Get-AzureRmContextAutosaveSetting.md)
<span data-ttu-id="e85ee-126">Visa metadata om funktionen för Autospara med kontext, inklusive whterh kontexten sparas automatiskt och där Sparad kontext och autentiseringsinformation kan hittas.</span><span class="sxs-lookup"><span data-stu-id="e85ee-126">Display metadata about the context autosave feature, including whterh the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="e85ee-127">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="e85ee-127">Get-AzureRmEnvironment</span></span>](Get-AzureRmEnvironment.md)
<span data-ttu-id="e85ee-128">Hämta slut punkter och metadata för en instans av Azure-tjänster.</span><span class="sxs-lookup"><span data-stu-id="e85ee-128">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="e85ee-129">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="e85ee-129">Get-AzureRmSubscription</span></span>](Get-AzureRmSubscription.md)
<span data-ttu-id="e85ee-130">Få prenumerationer som det aktuella kontot kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="e85ee-130">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="e85ee-131">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="e85ee-131">Get-AzureRmTenant</span></span>](Get-AzureRmTenant.md)
<span data-ttu-id="e85ee-132">Får klient organisationer som har behörighet för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="e85ee-132">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="e85ee-133">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e85ee-133">Import-AzureRmContext</span></span>](Import-AzureRmContext.md)
<span data-ttu-id="e85ee-134">Läser in Azure-autentiseringsinformation från en fil.</span><span class="sxs-lookup"><span data-stu-id="e85ee-134">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="e85ee-135">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="e85ee-135">Remove-AzureRmAccount</span></span>](Remove-AzureRmAccount.md)
<span data-ttu-id="e85ee-136">Ta bort alla autentiseringsuppgifter och sammanhang som är associerade med detta konto.</span><span class="sxs-lookup"><span data-stu-id="e85ee-136">Remove all credentials and contexts associated with this account.</span></span>

### [<span data-ttu-id="e85ee-137">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e85ee-137">Remove-AzureRmContext</span></span>](Remove-AzureRmContext.md)
<span data-ttu-id="e85ee-138">Ta bort en kontext från uppsättningen tillgängliga kontexter</span><span class="sxs-lookup"><span data-stu-id="e85ee-138">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="e85ee-139">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="e85ee-139">Remove-AzureRmEnvironment</span></span>](Remove-AzureRmEnvironment.md)
<span data-ttu-id="e85ee-140">Tar bort slut punkter och metadata för anslutning till en viss Azure-instans.</span><span class="sxs-lookup"><span data-stu-id="e85ee-140">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="e85ee-141">Rename – AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e85ee-141">Rename-AzureRmContext</span></span>](Rename-AzureRmContext.md)
<span data-ttu-id="e85ee-142">Byta namn på en Azure-kontext.</span><span class="sxs-lookup"><span data-stu-id="e85ee-142">Rename an Azure context.</span></span>  <span data-ttu-id="e85ee-143">Som standard får kontexterna namn av användar konto och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e85ee-143">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="e85ee-144">Lös-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="e85ee-144">Resolve-AzureRmError</span></span>](Resolve-AzureRmError.md)
<span data-ttu-id="e85ee-145">Visa detaljerad information om PowerShell-fel med utökad information för Azure PowerShell-fel.</span><span class="sxs-lookup"><span data-stu-id="e85ee-145">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="e85ee-146">Spara – AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e85ee-146">Save-AzureRmContext</span></span>](Save-AzureRmContext.md)
<span data-ttu-id="e85ee-147">Sparar den aktuella Autentiseringsinformationen för användning i andra PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="e85ee-147">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="e85ee-148">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e85ee-148">Select-AzureRmContext</span></span>](Select-AzureRmContext.md)
<span data-ttu-id="e85ee-149">Välj ett abonnemang för målet (eller kontot, innehavaren) i Azure PowerShell-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e85ee-149">Select a subscription to target (or account, tenant) in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="e85ee-150">Skicka feedback</span><span class="sxs-lookup"><span data-stu-id="e85ee-150">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="e85ee-151">Skickar feedback till Azure PowerShell-gruppen via en uppsättning instruktioner.</span><span class="sxs-lookup"><span data-stu-id="e85ee-151">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="e85ee-152">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e85ee-152">Set-AzureRmContext</span></span>](Set-AzureRmContext.md)
<span data-ttu-id="e85ee-153">Anger klient organisation, prenumeration och miljö för cmdlets som ska användas i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="e85ee-153">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="e85ee-154">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="e85ee-154">Set-AzureRmEnvironment</span></span>](Set-AzureRmEnvironment.md)
<span data-ttu-id="e85ee-155">Anger egenskaper för en Azure-miljö.</span><span class="sxs-lookup"><span data-stu-id="e85ee-155">Sets properties for an Azure environment.</span></span>

