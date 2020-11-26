---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320192"
---
# <span data-ttu-id="33f07-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="33f07-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="33f07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33f07-102">SYNOPSIS</span></span>
<span data-ttu-id="33f07-103">Skapa eller uppdatera en dedikerad HSM i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="33f07-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="33f07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33f07-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="33f07-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33f07-105">DESCRIPTION</span></span>
<span data-ttu-id="33f07-106">Skapa eller uppdatera en dedikerad HSM i det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="33f07-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="33f07-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33f07-107">EXAMPLES</span></span>

### <span data-ttu-id="33f07-108">Exempel 1: skapa en dedikerad HSM i ett befintligt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="33f07-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="33f07-109">Det här kommandot skapar en dedikerad HSM till ett befintligt virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="33f07-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="33f07-110">**Obs!** För närvarande är `New-AzDedicatedHsm` det en begränsning att den returneras innan HSM är fullt etablerad på Azure.</span><span class="sxs-lookup"><span data-stu-id="33f07-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="33f07-111">När du har skapat en ny HSM ber vi dig be om dess status `Get-AzDedicatedHsm` och kontrol lera att den `Provisioning State` är `Succeeded` före användning.</span><span class="sxs-lookup"><span data-stu-id="33f07-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="33f07-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33f07-112">PARAMETERS</span></span>

### <span data-ttu-id="33f07-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33f07-113">-AsJob</span></span>
<span data-ttu-id="33f07-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="33f07-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f07-115">-DefaultProfile</span></span>
<span data-ttu-id="33f07-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33f07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33f07-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="33f07-117">-Location</span></span>
<span data-ttu-id="33f07-118">Den Azure-plats där dedikerad HSM ska skapas.</span><span class="sxs-lookup"><span data-stu-id="33f07-118">The supported Azure location where the dedicated HSM should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="33f07-119">-Name</span></span>
<span data-ttu-id="33f07-120">Namn på dedikerad HSM</span><span class="sxs-lookup"><span data-stu-id="33f07-120">Name of the dedicated Hsm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="33f07-121">-NetworkInterface</span></span>
<span data-ttu-id="33f07-122">Anger listan med resurs-ID: n för de nätverks gränssnitt som är associerade med den dedikerade HSM.</span><span class="sxs-lookup"><span data-stu-id="33f07-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="33f07-123">För att konstruera kan du läsa avsnittet anteckningar för NETWORKINTERFACE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="33f07-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.INetworkInterface[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="33f07-124">-NoWait</span></span>
<span data-ttu-id="33f07-125">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="33f07-125">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33f07-126">-ResourceGroupName</span></span>
<span data-ttu-id="33f07-127">Namnet på resurs gruppen som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="33f07-127">The name of the Resource Group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="33f07-128">-Sku</span></span>
<span data-ttu-id="33f07-129">SKU för dedikerad HSM</span><span class="sxs-lookup"><span data-stu-id="33f07-129">SKU of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="33f07-130">-StampId</span></span>
<span data-ttu-id="33f07-131">Det här fältet används när RP inte stöder zoner för tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="33f07-131">This field will be used when RP does not support Availability zones.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="33f07-132">-SubnetId</span></span>
<span data-ttu-id="33f07-133">ARM-resurs-ID i form av/subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="33f07-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33f07-134">-SubscriptionId</span></span>
<span data-ttu-id="33f07-135">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="33f07-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="33f07-136">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="33f07-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="33f07-137">-Tag</span></span>
<span data-ttu-id="33f07-138">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="33f07-138">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="33f07-139">-Zone</span></span>
<span data-ttu-id="33f07-140">Dedikerade HSM-zoner.</span><span class="sxs-lookup"><span data-stu-id="33f07-140">The Dedicated Hsm zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33f07-141">-Confirm</span></span>
<span data-ttu-id="33f07-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33f07-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33f07-143">-WhatIf</span></span>
<span data-ttu-id="33f07-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33f07-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33f07-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33f07-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f07-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f07-146">CommonParameters</span></span>
<span data-ttu-id="33f07-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f07-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f07-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33f07-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f07-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33f07-149">INPUTS</span></span>

## <span data-ttu-id="33f07-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33f07-150">OUTPUTS</span></span>

### <span data-ttu-id="33f07-151">Microsoft. Azure. PowerShell. cmdletar. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="33f07-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="33f07-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33f07-152">NOTES</span></span>

<span data-ttu-id="33f07-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="33f07-153">ALIASES</span></span>

<span data-ttu-id="33f07-154">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="33f07-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33f07-155">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="33f07-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33f07-156">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="33f07-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33f07-157">NETWORKINTERFACE <INetworkInterface [] >: anger listan med resurs-ID för de nätverks gränssnitt som är kopplade till den dedikerade HSM.</span><span class="sxs-lookup"><span data-stu-id="33f07-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="33f07-158">`[PrivateIPAddress <String>]`: Gränssnittets privata IP-adress</span><span class="sxs-lookup"><span data-stu-id="33f07-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="33f07-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33f07-159">RELATED LINKS</span></span>
