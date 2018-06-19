---
title: Installera Azure PowerShell på macOS eller Linux
description: Så här installerar du Azure PowerShell på macOS eller Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323262"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="d9709-103">Installera Azure PowerShell på macOS eller Linux</span><span class="sxs-lookup"><span data-stu-id="d9709-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="d9709-104">På plattformar som inte använder Windows är det möjligt att både köra Azure PowerShell och PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="d9709-104">For non-Windows platforms, it's possible to run Azure PowerShell on top of PowerShell Core v6.</span></span> <span data-ttu-id="d9709-105">Den här produkten är utformad på .NET Core i stället för det vanliga Azure PowerShell som är skapat på .NET Framework för Windows. Den kan köras på alla plattformar som har stöd för körning på .NET Core.</span><span class="sxs-lookup"><span data-stu-id="d9709-105">Rather than the standard Azure PowerShell built on .NET Framework for Windows, this product is built for .NET Core and can run on any platform which supports the .Net Core runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="d9709-106">För tillfället är både PowerShell Core v6 och Azure PowerShell för .NET Core fortfarande i betaversioner.</span><span class="sxs-lookup"><span data-stu-id="d9709-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="d9709-107">De här produkterna har begränsad support.</span><span class="sxs-lookup"><span data-stu-id="d9709-107">Support for these products is limited.</span></span> <span data-ttu-id="d9709-108">Skicka gärna in ett ärende till GitHub om du har problem eller upptäcker buggar.</span><span class="sxs-lookup"><span data-stu-id="d9709-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="d9709-109">Problem med PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="d9709-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="d9709-110">Problem med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d9709-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a><span data-ttu-id="d9709-111">Installera PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="d9709-111">Install PowerShell Core v6</span></span>

<span data-ttu-id="d9709-112">Processen för att installera PowerShell Core v6 på Linux och macOS varierar beroende på Linux-distribution och operativsystemsversion.</span><span class="sxs-lookup"><span data-stu-id="d9709-112">Installing PowerShell Core v6 on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="d9709-113">Detaljerade anvisningar finns i följande artikel:</span><span class="sxs-lookup"><span data-stu-id="d9709-113">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="d9709-114">Installera PowerShell Core på macOS</span><span class="sxs-lookup"><span data-stu-id="d9709-114">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="d9709-115">Installera PowerShell Core på Linux</span><span class="sxs-lookup"><span data-stu-id="d9709-115">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="d9709-116">Installera Azure PowerShell för .NET Core</span><span class="sxs-lookup"><span data-stu-id="d9709-116">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="d9709-117">I PowerShell Core v6 är modulen PowerShellGet redan installerad.</span><span class="sxs-lookup"><span data-stu-id="d9709-117">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="d9709-118">Det gör det enkelt att installera alla moduler som har publicerats i PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="d9709-118">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="d9709-119">Öppna en ny PowerShell-session och kör följande kommando för att installera Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d9709-119">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a><span data-ttu-id="d9709-120">Läs in modulen AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="d9709-120">Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="d9709-121">När modulen har installerats måste du läsa in modulen i din PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="d9709-121">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="d9709-122">Moduler läses in med `Import-Module`-cmdleten enligt följande:</span><span class="sxs-lookup"><span data-stu-id="d9709-122">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="d9709-123">När importen är färdig kan du testa din nya installation och modulen genom att försöka logga in på Azure med hjälp av följande kommando:</span><span class="sxs-lookup"><span data-stu-id="d9709-123">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="d9709-124">När du har angivit kommandot ovan visas en dialogruta som ber dig att gå till `https://aka.ms/devicelogin` och ange koden som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="d9709-124">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="d9709-125">Tillgängliga cmdlet:ar</span><span class="sxs-lookup"><span data-stu-id="d9709-125">Available cmdlets</span></span>

<span data-ttu-id="d9709-126">Azure PowerShell-moduler för .NET Standard är fortfarande under utveckling.</span><span class="sxs-lookup"><span data-stu-id="d9709-126">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="d9709-127">De här modulerna tillhandahåller inte den fullständiga uppsättningen cmdlet:ar som är tillgängliga för Windows-versionen av modulerna.</span><span class="sxs-lookup"><span data-stu-id="d9709-127">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="d9709-128">Följande funktioner är implementerade i AzureRM.Netcore-moduler:</span><span class="sxs-lookup"><span data-stu-id="d9709-128">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="d9709-129">Kontohantering</span><span class="sxs-lookup"><span data-stu-id="d9709-129">Account management</span></span>
  - <span data-ttu-id="d9709-130">Logga in med ett Microsoft-konto, organisationskonto eller tjänstens huvudnamn via Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d9709-130">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="d9709-131">Spara autentiseringsuppgifterna till disken med Save-AzureRmContext och läs in sparade autentiseringsuppgifter med Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="d9709-131">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="d9709-132">Miljö</span><span class="sxs-lookup"><span data-stu-id="d9709-132">Environment</span></span>
  - <span data-ttu-id="d9709-133">Hämta andra Microsoft Azure-miljöer</span><span class="sxs-lookup"><span data-stu-id="d9709-133">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="d9709-134">Lägg till/Ange/Ta bort anpassade miljöer (t.ex. Azure Stack eller Windows Azure Pack-miljöer)</span><span class="sxs-lookup"><span data-stu-id="d9709-134">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="d9709-135">Cmdlet:ar på hanteringsnivå för Azure-tjänster med Resource Manager- och Service Management-gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d9709-135">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="d9709-136">Virtuell dator</span><span class="sxs-lookup"><span data-stu-id="d9709-136">Virtual Machine</span></span>
  - <span data-ttu-id="d9709-137">App Service (Websites)</span><span class="sxs-lookup"><span data-stu-id="d9709-137">App Service (Websites)</span></span>
  - <span data-ttu-id="d9709-138">SQL Database</span><span class="sxs-lookup"><span data-stu-id="d9709-138">SQL Database</span></span>
  - <span data-ttu-id="d9709-139">Storage</span><span class="sxs-lookup"><span data-stu-id="d9709-139">Storage</span></span>
  - <span data-ttu-id="d9709-140">Nätverk</span><span class="sxs-lookup"><span data-stu-id="d9709-140">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="d9709-141">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="d9709-141">Next Steps</span></span>

<span data-ttu-id="d9709-142">Mer information om användning av Azure PowerShell finns i artikeln [Kom igång med Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d9709-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
