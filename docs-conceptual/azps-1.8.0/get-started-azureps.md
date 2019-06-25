---
title: Komma igång med Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 0c3b749cb2ac7f11dacafca76b65944f523f727d
ms.sourcegitcommit: 5bdedc77b27b66998387486761ec67ed9326f169
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2019
ms.locfileid: "67346619"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="622fa-102">Komma igång med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="622fa-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="622fa-103">Azure PowerShell är utformat för att hantera och administrera Azure-resurser från kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="622fa-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="622fa-104">Använd Azure PowerShell när du vill skapa automatiserade verktyg som använder Azure Resource Manager-modellen.</span><span class="sxs-lookup"><span data-stu-id="622fa-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="622fa-105">Prova det i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator.</span><span class="sxs-lookup"><span data-stu-id="622fa-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="622fa-106">Den här artikeln hjälper dig att komma igång med Azure PowerShell och du får lära dig grundbegreppen.</span><span class="sxs-lookup"><span data-stu-id="622fa-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="622fa-107">Installera eller köra i Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="622fa-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="622fa-108">Det enklaste sättet att komma igång med Azure PowerShell är att prova det i en miljö med Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="622fa-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="622fa-109">Läs i [Snabbstart för PowerShell i Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell) för att komma igång.</span><span class="sxs-lookup"><span data-stu-id="622fa-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="622fa-110">Cloud Shell kör PowerShell 6 på en Linux-container, så Windows-specifika funktioner är inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="622fa-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="622fa-111">När du är redo att installera Azure PowerShell på din lokala dator följer du anvisningarna i [Installera Azure PowerShell-modulen](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="622fa-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="622fa-112">Logga in på Azure</span><span class="sxs-lookup"><span data-stu-id="622fa-112">Sign in to Azure</span></span>

