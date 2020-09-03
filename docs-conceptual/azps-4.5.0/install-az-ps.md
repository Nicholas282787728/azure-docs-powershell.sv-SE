---
title: Installera Azure PowerShell med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: a263f1d363b3d1a1cce433a6112c55afe65262a4
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239680"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="247eb-103">Installera Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="247eb-103">Install Azure PowerShell</span></span>

<span data-ttu-id="247eb-104">Den här artikeln beskriver hur du installerar Azure PowerShell-modulerna med hjälp av [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span><span class="sxs-lookup"><span data-stu-id="247eb-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="247eb-105">De här instruktionerna fungerar för Windows-, macOS- och Linux-plattformar.</span><span class="sxs-lookup"><span data-stu-id="247eb-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="247eb-106">Azure PowerShell är också tillgängligt i Azure [Cloud Shell](/azure/cloud-shell/overview) och är nu förinstallerat i [Docker-avbildningar](azureps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="247eb-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview) and is now preinstalled in [Docker images](azureps-in-docker.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="247eb-107">Krav</span><span class="sxs-lookup"><span data-stu-id="247eb-107">Requirements</span></span>

> [!NOTE]
> <span data-ttu-id="247eb-108">PowerShell 7.x och senare är den rekommenderade versionen av PowerShell för användning med Azure PowerShell på alla plattformar.</span><span class="sxs-lookup"><span data-stu-id="247eb-108">PowerShell 7.x and later is the recommended version of PowerShell for use with Azure PowerShell on all platforms.</span></span>

<span data-ttu-id="247eb-109">Azure PowerShell fungerar med PowerShell 6.2.4 och senare på alla plattformar.</span><span class="sxs-lookup"><span data-stu-id="247eb-109">Azure PowerShell works with PowerShell 6.2.4 and later on all platforms.</span></span> <span data-ttu-id="247eb-110">Modulen stöds även med PowerShell 5.1 i Windows.</span><span class="sxs-lookup"><span data-stu-id="247eb-110">It is also supported with PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="247eb-111">Installera [den senaste versionen av PowerShell](/powershell/scripting/install/installing-powershell) för ditt operativsystem.</span><span class="sxs-lookup"><span data-stu-id="247eb-111">Install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system.</span></span> <span data-ttu-id="247eb-112">Det finns inga ytterligare krav för Azure PowerShell när du kör verktyget på PowerShell 6.2.4 och senare.</span><span class="sxs-lookup"><span data-stu-id="247eb-112">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="247eb-113">Du kan kontrollera vilken PowerShell-version du har genom att köra kommandot:</span><span class="sxs-lookup"><span data-stu-id="247eb-113">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="247eb-114">Använda Azure PowerShell i PowerShell 5.1 på Windows:</span><span class="sxs-lookup"><span data-stu-id="247eb-114">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="247eb-115">Uppdatera till [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="247eb-115">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="247eb-116">Om du använder Windows 10 version 1607 eller senare är PowerShell 5.1 redan installerat.</span><span class="sxs-lookup"><span data-stu-id="247eb-116">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="247eb-117">Installera [.NET Framework 4.7.2 eller senare](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="247eb-117">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="247eb-118">Kontrollera att du har den senaste versionen av PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="247eb-118">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="247eb-119">Kör `Install-Module -Name PowerShellGet -Force`.</span><span class="sxs-lookup"><span data-stu-id="247eb-119">Run `Install-Module -Name PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="247eb-120">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="247eb-120">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="247eb-121">Det går inte att ha både modulen AzureRM och modulen Az installerade samtidigt för PowerShell 5.1 för Windows.</span><span class="sxs-lookup"><span data-stu-id="247eb-121">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="247eb-122">Om du vill behålla AzureRM på datorn installerar du Az-modulen för PowerShell 6.2.4 eller senare.</span><span class="sxs-lookup"><span data-stu-id="247eb-122">If you need to keep AzureRM available on your system, install the Az module for PowerShell 6.2.4 or later.</span></span>

<span data-ttu-id="247eb-123">Att använda PowerShellGet-cmdletar är den installationsmetod som föredras.</span><span class="sxs-lookup"><span data-stu-id="247eb-123">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="247eb-124">Installera Az-modulen endast för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="247eb-124">Install the Az module for the current user only.</span></span> <span data-ttu-id="247eb-125">Detta är det rekommenderade installationsomfånget.</span><span class="sxs-lookup"><span data-stu-id="247eb-125">This is the recommended installation scope.</span></span> <span data-ttu-id="247eb-126">Den här metoden fungerar på samma sätt för plattformarna Windows, macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="247eb-126">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="247eb-127">Kör följande kommando från en PowerShell-session:</span><span class="sxs-lookup"><span data-stu-id="247eb-127">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="247eb-128">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="247eb-128">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="247eb-129">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="247eb-129">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="247eb-130">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="247eb-130">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="247eb-131">Att installera modulen för alla användare i ett system kräver förhöjd behörighet.</span><span class="sxs-lookup"><span data-stu-id="247eb-131">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="247eb-132">Starta PowerShell-sessionen med **Kör som administratör** i Windows eller använd kommandot `sudo` på macOS eller Linux:</span><span class="sxs-lookup"><span data-stu-id="247eb-132">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="247eb-133">Az-modulen är en sammanslagen modul för Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="247eb-133">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="247eb-134">När du installerar den laddas alla allmänt tillgängliga Az PowerShell-moduler ned så att deras cmdletar blir tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="247eb-134">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="247eb-135">Installera offline</span><span class="sxs-lookup"><span data-stu-id="247eb-135">Install offline</span></span>

<span data-ttu-id="247eb-136">I en del miljöer går det inte att ansluta till PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="247eb-136">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="247eb-137">I sådana situationer kan du fortfarande installera offline på något av dessa sätt:</span><span class="sxs-lookup"><span data-stu-id="247eb-137">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="247eb-138">Ladda ned modulerna till en annan plats i nätverket och använd den som en installationskälla.</span><span class="sxs-lookup"><span data-stu-id="247eb-138">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="247eb-139">Med den här metoden kan du cachelagra PowerShell-moduler på en enda server eller filresurs så att de kan distribueras med PowerShellGet till frånkopplade system.</span><span class="sxs-lookup"><span data-stu-id="247eb-139">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="247eb-140">Läs artikeln om hur du [arbetar med lokala PowerShellGet-lagringsplatser](/powershell/scripting/gallery/how-to/working-with-local-psrepositories) för mer information om hur du konfigurerar lokala lagringsplatser och installerar på frånkopplade system.</span><span class="sxs-lookup"><span data-stu-id="247eb-140">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="247eb-141">[Ladda ned Azure PowerShell MSI](install-az-ps-msi.md) till en dator som är ansluten till nätverket, och kopiera sedan installationsprogrammet till system som saknar åtkomst till PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="247eb-141">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="247eb-142">Tänk på att MSI-installationsprogrammet endast fungerar för PowerShell 5.1 på Windows.</span><span class="sxs-lookup"><span data-stu-id="247eb-142">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="247eb-143">Spara modulen med [Save-Module](/powershell/module/PowershellGet/Save-Module) till en filresurs, eller spara den till en annan källa och kopiera den manuellt till andra datorer:</span><span class="sxs-lookup"><span data-stu-id="247eb-143">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="247eb-144">Felsökning</span><span class="sxs-lookup"><span data-stu-id="247eb-144">Troubleshooting</span></span>

<span data-ttu-id="247eb-145">Här är några vanliga problem som kan uppstå när du installerar Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="247eb-145">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="247eb-146">Om du stöter på ett problem som inte tas upp här kan du [öppna ett ärende på GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="247eb-146">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="247eb-147">Proxy blockerar anslutning</span><span class="sxs-lookup"><span data-stu-id="247eb-147">Proxy blocks connection</span></span>

<span data-ttu-id="247eb-148">Om du får felmeddelanden från `Install-Module` som indikerar att det inte går att nå PowerShell Gallery kan du hindras av en proxy.</span><span class="sxs-lookup"><span data-stu-id="247eb-148">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="247eb-149">Olika operativsystem och nätverksmiljöer har olika krav för att konfigurera en systemomfattande proxy.</span><span class="sxs-lookup"><span data-stu-id="247eb-149">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="247eb-150">Systemadministratören kan ge dig information om proxyinställningarna och hur du konfigurerar dem för din miljö.</span><span class="sxs-lookup"><span data-stu-id="247eb-150">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="247eb-151">Själva PowerShell kan inte konfigureras för att använda den här proxyn automatiskt.</span><span class="sxs-lookup"><span data-stu-id="247eb-151">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="247eb-152">Med PowerShell 5.1 och senare konfigurerar du proxyn för PowerShell-sessionen med följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="247eb-152">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="247eb-153">Om autentiseringsuppgifter för operativsystemet är rätt konfigurerade dirigerar den här konfigurationen PowerShell-begärandena genom proxyn.</span><span class="sxs-lookup"><span data-stu-id="247eb-153">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="247eb-154">För att den här inställningen ska finnas kvar mellan sessionerna lägger du till kommandona i en [PowerShell-profil](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="247eb-154">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="247eb-155">För att du ska kunna installera paketet måste proxyservern tillåta HTTPS-anslutningar till följande adress:</span><span class="sxs-lookup"><span data-stu-id="247eb-155">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="247eb-156">Logga in</span><span class="sxs-lookup"><span data-stu-id="247eb-156">Sign in</span></span>

<span data-ttu-id="247eb-157">Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="247eb-157">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="247eb-158">Om du har inaktiverat modulen för automatisk inläsning, kan du importera den manuellt med `Import-Module -Name Az`.</span><span class="sxs-lookup"><span data-stu-id="247eb-158">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="247eb-159">Det kan ta några sekunder. Det beror på hur modulen är strukturerad.</span><span class="sxs-lookup"><span data-stu-id="247eb-159">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="247eb-160">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="247eb-160">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="247eb-161">Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="247eb-161">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="247eb-162">Uppdatera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="247eb-162">Update the Azure PowerShell module</span></span>

<span data-ttu-id="247eb-163">Om du vill uppdatera en PowerShell-modul ska du använda samma metod som för att installera modulen.</span><span class="sxs-lookup"><span data-stu-id="247eb-163">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="247eb-164">Om du ursprungligen till exempel använde `Install-Module` använder du [Update-Module](/powershell/module/powershellget/update-module) för att hämta den senaste versionen.</span><span class="sxs-lookup"><span data-stu-id="247eb-164">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="247eb-165">Om du ursprungligen använde MSI-paketet laddar du ned och installerar det nya MSI-paketet.</span><span class="sxs-lookup"><span data-stu-id="247eb-165">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="247eb-166">PowerShellGet-cmdletar kan inte uppdatera moduler som har installerats från ett MSI-paket.</span><span class="sxs-lookup"><span data-stu-id="247eb-166">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="247eb-167">MSI-paket uppdaterar inte moduler som har installerats med PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="247eb-167">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="247eb-168">Om du har problem med att uppdatera med PowershellGet bör du **installera om**, i stället för **uppdatera**.</span><span class="sxs-lookup"><span data-stu-id="247eb-168">If you have any issues updating using PowershellGet, then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="247eb-169">Ominstallation görs på samma sätt som när du installerar, men du behöver lägga till parametern `-Force`:</span><span class="sxs-lookup"><span data-stu-id="247eb-169">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="247eb-170">Till skillnad från MSI-baserade installationer, tar installationer eller uppdateringar med PowerShellGet inte bort äldre versioner som kan finnas i systemet.</span><span class="sxs-lookup"><span data-stu-id="247eb-170">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="247eb-171">Om du vill ta bort äldre versioner av Azure PowerShell från ditt system går du till [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="247eb-171">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="247eb-172">Mer information om MSI-baserade installationer finns i [Installera Azure PowerShell med MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="247eb-172">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="247eb-173">Använd flera versioner av Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="247eb-173">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="247eb-174">Det är möjligt att installera fler än en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="247eb-174">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="247eb-175">Använd följande kommando för att kontrollera om du har flera versioner av Azure PowerShell installerade:</span><span class="sxs-lookup"><span data-stu-id="247eb-175">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="247eb-176">Se [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md) om du vill ta bort en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="247eb-176">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="247eb-177">Om du har flera versioner av modulen installerade läses den senaste versionen in som standard av automatisk inläsning och `Import-Module`.</span><span class="sxs-lookup"><span data-stu-id="247eb-177">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="247eb-178">Du kan installera eller läsa in en specifik version av `Az`-modulen med hjälp av parametern `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="247eb-178">You can install or load a specific version of the `Az` module using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="use-multiple-repositories-with-powershellget"></a><span data-ttu-id="247eb-179">Använd flera lagringsplatser med PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="247eb-179">Use multiple repositories with PowerShellGet</span></span>

<span data-ttu-id="247eb-180">Parametern **Repository** krävs om du har lagt till fler lagringsplatser i PowerShellGet i ditt system och Az-modulen finns på fler än en av dem.</span><span class="sxs-lookup"><span data-stu-id="247eb-180">The **Repository** parameter is required if you have added additional repositories to PowerShellGet on your system and the Az module can be found in more than one of them.</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a><span data-ttu-id="247eb-181">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="247eb-181">Provide feedback</span></span>

<span data-ttu-id="247eb-182">Om du upptäcker en bugg i Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="247eb-182">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="247eb-183">Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="247eb-183">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="247eb-184">Efterföljande moment</span><span class="sxs-lookup"><span data-stu-id="247eb-184">Next Steps</span></span>

<span data-ttu-id="247eb-185">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner.</span><span class="sxs-lookup"><span data-stu-id="247eb-185">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="247eb-186">Om du känner till Azure PowerShell och behöver migrera från AzureRM läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="247eb-186">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
