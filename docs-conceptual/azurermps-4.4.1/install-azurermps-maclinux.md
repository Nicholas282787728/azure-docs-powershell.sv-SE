---
title: Installera Azure PowerShell på macOS eller Linux
description: Så här installerar du Azure PowerShell på macOS eller Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 936bb24eecb4077080e172bf0d29fe57ec652187
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/12/2019
ms.locfileid: "56154100"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="acb56-103">Installera Azure PowerShell på macOS eller Linux</span><span class="sxs-lookup"><span data-stu-id="acb56-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="acb56-104">På plattformar som inte använder Windows är det möjligt att köra Azure PowerShell i PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="acb56-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="acb56-105">Den här versionen av PowerShell har skapats för användning på alla plattformar som har stöd för .NET Core.</span><span class="sxs-lookup"><span data-stu-id="acb56-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="acb56-106">En speciell .NET Core-version av Azure PowerShell finns tillgänglig för att arbeta med de här plattformarna.</span><span class="sxs-lookup"><span data-stu-id="acb56-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

## <a name="install-powershell-core"></a><span data-ttu-id="acb56-107">Installera PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="acb56-107">Install PowerShell Core</span></span>

<span data-ttu-id="acb56-108">Installationsanvisningarna för PowerShell Core är annorlunda för macOS och de flesta Linux-distributioner.</span><span class="sxs-lookup"><span data-stu-id="acb56-108">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="acb56-109">Detaljerade anvisningar finns i följande artikel:</span><span class="sxs-lookup"><span data-stu-id="acb56-109">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="acb56-110">Installera PowerShell Core på macOS</span><span class="sxs-lookup"><span data-stu-id="acb56-110">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="acb56-111">Installera PowerShell Core på Linux</span><span class="sxs-lookup"><span data-stu-id="acb56-111">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="acb56-112">Installera Azure PowerShell för .NET Core</span><span class="sxs-lookup"><span data-stu-id="acb56-112">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="acb56-113">I PowerShell Core är modulen PowerShellGet redan installerad.</span><span class="sxs-lookup"><span data-stu-id="acb56-113">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="acb56-114">Du måste ha utökade privilegier för att installera moduler i PowerShell, så du måste starta din session som en superanvändare:</span><span class="sxs-lookup"><span data-stu-id="acb56-114">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="acb56-115">Kör följande kommando för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="acb56-115">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="acb56-116">Modulen `AzureRM` som beskrivs i andra artiklar är inte byggd för .NET Core och fungerar inte med PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="acb56-116">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="acb56-117">Både `AzureRM` och `AzureRM.NetCore` använder samma cmdlet-namn, så den enda skillnaden är namnet på den samlade modulen och vilken .NET-version de är skapade för att användas med.</span><span class="sxs-lookup"><span data-stu-id="acb56-117">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="acb56-118">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="acb56-118">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="acb56-119">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="acb56-119">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="acb56-120">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="acb56-120">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="acb56-121">Logga in</span><span class="sxs-lookup"><span data-stu-id="acb56-121">Sign in</span></span>

<span data-ttu-id="acb56-122">Du måste läsa in `AzureRM.Netcore` till din PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="acb56-122">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="acb56-123">Du behöver __inte__ ha några utökade privilegier för att importera en modul.</span><span class="sxs-lookup"><span data-stu-id="acb56-123">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="acb56-124">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="acb56-124">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="acb56-125">Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="acb56-125">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="acb56-126">Du bör arbeta med din profil genom miljövariabeln `$Profile` på macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="acb56-126">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="acb56-127">Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="acb56-127">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="acb56-128">Tillgängliga cmdlet:ar</span><span class="sxs-lookup"><span data-stu-id="acb56-128">Available cmdlets</span></span>

<span data-ttu-id="acb56-129">Azure PowerShell-moduler för .NET Core håller fortfarande på att utvecklas.</span><span class="sxs-lookup"><span data-stu-id="acb56-129">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="acb56-130">De här modulerna tillhandahåller inte den fullständiga uppsättningen cmdlet:ar som är tillgängliga för Windows-versionen av modulerna.</span><span class="sxs-lookup"><span data-stu-id="acb56-130">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="acb56-131">Följande funktioner är implementerade i AzureRM.Netcore-moduler:</span><span class="sxs-lookup"><span data-stu-id="acb56-131">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="acb56-132">Kontohantering</span><span class="sxs-lookup"><span data-stu-id="acb56-132">Account management</span></span>
  * <span data-ttu-id="acb56-133">Logga in med ett Microsoft-konto, organisationskonto eller tjänstens huvudnamn via Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="acb56-133">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="acb56-134">Spara autentiseringsuppgifterna till disken med Save-AzureRmContext och läs in sparade autentiseringsuppgifter med Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="acb56-134">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="acb56-135">Miljö</span><span class="sxs-lookup"><span data-stu-id="acb56-135">Environment</span></span>
  * <span data-ttu-id="acb56-136">Hämta andra Microsoft Azure-miljöer</span><span class="sxs-lookup"><span data-stu-id="acb56-136">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="acb56-137">Lägg till/Ange/Ta bort anpassade miljöer (t.ex. Azure Stack eller Windows Azure Pack-miljöer)</span><span class="sxs-lookup"><span data-stu-id="acb56-137">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="acb56-138">Cmdlet:ar på hanteringsnivå för Azure-tjänster med Resource Manager- och Service Management-gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="acb56-138">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="acb56-139">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="acb56-139">Virtual Machine</span></span>
  * <span data-ttu-id="acb56-140">App Service (Websites)</span><span class="sxs-lookup"><span data-stu-id="acb56-140">App Service (Websites)</span></span>
  * <span data-ttu-id="acb56-141">SQL Database</span><span class="sxs-lookup"><span data-stu-id="acb56-141">SQL Database</span></span>
  * <span data-ttu-id="acb56-142">Storage</span><span class="sxs-lookup"><span data-stu-id="acb56-142">Storage</span></span>
  * <span data-ttu-id="acb56-143">Nätverk</span><span class="sxs-lookup"><span data-stu-id="acb56-143">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="acb56-144">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="acb56-144">Next Steps</span></span>

<span data-ttu-id="acb56-145">Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="acb56-145">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