<span data-ttu-id="622fa-113">Logga in interaktivt med cmdleten `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="622fa-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="622fa-114">Hoppa över det här steget om du använder Cloud Shell: Azure Cloud Shell-sessionen har redan autentiserats för den miljö, prenumeration och klientorganisation som Cloud Shell-sessionen startades från.</span><span class="sxs-lookup"><span data-stu-id="622fa-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="622fa-115">Om du är i en region som inte är i USA använder du parametern `-Environment` för att logga in.</span><span class="sxs-lookup"><span data-stu-id="622fa-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="622fa-116">Hämta namnet på miljön för din region med cmdleten [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="622fa-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="622fa-117">Exempel: För att logga in på Azure Kina 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="622fa-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="622fa-118">Du får ett token att använda på https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="622fa-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="622fa-119">Öppna den här sidan i webbläsaren och ange token. Logga sedan in med dina Azure-autentiseringsuppgifter och auktorisera Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="622fa-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="622fa-120">Efter att du loggat in ser du information om vilka av dina Azure-prenumerationer som är aktiva.</span><span class="sxs-lookup"><span data-stu-id="622fa-120">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="622fa-121">Om du har flera Azure-prenumerationer i ditt konto och vill välja en annan, hämtar du dina tillgängliga prenumerationer med [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) och använder cmdleten [Set-AzContext](/powershell/module/az.accounts/set-azcontext) med ditt prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="622fa-121">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="622fa-122">Mer information om hur du hanterar dina Azure-prenumerationer i Azure PowerShell finns i [Använda flera Azure-prenumerationer](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="622fa-122">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="622fa-123">När du är inloggad på ett Azure-konto kan du använda Azure PowerShell-cmdletar för att komma åt och hantera resurserna i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="622fa-123">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="622fa-124">Läs mer om inloggningsprocess och autentiseringsmetoder i [Logga in med Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="622fa-124">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="622fa-125">Hitta kommandon</span><span class="sxs-lookup"><span data-stu-id="622fa-125">Find commands</span></span>

<span data-ttu-id="622fa-126">Azure PowerShell-cmdletarna följer en standardkonvention för namngivning i PowerShell, `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="622fa-126">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="622fa-127">Verbet beskriver åtgärden (till exempel `Create`, `Get`, `Set`, `Delete`) och substantivet beskriver resurstypen (till exempel `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="622fa-127">The verb describes the action (examples include `Create`, `Get`, `Set`, `Delete`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="622fa-128">Substantiv i Azure PowerShell börjar alltid med prefixet `Az`.</span><span class="sxs-lookup"><span data-stu-id="622fa-128">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="622fa-129">En fullständig lista över standardverb finns i [Godkända verb för PowerShell-kommandon](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="622fa-129">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="622fa-130">Att känna till vilka substantiv, verb och Azure PowerShell-moduler som är tillgängliga hjälper dig att hitta kommandon med cmdleten [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="622fa-130">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="622fa-131">Exempel: Om du vill hitta alla VM-relaterade kommandon som använder verbet `Get`:</span><span class="sxs-lookup"><span data-stu-id="622fa-131">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="622fa-132">Som hjälp för dig att hitta vanliga kommandon finns här en tabell med resurstyp, motsvarande Azure PowerShell-modulen och de substantivprefix som ska användas med `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="622fa-132">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="622fa-133">Resurstyp</span><span class="sxs-lookup"><span data-stu-id="622fa-133">Resource type</span></span> | <span data-ttu-id="622fa-134">Azure PowerShell-modul</span><span class="sxs-lookup"><span data-stu-id="622fa-134">Azure PowerShell module</span></span> | <span data-ttu-id="622fa-135">Substantivprefix</span><span class="sxs-lookup"><span data-stu-id="622fa-135">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="622fa-136">Resursgrupp</span><span class="sxs-lookup"><span data-stu-id="622fa-136">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="622fa-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="622fa-137">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="622fa-138">Virtuella datorer</span><span class="sxs-lookup"><span data-stu-id="622fa-138">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="622fa-139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="622fa-139">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="622fa-140">Lagringskonton</span><span class="sxs-lookup"><span data-stu-id="622fa-140">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="622fa-141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="622fa-141">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="622fa-142">Key Vault</span><span class="sxs-lookup"><span data-stu-id="622fa-142">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="622fa-143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="622fa-143">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="622fa-144">Webbprogram</span><span class="sxs-lookup"><span data-stu-id="622fa-144">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="622fa-145">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="622fa-145">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="622fa-146">SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="622fa-146">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="622fa-147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="622fa-147">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="622fa-148">En fullständig lista över moduler i Azure PowerShell finns i [listan med Azure PowerShell-moduler](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) på GitHub.</span><span class="sxs-lookup"><span data-stu-id="622fa-148">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="622fa-149">Lär dig grunderna i Azure PowerShell med snabbstarter och självstudier</span><span class="sxs-lookup"><span data-stu-id="622fa-149">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="622fa-150">För att komma igång med Azure PowerShell kan du prova detaljerade självstudier där du konfigurerar virtuella datorer och lär dig att skicka frågor till dem.</span><span class="sxs-lookup"><span data-stu-id="622fa-150">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="622fa-151">Skapa virtuella datorer med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="622fa-151">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="622fa-152">Det finns även Azure PowerShell-snabbstarter för andra populära Azure-tjänster:</span><span class="sxs-lookup"><span data-stu-id="622fa-152">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="622fa-153">Skapa ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="622fa-153">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="622fa-154">Överföra objekt till och från Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="622fa-154">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="622fa-155">Skapa och hämta hemligheter från Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="622fa-155">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="622fa-156">Skapa en Azure SQL-databas och -brandvägg</span><span class="sxs-lookup"><span data-stu-id="622fa-156">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="622fa-157">Köra en container i Azure Container Instances</span><span class="sxs-lookup"><span data-stu-id="622fa-157">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="622fa-158">Skapa en VM-skalningsuppsättning med Virtual Machine Scale Sets (VMSS)</span><span class="sxs-lookup"><span data-stu-id="622fa-158">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="622fa-159">Skapa en standardbelastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="622fa-159">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="622fa-160">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="622fa-160">Next steps</span></span>

* [<span data-ttu-id="622fa-161">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="622fa-161">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="622fa-162">Hantera Azure-prenumerationer med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="622fa-162">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="622fa-163">Skapa huvudnamn för tjänsten med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="622fa-163">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="622fa-164">Få hjälp från communityn:</span><span class="sxs-lookup"><span data-stu-id="622fa-164">Get help from the community:</span></span>
  * [<span data-ttu-id="622fa-165">Azure-forumet på MSDN</span><span class="sxs-lookup"><span data-stu-id="622fa-165">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="622fa-166">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="622fa-166">Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
