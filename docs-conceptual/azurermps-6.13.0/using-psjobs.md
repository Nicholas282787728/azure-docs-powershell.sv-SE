---
title: Kör cmdletar parallellt med hjälp av PowerShell-jobb
description: Så här kör du cmdletar parallellt med parametern -AsJob.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 85e4612146c07b963ca51a7203ea7782d058b93d
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/12/2019
ms.locfileid: "56145217"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="a0a39-103">Kör cmdletar parallellt med hjälp av PowerShell-jobb</span><span class="sxs-lookup"><span data-stu-id="a0a39-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="a0a39-104">PowerShell har stöd för asynkrona åtgärder med [PowerShell-jobb](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="a0a39-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="a0a39-105">Azure PowerShell är kraftigt beroende av att utföra och vänta på nätverksanrop till Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a39-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="a0a39-106">Du kanske ofta behöver utföra icke-blockerande anrop.</span><span class="sxs-lookup"><span data-stu-id="a0a39-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="a0a39-107">För att uppfylla det behovet tillhandahåller Azure PowerShell förstklassigt [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs)-stöd.</span><span class="sxs-lookup"><span data-stu-id="a0a39-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="a0a39-108">Sammanhangsbeständighet och PSJobs</span><span class="sxs-lookup"><span data-stu-id="a0a39-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="a0a39-109">Eftersom PSJobs körs som separata processer måste Azure-anslutningen delas med dem.</span><span class="sxs-lookup"><span data-stu-id="a0a39-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="a0a39-110">När du har loggat in på ditt Azure-konto med `Connect-AzureRmAccount` överför du sammanhanget till ett jobb.</span><span class="sxs-lookup"><span data-stu-id="a0a39-110">After signing in to your Azure account with `Connect-AzureRmAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="a0a39-111">Men om du har valt att sammanhanget ska sparas automatiskt med `Enable-AzureRmContextAutosave` delas sammanhanget automatiskt med alla jobb som du skapar.</span><span class="sxs-lookup"><span data-stu-id="a0a39-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="a0a39-112">Automatiska jobb med `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="a0a39-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="a0a39-113">För att förenkla processen tillhandahåller Azure PowerShell även en `-AsJob`-växel på vissa tidskrävande-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="a0a39-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="a0a39-114">`-AsJob`-växeln gör det enklare att skapa PSJobs.</span><span class="sxs-lookup"><span data-stu-id="a0a39-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="a0a39-115">Du kan inspektera jobb och förlopp när som helst med `Get-Job` och `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="a0a39-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzureRmVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="a0a39-116">När jobbet har slutförts hämtar du resultatet av jobbet med `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="a0a39-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="a0a39-117">`Receive-Job` returnerar resultatet från cmdleten som om flaggan `-AsJob` inte fanns.</span><span class="sxs-lookup"><span data-stu-id="a0a39-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="a0a39-118">Till exempel, resultatet `Receive-Job` av `Do-Action -AsJob` är av samma typ som ett resultat av `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="a0a39-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

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

## <a name="example-scenarios"></a><span data-ttu-id="a0a39-119">Exempelscenarier</span><span class="sxs-lookup"><span data-stu-id="a0a39-119">Example Scenarios</span></span>

<span data-ttu-id="a0a39-120">Skapa flera virtuella datorer samtidigt:</span><span class="sxs-lookup"><span data-stu-id="a0a39-120">Create several VMs at once:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

<span data-ttu-id="a0a39-121">I det här exemplet gör cmdleten `Wait-Job` att skriptet pausas medan jobben fortfarande körs.</span><span class="sxs-lookup"><span data-stu-id="a0a39-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="a0a39-122">Skriptet fortsätter att köras när alla jobb har slutförts.</span><span class="sxs-lookup"><span data-stu-id="a0a39-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="a0a39-123">Flera jobb körs parallellt och sedan väntar skriptet på att de slutförs innan det fortsätter.</span><span class="sxs-lookup"><span data-stu-id="a0a39-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
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
