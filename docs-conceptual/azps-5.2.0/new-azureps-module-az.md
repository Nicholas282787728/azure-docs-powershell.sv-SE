---
title: Introduktion till Azure Az PowerShell-modulen
description: Vi presenterar Az PowerShell-modulen. Modulen ersätter AzureRM PowerShell-modulen och rekommenderas för interaktion med Azure.
ms.date: 12/1/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 9021a1d8fdc73aedb87b17631f8e67cb8ef79166
ms.sourcegitcommit: a6d92493a8d1b81b85f4db2a38f271134be5e6c5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/12/2020
ms.locfileid: "97353860"
---
# <a name="introducing-the-azure-az-powershell-module"></a><span data-ttu-id="c9230-103">Introduktion till Azure Az PowerShell-modulen</span><span class="sxs-lookup"><span data-stu-id="c9230-103">Introducing the Azure Az PowerShell module</span></span>

## <a name="overview"></a><span data-ttu-id="c9230-104">Översikt</span><span class="sxs-lookup"><span data-stu-id="c9230-104">Overview</span></span>

<span data-ttu-id="c9230-105">Az PowerShell-modulen är en uppsättning cmdlets för hantering av Azure-resurser direkt från PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9230-105">The Az PowerShell module is a set of cmdlets for managing Azure resources directly from PowerShell.</span></span> <span data-ttu-id="c9230-106">PowerShell har kraftfulla automatiseringsfunktioner som underlättar hanteringen av Azure-resurser exempelvis i kontexten för en CI/CD-pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9230-106">PowerShell provides powerful features for automation that can be leveraged for managing your Azure resources for examples in the context of a CI/CD pipeline.</span></span>

<span data-ttu-id="c9230-107">Az PowerShell-modulen ersätter AzureRM och är den rekommenderade versionen för interaktion med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9230-107">The Az PowerShell module is the replacement of AzureRM and is the recommended version to use for interacting with Azure.</span></span>

<span data-ttu-id="c9230-108">Du kan använda Az PowerShell-modulen genom att göra något av följande:</span><span class="sxs-lookup"><span data-stu-id="c9230-108">You can use the Az PowerShell module with one of the following methods:</span></span>

