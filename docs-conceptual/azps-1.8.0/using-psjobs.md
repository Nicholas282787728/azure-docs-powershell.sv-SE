---
title: Köra cmdletar parallellt med hjälp av PowerShell-jobb
description: Så här kör du cmdletar parallellt med parametern -AsJob.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 825a07e01194a07b747712a62384c7f162e63d7d
ms.sourcegitcommit: 5bdedc77b27b66998387486761ec67ed9326f169
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2019
ms.locfileid: "67346687"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="db0f9-103">Kör cmdletar parallellt med hjälp av PowerShell-jobb</span><span class="sxs-lookup"><span data-stu-id="db0f9-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="db0f9-104">PowerShell har stöd för asynkrona åtgärder med [PowerShell-jobb](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="db0f9-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="db0f9-105">Azure PowerShell är kraftigt beroende av att utföra och vänta på nätverksanrop till Azure.</span><span class="sxs-lookup"><span data-stu-id="db0f9-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="db0f9-106">Du kanske ofta behöver utföra icke-blockerande anrop.</span><span class="sxs-lookup"><span data-stu-id="db0f9-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="db0f9-107">För att uppfylla det behovet tillhandahåller Azure PowerShell förstklassigt [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs)-stöd.</span><span class="sxs-lookup"><span data-stu-id="db0f9-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="db0f9-108">Sammanhangsbeständighet och PSJobs</span><span class="sxs-lookup"><span data-stu-id="db0f9-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="db0f9-109">Eftersom PSJobs körs som separata processer måste Azure-anslutningen delas med dem.</span><span class="sxs-lookup"><span data-stu-id="db0f9-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="db0f9-110">När du har loggat in på ditt Azure-konto med `Connect-AzAccount` överför du sammanhanget till ett jobb.</span><span class="sxs-lookup"><span data-stu-id="db0f9-110">After signing in to your Azure account with `Connect-AzAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList (Get-AzContext),$creds
```

<span data-ttu-id="db0f9-111">Men om du har valt att sammanhanget ska sparas automatiskt med `Enable-AzContextAutosave` delas sammanhanget automatiskt med alla jobb som du skapar.</span><span class="sxs-lookup"><span data-stu-id="db0f9-111">However, if you have chosen to have your context automatically saved with `Enable-AzContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -ArgumentList $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="db0f9-112">Automatiska jobb med `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="db0f9-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="db0f9-113">För att förenkla processen tillhandahåller Azure PowerShell även en `-AsJob`-växel på vissa tidskrävande-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="db0f9-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="db0f9-114">`-AsJob`-växeln gör det enklare att skapa PSJobs.</span><span class="sxs-lookup"><span data-stu-id="db0f9-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="db0f9-115">Du kan inspektera jobb och förlopp när som helst med `Get-Job` och `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="db0f9-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzVM' AzureLongRunningJob`1 Running True        localhost New-AzVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="db0f9-116">När jobbet har slutförts hämtar du resultatet av jobbet med `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="db0f9-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="db0f9-117">`Receive-Job` returnerar resultatet från cmdleten som om flaggan `-AsJob` inte fanns.</span><span class="sxs-lookup"><span data-stu-id="db0f9-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="db0f9-118">Till exempel, resultatet `Receive-Job` av `Do-Action -AsJob` är av samma typ som ett resultat av `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="db0f9-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a><span data-ttu-id="db0f9-119">Exempelscenarier</span><span class="sxs-lookup"><span data-stu-id="db0f9-119">Example Scenarios</span></span>

<span data-ttu-id="db0f9-120">Skapa flera virtuella datorer samtidigt:</span><span class="sxs-lookup"><span data-stu-id="db0f9-120">Create several VMs at once:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzVM
```

<span data-ttu-id="db0f9-121">I det här exemplet gör cmdleten `Wait-Job` att skriptet pausas medan jobben fortfarande körs.</span><span class="sxs-lookup"><span data-stu-id="db0f9-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="db0f9-122">Skriptet fortsätter att köras när alla jobb har slutförts.</span><span class="sxs-lookup"><span data-stu-id="db0f9-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="db0f9-123">Flera jobb körs parallellt och sedan väntar skriptet på att de slutförs innan det fortsätter.</span><span class="sxs-lookup"><span data-stu-id="db0f9-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```
