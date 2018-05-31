---
title: Installera och konfigurera Azure PowerShell på macOS och Linux | Microsoft Docs
description: Så här installerar och konfigurerar du Azure PowerShell på macOS och Linux för första gången.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: e2d73f78563b550403e9fd8b66beeef431a384b6
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/23/2018
ms.locfileid: "34462157"
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="eedb3-103">Installera och konfigurera Azure PowerShell på macOS och Linux</span><span class="sxs-lookup"><span data-stu-id="eedb3-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="eedb3-104">Nu är det möjligt att installera PowerShell Core v6 och Azure PowerShell på andra plattformar än Windows-plattformar.</span><span class="sxs-lookup"><span data-stu-id="eedb3-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="eedb3-105">Processen för att installera Azure PowerShell på macOS och Linux är ungefär densamma som för Windows, men du måste först installera PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="eedb3-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="eedb3-106">För tillfället är både PowerShell Core v6 och Azure PowerShell för .NET Core fortfarande i betaversioner.</span><span class="sxs-lookup"><span data-stu-id="eedb3-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="eedb3-107">De här produkterna har begränsad support.</span><span class="sxs-lookup"><span data-stu-id="eedb3-107">Support for these products is limited.</span></span> <span data-ttu-id="eedb3-108">Skicka gärna in ärenden till GitHub om du har problem eller upptäcker buggar.</span><span class="sxs-lookup"><span data-stu-id="eedb3-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="eedb3-109">Problem med PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="eedb3-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="eedb3-110">Problem med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="eedb3-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="eedb3-111">Steg 1: Installera PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="eedb3-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="eedb3-112">Processen för att installera PowerShell Core v6 varierar beroende på måloperativsystem.</span><span class="sxs-lookup"><span data-stu-id="eedb3-112">The process of installing PowerShell Core v6 varies depending on the target operating system.</span></span>
<span data-ttu-id="eedb3-113">Det går att installera PowerShell Core v6 på Windows, men den här artikeln handlar om macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="eedb3-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="eedb3-114">Om du vill använda Azure PowerShell på Windows kan du läsa artikeln om att [installera](./install-azurerm-ps.md) på Windows.</span><span class="sxs-lookup"><span data-stu-id="eedb3-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="eedb3-115">Processen för att installera **PowerShell Core v6** på Linux och macOS varierar beroende på Linux-distribution och operativsystemsversion.</span><span class="sxs-lookup"><span data-stu-id="eedb3-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="eedb3-116">Detaljerade anvisningar finns i följande artikel:</span><span class="sxs-lookup"><span data-stu-id="eedb3-116">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="eedb3-117">Installera PowerShell Core på macOS</span><span class="sxs-lookup"><span data-stu-id="eedb3-117">Installing PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="eedb3-118">Installera PowerShell Core på Linux</span><span class="sxs-lookup"><span data-stu-id="eedb3-118">Installing PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="eedb3-119">Steg 2: Installera Azure PowerShell för .NET Core</span><span class="sxs-lookup"><span data-stu-id="eedb3-119">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="eedb3-120">I PowerShell Core v6 är modulen PowerShellGet redan installerad.</span><span class="sxs-lookup"><span data-stu-id="eedb3-120">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="eedb3-121">Det gör det enkelt att installera alla moduler som har publicerats i PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="eedb3-121">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="eedb3-122">Öppna en ny PowerShell-session och kör följande kommando för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="eedb3-122">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="eedb3-123">Steg 3: Läs in modulen AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="eedb3-123">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="eedb3-124">När modulen har installerats måste du läsa in modulen i din PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="eedb3-124">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="eedb3-125">Moduler läses in med `Import-Module`-cmdleten enligt följande:</span><span class="sxs-lookup"><span data-stu-id="eedb3-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="eedb3-126">När importen är färdig kan du testa din nya installation och modulen genom att försöka logga in på Azure med hjälp av följande kommando:</span><span class="sxs-lookup"><span data-stu-id="eedb3-126">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="eedb3-127">När du har angivit kommandot ovan visas en dialogruta som ber dig att gå till `https://aka.ms/devicelogin` och ange koden som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="eedb3-127">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="eedb3-128">Tillgängliga cmdlet:ar</span><span class="sxs-lookup"><span data-stu-id="eedb3-128">Available cmdlets</span></span>

<span data-ttu-id="eedb3-129">Azure PowerShell-moduler för .NET Standard är fortfarande under utveckling.</span><span class="sxs-lookup"><span data-stu-id="eedb3-129">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="eedb3-130">De här modulerna tillhandahåller inte den fullständiga uppsättningen cmdlet:ar som är tillgängliga för Windows-versionen av modulerna.</span><span class="sxs-lookup"><span data-stu-id="eedb3-130">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="eedb3-131">Följande funktioner är implementerade i AzureRM.Netcore-moduler:</span><span class="sxs-lookup"><span data-stu-id="eedb3-131">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="eedb3-132">Kontohantering</span><span class="sxs-lookup"><span data-stu-id="eedb3-132">Account management</span></span>
  - <span data-ttu-id="eedb3-133">Logga in med ett Microsoft-konto, organisationskonto eller tjänstens huvudnamn via Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="eedb3-133">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="eedb3-134">Spara autentiseringsuppgifterna till disken med Save-AzureRmContext och läs in sparade autentiseringsuppgifter med Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="eedb3-134">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="eedb3-135">Miljö</span><span class="sxs-lookup"><span data-stu-id="eedb3-135">Environment</span></span>
  - <span data-ttu-id="eedb3-136">Hämta andra Microsoft Azure-miljöer</span><span class="sxs-lookup"><span data-stu-id="eedb3-136">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="eedb3-137">Lägg till/Ange/Ta bort anpassade miljöer (t.ex. Azure Stack eller Windows Azure Pack-miljöer)</span><span class="sxs-lookup"><span data-stu-id="eedb3-137">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="eedb3-138">Cmdlet:ar på hanteringsnivå för Azure-tjänster med Resource Manager- och Service Management-gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="eedb3-138">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="eedb3-139">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="eedb3-139">Virtual Machine</span></span>
  - <span data-ttu-id="eedb3-140">App Service (Websites)</span><span class="sxs-lookup"><span data-stu-id="eedb3-140">App Service (Websites)</span></span>
  - <span data-ttu-id="eedb3-141">SQL Database</span><span class="sxs-lookup"><span data-stu-id="eedb3-141">SQL Database</span></span>
  - <span data-ttu-id="eedb3-142">Storage</span><span class="sxs-lookup"><span data-stu-id="eedb3-142">Storage</span></span>
  - <span data-ttu-id="eedb3-143">Nätverk</span><span class="sxs-lookup"><span data-stu-id="eedb3-143">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="eedb3-144">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="eedb3-144">Next Steps</span></span>

<span data-ttu-id="eedb3-145">Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="eedb3-145">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
