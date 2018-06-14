---
title: Fråga efter Azure-resurser och formatera resultat | Microsoft Docs
description: Så här frågar du efter resurser i Azure och formaterar resultaten.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 1584c8166078b7d7d24ce8748307fde0f565b662
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853346"
---
# <a name="querying-for-azure-resources"></a>Fråga efter Azure-resurser

Frågor i PowerShell kan utföras med hjälp av inbyggda cmdletar. I PowerShell har cmdlet formen **_Verb-substantiv_**. Cmdletar med verbet **_Get_** är fråge-cmdletar. Cmdletarnas substantiv är de typer av Azure-resurser som cmdletens verb agerar på.


## <a name="selecting-simple-properties"></a>Välja enkla egenskaper

Azure PowerShell har standardformat som definierats för varje cmdlet. De vanligaste egenskaperna för varje resurstyp visas automatiskt i tabell- eller listformat. Mer information om att formatera utdata finns i [Formatera frågeresultat](formatting-output.md).

Använd cmdleten `Get-AzureRmVM` för att fråga efter en lista över virtuella datorer i kontot.

```powershell
Get-AzureRmVM
```

Standardutdata formateras automatiskt som en tabell.

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Cmdleten `Select-Object` kan användas för att välja specifika egenskaper som är intressanta för dig.

```powershell
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a>Välja komplexa kapslade egenskaper

Om den egenskap du vill välja ligger djupt kapslad i JSON-utdata måste du ange den fullständiga sökvägen till den kapslade egenskapen. Följande exempel visar hur du väljer den virtuella datorns namn och operativsystemtyp i cmdleten `Get-AzureRmVM`.

```powershell
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a>Filtrera resultatet med hjälp av cmdleten Where-Object

Med cmdleten `Where-Object` kan du filtrera resultatet baserat på valfritt egenskapsvärde. I följande exempel väljer filtret endast virtuella datorer som har texten "RGD" i sina namn.

```powershell
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

Med nästa exempel visar resultaten de virtuella datorer som har vmSize ”Standard_DS1_V2”.

```powershell
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
