---
title: Installera Azure PowerShell på macOS eller Linux
description: Så här installerar du Azure PowerShell på macOS eller Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 47611281f67d68c9fc2686e0c6156b060a225158
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574489"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="5d989-103">Installera Azure PowerShell på macOS eller Linux</span><span class="sxs-lookup"><span data-stu-id="5d989-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="5d989-104">På plattformar som inte använder Windows är det möjligt att köra Azure PowerShell i PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="5d989-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="5d989-105">Den här versionen av PowerShell har skapats för användning på alla plattformar som har stöd för .NET Core.</span><span class="sxs-lookup"><span data-stu-id="5d989-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="5d989-106">En speciell .NET Core-version av Azure PowerShell finns tillgänglig för att arbeta med de här plattformarna.</span><span class="sxs-lookup"><span data-stu-id="5d989-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="5d989-107">För tillfället är både PowerShell Core v6 och Azure PowerShell för .NET Core fortfarande i betaversioner.</span><span class="sxs-lookup"><span data-stu-id="5d989-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="5d989-108">De här produkterna har begränsad support.</span><span class="sxs-lookup"><span data-stu-id="5d989-108">Support for these products is limited.</span></span> <span data-ttu-id="5d989-109">Skicka gärna in ett ärende till GitHub om du har problem eller upptäcker buggar.</span><span class="sxs-lookup"><span data-stu-id="5d989-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="5d989-110">Problem med PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="5d989-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="5d989-111">Problem med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d989-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="5d989-112">Installera PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="5d989-112">Install PowerShell Core</span></span>

<span data-ttu-id="5d989-113">Installationsanvisningarna för PowerShell Core är annorlunda för macOS och de flesta Linux-distributioner.</span><span class="sxs-lookup"><span data-stu-id="5d989-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="5d989-114">Detaljerade anvisningar finns i följande artikel:</span><span class="sxs-lookup"><span data-stu-id="5d989-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="5d989-115">Installera PowerShell Core på macOS</span><span class="sxs-lookup"><span data-stu-id="5d989-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="5d989-116">Installera PowerShell Core på Linux</span><span class="sxs-lookup"><span data-stu-id="5d989-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="5d989-117">Installera Azure PowerShell för .NET Core</span><span class="sxs-lookup"><span data-stu-id="5d989-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="5d989-118">I PowerShell Core är modulen PowerShellGet redan installerad.</span><span class="sxs-lookup"><span data-stu-id="5d989-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="5d989-119">Du måste ha utökade privilegier för att installera moduler i PowerShell, så du måste starta din session som en superanvändare:</span><span class="sxs-lookup"><span data-stu-id="5d989-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="5d989-120">Kör följande kommando för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5d989-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="5d989-121">Modulen `AzureRM` som beskrivs i andra artiklar är inte byggd för .NET Core och fungerar inte med PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="5d989-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="5d989-122">Både `AzureRM` och `AzureRM.NetCore` använder samma cmdlet-namn, så den enda skillnaden är namnet på den samlade modulen och vilken .NET-version de är skapade för att användas med.</span><span class="sxs-lookup"><span data-stu-id="5d989-122">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="5d989-123">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="5d989-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="5d989-124">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="5d989-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="5d989-125">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="5d989-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="5d989-126">Logga in</span><span class="sxs-lookup"><span data-stu-id="5d989-126">Sign in</span></span>

<span data-ttu-id="5d989-127">Du måste läsa in `AzureRM.Netcore` till din PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d989-127">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="5d989-128">Du behöver __inte__ ha några utökade privilegier för att importera en modul.</span><span class="sxs-lookup"><span data-stu-id="5d989-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="5d989-129">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="5d989-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="5d989-130">Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="5d989-130">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="5d989-131">Du bör arbeta med din profil genom miljövariabeln `$Profile` på macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="5d989-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="5d989-132">Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="5d989-132">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="5d989-133">Tillgängliga cmdlet:ar</span><span class="sxs-lookup"><span data-stu-id="5d989-133">Available cmdlets</span></span>

<span data-ttu-id="5d989-134">Azure PowerShell-moduler för .NET Core håller fortfarande på att utvecklas.</span><span class="sxs-lookup"><span data-stu-id="5d989-134">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="5d989-135">De här modulerna tillhandahåller inte den fullständiga uppsättningen cmdlet:ar som är tillgängliga för Windows-versionen av modulerna.</span><span class="sxs-lookup"><span data-stu-id="5d989-135">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="5d989-136">Följande funktioner är implementerade i AzureRM.Netcore-moduler:</span><span class="sxs-lookup"><span data-stu-id="5d989-136">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="5d989-137">Kontohantering</span><span class="sxs-lookup"><span data-stu-id="5d989-137">Account management</span></span>
  * <span data-ttu-id="5d989-138">Logga in med ett Microsoft-konto, organisationskonto eller tjänstens huvudnamn via Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5d989-138">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="5d989-139">Spara autentiseringsuppgifterna till disken med Save-AzureRmContext och läs in sparade autentiseringsuppgifter med Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5d989-139">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="5d989-140">Miljö</span><span class="sxs-lookup"><span data-stu-id="5d989-140">Environment</span></span>
  * <span data-ttu-id="5d989-141">Hämta andra Microsoft Azure-miljöer</span><span class="sxs-lookup"><span data-stu-id="5d989-141">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="5d989-142">Lägg till/Ange/Ta bort anpassade miljöer (t.ex. Azure Stack eller Windows Azure Pack-miljöer)</span><span class="sxs-lookup"><span data-stu-id="5d989-142">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="5d989-143">Cmdlet:ar på hanteringsnivå för Azure-tjänster med Resource Manager- och Service Management-gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="5d989-143">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="5d989-144">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="5d989-144">Virtual Machine</span></span>
  * <span data-ttu-id="5d989-145">App Service (Websites)</span><span class="sxs-lookup"><span data-stu-id="5d989-145">App Service (Websites)</span></span>
  * <span data-ttu-id="5d989-146">SQL Database</span><span class="sxs-lookup"><span data-stu-id="5d989-146">SQL Database</span></span>
  * <span data-ttu-id="5d989-147">Storage</span><span class="sxs-lookup"><span data-stu-id="5d989-147">Storage</span></span>
  * <span data-ttu-id="5d989-148">Nätverk</span><span class="sxs-lookup"><span data-stu-id="5d989-148">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="5d989-149">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="5d989-149">Next Steps</span></span>

<span data-ttu-id="5d989-150">Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="5d989-150">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
