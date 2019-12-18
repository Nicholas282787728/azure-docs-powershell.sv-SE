---
title: Fråga utdata från Azure PowerShell-cmdletar
description: Så här frågar du efter resurser i Azure och formaterar resultaten.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.openlocfilehash: 9141f5640467722608cb7748f425ce3942668fb8
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182119"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="4e454-103">Fråga utdata från Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4e454-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="4e454-104">Resultatet för varje Azure PowerShell-cmdlet är ett Azure PowerShell-objekt.</span><span class="sxs-lookup"><span data-stu-id="4e454-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="4e454-105">Även cmdletar som inte uttryckligen är `Get-`-åtgärder kan returnera ett värde som kan granskas för att ge information om en resurs som har skapats eller ändrats.</span><span class="sxs-lookup"><span data-stu-id="4e454-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="4e454-106">De flesta cmdletar returnerar ett enda objekt, men vissa returnerar vissa en matris som ska itereras.</span><span class="sxs-lookup"><span data-stu-id="4e454-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="4e454-107">I nästan alla fall kan du fråga utdata från Azure PowerShell med cmdleten [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), ofta förkortat till `select`.</span><span class="sxs-lookup"><span data-stu-id="4e454-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="4e454-108">Utdata kan filtreras med [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), eller dess alias `where`.</span><span class="sxs-lookup"><span data-stu-id="4e454-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="4e454-109">Välja enkla egenskaper</span><span class="sxs-lookup"><span data-stu-id="4e454-109">Select simple properties</span></span>

<span data-ttu-id="4e454-110">I standardtabellformatet visar inte Azure PowerShell-cmdletarna alla tillgängliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="4e454-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="4e454-111">Du kan se de fullständiga egenskaperna med cmdleten [Format-List](/powershell/module/microsoft.powershell.utility/format-list) eller genom att dirigera utdata till `Select-Object *`:</span><span class="sxs-lookup"><span data-stu-id="4e454-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="4e454-112">När du känner till namnen på de egenskaper som du är intresserad av kan du använda dem med `Select-Object` för att hämta dem direkt:</span><span class="sxs-lookup"><span data-stu-id="4e454-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="4e454-113">Utdata från användning av `Select-Object` formateras alltid så att den begärda informationen visas.</span><span class="sxs-lookup"><span data-stu-id="4e454-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="4e454-114">Information om hur du använder formatering som en del av frågor till cmdlet-resultat finns i [Formatera cmdlet-utdata i Azure PowerShell](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="4e454-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="4e454-115">Välja kapslade egenskaper</span><span class="sxs-lookup"><span data-stu-id="4e454-115">Select nested properties</span></span>

<span data-ttu-id="4e454-116">Vissa egenskaper i cmdlet-utdata i Azure PowerShell använder kapslade objekt som egenskapen `StorageProfile` i `Get-AzVM`-utdata.</span><span class="sxs-lookup"><span data-stu-id="4e454-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="4e454-117">Om du vill ha ett värde från en kapslad egenskap anger du ett visningsnamn och den fullständiga sökvägen till det värde du vill granska som en del av ett ordlisteargument för `Select-Object`:</span><span class="sxs-lookup"><span data-stu-id="4e454-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="4e454-118">Varje ordlisteargument väljer en egenskap från objektet.</span><span class="sxs-lookup"><span data-stu-id="4e454-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="4e454-119">Den egenskap som ska extraheras måste vara en del av ett uttryck.</span><span class="sxs-lookup"><span data-stu-id="4e454-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="4e454-120">Filtrera resultat</span><span class="sxs-lookup"><span data-stu-id="4e454-120">Filter results</span></span> 

<span data-ttu-id="4e454-121">Med cmdleten `Where-Object` kan du filtrera resultatet baserat på valfritt egenskapsvärde, inklusive kapslade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="4e454-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="4e454-122">I nästa exempel visas hur du använder `Where-Object` för att hitta de virtuella Linux-datorerna i en resursgrupp.</span><span class="sxs-lookup"><span data-stu-id="4e454-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="4e454-123">Du kan dirigera resultaten för `Select-Object` och `Where-Object` till varandra.</span><span class="sxs-lookup"><span data-stu-id="4e454-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="4e454-124">Av prestandaskäl rekommenderar vi alltid att du placerar åtgärden `Where-Object` före `Select-Object`:</span><span class="sxs-lookup"><span data-stu-id="4e454-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```