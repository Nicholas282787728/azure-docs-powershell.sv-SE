---
title: Andra sätt att installera Azure PowerShell
description: Så här installerar du Azure PowerShell utan PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 2fcd2307667d1f810fbcb3fe4d14e3b0def537ed
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001481"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="d00c6-103">Installera Azure PowerShell på Windows med MSI eller installationsprogrammet för webbplattformen</span><span class="sxs-lookup"><span data-stu-id="d00c6-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="d00c6-104">Den här artikeln beskriver hur du installerar Azure PowerShell på Windows med hjälp av en hanterad tjänstidentitet eller installationsprogrammet för webbplattformen (WebPI).</span><span class="sxs-lookup"><span data-stu-id="d00c6-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="d00c6-105">Använd endast dessa installationsmetoder om de är nödvändiga för ditt system.</span><span class="sxs-lookup"><span data-stu-id="d00c6-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="d00c6-106">PowerShellGet är det rekommenderade sättet att installera Azure PowerShell på Windows.</span><span class="sxs-lookup"><span data-stu-id="d00c6-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="d00c6-107">Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d00c6-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="d00c6-108">Information om hur du installerar i Linux- eller macOS-miljöer finns i [Installera Azure PowerShell på macOS eller Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="d00c6-108">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="d00c6-109">Installera eller uppdatera på Windows med hjälp av MSI-paketet</span><span class="sxs-lookup"><span data-stu-id="d00c6-109">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="d00c6-110">Azure PowerShell kan installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span><span class="sxs-lookup"><span data-stu-id="d00c6-110">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="d00c6-111">Om du har installerat tidigare versioner av Azure-moduler som MSI så tar installationsprogrammet automatiskt bort dem.</span><span class="sxs-lookup"><span data-stu-id="d00c6-111">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="d00c6-112">MSI-paketet installerar moduler i `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="d00c6-112">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="d00c6-113">Både modulerna `AzureRM` och `Azure` installeras.</span><span class="sxs-lookup"><span data-stu-id="d00c6-113">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="d00c6-114">Använd endast modulen `Azure` om du arbetar med den klassiska Azure-distributionsmodellen.</span><span class="sxs-lookup"><span data-stu-id="d00c6-114">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="d00c6-115">Du måste läsa in `AzureRM` till din nuvarande PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d00c6-115">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="d00c6-116">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="d00c6-116">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="d00c6-117">Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="d00c6-117">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="d00c6-118">Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d00c6-118">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="d00c6-119">Installera eller uppdatera på Windows med hjälp av installationsprogrammet för webbplattformen</span><span class="sxs-lookup"><span data-stu-id="d00c6-119">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="d00c6-120">Hämta [Azure PowerShell WebPI-paketet](http://aka.ms/webpi-azps) och starta installationen.</span><span class="sxs-lookup"><span data-stu-id="d00c6-120">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="d00c6-121">Om du har installerat tidigare versioner av Azure-moduler från MSI eller med installationsprogrammet för webbplattformen så tar installationsprogrammet automatiskt bort dem.</span><span class="sxs-lookup"><span data-stu-id="d00c6-121">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="d00c6-122">Moduler installeras till `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="d00c6-122">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="d00c6-123">Både modulerna `AzureRM` och `Azure` installeras.</span><span class="sxs-lookup"><span data-stu-id="d00c6-123">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="d00c6-124">Använd endast modulen `Azure` om du arbetar med den klassiska Azure-distributionsmodellen.</span><span class="sxs-lookup"><span data-stu-id="d00c6-124">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="d00c6-125">Du måste läsa in `AzureRM` till din nuvarande PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d00c6-125">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="d00c6-126">Du måste upprepa de här stegen för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="d00c6-126">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="d00c6-127">Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="d00c6-127">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="d00c6-128">Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d00c6-128">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
