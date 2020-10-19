---
title: Migrera Azure PowerShell-skript från AzureRM till Az
description: Läs om stegen och verktygen för att migrera skript från AzureRM-modulen till den nya Az-modulen.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: d0045e283ef062c74a223258fd4d5d6432bac531
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/14/2020
ms.locfileid: "92021099"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="b35ce-103">Migrera Azure PowerShell från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="b35ce-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="b35ce-104">Alla versioner av AzureRM PowerShell-modulen är inaktuella, men stöds fortfarande.</span><span class="sxs-lookup"><span data-stu-id="b35ce-104">All versions of the AzureRM PowerShell module are outdated, but not out of support.</span></span> <span data-ttu-id="b35ce-105">[Az PowerShell-modulen](install-az-ps.md) är nu den rekommenderade PowerShell-modulen för att interagera med Azure.</span><span class="sxs-lookup"><span data-stu-id="b35ce-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

<span data-ttu-id="b35ce-106">Skript som har skrivits för AzureRM-cmdletarna fungerar inte automatiskt med den nya modulen.</span><span class="sxs-lookup"><span data-stu-id="b35ce-106">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="b35ce-107">För att underlätta övergången utvecklades [verktyg för migrering från AzureRM till AZ](https://github.com/Azure/azure-powershell-migration).</span><span class="sxs-lookup"><span data-stu-id="b35ce-107">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="b35ce-108">Ingen migrering till en ny kommandouppsättning är någonsin läglig, men i den här artikeln får du hjälp att komma igång med övergången till Az PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="b35ce-108">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="b35ce-109">Mer information om varför Az PowerShell-modulen skapades finns i [Introduktion till den nya Azure PowerShell Az-modulen](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="b35ce-109">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="b35ce-110">En fullständig lista över icke-bakåtkompatibla ändringar mellan AzureRM och Az finns i de [fullständiga ändringarna från AzureRM till Az](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="b35ce-110">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="b35ce-111">Se till att befintliga skript fungerar med den senaste versionen av AzureRM</span><span class="sxs-lookup"><span data-stu-id="b35ce-111">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="b35ce-112">Innan du påbörjar migreringen bör du kontrollera vilka versioner av AzureRM som finns installerade på datorn.</span><span class="sxs-lookup"><span data-stu-id="b35ce-112">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="b35ce-113">Du kan då se till att skripten redan körs med den senaste versionen, och du ser vilka versioner av AzureRM som behöver avinstalleras.</span><span class="sxs-lookup"><span data-stu-id="b35ce-113">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="b35ce-114">Om du vill kontrollera vilka versioner av AzureRM du har installerade kör du följande exempel:</span><span class="sxs-lookup"><span data-stu-id="b35ce-114">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="b35ce-115">Den **senaste** tillgängliga versionen av AzureRM är **6.13.1**.</span><span class="sxs-lookup"><span data-stu-id="b35ce-115">The **latest** available release of AzureRM is **6.13.1**.</span></span> <span data-ttu-id="b35ce-116">Om du inte har den här versionen kan de befintliga skripten behöva ytterligare modifieringar för att de ska fungera med Az-modulen, förutom det som beskrivs i den här artikeln och i [listan över icke-bakåtkompatibla ändringar](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="b35ce-116">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="b35ce-117">Om skripten inte fungerar med AzureRM 6.13.1 uppdaterar du dem enligt [migreringsguiden för AzureRM 5.x till 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).</span><span class="sxs-lookup"><span data-stu-id="b35ce-117">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="b35ce-118">Om du använder en tidigare version av AzureRM-modulen finns det migreringsguider för varje större version.</span><span class="sxs-lookup"><span data-stu-id="b35ce-118">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="b35ce-119">Installera verktygen för migrering från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="b35ce-119">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="b35ce-120">Migrera PowerShell-skript automatiskt</span><span class="sxs-lookup"><span data-stu-id="b35ce-120">Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="b35ce-121">Med verktygen för migrering från AzureRM till Az kan du skapa en plan för att bestämma vilka ändringar som ska utföras för dina skript innan du ändrar dem och innan du installerar Az PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="b35ce-121">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="b35ce-122">Snabbstarten [Migrera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen](quickstart-migrate-azurerm-to-az-automatically.md) vägleder dig genom hela processen med att uppdatera PowerShell-skript automatiskt från AzureRM till Az PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="b35ce-122">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b35ce-123">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="b35ce-123">Next steps</span></span>

<span data-ttu-id="b35ce-124">[Installera Azure PowerShell](install-az-ps.md)
[Avinstallera AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="b35ce-124">[Install Azure PowerShell](install-az-ps.md)
[Uninstall AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span></span>
