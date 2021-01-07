---
title: Installera Azure PowerShell med MSI
description: Så här installerar du Azure PowerShell utan PowerShellGet med MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: de9ac41b86e97c948943d22b2019c8022bdf52e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893981"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="745f0-103">Installera Azure PowerShell på Windows med MSI</span><span class="sxs-lookup"><span data-stu-id="745f0-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="745f0-104">Den här artikeln beskriver hur du installerar Azure PowerShell på Windows med ett MSI-installationsprogram.</span><span class="sxs-lookup"><span data-stu-id="745f0-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="745f0-105">MSI-installationsprogrammet kan användas för miljöer där PowerShell-galleriet kan vara blockerat av en brandvägg eller då ett installationsprogram för offlinemiljöer behövs.</span><span class="sxs-lookup"><span data-stu-id="745f0-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="745f0-106">PowerShellGet är det rekommenderade sättet att installera Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="745f0-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="745f0-107">Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="745f0-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="745f0-108">Krav</span><span class="sxs-lookup"><span data-stu-id="745f0-108">Requirements</span></span>

<span data-ttu-id="745f0-109">MSI-installationsprogrammet i Windows är utformat för att endast installera Azure PowerShell för PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="745f0-109">The MSI installer on Windows is designed to install Azure PowerShell for PowerShell 5.1 only.</span></span> <span data-ttu-id="745f0-110">Om du vill installera på andra plattformar än Windows eller för senare versioner av PowerShell [installerar du med PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="745f0-110">For installation on non-Windows platforms or later versions of PowerShell, [Install with PowerShellGet](install-az-ps.md).</span></span> <span data-ttu-id="745f0-111">Du kan kontrollera vilken PowerShell-version du har genom att köra kommandot:</span><span class="sxs-lookup"><span data-stu-id="745f0-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="745f0-112">Du måste göra följande för att använda Azure PowerShell i PowerShell 5.1:</span><span class="sxs-lookup"><span data-stu-id="745f0-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="745f0-113">Uppdatera vid behov till [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="745f0-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="745f0-114">Om du använder Windows 10 kan PowerShell 5.1 redan vara installerat.</span><span class="sxs-lookup"><span data-stu-id="745f0-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="745f0-115">Installera [.NET Framework 4.7.2 eller senare](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="745f0-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="745f0-116">Installera eller uppdatera på Windows med hjälp av MSI-paketet</span><span class="sxs-lookup"><span data-stu-id="745f0-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="745f0-117">MSI-paketet för Azure PowerShell finns på [GitHub](https://github.com/Azure/azure-powershell/releases):</span><span class="sxs-lookup"><span data-stu-id="745f0-117">The MSI package for Azure PowerShell is available from [GitHub](https://github.com/Azure/azure-powershell/releases):</span></span>

1. <span data-ttu-id="745f0-118">Gå till https://github.com/Azure/azure-powershell/releases.</span><span class="sxs-lookup"><span data-stu-id="745f0-118">Go to https://github.com/Azure/azure-powershell/releases.</span></span>
2. <span data-ttu-id="745f0-119">Leta efter den senaste gallerimodulen för Azure PowerShell (de visas kronologiskt och är vanligtvis bara en version utan namn, som ”4.7.0”).</span><span class="sxs-lookup"><span data-stu-id="745f0-119">Look for the most recent Gallery Module for Azure PowerShell (these are listed chronologically and are typically just a release version with no name like "4.7.0").</span></span>
3. <span data-ttu-id="745f0-120">Rulla ned till slutet av korrigeringsanteckningarna och klicka på pilen bredvid ”Assets” (tillgångar) om du vill se MSI-alternativen.</span><span class="sxs-lookup"><span data-stu-id="745f0-120">Scroll down to the bottom of the patch notes and click on the arrow next to "Assets" to reveal the MSI options.</span></span>
4. <span data-ttu-id="745f0-121">Klicka på önskad Az-Cmdlets MSI för att starta nedladdningen.</span><span class="sxs-lookup"><span data-stu-id="745f0-121">Click on the Az-Cmdlets MSI of your choice to start the download.</span></span>

<span data-ttu-id="745f0-122">Om du har installerat tidigare versioner av Azure PowerShell med hjälp av MSI tar installationsprogrammet automatiskt bort dem.</span><span class="sxs-lookup"><span data-stu-id="745f0-122">If you have installed earlier versions of Azure PowerShell using the MSI, the installer automatically removes them.</span></span> <span data-ttu-id="745f0-123">MSI-paketet installerar moduler i `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="745f0-123">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="745f0-124">Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="745f0-124">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="745f0-125">Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="745f0-125">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="745f0-126">Det kan ta upp till en minut. Det beror på hur modulen är strukturerad.</span><span class="sxs-lookup"><span data-stu-id="745f0-126">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="745f0-127">Du måste upprepa det här steget för varje ny PowerShell-session du startar.</span><span class="sxs-lookup"><span data-stu-id="745f0-127">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="745f0-128">Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="745f0-128">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="745f0-129">Ge feedback</span><span class="sxs-lookup"><span data-stu-id="745f0-129">Provide feedback</span></span>

<span data-ttu-id="745f0-130">Om du upptäcker en bugg i Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="745f0-130">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="745f0-131">Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="745f0-131">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="745f0-132">Efterföljande moment</span><span class="sxs-lookup"><span data-stu-id="745f0-132">Next Steps</span></span>

<span data-ttu-id="745f0-133">Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner.</span><span class="sxs-lookup"><span data-stu-id="745f0-133">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="745f0-134">Om du känner till Azure PowerShell och behöver migrera från AzureRM läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="745f0-134">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
