---
title: Installera Azure PowerShell på macOS eller Linux
description: Så här installerar du Azure PowerShell på macOS eller Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2018
ms.locfileid: "51576427"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="0f37a-103">Installera Azure PowerShell på macOS eller Linux</span><span class="sxs-lookup"><span data-stu-id="0f37a-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="0f37a-104">På plattformar som inte använder Windows är det möjligt att köra Azure PowerShell i PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="0f37a-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="0f37a-105">Den här versionen av PowerShell har skapats för användning på alla plattformar som har stöd för .NET Core.</span><span class="sxs-lookup"><span data-stu-id="0f37a-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="0f37a-106">En .NET Standard-version av Azure PowerShell finns tillgänglig för att arbeta med de här plattformarna.</span><span class="sxs-lookup"><span data-stu-id="0f37a-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="0f37a-107">För tillfället är Azure PowerShell för .NET Standard fortfarande i betaversion.</span><span class="sxs-lookup"><span data-stu-id="0f37a-107">At this time, Azure PowerShell for .NET Standard is still in beta.</span></span>
> <span data-ttu-id="0f37a-108">Skicka gärna in ett ärende till GitHub om du har problem eller upptäcker buggar.</span><span class="sxs-lookup"><span data-stu-id="0f37a-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="0f37a-109">Problem med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0f37a-109">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="0f37a-110">Installera PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="0f37a-110">Install PowerShell Core</span></span>

<span data-ttu-id="0f37a-111">Installationsanvisningarna för PowerShell Core är annorlunda för macOS och de flesta Linux-distributioner.</span><span class="sxs-lookup"><span data-stu-id="0f37a-111">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="0f37a-112">Detaljerade anvisningar finns i följande artikel:</span><span class="sxs-lookup"><span data-stu-id="0f37a-112">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="0f37a-113">Installera PowerShell Core på macOS</span><span class="sxs-lookup"><span data-stu-id="0f37a-113">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="0f37a-114">Installera PowerShell Core på Linux</span><span class="sxs-lookup"><span data-stu-id="0f37a-114">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="0f37a-115">Installera Azure PowerShell för .NET Standard</span><span class="sxs-lookup"><span data-stu-id="0f37a-115">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f37a-116">Modulen `AzureRM` som beskrivs i andra artiklar fungerar inte med PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="0f37a-116">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="0f37a-117">Du måste installera modulen `Az` för att få tillgång till Azure PowerShell-funktioner i PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="0f37a-117">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="0f37a-118">I PowerShell Core är modulen PowerShellGet redan installerad.</span><span class="sxs-lookup"><span data-stu-id="0f37a-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="0f37a-119">Starta PowerShell med kommandot:</span><span class="sxs-lookup"><span data-stu-id="0f37a-119">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="0f37a-120">Kör följande kommando för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="0f37a-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="0f37a-121">Om ett behörighetsfel uppstår när du försöker installera modulen kan du behöva köra PowerShell i läget för superanvändare för att installera moduler.</span><span class="sxs-lookup"><span data-stu-id="0f37a-121">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="0f37a-122">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0f37a-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="0f37a-123">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="0f37a-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="0f37a-124">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="0f37a-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="0f37a-125">Aktivera alias</span><span class="sxs-lookup"><span data-stu-id="0f37a-125">Enable aliases</span></span>

<span data-ttu-id="0f37a-126">För kompatibilitet med den befintliga modulen `AzureRM` kan den nya modulen `Az` skapa bakåtkompatibla alias för `AzureRM`-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="0f37a-126">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="0f37a-127">Innan du använder modulen för första gången bör du konfigurera dessa alias med följande kommando:</span><span class="sxs-lookup"><span data-stu-id="0f37a-127">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="0f37a-128">Då konfigureras alias endast för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="0f37a-128">This sets up aliases for the current user only.</span></span> <span data-ttu-id="0f37a-129">Cmdlet-hjälpen innehåller andra värden som kan anges för `-Scope` för att konfigurera alias.</span><span class="sxs-lookup"><span data-stu-id="0f37a-129">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="0f37a-130">Om ett sökvägsfel uppstår bör du kontrollera att sökvägen finns i ditt lokala system.</span><span class="sxs-lookup"><span data-stu-id="0f37a-130">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="0f37a-131">För omfattningen `CurrentUser` kan det här felet lösas genom att köra följande kommando i `bash`:</span><span class="sxs-lookup"><span data-stu-id="0f37a-131">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="0f37a-132">Logga in</span><span class="sxs-lookup"><span data-stu-id="0f37a-132">Sign in</span></span>

<span data-ttu-id="0f37a-133">Du måste läsa in `Az` till din PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f37a-133">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="0f37a-134">Du behöver __inte__ ha några utökade privilegier för att importera en modul.</span><span class="sxs-lookup"><span data-stu-id="0f37a-134">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="0f37a-135">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="0f37a-135">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="0f37a-136">Om du vill importera modulen `Az` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="0f37a-136">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="0f37a-137">Du bör arbeta med din profil genom miljövariabeln `$Profile` på macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="0f37a-137">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="0f37a-138">Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="0f37a-138">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="0f37a-139">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="0f37a-139">Next Steps</span></span>

<span data-ttu-id="0f37a-140">Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0f37a-140">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
