---
title: Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen
description: Lär dig hur du migrerar PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/18/2020
ms.openlocfilehash: 3a26dfbb89f83a9d1983ea8d69cd47c9f74eab38
ms.sourcegitcommit: dd90c54d8794109fa7984543649bb3faa0cbb544
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/19/2020
ms.locfileid: "97701297"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="c0bf6-103">Snabbstart: Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="c0bf6-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="c0bf6-104">I den här artikeln får du lära dig hur du uppgraderar dina PowerShell-skript och skriptmoduler från AzureRM till Az PowerShell-modulen automatiskt med hjälp av PowerShell-modulen Az.Tools.Migration.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span> <span data-ttu-id="c0bf6-105">Fler migreringsalternativ finns i [Migrera Azure PowerShell från AzureRM till Az](/powershell/azure/migrate-from-azurerm-to-az).</span><span class="sxs-lookup"><span data-stu-id="c0bf6-105">For additional migration options, see [Migrate Azure PowerShell from AzureRM to Az](/powershell/azure/migrate-from-azurerm-to-az).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0bf6-106">Krav</span><span class="sxs-lookup"><span data-stu-id="c0bf6-106">Requirements</span></span>

* <span data-ttu-id="c0bf6-107">Uppdatera dina befintliga PowerShell-skript till den senaste versionen av [AzureRM PowerShell-modulen (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="c0bf6-107">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="c0bf6-108">Installera PowerShell-modulen Az.Tools.Migration.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-108">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="c0bf6-109">Steg 1: Skapa en uppgraderingsplan</span><span class="sxs-lookup"><span data-stu-id="c0bf6-109">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="c0bf6-110">Med cmdleten **`New-AzUpgradeModulePlan`** skapar du en uppgraderingsplan för att migrera dina skript och moduler till Az PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-110">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="c0bf6-111">Denna cmdlet gör inga ändringar i dina befintliga skript.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-111">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="c0bf6-112">Använd **`FilePath`** -parametern för att rikta in på ett särskilt skript eller **`DirectoryPath`** -parameter för att rikta in på alla skript i en speciell mapp.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-112">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="c0bf6-113">Cmdleten **`New-AzUpgradeModulePlan`** kör inte planen. Den genererar bara uppgraderingsstegen.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-113">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="c0bf6-114">I följande exempel skapas en plan för alla skript i mappen _`C:\Scripts`_ .</span><span class="sxs-lookup"><span data-stu-id="c0bf6-114">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="c0bf6-115">**`OutVariable`** -parametern anges så att resultaten returneras och lagras samtidigt i en variabel med namnet **`Plan`** .</span><span class="sxs-lookup"><span data-stu-id="c0bf6-115">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="c0bf6-116">Som du ser i följande utdata specificerar uppgraderingsplanen den specifika filen och de offsetpunkter som behöver ändras vid flytten från AzureRM till Az PowerShell-cmdletarna.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-116">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

<span data-ttu-id="c0bf6-117">Innan du utför uppgraderingen måste du se resultatet av planen för problem.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-117">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="c0bf6-118">I följande exempel returneras en lista över skript och objekten i dessa skript som hindrar dem från att uppgraderas automatiskt.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-118">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="c0bf6-119">De objekt som visas i följande utdata kommer inte att uppgraderas automatiskt utan att problemen först korrigeras manuellt.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-119">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span> <span data-ttu-id="c0bf6-120">Kända problem som inte kan uppgraderas automatiskt innehåller alla kommandon som använder ihopbuntning.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-120">Known issues that can’t be upgraded automatically include any commands that use splatting.</span></span>

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="c0bf6-121">Steg 2: Genomför uppgraderingen</span><span class="sxs-lookup"><span data-stu-id="c0bf6-121">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="c0bf6-122">Detta går inte att ångra.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-122">There is no undo operation.</span></span> <span data-ttu-id="c0bf6-123">Se alltid till att du har en säkerhetskopia av de PowerShell-skript och moduler som du tänker uppgradera.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-123">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="c0bf6-124">När du är nöjd med planen utförs uppgraderingen med **`Invoke-AzUpgradeModulePlan`** -cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-124">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="c0bf6-125">Ange **`SaveChangesToNewFiles`** för parametervärdet **`FileEditMode`** för att förhindra att ändringar görs i de ursprungliga skripten.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-125">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="c0bf6-126">När du använder det här läget utförs uppgraderingen genom att skapa en kopia av varje inriktat skript med _`_az_upgraded`_ i filnamnet.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-126">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="c0bf6-127">Cmdleten **`Invoke-AzUpgradeModulePlan`** är destruktiv när alternativet **`-FileEditMode ModifyExistingFiles`** har angetts!</span><span class="sxs-lookup"><span data-stu-id="c0bf6-127">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="c0bf6-128">Den ändrar dina skript och funktioner på plats enligt den moduluppgraderingsplan som skapades av cmdleten **`New-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="c0bf6-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="c0bf6-129">Som icke-destruktivt alternativ anger du i stället **`-FileEditMode SaveChangesToNewFiles`** .</span><span class="sxs-lookup"><span data-stu-id="c0bf6-129">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

<span data-ttu-id="c0bf6-130">Om fel returneras kan du ta en närmare titt på felresultaten med hjälp av följande kommando:</span><span class="sxs-lookup"><span data-stu-id="c0bf6-130">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a><span data-ttu-id="c0bf6-131">Begränsningar</span><span class="sxs-lookup"><span data-stu-id="c0bf6-131">Limitations</span></span>

* <span data-ttu-id="c0bf6-132">Automatiserade ändringar av parameternamn till ihopslagna parameteruppsättningar stöds inte.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-132">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="c0bf6-133">Om det påträffas när en uppgraderingsplan skapas returneras en varning.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-133">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="c0bf6-134">Fil-I/O-åtgärder använder standardkodning.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-134">File I/O operations use default encoding.</span></span> <span data-ttu-id="c0bf6-135">Ovanliga filkodningssituationer kan orsaka problem.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-135">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="c0bf6-136">AzureRM-cmdletar som skickats som argument till testuttryck i Pester-enhetstester identifieras inte.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-136">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="c0bf6-137">För närvarande stöds endast AZ PowerShell-modul version 4.6.1 som mål.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-137">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="c0bf6-138">Så här rapporterar du problem</span><span class="sxs-lookup"><span data-stu-id="c0bf6-138">How to report issues</span></span>

<span data-ttu-id="c0bf6-139">Du kan ge feedback och rapportera problem med PowerShell-modulen Az.Tools.Migration via [ett GitHub-ärende](https://github.com/Azure/azure-powershell-migration/issues) på lagringsplatsen `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="c0bf6-139">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c0bf6-140">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="c0bf6-140">Next steps</span></span>

<span data-ttu-id="c0bf6-141">Du kan läsa mer om Azure PowerShell-modulen i [Azure PowerShell-dokumentationen](/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="c0bf6-141">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>