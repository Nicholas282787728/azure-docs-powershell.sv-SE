---
title: Andra sätt att installera Azure PowerShell
description: Så här installerar du Azure PowerShell utan PowerShellGet med MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: e1d8877c185b4537c476128e279eda563f2575d1
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/14/2020
ms.locfileid: "83385872"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="ff758-103">Installera Azure PowerShell på Windows med MSI</span><span class="sxs-lookup"><span data-stu-id="ff758-103">Install Azure PowerShell on Windows with MSI</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="ff758-104">Den här artikeln beskriver hur du installerar Azure PowerShell på Windows med ett MSI-installationsprogram.</span><span class="sxs-lookup"><span data-stu-id="ff758-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="ff758-105">Använd endast dessa installationsmetoder om de är nödvändiga för ditt system.</span><span class="sxs-lookup"><span data-stu-id="ff758-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="ff758-106">PowerShellGet är det rekommenderade sättet att installera Azure PowerShell på Windows.</span><span class="sxs-lookup"><span data-stu-id="ff758-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="ff758-107">Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="ff758-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ff758-108">Metoden att installera med installationsprogrammet för webbplattformen är inte längre tillgänglig för versioner av Azure PowerShell 6.x eller senare.</span><span class="sxs-lookup"><span data-stu-id="ff758-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="ff758-109">Om du måste använda installationsprogrammet för webbplattformen kan du överväga att använda MSI istället, eller installera en tidigare version av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff758-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="ff758-110">Installera eller uppdatera på Windows med hjälp av MSI-paketet</span><span class="sxs-lookup"><span data-stu-id="ff758-110">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="ff758-111">Azure PowerShell för Windows PowerShell 5.x kan installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="ff758-111">Azure PowerShell for Windows PowerShell 5.x can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span> <span data-ttu-id="ff758-112">Om du har installerat tidigare versioner av Azure-moduler som MSI så tar installationsprogrammet automatiskt bort dem.</span><span class="sxs-lookup"><span data-stu-id="ff758-112">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="ff758-113">MSI-paketet installerar moduler i `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="ff758-113">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="ff758-114">Både modulerna `AzureRM` och `Azure` installeras.</span><span class="sxs-lookup"><span data-stu-id="ff758-114">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="ff758-115">Använd endast modulen `Azure` om du arbetar med den klassiska Azure-distributionsmodellen.</span><span class="sxs-lookup"><span data-stu-id="ff758-115">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="ff758-116">Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="ff758-116">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="ff758-117">Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="ff758-117">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="ff758-118">Det kan ta några sekunder. Det beror på hur modulen är strukturerad.</span><span class="sxs-lookup"><span data-stu-id="ff758-118">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="ff758-119">Du måste upprepa det här steget för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="ff758-119">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="ff758-120">Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ff758-120">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
