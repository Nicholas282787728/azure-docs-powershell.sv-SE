---
title: Installera Azure PowerShell med MSI
description: Så här installerar du Azure PowerShell utan PowerShellGet med MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: d51a65d3e8600e8b381da0f485725c0345e37215
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387079"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="5f628-103">Installera Azure PowerShell på Windows med MSI</span><span class="sxs-lookup"><span data-stu-id="5f628-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="5f628-104">Den här artikeln beskriver hur du installerar Azure PowerShell på Windows med ett MSI-installationsprogram.</span><span class="sxs-lookup"><span data-stu-id="5f628-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="5f628-105">MSI-installationsprogrammet kan användas för miljöer där PowerShell-galleriet kan vara blockerat av en brandvägg eller då ett installationsprogram för offlinemiljöer behövs.</span><span class="sxs-lookup"><span data-stu-id="5f628-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="5f628-106">PowerShellGet är det rekommenderade sättet att installera Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5f628-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="5f628-107">Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="5f628-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f628-108">Krav</span><span class="sxs-lookup"><span data-stu-id="5f628-108">Requirements</span></span>

<span data-ttu-id="5f628-109">MSI-installationsprogrammet för Azure PowerShell fungerar __endast__ för PowerShell 5.1 på Windows.</span><span class="sxs-lookup"><span data-stu-id="5f628-109">The MSI installer for Azure PowerShell works __only__ for PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="5f628-110">Om du vill installera på andra plattformar än Windows eller för senare versioner av PowerShell [installerar du med PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="5f628-110">For installation on non-Windows platforms or later versions of powershell, [Install with PowerShellGet](install-az-ps.md).</span></span>
<span data-ttu-id="5f628-111">Du kan kontrollera vilken PowerShell-version du har genom att köra kommandot:</span><span class="sxs-lookup"><span data-stu-id="5f628-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="5f628-112">Du måste göra följande för att använda Azure PowerShell i PowerShell 5.1:</span><span class="sxs-lookup"><span data-stu-id="5f628-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="5f628-113">Uppdatera vid behov till [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="5f628-113">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="5f628-114">Om du använder Windows 10 kan PowerShell 5.1 redan vara installerat.</span><span class="sxs-lookup"><span data-stu-id="5f628-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="5f628-115">Installera [.NET Framework 4.7.2 eller senare](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="5f628-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="5f628-116">Installera eller uppdatera på Windows med hjälp av MSI-paketet</span><span class="sxs-lookup"><span data-stu-id="5f628-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="5f628-117">Azure PowerShell för Windows installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v1.8.0-April2019).</span><span class="sxs-lookup"><span data-stu-id="5f628-117">Azure PowerShell for Windows is installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v1.8.0-April2019).</span></span> <span data-ttu-id="5f628-118">Om du har installerat tidigare versioner av Azure-moduler som MSI tar installationsprogrammet automatiskt bort dem.</span><span class="sxs-lookup"><span data-stu-id="5f628-118">If you have installed earlier versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="5f628-119">MSI-paketet installerar moduler i `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="5f628-119">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="5f628-120">Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="5f628-120">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="5f628-121">Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="5f628-121">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="5f628-122">Det kan ta upp till en minut. Det beror på hur modulen är strukturerad.</span><span class="sxs-lookup"><span data-stu-id="5f628-122">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="5f628-123">Du måste upprepa det här steget för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="5f628-123">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="5f628-124">Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="5f628-124">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="5f628-125">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="5f628-125">Provide feedback</span></span>

<span data-ttu-id="5f628-126">Om du upptäcker en bugg i Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="5f628-126">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="5f628-127">Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="5f628-127">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5f628-128">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="5f628-128">Next Steps</span></span>

<span data-ttu-id="5f628-129">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner.</span><span class="sxs-lookup"><span data-stu-id="5f628-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="5f628-130">Om du känner till Azure PowerShell och behöver migrera från AzureRM läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="5f628-130">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
