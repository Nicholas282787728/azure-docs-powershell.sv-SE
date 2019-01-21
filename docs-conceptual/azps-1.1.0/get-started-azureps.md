---
title: Komma igång med Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 483e74d7d047562b1c170c3767495161b9c5eb2f
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342134"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="d89e1-102">Komma igång med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d89e1-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="d89e1-103">Azure PowerShell är utformat för att hantera och administrera Azure-resurser från kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="d89e1-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="d89e1-104">Använd Azure PowerShell när du vill skapa automatiserade verktyg som använder Azure Resource Manager-modellen.</span><span class="sxs-lookup"><span data-stu-id="d89e1-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="d89e1-105">Prova det i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator.</span><span class="sxs-lookup"><span data-stu-id="d89e1-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="d89e1-106">Den här artikeln hjälper dig att komma igång med Azure PowerShell och du får lära dig grundbegreppen.</span><span class="sxs-lookup"><span data-stu-id="d89e1-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="d89e1-107">Installera eller köra i Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="d89e1-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="d89e1-108">Det enklaste sättet att komma igång med Azure PowerShell är att prova det i en miljö med Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="d89e1-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="d89e1-109">Läs i [Snabbstart för PowerShell i Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell) för att komma igång.</span><span class="sxs-lookup"><span data-stu-id="d89e1-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="d89e1-110">Cloud Shell kör PowerShell 6 på en Linux-container, så Windows-specifika funktioner är inte tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="d89e1-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="d89e1-111">När du är redo att installera Azure PowerShell på din lokala dator följer du anvisningarna i [Installera Azure PowerShell-modulen](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d89e1-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="d89e1-112">Logga in på Azure</span><span class="sxs-lookup"><span data-stu-id="d89e1-112">Sign in to Azure</span></span>

