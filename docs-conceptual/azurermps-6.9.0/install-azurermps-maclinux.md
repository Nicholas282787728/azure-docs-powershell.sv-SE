---
title: Installera Azure PowerShell på macOS eller Linux
description: Så här installerar du Azure PowerShell på macOS eller Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/24/2018
ms.openlocfilehash: 05e86d96b345455f3d3bb3fe6dedf933fff6187c
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/04/2018
ms.locfileid: "47424759"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="fe262-103">Installera Azure PowerShell på macOS eller Linux</span><span class="sxs-lookup"><span data-stu-id="fe262-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="fe262-104">På plattformar som inte använder Windows är det möjligt att köra Azure PowerShell i PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="fe262-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="fe262-105">Den här versionen av PowerShell har skapats för användning på alla plattformar som har stöd för .NET Core.</span><span class="sxs-lookup"><span data-stu-id="fe262-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="fe262-106">En .NET Standard-version av Azure PowerShell finns tillgänglig för att arbeta med de här plattformarna.</span><span class="sxs-lookup"><span data-stu-id="fe262-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="fe262-107">För tillfället är både PowerShell Core v6 och Azure PowerShell för .NET Standard fortfarande i betaversioner.</span><span class="sxs-lookup"><span data-stu-id="fe262-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Standard are still in beta.</span></span>
> <span data-ttu-id="fe262-108">De här produkterna har begränsad support.</span><span class="sxs-lookup"><span data-stu-id="fe262-108">Support for these products is limited.</span></span> <span data-ttu-id="fe262-109">Skicka gärna in ett ärende till GitHub om du har problem eller upptäcker buggar.</span><span class="sxs-lookup"><span data-stu-id="fe262-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="fe262-110">Problem med PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="fe262-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="fe262-111">Problem med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe262-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="fe262-112">Installera PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="fe262-112">Install PowerShell Core</span></span>

<span data-ttu-id="fe262-113">Installationsanvisningarna för PowerShell Core är annorlunda för macOS och de flesta Linux-distributioner.</span><span class="sxs-lookup"><span data-stu-id="fe262-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="fe262-114">Detaljerade anvisningar finns i följande artikel:</span><span class="sxs-lookup"><span data-stu-id="fe262-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="fe262-115">Installera PowerShell Core på macOS</span><span class="sxs-lookup"><span data-stu-id="fe262-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="fe262-116">Installera PowerShell Core på Linux</span><span class="sxs-lookup"><span data-stu-id="fe262-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="fe262-117">Installera Azure PowerShell för .NET Standard</span><span class="sxs-lookup"><span data-stu-id="fe262-117">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe262-118">Modulen `AzureRM` som beskrivs i andra artiklar fungerar inte med PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="fe262-118">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="fe262-119">Du måste installera modulen `Az` för att få tillgång till Azure PowerShell-funktioner i PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="fe262-119">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="fe262-120">I PowerShell Core är modulen PowerShellGet redan installerad.</span><span class="sxs-lookup"><span data-stu-id="fe262-120">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="fe262-121">Starta PowerShell med kommandot:</span><span class="sxs-lookup"><span data-stu-id="fe262-121">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="fe262-122">Kör följande kommando för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="fe262-122">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="fe262-123">Om ett behörighetsfel uppstår när du försöker installera modulen kan du behöva köra PowerShell i läget för superanvändare för att installera moduler.</span><span class="sxs-lookup"><span data-stu-id="fe262-123">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="fe262-124">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="fe262-124">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="fe262-125">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="fe262-125">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="fe262-126">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="fe262-126">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="fe262-127">Aktivera alias</span><span class="sxs-lookup"><span data-stu-id="fe262-127">Enable aliases</span></span>

<span data-ttu-id="fe262-128">För kompatibilitet med den befintliga modulen `AzureRM` kan den nya modulen `Az` skapa bakåtkompatibla alias för `AzureRM`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="fe262-128">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="fe262-129">Innan du använder modulen för första gången bör du konfigurera dessa alias med följande kommando:</span><span class="sxs-lookup"><span data-stu-id="fe262-129">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="fe262-130">Då konfigureras alias endast för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="fe262-130">This sets up aliases for the current user only.</span></span> <span data-ttu-id="fe262-131">Cmdlet-hjälpen innehåller andra värden som kan anges för `-Scope` för att konfigurera alias.</span><span class="sxs-lookup"><span data-stu-id="fe262-131">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="fe262-132">Om ett sökvägsfel uppstår bör du kontrollera att sökvägen finns i ditt lokala system.</span><span class="sxs-lookup"><span data-stu-id="fe262-132">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="fe262-133">För omfattningen `CurrentUser` kan det här felet lösas genom att köra följande kommando i `bash`:</span><span class="sxs-lookup"><span data-stu-id="fe262-133">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="fe262-134">Logga in</span><span class="sxs-lookup"><span data-stu-id="fe262-134">Sign in</span></span>

<span data-ttu-id="fe262-135">Du måste läsa in `Az` till din PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe262-135">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="fe262-136">Du behöver __inte__ ha några utökade privilegier för att importera en modul.</span><span class="sxs-lookup"><span data-stu-id="fe262-136">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="fe262-137">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="fe262-137">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="fe262-138">Om du vill importera modulen `Az` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="fe262-138">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="fe262-139">Du bör arbeta med din profil genom miljövariabeln `$Profile` på macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="fe262-139">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="fe262-140">Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="fe262-140">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="fe262-141">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="fe262-141">Next Steps</span></span>

<span data-ttu-id="fe262-142">Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="fe262-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
