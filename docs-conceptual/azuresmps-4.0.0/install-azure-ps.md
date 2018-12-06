---
title: Installera och konfigurera Azure PowerShell Service Management-modulen | Microsoft Docs
description: Installera och konfigurera Azure PowerShell för första gången.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 6cc6d9984e49c0cbc23c7ef3a77b98c0b7f3a8e0
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828339"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="7165e-103">Installera Azure PowerShell Service Management-modulen</span><span class="sxs-lookup"><span data-stu-id="7165e-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="7165e-104">Vi rekommenderar att du installerar Azure PowerShell från [PowerShell-galleriet](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="7165e-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="7165e-105">Steg 1: Installera PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="7165e-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="7165e-106">Du måste ha modulen PowerShellGet för att kunna installera objekt från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="7165e-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="7165e-107">Kontrollera att du har rätt version av PowerShellGet och att datorn uppfyller övriga systemkrav.</span><span class="sxs-lookup"><span data-stu-id="7165e-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="7165e-108">Kör följande kommando för att se om du har PowerShellGet installerat på datorn.</span><span class="sxs-lookup"><span data-stu-id="7165e-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="7165e-109">Nu bör du se utdata som ser ut ungefär så här:</span><span class="sxs-lookup"><span data-stu-id="7165e-109">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="7165e-110">Om du inte har installerat PowerShellGet kan du läsa avsnittet [Hämta PowerShellGet](#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="7165e-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="7165e-111">Steg 2: Installera Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7165e-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="7165e-112">Kör följande kommando från Windows PowerShell-konsolen som körs som administratör:</span><span class="sxs-lookup"><span data-stu-id="7165e-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="7165e-113">Azure-modulen är en sammanslagen modul för Azure Resource Manager-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="7165e-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="7165e-114">När du installerar AzureRM-modulen kommer alla övriga Azure-moduler som inte har installerats att hämtas och installeras från PowerShell-galleriet.</span><span class="sxs-lookup"><span data-stu-id="7165e-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="7165e-115">Azure Service Management-modulen delar beroenden med Azure PowerShell Resource Manager-modulerna.</span><span class="sxs-lookup"><span data-stu-id="7165e-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="7165e-116">Om du har installerat Azure PowerShell Resource Manager-modulerna måste du lägga till parametern `-AllowClobber` i installationskommandot.</span><span class="sxs-lookup"><span data-stu-id="7165e-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="7165e-117">Det tillåter att befintliga delade beroenden uppdateras.</span><span class="sxs-lookup"><span data-stu-id="7165e-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="7165e-118">Utan den här parametern misslyckas installationen av modulen.</span><span class="sxs-lookup"><span data-stu-id="7165e-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="7165e-119">När du har installerat den här modulen kan du importera modulen genom att köra följande kommando:</span><span class="sxs-lookup"><span data-stu-id="7165e-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="7165e-120">Använda cmdletar</span><span class="sxs-lookup"><span data-stu-id="7165e-120">To use the cmdlets</span></span>

<span data-ttu-id="7165e-121">Logga först in på ditt Azure-konto om du vill börja arbeta med cmdletar för Azure Service Management.</span><span class="sxs-lookup"><span data-stu-id="7165e-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="7165e-122">Kör följande kommando för att logga in på ditt konto:</span><span class="sxs-lookup"><span data-stu-id="7165e-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="7165e-123">När du har loggat in på Azure skapar Azure PowerShell en kontext för den angivna sessionen.</span><span class="sxs-lookup"><span data-stu-id="7165e-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="7165e-124">Den kontexten innehåller miljö, konto, klient och prenumeration för Azure PowerShell som ska användas för alla cmdletar i den sessionen.</span><span class="sxs-lookup"><span data-stu-id="7165e-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="7165e-125">Du är nu redo att använda modulerna nedan.</span><span class="sxs-lookup"><span data-stu-id="7165e-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="7165e-126">Azure Service Management-cmdletar</span><span class="sxs-lookup"><span data-stu-id="7165e-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="7165e-127">Azure PowerShell-modulerna uppdateras kontinuerligt.</span><span class="sxs-lookup"><span data-stu-id="7165e-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="7165e-128">Om du märker att onlinehjälpen för cmdletar omfattar cmdletar eller parametrar som inte finns i din modul bör du hämta och installera den senaste versionen av modulen.</span><span class="sxs-lookup"><span data-stu-id="7165e-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="7165e-129">Du kan hitta modulens version genom att skriva in: `(Get-Module Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="7165e-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="7165e-130">Om du vill ha exempelskript som kan hjälpa dig att automatisera vissa av de vanliga uppgifterna i Azure kan du se [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="7165e-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="7165e-131">Allmän information om installation, inlärning, användning och anpassning av Windows PowerShell finns i [Skript med Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span><span class="sxs-lookup"><span data-stu-id="7165e-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="7165e-132">Hämta PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="7165e-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="7165e-133">OS-version</span><span class="sxs-lookup"><span data-stu-id="7165e-133">OS Version</span></span>|<span data-ttu-id="7165e-134">Installationsinstruktioner</span><span class="sxs-lookup"><span data-stu-id="7165e-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="7165e-135">Jag har Windows 10 eller Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7165e-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="7165e-136">Inbyggt i Windows Management Framework (WMF) 5.0 som ingår i operativsystemet</span><span class="sxs-lookup"><span data-stu-id="7165e-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="7165e-137">Jag vill uppgradera till PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="7165e-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="7165e-138">Installera den senaste versionen av WMF</span><span class="sxs-lookup"><span data-stu-id="7165e-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="7165e-139">Jag använder en Windows-version med PowerShell 3 eller PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="7165e-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="7165e-140">Hämta PackageManagement-moduler</span><span class="sxs-lookup"><span data-stu-id="7165e-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="7165e-141">Kontrollera Azure PowerShell-versionen</span><span class="sxs-lookup"><span data-stu-id="7165e-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="7165e-142">Flera versioner av Azure PowerShell stöds, men vi rekommenderar att du uppgraderar till den senaste versionen så snabbt som möjligt.</span><span class="sxs-lookup"><span data-stu-id="7165e-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="7165e-143">Om du vill kontrollera vilken version av Azure PowerShell som du har installerat kör du `Get-Module AzureRM` från kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="7165e-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
