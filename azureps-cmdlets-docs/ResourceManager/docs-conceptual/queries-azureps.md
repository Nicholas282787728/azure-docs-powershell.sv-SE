---
title: "Fråga efter Azure-resurser och formatera resultat | Microsoft Docs"
description: "Så här frågar du efter resurser i Azure och formaterar resultaten."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 93a031ce90352286bb1a5e01dc65e6db7cbe5c7e
ms.sourcegitcommit: be8389f126196e50b513f26c296e08a59601ecc6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2017
---
# <a name="querying-for-azure-resources"></a><span data-ttu-id="3abcf-103">Fråga efter Azure-resurser</span><span class="sxs-lookup"><span data-stu-id="3abcf-103">Querying for Azure resources</span></span>

<span data-ttu-id="3abcf-104">Frågor i PowerShell kan utföras med hjälp av inbyggda cmdletar.</span><span class="sxs-lookup"><span data-stu-id="3abcf-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="3abcf-105">I PowerShell har cmdlet formen **_Verb-substantiv_**.</span><span class="sxs-lookup"><span data-stu-id="3abcf-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="3abcf-106">Cmdletar med verbet **_Get_** är fråge-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="3abcf-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="3abcf-107">Cmdletarnas substantiv är de typer av Azure-resurser som cmdletens verb agerar på.</span><span class="sxs-lookup"><span data-stu-id="3abcf-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>


## <a name="selecting-simple-properties"></a><span data-ttu-id="3abcf-108">Välja enkla egenskaper</span><span class="sxs-lookup"><span data-stu-id="3abcf-108">Selecting simple properties</span></span>

<span data-ttu-id="3abcf-109">Azure PowerShell har standardformat som definierats för varje cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3abcf-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="3abcf-110">De vanligaste egenskaperna för varje resurstyp visas automatiskt i tabell- eller listformat.</span><span class="sxs-lookup"><span data-stu-id="3abcf-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="3abcf-111">Mer information om att formatera utdata finns i [Formatera frågeresultat](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="3abcf-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="3abcf-112">Använd cmdleten `Get-AzureRmVM` för att fråga efter en lista över virtuella datorer i kontot.</span><span class="sxs-lookup"><span data-stu-id="3abcf-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell
Get-AzureRmVM
```

<span data-ttu-id="3abcf-113">Standardutdata formateras automatiskt som en tabell.</span><span class="sxs-lookup"><span data-stu-id="3abcf-113">The default output is automatically formatted as a table.</span></span>

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="3abcf-114">Cmdleten `Select-Object` kan användas för att välja specifika egenskaper som är intressanta för dig.</span><span class="sxs-lookup"><span data-stu-id="3abcf-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="3abcf-115">Välja komplexa kapslade egenskaper</span><span class="sxs-lookup"><span data-stu-id="3abcf-115">Selecting complex nested properties</span></span>

<span data-ttu-id="3abcf-116">Om den egenskap du vill välja ligger djupt kapslad i JSON-utdata måste du ange den fullständiga sökvägen till den kapslade egenskapen.</span><span class="sxs-lookup"><span data-stu-id="3abcf-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="3abcf-117">Följande exempel visar hur du väljer den virtuella datorns namn och operativsystemtyp i cmdleten `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="3abcf-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a><span data-ttu-id="3abcf-118">Filtrera resultatet med hjälp av cmdleten Where-Object</span><span class="sxs-lookup"><span data-stu-id="3abcf-118">Filter result using the Where-Object cmdlet</span></span>

<span data-ttu-id="3abcf-119">Med cmdleten `Where-Object` kan du filtrera resultatet baserat på valfritt egenskapsvärde.</span><span class="sxs-lookup"><span data-stu-id="3abcf-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="3abcf-120">I följande exempel väljer filtret endast virtuella datorer som har texten "RGD" i sina namn.</span><span class="sxs-lookup"><span data-stu-id="3abcf-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="3abcf-121">Med nästa exempel visar resultaten de virtuella datorer som har vmSize ”Standard_DS1_V2”.</span><span class="sxs-lookup"><span data-stu-id="3abcf-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
