---
title: Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen
description: Lär dig hur du migrerar PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: d342ca65baf7664f430de3b7d294c0fc9815c0a0
ms.sourcegitcommit: d0045e283ef062c74a223258fd4d5d6432bac531
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/14/2020
ms.locfileid: "92021157"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="b2312-103">Snabbstart: Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="b2312-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="b2312-104">I den här artikeln får du lära dig hur du uppgraderar dina PowerShell-skript och skriptmoduler från AzureRM till Az PowerShell-modulen automatiskt med hjälp av PowerShell-modulen Az.Tools.Migration.</span><span class="sxs-lookup"><span data-stu-id="b2312-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2312-105">PowerShell-modulen Az.Tools.Migration finns för närvarande som allmänt tillgänglig förhandsversion.</span><span class="sxs-lookup"><span data-stu-id="b2312-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="b2312-106">Förhandsversionen tillhandahålls utan serviceavtal.</span><span class="sxs-lookup"><span data-stu-id="b2312-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="b2312-107">Den rekommenderas inte för produktionsarbetsbelastningar.</span><span class="sxs-lookup"><span data-stu-id="b2312-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="b2312-108">Vissa funktioner kanske inte stöds eller kan vara begränsade.</span><span class="sxs-lookup"><span data-stu-id="b2312-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="b2312-109">Mer information finns i [Kompletterande villkor för användning av Microsoft Azure-förhandsversioner](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="b2312-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

