---
title: Fråga utdata från Azure PowerShell-cmdletar
description: Så här frågar du efter resurser i Azure och formaterar resultaten.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: 52e3611e1587aea5eccb14d86042940bca1b3312
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387470"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="90d5f-103">Fråga utdata från Azure PowerShell-cmdletar</span><span class="sxs-lookup"><span data-stu-id="90d5f-103">Query output of Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="90d5f-104">Frågor i PowerShell kan utföras med hjälp av inbyggda cmdletar.</span><span class="sxs-lookup"><span data-stu-id="90d5f-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="90d5f-105">I PowerShell har cmdlet formen **_Verb-substantiv_**.</span><span class="sxs-lookup"><span data-stu-id="90d5f-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="90d5f-106">Cmdletar med verbet **_Get_** är fråge-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="90d5f-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="90d5f-107">Cmdletarnas substantiv är de typer av Azure-resurser som cmdletens verb agerar på.</span><span class="sxs-lookup"><span data-stu-id="90d5f-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="90d5f-108">Välja enkla egenskaper</span><span class="sxs-lookup"><span data-stu-id="90d5f-108">Select simple properties</span></span>

<span data-ttu-id="90d5f-109">Azure PowerShell har standardformat som definierats för varje cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90d5f-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="90d5f-110">De vanligaste egenskaperna för varje resurstyp visas automatiskt i tabell- eller listformat.</span><span class="sxs-lookup"><span data-stu-id="90d5f-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="90d5f-111">Mer information om att formatera utdata finns i [Formatera frågeresultat](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="90d5f-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="90d5f-112">Använd cmdleten `Get-AzureRmVM` för att fråga efter en lista över virtuella datorer i kontot.</span><span class="sxs-lookup"><span data-stu-id="90d5f-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="90d5f-113">Standardutdata formateras automatiskt som en tabell.</span><span class="sxs-lookup"><span data-stu-id="90d5f-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="90d5f-114">Cmdleten `Select-Object` kan användas för att välja specifika egenskaper som är intressanta för dig.</span><span class="sxs-lookup"><span data-stu-id="90d5f-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="90d5f-115">Välja komplexa kapslade egenskaper</span><span class="sxs-lookup"><span data-stu-id="90d5f-115">Select complex nested properties</span></span>

<span data-ttu-id="90d5f-116">Om den egenskap du vill välja ligger djupt kapslad i JSON-utdata måste du ange den fullständiga sökvägen till den kapslade egenskapen.</span><span class="sxs-lookup"><span data-stu-id="90d5f-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="90d5f-117">Följande exempel visar hur du väljer den virtuella datorns namn och operativsystemtyp i cmdleten `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="90d5f-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="90d5f-118">Filtrera resultat med hjälp av cmdleten Where-Object</span><span class="sxs-lookup"><span data-stu-id="90d5f-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="90d5f-119">Med cmdleten `Where-Object` kan du filtrera resultatet baserat på valfritt egenskapsvärde.</span><span class="sxs-lookup"><span data-stu-id="90d5f-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="90d5f-120">I följande exempel väljer filtret endast virtuella datorer som har texten "RGD" i sina namn.</span><span class="sxs-lookup"><span data-stu-id="90d5f-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="90d5f-121">Med nästa exempel visar resultaten de virtuella datorer som har vmSize ”Standard_DS1_V2”.</span><span class="sxs-lookup"><span data-stu-id="90d5f-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
