---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320191"
---
# <span data-ttu-id="e44ab-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="e44ab-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="e44ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e44ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e44ab-103">Hämtar den angivna Azure-dedikerade HSM.</span><span class="sxs-lookup"><span data-stu-id="e44ab-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="e44ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e44ab-104">SYNTAX</span></span>

### <span data-ttu-id="e44ab-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="e44ab-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e44ab-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e44ab-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e44ab-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e44ab-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e44ab-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="e44ab-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e44ab-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e44ab-109">DESCRIPTION</span></span>
<span data-ttu-id="e44ab-110">Hämtar den angivna Azure-dedikerade HSM.</span><span class="sxs-lookup"><span data-stu-id="e44ab-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="e44ab-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e44ab-111">EXAMPLES</span></span>

### <span data-ttu-id="e44ab-112">Exempel 1: Hämta alla dedikerade HSM under ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="e44ab-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e44ab-113">Det här kommandot får alla dedikerad HSM under ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="e44ab-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="e44ab-114">Exempel 2: Hämta alla dedikerade HSM under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e44ab-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e44ab-115">Det här kommandot får alla dedikerad HSM under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e44ab-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="e44ab-116">Exempel 3: skaffa en dedikerad HSM efter namn</span><span class="sxs-lookup"><span data-stu-id="e44ab-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e44ab-117">Det här kommandot får en dedikerad HSM efter namn.</span><span class="sxs-lookup"><span data-stu-id="e44ab-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="e44ab-118">Exempel 4: Hämta en dedikerad HSM efter objekt</span><span class="sxs-lookup"><span data-stu-id="e44ab-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e44ab-119">Det här kommandot får en dedikerad HSM efter objekt.</span><span class="sxs-lookup"><span data-stu-id="e44ab-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="e44ab-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e44ab-120">PARAMETERS</span></span>

### <span data-ttu-id="e44ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44ab-121">-DefaultProfile</span></span>
<span data-ttu-id="e44ab-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e44ab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44ab-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e44ab-123">-InputObject</span></span>
<span data-ttu-id="e44ab-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e44ab-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e44ab-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="e44ab-125">-Name</span></span>
<span data-ttu-id="e44ab-126">Namnet på den dedikerade HSM.</span><span class="sxs-lookup"><span data-stu-id="e44ab-126">The name of the dedicated HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44ab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e44ab-127">-ResourceGroupName</span></span>
<span data-ttu-id="e44ab-128">Namnet på resurs gruppen som den dedikerade HSM tillhör.</span><span class="sxs-lookup"><span data-stu-id="e44ab-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44ab-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e44ab-129">-SubscriptionId</span></span>
<span data-ttu-id="e44ab-130">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e44ab-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e44ab-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e44ab-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44ab-132">-Överst</span><span class="sxs-lookup"><span data-stu-id="e44ab-132">-Top</span></span>
<span data-ttu-id="e44ab-133">Maximalt antal resultat som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="e44ab-133">Maximum number of results to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44ab-134">CommonParameters</span></span>
<span data-ttu-id="e44ab-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44ab-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e44ab-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44ab-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e44ab-137">INPUTS</span></span>

### <span data-ttu-id="e44ab-138">Microsoft. Azure. PowerShell. cmdletar. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="e44ab-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="e44ab-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e44ab-139">OUTPUTS</span></span>

### <span data-ttu-id="e44ab-140">Microsoft. Azure. PowerShell. cmdletar. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="e44ab-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="e44ab-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e44ab-141">NOTES</span></span>

<span data-ttu-id="e44ab-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e44ab-142">ALIASES</span></span>

<span data-ttu-id="e44ab-143">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e44ab-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e44ab-144">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e44ab-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e44ab-145">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e44ab-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e44ab-146">INPUTOBJECT <IDedicatedHsmIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e44ab-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e44ab-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e44ab-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e44ab-148">`[Name <String>]`: Namnet på den dedikerade HSM</span><span class="sxs-lookup"><span data-stu-id="e44ab-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="e44ab-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="e44ab-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="e44ab-150">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e44ab-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e44ab-151">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e44ab-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e44ab-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e44ab-152">RELATED LINKS</span></span>

