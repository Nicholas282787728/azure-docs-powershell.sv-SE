---
title: Fråga utdata från Azure PowerShell-cmdletar
description: Så här frågar du efter resurser i Azure och formaterar resultaten.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: 30778a650e7e6769cac814f8da581371a7943de4
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/12/2019
ms.locfileid: "56145082"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a>Fråga utdata från Azure PowerShell-cmdletar

Frågor i PowerShell kan utföras med hjälp av inbyggda cmdletar. I PowerShell har cmdlet formen **_Verb-substantiv_**. Cmdletar med verbet **_Get_** är fråge-cmdletar. Cmdletarnas substantiv är de typer av Azure-resurser som cmdletens verb agerar på.

## <a name="select-simple-properties"></a>Välja enkla egenskaper

Azure PowerShell har standardformat som definierats för varje cmdlet. De vanligaste egenskaperna för varje resurstyp visas automatiskt i tabell- eller listformat. Mer information om att formatera utdata finns i [Formatera frågeresultat](formatting-output.md).

Använd cmdleten `Get-AzureRmVM` för att fråga efter en lista över virtuella datorer i kontot.

```azurepowershell-interactive
Get-AzureRmVM
```

Standardutdata formateras automatiskt som en tabell.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Cmdleten `Select-Object` kan användas för att välja specifika egenskaper som är intressanta för dig.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a>Välja komplexa kapslade egenskaper

Om den egenskap du vill välja ligger djupt kapslad i JSON-utdata måste du ange den fullständiga sökvägen till den kapslade egenskapen. Följande exempel visar hur du väljer den virtuella datorns namn och operativsystemtyp i cmdleten `Get-AzureRmVM`.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a>Filtrera resultat med hjälp av cmdleten Where-Object

Med cmdleten `Where-Object` kan du filtrera resultatet baserat på valfritt egenskapsvärde. I följande exempel väljer filtret endast virtuella datorer som har texten "RGD" i sina namn.

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

Med nästa exempel visar resultaten de virtuella datorer som har vmSize ”Standard_DS1_V2”.

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
