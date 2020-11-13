---
title: Formatera cmdlet-utdata för Azure PowerShell
description: Så här formaterar du cmdlet-utdata för Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 44016cc9546869b05693276293119c21ca02e4b0
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410289"
---
# <a name="format-azure-powershell-cmdlet-output"></a><span data-ttu-id="b95f0-103">Formatera cmdlet-utdata för Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b95f0-103">Format Azure PowerShell cmdlet output</span></span>

<span data-ttu-id="b95f0-104">Som standard formaterar alla Azure PowerShell-cmdletar utdata för att förbättra läsbarheten.</span><span class="sxs-lookup"><span data-stu-id="b95f0-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="b95f0-105">Med PowerShell kan du konvertera eller formatera cmdlet-utdata genom att dirigera till en av följande cmdletar:</span><span class="sxs-lookup"><span data-stu-id="b95f0-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="b95f0-106">Formatering</span><span class="sxs-lookup"><span data-stu-id="b95f0-106">Formatting</span></span>      | <span data-ttu-id="b95f0-107">Konvertering</span><span class="sxs-lookup"><span data-stu-id="b95f0-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="b95f0-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="b95f0-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="b95f0-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="b95f0-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="b95f0-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="b95f0-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="b95f0-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="b95f0-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="b95f0-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="b95f0-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="b95f0-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="b95f0-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="b95f0-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="b95f0-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="b95f0-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="b95f0-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="b95f0-116">Formatering används för visning i en PowerShell-terminal och konvertering används för att generera data som ska användas av andra skript eller program.</span><span class="sxs-lookup"><span data-stu-id="b95f0-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="b95f0-117">Format för tabellutdata</span><span class="sxs-lookup"><span data-stu-id="b95f0-117">Table output format</span></span>

<span data-ttu-id="b95f0-118">Som standard är utdata från Azure PowerShell-cmdletar i tabellformatet.</span><span class="sxs-lookup"><span data-stu-id="b95f0-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="b95f0-119">Detta format visar inte all information om den begärda resursen:</span><span class="sxs-lookup"><span data-stu-id="b95f0-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="b95f0-120">Mängden data som visas av `Format-Table` kan påverkas av bredden på fönstret för PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="b95f0-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="b95f0-121">Om du vill begränsa utdata till specifika egenskaper och sortera dem kan egenskapsnamn anges som argument till `Format-Table`:</span><span class="sxs-lookup"><span data-stu-id="b95f0-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="b95f0-122">Skapa lista för utdataformat</span><span class="sxs-lookup"><span data-stu-id="b95f0-122">List output format</span></span>

<span data-ttu-id="b95f0-123">När du skapar en lista för utdataformat så skapas två kolumner med egenskapsnamn följt av värdet.</span><span class="sxs-lookup"><span data-stu-id="b95f0-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="b95f0-124">För komplexa objekt visas typen av objekt istället.</span><span class="sxs-lookup"><span data-stu-id="b95f0-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="b95f0-125">I följande utdata har vissa fält tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b95f0-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="b95f0-126">I likhet med `Format-Table` kan egenskapsnamn anges för att ordna och begränsa utdata:</span><span class="sxs-lookup"><span data-stu-id="b95f0-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="b95f0-127">Brett utdataformat</span><span class="sxs-lookup"><span data-stu-id="b95f0-127">Wide output format</span></span>

<span data-ttu-id="b95f0-128">Med brett utdataformat skapas endast ett egenskapsnamn per fråga.</span><span class="sxs-lookup"><span data-stu-id="b95f0-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="b95f0-129">Du kan kontrollera vilken egenskap som visas genom att ange en egenskap som ett argument.</span><span class="sxs-lookup"><span data-stu-id="b95f0-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="b95f0-130">Anpassat utdataformat</span><span class="sxs-lookup"><span data-stu-id="b95f0-130">Custom output format</span></span>

<span data-ttu-id="b95f0-131">Utdatatypen `Custom-Format` är avsedd för att formatera anpassade objekt.</span><span class="sxs-lookup"><span data-stu-id="b95f0-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="b95f0-132">Utan några argument fungerar den som `Format-List`, men den visar egenskapsnamnen på anpassade klasser.</span><span class="sxs-lookup"><span data-stu-id="b95f0-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="b95f0-133">I följande utdata har vissa fält tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b95f0-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="b95f0-134">Ange egenskapsnamn som argument till `Custom-Format` för att visa egenskaper och värden för anpassade objekt som värden:</span><span class="sxs-lookup"><span data-stu-id="b95f0-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="b95f0-135">I följande utdata har vissa fält tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b95f0-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="b95f0-136">Konvertering till andra dataformat</span><span class="sxs-lookup"><span data-stu-id="b95f0-136">Conversion to other data formats</span></span>

<span data-ttu-id="b95f0-137">Med cmdletar i `ConvertTo-*`-serien kan du konvertera resultaten från Azure PowerShell-cmdletar till maskinläsbara format.</span><span class="sxs-lookup"><span data-stu-id="b95f0-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="b95f0-138">Använd kommandot `Select-Object` i en pipeline innan du utför konverteringen för att endast hämta vissa egenskaper från Azure PowerShell-resultaten.</span><span class="sxs-lookup"><span data-stu-id="b95f0-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="b95f0-139">I följande exempel visas de olika typerna av utdata som varje konvertering producerar.</span><span class="sxs-lookup"><span data-stu-id="b95f0-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="b95f0-140">Konvertering till CSV</span><span class="sxs-lookup"><span data-stu-id="b95f0-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="b95f0-141">Konvertering till JSON</span><span class="sxs-lookup"><span data-stu-id="b95f0-141">Conversion to JSON</span></span>

<span data-ttu-id="b95f0-142">I JSON-utdata visas inte alla egenskaper som standard.</span><span class="sxs-lookup"><span data-stu-id="b95f0-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="b95f0-143">Använd argumentet `-Depth` för att ändra djupet för egenskaper som visas.</span><span class="sxs-lookup"><span data-stu-id="b95f0-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="b95f0-144">Som standard är expansionsdjupet `2`.</span><span class="sxs-lookup"><span data-stu-id="b95f0-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="b95f0-145">I följande utdata har vissa fält tagits bort.</span><span class="sxs-lookup"><span data-stu-id="b95f0-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="b95f0-146">Konvertering till XML</span><span class="sxs-lookup"><span data-stu-id="b95f0-146">Conversion to XML</span></span>

<span data-ttu-id="b95f0-147">Cmdleten `ConvertTo-XML` konverterar Azure PowerShell-svarsobjekt till ett rent XML-objekt som kan hanteras på samma sätt som andra XML-objekt i PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b95f0-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="b95f0-148">Konvertering till HTML</span><span class="sxs-lookup"><span data-stu-id="b95f0-148">Conversion to HTML</span></span>

<span data-ttu-id="b95f0-149">Vid konvertering av ett objekt till HTML skapas utdata som återges som en HTML-tabell.</span><span class="sxs-lookup"><span data-stu-id="b95f0-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="b95f0-150">HTML-renderingen beror på din webbläsares beteende för rendering av tabeller som inte innehåller information om bredd.</span><span class="sxs-lookup"><span data-stu-id="b95f0-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="b95f0-151">Inga anpassade klassobjekt visas.</span><span class="sxs-lookup"><span data-stu-id="b95f0-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```
