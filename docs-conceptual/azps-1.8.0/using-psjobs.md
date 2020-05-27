---
title: Köra Azure PowerShell-cmdletar i PowerShell-jobb
description: Lär dig hur du kör Azure PowerShell-cmdletar parallellt eller som bakgrundsaktiviteter med hjälp av -AsJob och Start-Job.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: 36fcfc42fed91c5a0c8eff200c662e1e31cacfb9
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387742"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="281c3-103">Köra Azure PowerShell-cmdletar i PowerShell-jobb</span><span class="sxs-lookup"><span data-stu-id="281c3-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="281c3-104">Azure PowerShell är beroende av att ansluta till ett Azure-moln och vänta på svar, så att de flesta av dessa cmdletar blockerar PowerShell-sessionen tills de får ett svar från molnet.</span><span class="sxs-lookup"><span data-stu-id="281c3-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="281c3-105">Med PowerShell-jobb kan du köra cmdletar i bakgrunden eller utföra flera uppgifter på Azure samtidigt, inifrån en och samma PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="281c3-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="281c3-106">Den här artikeln ger en kort översikt över hur du kör Azure PowerShell-cmdletar som PowerShell-jobb och kontrollerar att de är klara.</span><span class="sxs-lookup"><span data-stu-id="281c3-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="281c3-107">Om du ska köra kommandon i Azure PowerShell måste du använda Azure PowerShell-kontexter som beskrivs i detalj i [Azure-kontexter och inloggningsuppgifter](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="281c3-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="281c3-108">Mer information om PowerShell-jobb finns i [Om PowerShell-jobb](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="281c3-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="281c3-109">Azure-kontexter med PowerShell-jobb</span><span class="sxs-lookup"><span data-stu-id="281c3-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="281c3-110">PowerShell-jobb körs som separata processer utan en ansluten PowerShell-session, så dina Azure-autentiseringsuppgifter måste delas med dem.</span><span class="sxs-lookup"><span data-stu-id="281c3-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="281c3-111">Autentiseringsuppgifterna skickas som Azure-kontextobjekt med någon av följande metoder:</span><span class="sxs-lookup"><span data-stu-id="281c3-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="281c3-112">Automatisk kontextpersistens.</span><span class="sxs-lookup"><span data-stu-id="281c3-112">Automatic context persistence.</span></span> <span data-ttu-id="281c3-113">Kontextpersistens är aktiverat som standard och bevarar din inloggningsinformation över flera sessioner.</span><span class="sxs-lookup"><span data-stu-id="281c3-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="281c3-114">Med kontextpersistens aktiverat skickas den aktuella Azure-kontexten till den nya processen:</span><span class="sxs-lookup"><span data-stu-id="281c3-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="281c3-115">Använd parametern `-AzContext` med alla Azure PowerShell-cmdletar för att ange ett Azure-kontextobjekt:</span><span class="sxs-lookup"><span data-stu-id="281c3-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="281c3-116">Om kontextpersistens är inaktiverat krävs argumentet `-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="281c3-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="281c3-117">Använd växeln `-AsJob` som tillhandahålls av vissa Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="281c3-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="281c3-118">Den här växeln startar automatiskt cmdleten som ett PowerShell-jobb med den aktuella aktiva Azure-kontexten:</span><span class="sxs-lookup"><span data-stu-id="281c3-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="281c3-119">Om du vill se om en cmdlet stöder `-AsJob` kan du kontrollera referensdokumentationen.</span><span class="sxs-lookup"><span data-stu-id="281c3-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="281c3-120">Växeln `-AsJob` kräver inte att kontexten sparas automatiskt.</span><span class="sxs-lookup"><span data-stu-id="281c3-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="281c3-121">Du kan kontrollera statusen för ett jobb som körs med cmdleten [Get-Job](/powershell/module/microsoft.powershell.core/get-job).</span><span class="sxs-lookup"><span data-stu-id="281c3-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="281c3-122">Om du vill hämta utdata från ett jobb hittills använder du cmdleten [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).</span><span class="sxs-lookup"><span data-stu-id="281c3-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="281c3-123">Om du vill kontrollera en åtgärds status på Azure via en fjärranslutning använder du de `Get-`-cmdletar som är kopplade till den typ av resurs som ändras av jobbet:</span><span class="sxs-lookup"><span data-stu-id="281c3-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="281c3-124">Se även</span><span class="sxs-lookup"><span data-stu-id="281c3-124">See Also</span></span>

* [<span data-ttu-id="281c3-125">Azure PowerShell-kontexter</span><span class="sxs-lookup"><span data-stu-id="281c3-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* [<span data-ttu-id="281c3-126">Om PowerShell-jobb</span><span class="sxs-lookup"><span data-stu-id="281c3-126">About PowerShell Jobs</span></span>](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [<span data-ttu-id="281c3-127">Referens för Get-Job</span><span class="sxs-lookup"><span data-stu-id="281c3-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="281c3-128">Referens för Receive-Job</span><span class="sxs-lookup"><span data-stu-id="281c3-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
