---
title: Installera och konfigurera Azure PowerShell på macOS och Linux | Microsoft Docs
description: Så här installerar och konfigurerar du Azure PowerShell på macOS och Linux för första gången.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: eed7a35fcf20a17c83d9e5e3272be4b77fa12c34
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="ee7d8-103">Installera och konfigurera Azure PowerShell på macOS och Linux</span><span class="sxs-lookup"><span data-stu-id="ee7d8-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="ee7d8-104">Nu är det möjligt att installera PowerShell Core v6 och Azure PowerShell på andra plattformar än Windows-plattformar.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="ee7d8-105">Processen för att installera Azure PowerShell på macOS och Linux är ungefär densamma som för Windows, men du måste först installera PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="ee7d8-106">För tillfället är både PowerShell Core v6 och Azure PowerShell för .NET Core fortfarande i betaversioner.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="ee7d8-107">De här produkterna har begränsad support.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-107">Support for these products is limited.</span></span> <span data-ttu-id="ee7d8-108">Skicka gärna in ärenden till GitHub om du har problem eller upptäcker buggar.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="ee7d8-109">Problem med PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="ee7d8-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="ee7d8-110">Problem med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee7d8-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="ee7d8-111">Steg 1: Installera PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="ee7d8-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="ee7d8-112">Processen för att installera PowerShell Core v6 varierar beroende på måloperativsystem.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-112">The process of installing PowerShell Core v6 varies depending on the target operating system.</span></span>
<span data-ttu-id="ee7d8-113">Det går att installera PowerShell Core v6 på Windows, men den här artikeln handlar om macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="ee7d8-114">Om du vill använda Azure PowerShell på Windows kan du läsa artikeln om att [installera](./install-azurerm-ps.md) på Windows.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="ee7d8-115">Processen för att installera **PowerShell Core v6** på Linux och macOS varierar beroende på Linux-distribution och operativsystemsversion.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="ee7d8-116">Detaljerade anvisningar finns i följande artikel:</span><span class="sxs-lookup"><span data-stu-id="ee7d8-116">Detailed instructions can be found in the following article:</span></span>

- [<span data-ttu-id="ee7d8-117">Installera PowerShell Core på macOS och Linux</span><span class="sxs-lookup"><span data-stu-id="ee7d8-117">Installing PowerShell Core on macOS and Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="ee7d8-118">Steg 2: Installera Azure PowerShell för .NET Core</span><span class="sxs-lookup"><span data-stu-id="ee7d8-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="ee7d8-119">I PowerShell Core v6 är modulen PowerShellGet redan installerad.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="ee7d8-120">Det gör det enkelt att installera alla moduler som har publicerats i PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="ee7d8-121">Öppna en ny PowerShell-session och kör följande kommando för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ee7d8-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="ee7d8-122">Steg 3: Läs in modulen AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="ee7d8-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="ee7d8-123">När modulen har installerats måste du läsa in modulen i din PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="ee7d8-124">Moduler läses in med `Import-Module`-cmdleten enligt följande:</span><span class="sxs-lookup"><span data-stu-id="ee7d8-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="ee7d8-125">När importen är färdig kan du testa din nya installation och modulen genom att försöka logga in på Azure med hjälp av följande kommando:</span><span class="sxs-lookup"><span data-stu-id="ee7d8-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="ee7d8-126">När du har angivit kommandot ovan visas en dialogruta som ber dig att gå till `https://aka.ms/devicelogin` och ange koden som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="ee7d8-127">Tillgängliga cmdlet:ar</span><span class="sxs-lookup"><span data-stu-id="ee7d8-127">Available cmdlets</span></span>

<span data-ttu-id="ee7d8-128">Azure PowerShell-moduler för .NET Standard är fortfarande under utveckling.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="ee7d8-129">De här modulerna tillhandahåller inte den fullständiga uppsättningen cmdlet:ar som är tillgängliga för Windows-versionen av modulerna.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="ee7d8-130">Följande funktioner är implementerade i AzureRM.Netcore-moduler:</span><span class="sxs-lookup"><span data-stu-id="ee7d8-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="ee7d8-131">Kontohantering</span><span class="sxs-lookup"><span data-stu-id="ee7d8-131">Account management</span></span>
  - <span data-ttu-id="ee7d8-132">Logga in med ett Microsoft-konto, organisationskonto eller tjänstens huvudnamn via Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ee7d8-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="ee7d8-133">Spara autentiseringsuppgifterna till disken med Save-AzureRmContext och läs in sparade autentiseringsuppgifter med Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ee7d8-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="ee7d8-134">Miljö</span><span class="sxs-lookup"><span data-stu-id="ee7d8-134">Environment</span></span>
  - <span data-ttu-id="ee7d8-135">Hämta andra Microsoft Azure-miljöer</span><span class="sxs-lookup"><span data-stu-id="ee7d8-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="ee7d8-136">Lägg till/Ange/Ta bort anpassade miljöer (t.ex. Azure Stack eller Windows Azure Pack-miljöer)</span><span class="sxs-lookup"><span data-stu-id="ee7d8-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="ee7d8-137">Cmdlet:ar på hanteringsnivå för Azure-tjänster med Resource Manager- och Service Management-gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="ee7d8-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="ee7d8-138">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ee7d8-138">Virtual Machine</span></span>
  - <span data-ttu-id="ee7d8-139">App Service (Websites)</span><span class="sxs-lookup"><span data-stu-id="ee7d8-139">App Service (Websites)</span></span>
  - <span data-ttu-id="ee7d8-140">SQL Database</span><span class="sxs-lookup"><span data-stu-id="ee7d8-140">SQL Database</span></span>
  - <span data-ttu-id="ee7d8-141">Storage</span><span class="sxs-lookup"><span data-stu-id="ee7d8-141">Storage</span></span>
  - <span data-ttu-id="ee7d8-142">Nätverk</span><span class="sxs-lookup"><span data-stu-id="ee7d8-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="ee7d8-143">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="ee7d8-143">Next Steps</span></span>

<span data-ttu-id="ee7d8-144">Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ee7d8-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
