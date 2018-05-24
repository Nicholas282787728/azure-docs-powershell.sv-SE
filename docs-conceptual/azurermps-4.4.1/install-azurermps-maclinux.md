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
ms.openlocfilehash: 9e4c727c9adc378b9f1a65d3cb3dda7af05c33f5
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="79c74-103">Installera och konfigurera Azure PowerShell på macOS och Linux</span><span class="sxs-lookup"><span data-stu-id="79c74-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="79c74-104">Nu är det möjligt att installera PowerShell Core v6 och Azure PowerShell på andra plattformar än Windows-plattformar.</span><span class="sxs-lookup"><span data-stu-id="79c74-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="79c74-105">Processen för att installera Azure PowerShell på macOS och Linux är ungefär densamma som för Windows, men du måste först installera PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="79c74-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="79c74-106">För tillfället är både PowerShell Core v6 och Azure PowerShell för .NET Core fortfarande i betaversioner.</span><span class="sxs-lookup"><span data-stu-id="79c74-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="79c74-107">De här produkterna har begränsad support.</span><span class="sxs-lookup"><span data-stu-id="79c74-107">Support for these products is limited.</span></span> <span data-ttu-id="79c74-108">Skicka gärna in ärenden till GitHub om du har problem eller upptäcker buggar.</span><span class="sxs-lookup"><span data-stu-id="79c74-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="79c74-109">Problem med PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="79c74-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="79c74-110">Problem med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="79c74-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="79c74-111">Steg 1: Installera PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="79c74-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="79c74-112">Processen för att installera PowerShell Core v6 varierar beroende på måloperativsystem.</span><span class="sxs-lookup"><span data-stu-id="79c74-112">The process of installing PowerShell Core v6 on varies depending on the target operating system.</span></span>
<span data-ttu-id="79c74-113">Det går att installera PowerShell Core v6 på Windows, men den här artikeln handlar om macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="79c74-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="79c74-114">Om du vill använda Azure PowerShell på Windows kan du läsa artikeln om att [installera](./install-azurerm-ps.md) på Windows.</span><span class="sxs-lookup"><span data-stu-id="79c74-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="79c74-115">Processen för att installera **PowerShell Core v6** på Linux och macOS varierar beroende på Linux-distribution och operativsystemsversion.</span><span class="sxs-lookup"><span data-stu-id="79c74-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="79c74-116">Detaljerade anvisningar finns i följande artikel:</span><span class="sxs-lookup"><span data-stu-id="79c74-116">Detailed instructions can be found in the following article:</span></span>

- [<span data-ttu-id="79c74-117">Installera PowerShell Core på macOS och Linux</span><span class="sxs-lookup"><span data-stu-id="79c74-117">Installing PowerShell Core on macOS and Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="79c74-118">Steg 2: Installera Azure PowerShell för .NET Core</span><span class="sxs-lookup"><span data-stu-id="79c74-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="79c74-119">I PowerShell Core v6 är modulen PowerShellGet redan installerad.</span><span class="sxs-lookup"><span data-stu-id="79c74-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="79c74-120">Det gör det enkelt att installera alla moduler som har publicerats i PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="79c74-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="79c74-121">Öppna en ny PowerShell-session och kör följande kommando för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="79c74-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="79c74-122">Steg 3: Läs in modulen AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="79c74-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="79c74-123">När modulen har installerats måste du läsa in modulen i din PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="79c74-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="79c74-124">Moduler läses in med `Import-Module`-cmdleten enligt följande:</span><span class="sxs-lookup"><span data-stu-id="79c74-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="79c74-125">När importen är färdig kan du testa din nya installation och modulen genom att försöka logga in på Azure med hjälp av följande kommando:</span><span class="sxs-lookup"><span data-stu-id="79c74-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="79c74-126">När du har angivit kommandot ovan visas en dialogruta som ber dig att gå till `https://aka.ms/devicelogin` och ange koden som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="79c74-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="79c74-127">Tillgängliga cmdlet:ar</span><span class="sxs-lookup"><span data-stu-id="79c74-127">Available cmdlets</span></span>

<span data-ttu-id="79c74-128">Azure PowerShell-moduler för .NET Standard är fortfarande under utveckling.</span><span class="sxs-lookup"><span data-stu-id="79c74-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="79c74-129">De här modulerna tillhandahåller inte den fullständiga uppsättningen cmdlet:ar som är tillgängliga för Windows-versionen av modulerna.</span><span class="sxs-lookup"><span data-stu-id="79c74-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="79c74-130">Följande funktioner är implementerade i AzureRM.Netcore-moduler:</span><span class="sxs-lookup"><span data-stu-id="79c74-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="79c74-131">Kontohantering</span><span class="sxs-lookup"><span data-stu-id="79c74-131">Account management</span></span>
  - <span data-ttu-id="79c74-132">Logga in med ett Microsoft-konto, organisationskonto eller tjänstens huvudnamn via Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="79c74-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="79c74-133">Spara autentiseringsuppgifterna till disken med Save-AzureRmContext och läs in sparade autentiseringsuppgifter med Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="79c74-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="79c74-134">Miljö</span><span class="sxs-lookup"><span data-stu-id="79c74-134">Environment</span></span>
  - <span data-ttu-id="79c74-135">Hämta andra Microsoft Azure-miljöer</span><span class="sxs-lookup"><span data-stu-id="79c74-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="79c74-136">Lägg till/Ange/Ta bort anpassade miljöer (t.ex. Azure Stack eller Windows Azure Pack-miljöer)</span><span class="sxs-lookup"><span data-stu-id="79c74-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="79c74-137">Cmdlet:ar på hanteringsnivå för Azure-tjänster med Resource Manager- och Service Management-gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="79c74-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="79c74-138">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="79c74-138">Virtual Machine</span></span>
  - <span data-ttu-id="79c74-139">App Service (Websites)</span><span class="sxs-lookup"><span data-stu-id="79c74-139">App Service (Websites)</span></span>
  - <span data-ttu-id="79c74-140">SQL Database</span><span class="sxs-lookup"><span data-stu-id="79c74-140">SQL Database</span></span>
  - <span data-ttu-id="79c74-141">Storage</span><span class="sxs-lookup"><span data-stu-id="79c74-141">Storage</span></span>
  - <span data-ttu-id="79c74-142">Nätverk</span><span class="sxs-lookup"><span data-stu-id="79c74-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="79c74-143">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="79c74-143">Next Steps</span></span>

<span data-ttu-id="79c74-144">Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="79c74-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