<span data-ttu-id="d89e1-113">Logga in interaktivt med cmdleten `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="d89e1-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="d89e1-114">Hoppa över det här steget om du använder Cloud Shell: Azure Cloud Shell-sessionen har redan autentiserats för den miljö, prenumeration och klientorganisation som Cloud Shell-sessionen startades från.</span><span class="sxs-lookup"><span data-stu-id="d89e1-114">Skip this step if you use Cloud Shell: Your Auzre Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="d89e1-115">Om du är i en region som inte är i USA använder du parametern `-Environment` för att logga in.</span><span class="sxs-lookup"><span data-stu-id="d89e1-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="d89e1-116">Hämta namnet på miljön för din region med cmdleten [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="d89e1-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="d89e1-117">Exempel: För att logga in på Azure Kina 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="d89e1-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="d89e1-118">Du får ett token att använda på https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="d89e1-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="d89e1-119">Öppna den här sidan i webbläsaren och ange token. Logga sedan in med dina Azure-autentiseringsuppgifter och auktorisera Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d89e1-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="d89e1-120">När du är inloggad på ett Azure-konto kan du använda Azure PowerShell-cmdletar för att komma åt och hantera resurserna i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d89e1-120">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="d89e1-121">Läs mer om inloggningsprocess och autentiseringsmetoder i [Logga in med Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d89e1-121">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="d89e1-122">Hitta kommandon</span><span class="sxs-lookup"><span data-stu-id="d89e1-122">Find commands</span></span>

<span data-ttu-id="d89e1-123">Azure PowerShell-cmdletarna följer en standardkonvention för namngivning i PowerShell, `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="d89e1-123">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="d89e1-124">Verbet beskriver åtgärden (till exempel `Create`, `Get`, `Set`, `Delete`) och substantivet beskriver resurstypen (till exempel `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="d89e1-124">The verb describes the action (examples include `Create`, `Get`, `Set`, `Delete`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="d89e1-125">Substantiv i Azure PowerShell börjar alltid med prefixet `Az`.</span><span class="sxs-lookup"><span data-stu-id="d89e1-125">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="d89e1-126">En fullständig lista över standardverb finns i [Godkända verb för PowerShell-kommandon](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="d89e1-126">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="d89e1-127">Att känna till vilka substantiv, verb och Azure PowerShell-moduler som är tillgängliga hjälper dig att hitta kommandon med cmdleten [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="d89e1-127">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="d89e1-128">Exempel: Om du vill hitta alla VM-relaterade kommandon som använder verbet `Get`:</span><span class="sxs-lookup"><span data-stu-id="d89e1-128">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="d89e1-129">Som hjälp för dig att hitta vanliga kommandon finns här en tabell med resurstyp, motsvarande Azure PowerShell-modulen och de substantivprefix som ska användas med `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="d89e1-129">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="d89e1-130">Resurstyp</span><span class="sxs-lookup"><span data-stu-id="d89e1-130">Resource type</span></span> | <span data-ttu-id="d89e1-131">Azure PowerShell-modul</span><span class="sxs-lookup"><span data-stu-id="d89e1-131">Azure PowerShell module</span></span> | <span data-ttu-id="d89e1-132">Substantivprefix</span><span class="sxs-lookup"><span data-stu-id="d89e1-132">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="d89e1-133">Resursgrupp</span><span class="sxs-lookup"><span data-stu-id="d89e1-133">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="d89e1-134">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d89e1-134">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="d89e1-135">Virtuella datorer</span><span class="sxs-lookup"><span data-stu-id="d89e1-135">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="d89e1-136">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d89e1-136">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="d89e1-137">Lagringskonton</span><span class="sxs-lookup"><span data-stu-id="d89e1-137">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="d89e1-138">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d89e1-138">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="d89e1-139">Key Vault</span><span class="sxs-lookup"><span data-stu-id="d89e1-139">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="d89e1-140">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d89e1-140">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="d89e1-141">Webbprogram</span><span class="sxs-lookup"><span data-stu-id="d89e1-141">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="d89e1-142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d89e1-142">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="d89e1-143">SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="d89e1-143">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="d89e1-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d89e1-144">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="d89e1-145">En fullständig lista över moduler i Azure PowerShell finns i [listan med Azure PowerShell-moduler](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) på GitHub.</span><span class="sxs-lookup"><span data-stu-id="d89e1-145">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="d89e1-146">Lär dig grunderna i Azure PowerShell med snabbstarter och självstudier</span><span class="sxs-lookup"><span data-stu-id="d89e1-146">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="d89e1-147">För att komma igång med Azure PowerShell kan du prova detaljerade självstudier där du konfigurerar virtuella datorer och lär dig att skicka frågor till dem.</span><span class="sxs-lookup"><span data-stu-id="d89e1-147">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d89e1-148">Skapa virtuella datorer med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d89e1-148">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="d89e1-149">Det finns även Azure PowerShell-snabbstarter för andra populära Azure-tjänster:</span><span class="sxs-lookup"><span data-stu-id="d89e1-149">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="d89e1-150">Skapa ett lagringskonto</span><span class="sxs-lookup"><span data-stu-id="d89e1-150">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="d89e1-151">Överföra objekt till och från Azure Blob Storage</span><span class="sxs-lookup"><span data-stu-id="d89e1-151">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="d89e1-152">Skapa och hämta hemligheter från Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d89e1-152">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="d89e1-153">Skapa en Azure SQL-databas och -brandvägg</span><span class="sxs-lookup"><span data-stu-id="d89e1-153">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="d89e1-154">Köra en container i Azure Container Instances</span><span class="sxs-lookup"><span data-stu-id="d89e1-154">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="d89e1-155">Skapa en VM-skalningsuppsättning med Virtual Machine Scale Sets (VMSS)</span><span class="sxs-lookup"><span data-stu-id="d89e1-155">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="d89e1-156">Skapa en standardbelastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="d89e1-156">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="d89e1-157">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="d89e1-157">Next steps</span></span>

* [<span data-ttu-id="d89e1-158">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d89e1-158">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="d89e1-159">Hantera Azure-prenumerationer med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d89e1-159">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="d89e1-160">Skapa huvudnamn för tjänsten med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d89e1-160">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="d89e1-161">Få hjälp från communityn:</span><span class="sxs-lookup"><span data-stu-id="d89e1-161">Get help from the community:</span></span>
  * [<span data-ttu-id="d89e1-162">Azure-forumet på MSDN</span><span class="sxs-lookup"><span data-stu-id="d89e1-162">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="d89e1-163">Stacki Overflow</span><span class="sxs-lookup"><span data-stu-id="d89e1-163">Stacki Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
