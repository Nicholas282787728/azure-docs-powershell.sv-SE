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
ms.sourcegitcommit: eeb720e053939a68873ae3973bc81d5826358c9f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2020
ms.locfileid: "80440681"
---
# <a name="query-output-of-azure-powershell"></a>Fråga utdata från Azure PowerShell 

Resultatet för varje Azure PowerShell-cmdlet är ett Azure PowerShell-objekt. Även cmdletar som inte uttryckligen är `Get-`-åtgärder kan returnera ett värde som kan granskas för att ge information om en resurs som har skapats eller ändrats. De flesta cmdletar returnerar ett enda objekt, men vissa returnerar vissa en matris som ska itereras.

I nästan alla fall kan du fråga utdata från Azure PowerShell med cmdleten [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), ofta förkortat till `select`. Utdata kan filtreras med [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), eller dess alias `where`.

## <a name="select-simple-properties"></a>Välja enkla egenskaper

I standardtabellformatet visar inte Azure PowerShell-cmdletarna alla tillgängliga egenskaper. Du kan se de fullständiga egenskaperna med cmdleten [Format-List](/powershell/module/microsoft.powershell.utility/format-list) eller genom att dirigera utdata till `Select-Object *`:

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

När du känner till namnen på de egenskaper som du är intresserad av kan du använda dem med `Select-Object` för att hämta dem direkt:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

Utdata från användning av `Select-Object` formateras alltid så att den begärda informationen visas. Information om hur du använder formatering som en del av frågor till cmdlet-resultat finns i [Formatera cmdlet-utdata i Azure PowerShell](formatting-output.md).

## <a name="select-nested-properties"></a>Välja kapslade egenskaper

Vissa egenskaper i cmdlet-utdata i Azure PowerShell använder kapslade objekt som egenskapen `StorageProfile` i `Get-AzVM`-utdata. Om du vill ha ett värde från en kapslad egenskap anger du ett visningsnamn och den fullständiga sökvägen till det värde du vill granska som en del av ett ordlisteargument för `Select-Object`:

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

Varje ordlisteargument väljer en egenskap från objektet. Den egenskap som ska extraheras måste vara en del av ett uttryck.

## <a name="filter-results"></a>Filtrera resultat 

Med cmdleten `Where-Object` kan du filtrera resultatet baserat på valfritt egenskapsvärde, inklusive kapslade egenskaper. I nästa exempel visas hur du använder `Where-Object` för att hitta de virtuella Linux-datorerna i en resursgrupp.

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

Du kan dirigera resultaten för `Select-Object` och `Where-Object` till varandra. Av prestandaskäl rekommenderar vi alltid att du placerar åtgärden `Where-Object` före `Select-Object`:

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