* <span data-ttu-id="c9230-109">[Installera Az PowerShell-modulen via PowerShellGet](install-az-ps.md) (rekommenderat alternativ).</span><span class="sxs-lookup"><span data-stu-id="c9230-109">[Install the Az PowerShell module via PowerShellGet](install-az-ps.md) (recommended option).</span></span>
* <span data-ttu-id="c9230-110">[Installera Az PowerShell-modulen med MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="c9230-110">[Install the Az PowerShell module with MSI](install-az-ps-msi.md).</span></span>
* <span data-ttu-id="c9230-111">[Använd Azure Cloud Shell](/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="c9230-111">[Use Azure Cloud Shell](/azure/cloud-shell/overview).</span></span>
* <span data-ttu-id="c9230-112">[Använd Az PowerShell Docker-containern](azureps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="c9230-112">[Use the Az PowerShell Docker container](azureps-in-docker.md).</span></span>

## <a name="features"></a><span data-ttu-id="c9230-113">Funktioner</span><span class="sxs-lookup"><span data-stu-id="c9230-113">Features</span></span>

<span data-ttu-id="c9230-114">Az PowerShell-modulen har följande fördelar:</span><span class="sxs-lookup"><span data-stu-id="c9230-114">The Az PowerShell module features the following benefits:</span></span>

* <span data-ttu-id="c9230-115">Säkerhet och stabilitet</span><span class="sxs-lookup"><span data-stu-id="c9230-115">Security and stability</span></span>
  * <span data-ttu-id="c9230-116">Kryptering av tokencache</span><span class="sxs-lookup"><span data-stu-id="c9230-116">Token cache encryption</span></span>
  * <span data-ttu-id="c9230-117">Förhindrande av attacktypen man-in–the-middle</span><span class="sxs-lookup"><span data-stu-id="c9230-117">Prevention of man-in-the-middle attack type</span></span>
  * <span data-ttu-id="c9230-118">Stöd för autentisering med ADFS 2019</span><span class="sxs-lookup"><span data-stu-id="c9230-118">Support authentication with ADFS 2019</span></span>
  * <span data-ttu-id="c9230-119">Autentisering med användarnamn och lösenord i PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="c9230-119">Username and password authentication in PowerShell 7</span></span>
  * <span data-ttu-id="c9230-120">Stöd för funktioner som Kontinuerlig tillgänglighetskontroll (kommer 2021)</span><span class="sxs-lookup"><span data-stu-id="c9230-120">Support for features like continuous access evaluation (coming in 2021)</span></span>
* <span data-ttu-id="c9230-121">Stöd för alla Azure-tjänster</span><span class="sxs-lookup"><span data-stu-id="c9230-121">Support for all Azure services</span></span>
  * <span data-ttu-id="c9230-122">Alla allmänt tillgängliga Azure-tjänster har en motsvarande PowerShell-modul som stöds</span><span class="sxs-lookup"><span data-stu-id="c9230-122">All generally available Azure services have a corresponding supported PowerShell module</span></span>
  * <span data-ttu-id="c9230-123">Flera felkorrigeringar och uppgraderingar av API-versioner sedan AzureRM</span><span class="sxs-lookup"><span data-stu-id="c9230-123">Multiple bug fixes and API version upgrades since AzureRM</span></span>
* <span data-ttu-id="c9230-124">Nya funktioner</span><span class="sxs-lookup"><span data-stu-id="c9230-124">New capabilities</span></span>
  * <span data-ttu-id="c9230-125">Stöd i Cloud Shell och på alla plattformar</span><span class="sxs-lookup"><span data-stu-id="c9230-125">Support in Cloud Shell and cross-platform</span></span>
  * <span data-ttu-id="c9230-126">Kan hämta och använda åtkomsttoken för åtkomst till Azure-resurser</span><span class="sxs-lookup"><span data-stu-id="c9230-126">Can get and use access token to access Azure resources</span></span>
  * <span data-ttu-id="c9230-127">Cmdlet som är tillgänglig för avancerade REST-åtgärder med Azure-resurser</span><span class="sxs-lookup"><span data-stu-id="c9230-127">Cmdlet available for advanced REST operations with Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="c9230-128">PowerShell 7 och senare är den rekommenderade versionen av PowerShell för användning med Az PowerShell på alla plattformar.</span><span class="sxs-lookup"><span data-stu-id="c9230-128">PowerShell 7 and later is the recommended version of PowerShell for use with Az PowerShell on all platforms.</span></span>

<span data-ttu-id="c9230-129">Az PowerShell-modulen baseras på .NET Standard-biblioteket och fungerar med PowerShell 7 och senare på alla plattformar, t.ex. Windows, macOS och Linux.</span><span class="sxs-lookup"><span data-stu-id="c9230-129">The Az PowerShell module is based on the .NET Standard library and works with PowerShell 7 and later on all platforms including Windows, macOS, and Linux.</span></span> <span data-ttu-id="c9230-130">Den är också kompatibel med Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="c9230-130">It's also compatible with Windows PowerShell 5.1.</span></span>

<span data-ttu-id="c9230-131">Vår ambition är att alla plattformar ska ha stöd för Azure och att alla Az PowerShell-moduler ska vara plattformsoberoende.</span><span class="sxs-lookup"><span data-stu-id="c9230-131">We're committed to bringing Azure support to all platforms and all Az PowerShell modules are cross-platforms.</span></span>

## <a name="upgrade-your-environment-to-az"></a><span data-ttu-id="c9230-132">Uppgradera din miljö till Az</span><span class="sxs-lookup"><span data-stu-id="c9230-132">Upgrade your environment to Az</span></span>

<span data-ttu-id="c9230-133">För att dra nytta av de senaste Azure-funktionerna i PowerShell rekommenderar vi att du migrerar till Az-modulen.</span><span class="sxs-lookup"><span data-stu-id="c9230-133">To keep up with the latest Azure features in PowerShell, you should migrate to the Az module.</span></span> <span data-ttu-id="c9230-134">Om du inte är redo att ersätta AzureRM med Az-modulen finns det ett par alternativ för att experimentera med Az:</span><span class="sxs-lookup"><span data-stu-id="c9230-134">If you're not ready to install the Az module as a replacement for AzureRM, you have a couple of options available to experiment with Az:</span></span>

* <span data-ttu-id="c9230-135">Du kan använda en `PowerShell`-miljö med [Azure Cloud Shell](/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="c9230-135">Use a `PowerShell` environment with [Azure Cloud Shell](/azure/cloud-shell/overview).</span></span> <span data-ttu-id="c9230-136">Azure Cloud Shell är en webbläsarbaserad skalmiljö där Az-modulen redan är installerad och `Enable-AzureRM`-kompatibilitetsalias aktiverade.</span><span class="sxs-lookup"><span data-stu-id="c9230-136">Azure Cloud Shell is a browser-based shell environment that comes with the Az module installed and `Enable-AzureRM` compatibility aliases enabled.</span></span>
* <span data-ttu-id="c9230-137">Behåll AzureRM-modulen i Windows PowerShell 5.1 och installera Az-modulen i PowerShell 7 eller senare.</span><span class="sxs-lookup"><span data-stu-id="c9230-137">Keep the AzureRM module installed in Windows PowerShell 5.1 and install the Az module in PowerShell 7 or later.</span></span> <span data-ttu-id="c9230-138">Windows PowerShell 5.1 och PowerShell 7 och senare använder separata samlingar med moduler.</span><span class="sxs-lookup"><span data-stu-id="c9230-138">Windows PowerShell 5.1 and PowerShell 7 and later use separate collections of modules.</span></span> <span data-ttu-id="c9230-139">Följ anvisningarna för att installera den [senaste versionen av PowerShell](/powershell/scripting/install/installing-powershell) och [installera sedan Az-modulen](install-az-ps.md) från PowerShell 7 eller senare.</span><span class="sxs-lookup"><span data-stu-id="c9230-139">Follow the instructions to install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) and then [install the Az module](install-az-ps.md) from PowerShell 7 or later.</span></span>

<span data-ttu-id="c9230-140">Så uppgraderar du från en befintlig AzureRM-installation:</span><span class="sxs-lookup"><span data-stu-id="c9230-140">To upgrade from an existing AzureRM install:</span></span>

1. [<span data-ttu-id="c9230-141">Avinstallera Azure PowerShell AzureRM-modulen</span><span class="sxs-lookup"><span data-stu-id="c9230-141">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [<span data-ttu-id="c9230-142">Installera Azure PowerShell Az-modulen</span><span class="sxs-lookup"><span data-stu-id="c9230-142">Install the Azure PowerShell Az module</span></span>](install-az-ps.md)
1. <span data-ttu-id="c9230-143">**VALFRITT**: Aktivera kompatibilitetsläge för att lägga till alias för AzureRM-cmdletar med [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) medan du bekantar dig med den nya kommandouppsättningen.</span><span class="sxs-lookup"><span data-stu-id="c9230-143">**OPTIONAL**: Enable compatibility mode to add aliases for AzureRM cmdlets with [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) while you become familiar with the new command set.</span></span> <span data-ttu-id="c9230-144">Mer information finns i nästa avsnitt och i [Starta migrering från AzureRM till Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="c9230-144">For more information, see the next section or [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a><span data-ttu-id="c9230-145">Migrera befintliga skript från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="c9230-145">Migrate existing scripts from AzureRM to Az</span></span>

<span data-ttu-id="c9230-146">Om dina skript fortfarande baseras på AzureRM-modulen har vi flera resurser som hjälper dig med migreringen:</span><span class="sxs-lookup"><span data-stu-id="c9230-146">If your scripts are still based on the AzureRM module, we have several resources to help you with the migration:</span></span>

* [<span data-ttu-id="c9230-147">Kom igång med migrering från AzureRM till Az</span><span class="sxs-lookup"><span data-stu-id="c9230-147">Get started with migration from AzureRM to Az</span></span>](migrate-from-azurerm-to-az.md)
* [<span data-ttu-id="c9230-148">Fullständig lista över icke-bakåtkompatibla ändringar från AzureRM till Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="c9230-148">Full list of breaking changes from AzureRM to Az 1.0.0</span></span>](migrate-az-1.0.0.md)
* <span data-ttu-id="c9230-149">Cmdleten [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)</span><span class="sxs-lookup"><span data-stu-id="c9230-149">The [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet</span></span>

## <a name="supportability"></a><span data-ttu-id="c9230-150">Support</span><span class="sxs-lookup"><span data-stu-id="c9230-150">Supportability</span></span>

<span data-ttu-id="c9230-151">Az är den mest aktuella PowerShell-modulen för Azure.</span><span class="sxs-lookup"><span data-stu-id="c9230-151">Az is the most current PowerShell module for Azure.</span></span> <span data-ttu-id="c9230-152">Problem eller önskemål om funktioner kan loggas direkt på [GitHub-lagringsplatsen](https://github.com/Azure/azure-powershell) eller via Microsofts support om du har ett supportavtal.</span><span class="sxs-lookup"><span data-stu-id="c9230-152">Issues or feature requests can be logged directly on the [GitHub repository](https://github.com/Azure/azure-powershell), or via Microsoft support if you have a support contract.</span></span> <span data-ttu-id="c9230-153">Nya efterfrågade funktioner implementeras i den senaste versionen av Az.</span><span class="sxs-lookup"><span data-stu-id="c9230-153">Feature requests will be implemented in the latest version of Az.</span></span> <span data-ttu-id="c9230-154">Korrigeringar av kritiska problem implementeras i de två senaste versionerna av Az.</span><span class="sxs-lookup"><span data-stu-id="c9230-154">Critical issues will be implemented on the last two versions of Az.</span></span>

<span data-ttu-id="c9230-155">Inga nya cmdletar eller funktioner kommer att ges ut för AzureRM,</span><span class="sxs-lookup"><span data-stu-id="c9230-155">AzureRM will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="c9230-156">Officiellt underhålls AzureRM-modulen fortfarande och kritiska korrigeringar erbjuds till slutet av februari 2021.</span><span class="sxs-lookup"><span data-stu-id="c9230-156">However, the AzureRM module is still officially maintained and will receive critical fixes through February 2021.</span></span>

## <a name="data-collection"></a><span data-ttu-id="c9230-157">Datainsamling</span><span class="sxs-lookup"><span data-stu-id="c9230-157">Data collection</span></span>

<span data-ttu-id="c9230-158">Azure PowerShell samlar in telemetridata som standard.</span><span class="sxs-lookup"><span data-stu-id="c9230-158">Azure PowerShell collects telemetry data by default.</span></span> <span data-ttu-id="c9230-159">Microsoft samlar in data för att upptäcka användningsmönster, identifiera vanliga problem och förbättra upplevelsen av Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9230-159">Microsoft aggregates collected data to identify patterns of usage to identify common issues and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="c9230-160">Microsoft Azure PowerShell samlar inte in privata eller personliga data.</span><span class="sxs-lookup"><span data-stu-id="c9230-160">Microsoft Azure PowerShell does not collect any private or personal data.</span></span> <span data-ttu-id="c9230-161">Användningsdata hjälper oss att identifiera problem, t.ex. cmdlets som inte ger väntat resultat, och att prioritera vårt arbete.</span><span class="sxs-lookup"><span data-stu-id="c9230-161">For example, the usage data helps identify issues such as cmdlets with low success and helps prioritize our work.</span></span>

<span data-ttu-id="c9230-162">Även om vi har stor nytta av insikterna från dessa data, förstår vi att inte alla vill skicka sina användningsdata.</span><span class="sxs-lookup"><span data-stu-id="c9230-162">While we appreciate the insights this data provides, we also understand that not everyone wants to send usage data.</span></span> <span data-ttu-id="c9230-163">Du kan inaktivera datainsamling med cmdleten [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection).</span><span class="sxs-lookup"><span data-stu-id="c9230-163">You can disable data collection with the [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) cmdlet.</span></span> <span data-ttu-id="c9230-164">Du kan också läsa vår [sekretesspolicy](https://privacy.microsoft.com/privacystatement) om du vill ha mer information.</span><span class="sxs-lookup"><span data-stu-id="c9230-164">You can also read our [privacy statement](https://privacy.microsoft.com/privacystatement) to learn more.</span></span>
