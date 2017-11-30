---
title: "Formatera frågeresultat | Microsoft Docs"
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
ms.openlocfilehash: 916cf8590de89762bade4f01ce5a502383d51796
ms.sourcegitcommit: 95f216dfda4841358d4656fbdea1b7faaeecbdbd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/27/2017
---
# <a name="formatting-query-results"></a><span data-ttu-id="06481-103">Formatera frågeresultat</span><span class="sxs-lookup"><span data-stu-id="06481-103">Formatting query results</span></span>

<span data-ttu-id="06481-104">Som standard har varje PowerShell-cmdlet fördefinierad formatering av utdata, vilket gör det enklare att läsa.</span><span class="sxs-lookup"><span data-stu-id="06481-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="06481-105">PowerShell ger också flexibiliteten att justera utdata eller konvertera cmdlet-utdata till ett annat format med följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="06481-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="06481-106">Formatering</span><span class="sxs-lookup"><span data-stu-id="06481-106">Formatting</span></span>      | <span data-ttu-id="06481-107">Konvertering</span><span class="sxs-lookup"><span data-stu-id="06481-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="06481-108">Formateringsexempel</span><span class="sxs-lookup"><span data-stu-id="06481-108">Formatting examples</span></span>

<span data-ttu-id="06481-109">I det här exemplet får vi en lista över virtuella Azure-datorer i standardprenumerationen.</span><span class="sxs-lookup"><span data-stu-id="06481-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="06481-110">Kommandot Get-AzureRmVM formaterar som standard utdata i tabellformat.</span><span class="sxs-lookup"><span data-stu-id="06481-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell
Get-AzureRmVM
```

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="06481-111">Om du vill begränsa de kolumner som returneras kan du använda cmdleten `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="06481-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="06481-112">I följande exempel har vi samma lista över virtuella datorer men begränsar utdata till endast den virtuella datorns namn, resursgrupp och den virtuella datorns plats.</span><span class="sxs-lookup"><span data-stu-id="06481-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="06481-113">Parametern `-Autosize` ändrar storleken på kolumner enligt storleken på data.</span><span class="sxs-lookup"><span data-stu-id="06481-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="06481-114">Om du så önskar kan du kan se information i ett listformat.</span><span class="sxs-lookup"><span data-stu-id="06481-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="06481-115">I följande exempel ser du detta med cmdleten `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="06481-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="converting-to-other-data-types"></a><span data-ttu-id="06481-116">Konvertera till andra datatyper</span><span class="sxs-lookup"><span data-stu-id="06481-116">Converting to other data types</span></span>

<span data-ttu-id="06481-117">PowerShell erbjuder även flera utdataformat som du kan använda för att fylla dina behov.</span><span class="sxs-lookup"><span data-stu-id="06481-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="06481-118">I följande exempel använder vi cmdleten `Select-Object` för att hämta attributen för de virtuella datorerna i vår prenumeration och konvertera utdata till ett CSV-format för enkel import till en databas eller ett kalkylblad.</span><span class="sxs-lookup"><span data-stu-id="06481-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="06481-119">Du kan även konvertera utdata till JSON-format.</span><span class="sxs-lookup"><span data-stu-id="06481-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="06481-120">Följande exempel skapar samma lista över virtuella datorer, men ändrar formatet för utdata till JSON.</span><span class="sxs-lookup"><span data-stu-id="06481-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```
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
