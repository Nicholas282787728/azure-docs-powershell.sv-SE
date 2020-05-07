---
title: Formatera cmdlet-utdata för Azure PowerShell
description: Så här formaterar du cmdlet-utdata för Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 6a35024e1bac819fa9b69174195e5245361cb7cc
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/05/2020
ms.locfileid: "65535002"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="ad2e6-103">Formatera cmdlet-utdata för Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ad2e6-103">Format AzurePowerShell cmdlet output</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="ad2e6-104">Som standard har varje Azure PowerShell-cmdlet fördefinierad formatering av utdata, vilket gör det enklare att läsa.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="ad2e6-105">PowerShell ger också flexibiliteten att justera utdata eller konvertera cmdlet-utdata till ett annat format med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="ad2e6-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="ad2e6-106">Formatering</span><span class="sxs-lookup"><span data-stu-id="ad2e6-106">Formatting</span></span>      | <span data-ttu-id="ad2e6-107">Konvertering</span><span class="sxs-lookup"><span data-stu-id="ad2e6-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="ad2e6-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="ad2e6-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="ad2e6-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="ad2e6-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="ad2e6-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="ad2e6-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="ad2e6-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="ad2e6-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="ad2e6-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="ad2e6-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="ad2e6-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="ad2e6-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="ad2e6-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="ad2e6-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="ad2e6-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="ad2e6-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="ad2e6-116">Formatexempel</span><span class="sxs-lookup"><span data-stu-id="ad2e6-116">Format examples</span></span>

<span data-ttu-id="ad2e6-117">I det här exemplet får vi en lista över virtuella Azure-datorer i standardprenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-117">In this example, we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="ad2e6-118">Kommandot `Get-AzureRmVM` formaterar som standard utdata i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="ad2e6-119">Om du vill begränsa de kolumner som returneras kan du använda cmdleten `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="ad2e6-120">I följande exempel har vi samma lista över virtuella datorer men begränsar utdata till endast den virtuella datorns namn, resursgrupp och den virtuella datorns plats.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-120">In the following example, we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="ad2e6-121">Parametern `-Autosize` ändrar storleken på kolumner enligt storleken på data.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="ad2e6-122">Utdata kan även formateras i en lista.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="ad2e6-123">I följande exempel ser du detta med cmdleten `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-123">The following example shows this using the`Format-List` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a><span data-ttu-id="ad2e6-124">Konvertera till andra datatyper</span><span class="sxs-lookup"><span data-stu-id="ad2e6-124">Convert to other data types</span></span>

<span data-ttu-id="ad2e6-125">PowerShell kan också ta kommandoutdata och konvertera dem till flera dataformat.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="ad2e6-126">I följande exempel använder vi cmdleten `Select-Object` för att hämta attributen för de virtuella datorerna i vår prenumeration och konvertera utdata till CSV-format för enkel import till en databas eller ett kalkylblad.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-126">In the following example, the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="ad2e6-127">Utdata kan även konverteras till JSON-format.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="ad2e6-128">Följande exempel skapar samma lista över virtuella datorer, men ändrar formatet för utdata till JSON.</span><span class="sxs-lookup"><span data-stu-id="ad2e6-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
