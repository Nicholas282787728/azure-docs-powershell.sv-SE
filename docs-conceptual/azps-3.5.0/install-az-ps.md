---
title: Installera Azure PowerShell med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 66d755384e532d434811f3e6122dcba97d5c48b5
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477856"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="48f56-103">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="48f56-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="48f56-104">Den här artikeln beskriver hur du installerar Azure PowerShell-modulerna med hjälp av PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="48f56-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="48f56-105">De här instruktionerna fungerar för Windows-, macOS- och Linux-plattformar.</span><span class="sxs-lookup"><span data-stu-id="48f56-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="48f56-106">För Az-modulen kan för närvarande inga andra installationsmetoder användas.</span><span class="sxs-lookup"><span data-stu-id="48f56-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="48f56-107">Krav</span><span class="sxs-lookup"><span data-stu-id="48f56-107">Requirements</span></span>

<span data-ttu-id="48f56-108">Azure PowerShell fungerar med PowerShell 5.1 och senare i Windows och med PowerShell Core 6.x och senare på valfri plattform.</span><span class="sxs-lookup"><span data-stu-id="48f56-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="48f56-109">Om du är osäker på om du har PowerShell, eller macOS eller Linux, [installerar du senaste versionen av PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="48f56-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="48f56-110">Du kan kontrollera vilken PowerShell-version du har genom att köra kommandot:</span><span class="sxs-lookup"><span data-stu-id="48f56-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="48f56-111">Köra Azure PowerShell på PowerShell 5.1 på Windows:</span><span class="sxs-lookup"><span data-stu-id="48f56-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="48f56-112">Uppdatera vid behov till [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="48f56-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="48f56-113">Om du använder Windows 10 kan PowerShell 5.1 redan vara installerat.</span><span class="sxs-lookup"><span data-stu-id="48f56-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="48f56-114">Installera [.NET Framework 4.7.2 eller senare](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="48f56-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="48f56-115">Det finns inga ytterligare krav för Azure PowerShell när du använder PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="48f56-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="48f56-116">Installera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="48f56-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="48f56-117">Det går __inte__ både modulen AzureRM och modulen Az installerade samtidigt för PowerShell 5.1 för Windows.</span><span class="sxs-lookup"><span data-stu-id="48f56-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="48f56-118">Om du vill behålla AzureRM på datorn installerar du Az-modulen för PowerShell Core 6.x eller senare.</span><span class="sxs-lookup"><span data-stu-id="48f56-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="48f56-119">För att göra det [installerar du PowerShell Core 6.x eller senare](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) och följer instruktionerna i PowerShell Core-terminalen.</span><span class="sxs-lookup"><span data-stu-id="48f56-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="48f56-120">Den rekommenderade installationsmetoden är att begränsa installationen till den aktiva användaren:</span><span class="sxs-lookup"><span data-stu-id="48f56-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="48f56-121">Om du vill installera för alla användare i ett system krävs administratörsbehörighet.</span><span class="sxs-lookup"><span data-stu-id="48f56-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="48f56-122">I macOS eller Linux kör du som administratör eller med `sudo`-kommandot i en PowerShell-session med förhöjd behörighet:</span><span class="sxs-lookup"><span data-stu-id="48f56-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="48f56-123">Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="48f56-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="48f56-124">Första gången du använder PSGallery visas följande meddelande:</span><span class="sxs-lookup"><span data-stu-id="48f56-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="48f56-125">Svara `Yes` eller `Yes to All` för att fortsätta med installationen.</span><span class="sxs-lookup"><span data-stu-id="48f56-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="48f56-126">Az-modulen är en sammanslagen modul för Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="48f56-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="48f56-127">När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.</span><span class="sxs-lookup"><span data-stu-id="48f56-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="48f56-128">Installera offline</span><span class="sxs-lookup"><span data-stu-id="48f56-128">Install offline</span></span>

<span data-ttu-id="48f56-129">I en del miljöer går det inte att ansluta till PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="48f56-129">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="48f56-130">I sådana situationer kan du fortfarande installera offline på något av dessa sätt:</span><span class="sxs-lookup"><span data-stu-id="48f56-130">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="48f56-131">Ladda ned modulerna till en annan plats och använd det som en installationskälla på ditt nätverk.</span><span class="sxs-lookup"><span data-stu-id="48f56-131">Download the modules to another location and use that as an installation source on your network.</span></span> <span data-ttu-id="48f56-132">Det här kan vara komplicerat, men då kan du cachelagra PowerShell-moduler på en enda server eller filresurs så att de kan distribueras med PowerShellGet till frånkopplade system.</span><span class="sxs-lookup"><span data-stu-id="48f56-132">This can be a complicated process, but will let you cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="48f56-133">Läs artikeln om hur du [arbetar med lokala PowerShellGet-lagringsplatser](/powershell/scripting/gallery/how-to/working-with-local-psrepositories) för mer information om hur du konfigurerar lokala lagringsplatser och installerar på frånkopplade system.</span><span class="sxs-lookup"><span data-stu-id="48f56-133">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="48f56-134">[Ladda ned Azure PowerShell MSI](install-az-ps-msi.md) till en dator som är ansluten till nätverket, och kopiera sedan installationsprogrammet till system som saknar åtkomst till PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="48f56-134">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="48f56-135">Tänk på att MSI-installationsprogrammet endast fungerar för PowerShell 5.1 på Windows.</span><span class="sxs-lookup"><span data-stu-id="48f56-135">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="48f56-136">Spara modulen med [Save-Module](/powershell/module/PowershellGet/Save-Module) till en filresurs, eller spara den till en annan källa och kopiera den manuellt till andra datorer:</span><span class="sxs-lookup"><span data-stu-id="48f56-136">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="48f56-137">Felsökning</span><span class="sxs-lookup"><span data-stu-id="48f56-137">Troubleshooting</span></span>

<span data-ttu-id="48f56-138">Här är några vanliga problem som kan uppstå när du installerar Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="48f56-138">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="48f56-139">Om du stöter på ett problem som inte tas upp här kan du [öppna ett ärende på GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="48f56-139">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="48f56-140">Proxy blockerar anslutning</span><span class="sxs-lookup"><span data-stu-id="48f56-140">Proxy blocks connection</span></span>

<span data-ttu-id="48f56-141">Om du får felmeddelanden från `Install-Module` som indikerar att det inte går att nå PowerShell Gallery kan du hindras av en proxy.</span><span class="sxs-lookup"><span data-stu-id="48f56-141">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="48f56-142">Olika operativsystem har olika krav för att konfigurera en systemomfattande proxy. Det tas inte upp i detalj här.</span><span class="sxs-lookup"><span data-stu-id="48f56-142">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="48f56-143">Systemadministratören kan ge dig information om proxyinställningarna och hur du konfigurerar dem för operativsystemet.</span><span class="sxs-lookup"><span data-stu-id="48f56-143">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="48f56-144">Själva PowerShell kan inte konfigureras för att använda den här proxyn automatiskt.</span><span class="sxs-lookup"><span data-stu-id="48f56-144">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="48f56-145">Med PowerShell 5.1 och senare konfigurerar du proxyn för PowerShell-sessionen med följande kommando:</span><span class="sxs-lookup"><span data-stu-id="48f56-145">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="48f56-146">Om autentiseringsuppgifter för operativsystemet är rätt konfigurerade dirigeras PowerShell-begärandena genom proxyn.</span><span class="sxs-lookup"><span data-stu-id="48f56-146">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="48f56-147">För att den här inställningen ska finnas kvar mellan sessionerna lägger du till kommandot i en [PowerShell profil](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="48f56-147">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="48f56-148">För att du ska kunna installera paketet måste proxyservern tillåta HTTPS-anslutningar till följande adress:</span><span class="sxs-lookup"><span data-stu-id="48f56-148">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="48f56-149">Logga in</span><span class="sxs-lookup"><span data-stu-id="48f56-149">Sign in</span></span>

<span data-ttu-id="48f56-150">Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="48f56-150">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="48f56-151">Om du har inaktiverat modulen för automatisk inläsning, kan du importera den manuellt med `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="48f56-151">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="48f56-152">Det kan ta några sekunder. Det beror på hur modulen är strukturerad.</span><span class="sxs-lookup"><span data-stu-id="48f56-152">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="48f56-153">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="48f56-153">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="48f56-154">Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="48f56-154">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="48f56-155">Uppdatera Azure PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="48f56-155">Update the Azure PowerShell module</span></span>

<span data-ttu-id="48f56-156">Om du ursprungligen använde Install-Module använder du [Update-Module](/powershell/module/powershellget/update-module) för att hämta den senaste versionen.</span><span class="sxs-lookup"><span data-stu-id="48f56-156">If you originally used Install-Module, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="48f56-157">Om du ursprungligen använde MSI-paketet laddar du ned och installerar det nya MSI-paketet för att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="48f56-157">If you originally used the MSI package then you should download and install the new MSI in order to udpate.</span></span> <span data-ttu-id="48f56-158">Om du har problem med att uppdatera med hjälp av paketet från PowershellGet måste du __installera om__, i stället för att bara __uppdatera__.</span><span class="sxs-lookup"><span data-stu-id="48f56-158">If you have any issues with updating using the package from PowershellGet then you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="48f56-159">Det gör du på samma sätt som när du installerar, men du kan behöva lägga till argumentet `-Force`:</span><span class="sxs-lookup"><span data-stu-id="48f56-159">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="48f56-160">Det här kan skriva över installerade moduler, men du kan fortfarande ha äldre versioner kvar på datorn.</span><span class="sxs-lookup"><span data-stu-id="48f56-160">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="48f56-161">Om du vill ta bort äldre versioner av Azure PowerShell från ditt system läser du [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="48f56-161">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="48f56-162">Använd flera versioner av Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="48f56-162">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="48f56-163">Det är möjligt att installera fler än en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48f56-163">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="48f56-164">Använd följande kommando för att kontrollera om du har flera versioner av Azure PowerShell installerade:</span><span class="sxs-lookup"><span data-stu-id="48f56-164">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="48f56-165">Se [Avinstallera Azure PowerShell-modulen](uninstall-az-ps.md) om du vill ta bort en version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="48f56-165">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="48f56-166">Du kan installera eller läsa in en specifik version av `Az`-modulen med hjälp av argumentet `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="48f56-166">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="48f56-167">Om du har flera versioner av modulen installerade läses den senaste versionen in som standard av automatisk inläsning och `Import-Module`.</span><span class="sxs-lookup"><span data-stu-id="48f56-167">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="48f56-168">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="48f56-168">Provide feedback</span></span>

<span data-ttu-id="48f56-169">Om du upptäcker en bugg i Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="48f56-169">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="48f56-170">Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="48f56-170">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="48f56-171">Efterföljande moment</span><span class="sxs-lookup"><span data-stu-id="48f56-171">Next Steps</span></span>

<span data-ttu-id="48f56-172">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner.</span><span class="sxs-lookup"><span data-stu-id="48f56-172">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="48f56-173">Om du känner till Azure PowerShell och behöver migrera från AzureRM läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="48f56-173">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
