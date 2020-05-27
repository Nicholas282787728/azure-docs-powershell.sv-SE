---
title: Andra sätt att installera Azure PowerShell
description: Så här installerar du Azure PowerShell utan PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 55a89861c3bcca41b940d34d945cd43690331f3e
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/14/2020
ms.locfileid: "83385770"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="1ef9b-103">Installera Azure PowerShell på Windows med MSI eller installationsprogrammet för webbplattformen</span><span class="sxs-lookup"><span data-stu-id="1ef9b-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="1ef9b-104">Den här artikeln beskriver hur du installerar Azure PowerShell på Windows med hjälp av en hanterad tjänstidentitet eller installationsprogrammet för webbplattformen (WebPI).</span><span class="sxs-lookup"><span data-stu-id="1ef9b-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="1ef9b-105">Använd endast dessa installationsmetoder om de är nödvändiga för ditt system.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="1ef9b-106">PowerShellGet är det rekommenderade sättet att installera Azure PowerShell på Windows.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="1ef9b-107">Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1ef9b-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="1ef9b-108">Installera eller uppdatera på Windows med hjälp av MSI-paketet</span><span class="sxs-lookup"><span data-stu-id="1ef9b-108">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="1ef9b-109">Azure PowerShell kan installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span><span class="sxs-lookup"><span data-stu-id="1ef9b-109">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="1ef9b-110">Om du har installerat tidigare versioner av Azure-moduler som MSI så tar installationsprogrammet automatiskt bort dem.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-110">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="1ef9b-111">MSI-paketet installerar moduler i `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-111">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="1ef9b-112">Både modulerna `AzureRM` och `Azure` installeras.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-112">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="1ef9b-113">Använd endast modulen `Azure` om du arbetar med den klassiska Azure-distributionsmodellen.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-113">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="1ef9b-114">Du måste läsa in `AzureRM` till din nuvarande PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-114">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="1ef9b-115">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-115">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="1ef9b-116">Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="1ef9b-116">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="1ef9b-117">Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1ef9b-117">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="1ef9b-118">Installera eller uppdatera på Windows med hjälp av installationsprogrammet för webbplattformen</span><span class="sxs-lookup"><span data-stu-id="1ef9b-118">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="1ef9b-119">Hämta [Azure PowerShell WebPI-paketet](https://aka.ms/webpi-azps) och starta installationen.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-119">Download the [Azure PowerShell WebPI package](https://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="1ef9b-120">Om du har installerat tidigare versioner av Azure-moduler från MSI eller med installationsprogrammet för webbplattformen så tar installationsprogrammet automatiskt bort dem.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-120">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="1ef9b-121">Moduler installeras till `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-121">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="1ef9b-122">Både modulerna `AzureRM` och `Azure` installeras.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-122">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="1ef9b-123">Använd endast modulen `Azure` om du arbetar med den klassiska Azure-distributionsmodellen.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-123">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="1ef9b-124">Du måste läsa in `AzureRM` till din nuvarande PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-124">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="1ef9b-125">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="1ef9b-125">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="1ef9b-126">Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="1ef9b-126">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="1ef9b-127">Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1ef9b-127">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