<span data-ttu-id="b2312-110">Du kan ge feedback och rapportera problem med PowerShell-modulen Az.Tools.Migration via [ett GitHub-ärende](https://github.com/Azure/azure-powershell-migration/issues) på lagringsplatsen `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="b2312-110">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2312-111">Krav</span><span class="sxs-lookup"><span data-stu-id="b2312-111">Requirements</span></span>

* <span data-ttu-id="b2312-112">Uppdatera dina befintliga PowerShell-skript till den senaste versionen av [AzureRM PowerShell-modulen (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="b2312-112">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="b2312-113">Installera PowerShell-modulen Az.Tools.Migration.</span><span class="sxs-lookup"><span data-stu-id="b2312-113">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="b2312-114">Steg 1: Skapa en uppgraderingsplan</span><span class="sxs-lookup"><span data-stu-id="b2312-114">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="b2312-115">Med cmdleten `New-AzUpgradeModulePlan` skapar du en uppgraderingsplan för att migrera dina skript och moduler till Az PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="b2312-115">You use the `New-AzUpgradeModulePlan` cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="b2312-116">Uppgraderingsplanen specificerar den specifika filen och de offsetpunkter som behöver ändras vid flytten från AzureRM till Az PowerShell-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="b2312-116">The upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="b2312-117">Cmdleten `New-AzUpgradeModulePlan` kör inte planen. Den genererar bara uppgraderingsstegen.</span><span class="sxs-lookup"><span data-stu-id="b2312-117">The `New-AzUpgradeModulePlan` cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

<span data-ttu-id="b2312-118">Granska resultatet av uppgraderingsplanen.</span><span class="sxs-lookup"><span data-stu-id="b2312-118">Review the results of the upgrade plan.</span></span>

```powershell
# Show the entire upgrade plan
$Plan
```

<span data-ttu-id="b2312-119">Kör följande kommando för att filtrera resultatet och visa kommandon som har varningar eller fel.</span><span class="sxs-lookup"><span data-stu-id="b2312-119">Run the following command to filter the results to commands that have warnings or errors.</span></span> <span data-ttu-id="b2312-120">På så sätt kan du snabbt identifiera fel innan du utför uppgraderingen, vilket är praktiskt om du har stora resultatmängder.</span><span class="sxs-lookup"><span data-stu-id="b2312-120">This may be helpful on large result sets to quickly identify errors before performing the upgrade.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="b2312-121">Steg 2: Genomför uppgraderingen</span><span class="sxs-lookup"><span data-stu-id="b2312-121">Step 2: Perform the upgrade</span></span>

<span data-ttu-id="b2312-122">Uppgraderingsplanen utförs när du kör cmdleten `Invoke-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="b2312-122">The upgrade plan is executed when you run the `Invoke-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="b2312-123">Det här kommandot utför en uppgradering av den angivna filen eller mapparna förutom eventuella fel som identifierades av cmdleten `New-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="b2312-123">This command performs an upgrade of the specified file or folders except for any errors that were identified by the `New-AzUpgradeModulePlan` cmdlet.</span></span>

<span data-ttu-id="b2312-124">Det här kommandot kräver att du anger om filerna ska ändras på plats eller om nya filer ska sparas vid sidan av dina ursprungliga filer (de ursprungliga filerna lämnas oförändrade).</span><span class="sxs-lookup"><span data-stu-id="b2312-124">This command requires you to specify if the files should be modified in place or if new files should be saved alongside your original files (leaving originals unmodified).</span></span>

> [!CAUTION]
> <span data-ttu-id="b2312-125">Detta går inte att ångra.</span><span class="sxs-lookup"><span data-stu-id="b2312-125">There is no undo operation.</span></span> <span data-ttu-id="b2312-126">Se alltid till att du har en säkerhetskopia av dina PowerShell-skript och moduler som du tänker uppgradera.</span><span class="sxs-lookup"><span data-stu-id="b2312-126">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

> [!WARNING]
> <span data-ttu-id="b2312-127">Cmdleten `Invoke-AzUpgradeModulePlan` är destruktiv när alternativet `-FileEditMode ModifyExistingFiles` har angetts!</span><span class="sxs-lookup"><span data-stu-id="b2312-127">The `Invoke-AzUpgradeModulePlan` cmdlet is destructive when the `-FileEditMode ModifyExistingFiles` option is specified!</span></span> <span data-ttu-id="b2312-128">Den ändrar dina skript och funktioner på plats enligt den moduluppgraderingsplan som skapades av cmdleten `New-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="b2312-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the `New-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="b2312-129">Som icke-destruktivt alternativ anger du i stället `-FileEditMode SaveChangesToNewFiles`.</span><span class="sxs-lookup"><span data-stu-id="b2312-129">For the non-destructive option specify `-FileEditMode SaveChangesToNewFiles` instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

<span data-ttu-id="b2312-130">Granska resultatet av uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="b2312-130">Review the results of the upgrade operation.</span></span>

```powershell
# Show the results for the entire upgrade operation
$Results
```

<span data-ttu-id="b2312-131">Om fel returneras kan du ta en närmare titt på felresultaten med hjälp av följande kommando:</span><span class="sxs-lookup"><span data-stu-id="b2312-131">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a><span data-ttu-id="b2312-132">Begränsningar</span><span class="sxs-lookup"><span data-stu-id="b2312-132">Limitations</span></span>

* <span data-ttu-id="b2312-133">Automatiserade ändringar av parameternamn till ihopslagna parameteruppsättningar stöds inte.</span><span class="sxs-lookup"><span data-stu-id="b2312-133">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="b2312-134">Om det påträffas när en uppgraderingsplan skapas returneras en varning.</span><span class="sxs-lookup"><span data-stu-id="b2312-134">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="b2312-135">Fil-I/O-åtgärder använder standardkodning.</span><span class="sxs-lookup"><span data-stu-id="b2312-135">File I/O operations use default encoding.</span></span> <span data-ttu-id="b2312-136">Ovanliga filkodningssituationer kan orsaka problem.</span><span class="sxs-lookup"><span data-stu-id="b2312-136">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="b2312-137">AzureRM-cmdletar som skickats som argument till testuttryck i Pester-enhetstester identifieras inte.</span><span class="sxs-lookup"><span data-stu-id="b2312-137">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="b2312-138">För närvarande stöds endast AZ PowerShell-modul version 4.6.1 som mål.</span><span class="sxs-lookup"><span data-stu-id="b2312-138">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b2312-139">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="b2312-139">Next steps</span></span>

<span data-ttu-id="b2312-140">Du kan läsa mer om Azure PowerShell-modulen i [Azure PowerShell-dokumentationen](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="b2312-140">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](https://docs.microsoft.com/powershell/azure/)</span></span>