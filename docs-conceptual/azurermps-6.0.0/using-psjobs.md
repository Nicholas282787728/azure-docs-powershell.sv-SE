---
title: Kör cmdletar parallellt med hjälp av PowerShell-jobb
description: Så här kör du cmdletar parallellt med parametern -AsJob.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: dfc1efa752c9c9fa42ad5904adacd83c2dc333b8
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="f0729-103">Kör cmdletar parallellt med hjälp av PowerShell-jobb</span><span class="sxs-lookup"><span data-stu-id="f0729-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="f0729-104">PowerShell har stöd för asynkrona åtgärder med [PowerShell-jobb](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="f0729-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="f0729-105">Azure PowerShell är kraftigt beroende av att utföra och vänta på nätverksanrop till Azure.</span><span class="sxs-lookup"><span data-stu-id="f0729-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="f0729-106">Som utvecklare vill du ofta utföra flera icke-blockerande anrop till Azure i ett skript. Det kan även hända att du vill skapa Azure-resurser i REPL utan att blockera den pågående sessionen.</span><span class="sxs-lookup"><span data-stu-id="f0729-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="f0729-107">För att uppfylla dessa behov tillhandahåller Azure PowerShell förstklassigt [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs)-stöd.</span><span class="sxs-lookup"><span data-stu-id="f0729-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="f0729-108">Sammanhangsbeständighet och PSJobs</span><span class="sxs-lookup"><span data-stu-id="f0729-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="f0729-109">PSJobs körs i separata processer, vilket innebär att information om Azure-anslutningen måste delas korrekt med de jobb som du skapar.</span><span class="sxs-lookup"><span data-stu-id="f0729-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="f0729-110">Vid anslutning av ditt Azure-konto till PowerShell-sessionen med `Connect-AzureRmAccount` kan du överföra sammanhanget till ett jobb.</span><span class="sxs-lookup"><span data-stu-id="f0729-110">Upon connecting your Azure account to your PowerShell session with `Connect-AzureRmAccount`, you can pass the context to a job.</span></span>

```powershell
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="f0729-111">Men om du har valt att sammanhanget ska sparas automatiskt med `Enable-AzureRmContextAutosave` delas sammanhanget automatiskt med alla jobb som du skapar.</span><span class="sxs-lookup"><span data-stu-id="f0729-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```powershell
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="f0729-112">Automatiska jobb med `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="f0729-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="f0729-113">För att förenkla processen tillhandahåller Azure PowerShell även en `-AsJob`-växel på vissa tidskrävande-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f0729-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="f0729-114">`-AsJob`-växeln gör det enklare att skapa PSJobs.</span><span class="sxs-lookup"><span data-stu-id="f0729-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```powershell
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="f0729-115">Du kan inspektera jobb och förlopp när som helst med `Get-Job` och `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="f0729-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```powershell
Get-Job $job
Get-AzureRmVM MyVm
```

```Output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="f0729-116">Därefter kan du hämta resultatet av jobbet med `Receive-Job` vid slutförande.</span><span class="sxs-lookup"><span data-stu-id="f0729-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="f0729-117">`Receive-Job` returnerar resultatet från cmdleten som om flaggan `-AsJob` inte fanns.</span><span class="sxs-lookup"><span data-stu-id="f0729-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="f0729-118">Till exempel, resultatet `Receive-Job` av `Do-Action -AsJob` är av samma typ som ett resultat av `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="f0729-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```powershell
$vm = Receive-Job $job
$vm
```

```Output
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

## <a name="example-scenarios"></a><span data-ttu-id="f0729-119">Exempelscenarier</span><span class="sxs-lookup"><span data-stu-id="f0729-119">Example Scenarios</span></span>

<span data-ttu-id="f0729-120">Skapa flera virtuella datorer samtidigt.</span><span class="sxs-lookup"><span data-stu-id="f0729-120">Create multiple VMs at once.</span></span>

```powershell
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

<span data-ttu-id="f0729-121">I det här exemplet gör cmdleten `Wait-Job` att skriptet pausas medan jobben fortfarande körs.</span><span class="sxs-lookup"><span data-stu-id="f0729-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="f0729-122">Skriptet fortsätter att köras när alla jobb har slutförts.</span><span class="sxs-lookup"><span data-stu-id="f0729-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="f0729-123">På så sätt kan du skapa flera jobb som körs parallellt och sedan vänta på att de slutförs innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="f0729-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

```Output
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
