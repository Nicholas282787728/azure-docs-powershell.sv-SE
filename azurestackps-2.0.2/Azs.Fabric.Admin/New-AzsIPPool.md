---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/new-azsippool
schema: 2.0.0
ms.openlocfilehash: 2b04c5c1eb4d0a2b79543bf81bbfc02d1f0fb4ad
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100114"
---
# <span data-ttu-id="a5186-101">New-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="a5186-101">New-AzsIPPool</span></span>

## <span data-ttu-id="a5186-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5186-102">SYNOPSIS</span></span>
<span data-ttu-id="a5186-103">Skapa en IP-pool.</span><span class="sxs-lookup"><span data-stu-id="a5186-103">Create an IP pool.</span></span>
<span data-ttu-id="a5186-104">När du har skapat en IP-pool kan den inte tas bort.</span><span class="sxs-lookup"><span data-stu-id="a5186-104">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="a5186-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5186-105">SYNTAX</span></span>

### <span data-ttu-id="a5186-106">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="a5186-106">CreateExpanded (Default)</span></span>
```
New-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AddressPrefix <String>] [-EndIPAddress <String>]
 [-NumberOfAllocatedIPAddress <Int64>] [-NumberOfIPAddress <Int64>] [-NumberOfIPAddressesInTransition <Int64>]
 [-StartIPAddress <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a5186-107">Göra</span><span class="sxs-lookup"><span data-stu-id="a5186-107">Create</span></span>
```
New-AzsIPPool -Name <String> -Pool <IIPPool> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a5186-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5186-108">DESCRIPTION</span></span>
<span data-ttu-id="a5186-109">Skapa en IP-pool.</span><span class="sxs-lookup"><span data-stu-id="a5186-109">Create an IP pool.</span></span>
<span data-ttu-id="a5186-110">När du har skapat en IP-pool kan den inte tas bort.</span><span class="sxs-lookup"><span data-stu-id="a5186-110">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="a5186-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5186-111">EXAMPLES</span></span>

### <span data-ttu-id="a5186-112">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="a5186-112">Example 1:</span></span>
```powershell
PS C:\> New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24

```

<span data-ttu-id="a5186-113">Skapa en ny IP-pool.</span><span class="sxs-lookup"><span data-stu-id="a5186-113">Create a new IP pool.</span></span>



## <span data-ttu-id="a5186-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5186-114">PARAMETERS</span></span>

### <span data-ttu-id="a5186-115">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a5186-115">-AddressPrefix</span></span>
<span data-ttu-id="a5186-116">Adressprefixet.</span><span class="sxs-lookup"><span data-stu-id="a5186-116">The address prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a5186-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5186-117">-AsJob</span></span>
<span data-ttu-id="a5186-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="a5186-118">Run the command as a job</span></span>

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

### <span data-ttu-id="a5186-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5186-119">-DefaultProfile</span></span>
<span data-ttu-id="a5186-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5186-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5186-121">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="a5186-121">-EndIPAddress</span></span>
<span data-ttu-id="a5186-122">Den sista IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="a5186-122">The ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a5186-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="a5186-123">-Location</span></span>
<span data-ttu-id="a5186-124">Den region där resursen finns.</span><span class="sxs-lookup"><span data-stu-id="a5186-124">The region where the resource is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a5186-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5186-125">-Name</span></span>
<span data-ttu-id="a5186-126">IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="a5186-126">IP pool name.</span></span>

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

### <span data-ttu-id="a5186-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a5186-127">-NoWait</span></span>
<span data-ttu-id="a5186-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="a5186-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5186-129">-NumberOfAllocatedIPAddress</span><span class="sxs-lookup"><span data-stu-id="a5186-129">-NumberOfAllocatedIPAddress</span></span>
<span data-ttu-id="a5186-130">Antalet för tillfället tilldelade IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="a5186-130">The number of currently allocated IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a5186-131">-NumberOfIPAddress</span><span class="sxs-lookup"><span data-stu-id="a5186-131">-NumberOfIPAddress</span></span>
<span data-ttu-id="a5186-132">Totalt antal IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="a5186-132">The total number of IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a5186-133">-NumberOfIPAddressesInTransition</span><span class="sxs-lookup"><span data-stu-id="a5186-133">-NumberOfIPAddressesInTransition</span></span>
<span data-ttu-id="a5186-134">Aktuellt antal IP-adresser i över gången.</span><span class="sxs-lookup"><span data-stu-id="a5186-134">The current number of IP addresses in transition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a5186-135">-Pool</span><span class="sxs-lookup"><span data-stu-id="a5186-135">-Pool</span></span>
<span data-ttu-id="a5186-136">Den här resursen definierar intervallet med IP-adresser som adresser tilldelas till för noder inom ett undernät.</span><span class="sxs-lookup"><span data-stu-id="a5186-136">This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
<span data-ttu-id="a5186-137">Om du vill bygga kan du läsa avsnittet anteckningar för egenskaper för pooler och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a5186-137">To construct, see NOTES section for POOL properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a5186-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5186-138">-ResourceGroupName</span></span>
<span data-ttu-id="a5186-139">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a5186-139">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a5186-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="a5186-140">-StartIPAddress</span></span>
<span data-ttu-id="a5186-141">Första IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="a5186-141">The starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a5186-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5186-142">-SubscriptionId</span></span>
<span data-ttu-id="a5186-143">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a5186-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5186-144">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a5186-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a5186-145">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a5186-145">-Tag</span></span>
<span data-ttu-id="a5186-146">Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a5186-146">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a5186-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5186-147">-Confirm</span></span>
<span data-ttu-id="a5186-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5186-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5186-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5186-149">-WhatIf</span></span>
<span data-ttu-id="a5186-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5186-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5186-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5186-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5186-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5186-152">CommonParameters</span></span>
<span data-ttu-id="a5186-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5186-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5186-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5186-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5186-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5186-155">INPUTS</span></span>

### <span data-ttu-id="a5186-156">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="a5186-156">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>

## <span data-ttu-id="a5186-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5186-157">OUTPUTS</span></span>

### <span data-ttu-id="a5186-158">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="a5186-158">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="a5186-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5186-159">NOTES</span></span>

<span data-ttu-id="a5186-160">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a5186-160">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5186-161">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a5186-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a5186-162">POOL <IIPPool> : den här resursen definierar intervallet med IP-adresser från vilka adresser tilldelas till noder inom ett undernät.</span><span class="sxs-lookup"><span data-stu-id="a5186-162">POOL <IIPPool>: This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
  - <span data-ttu-id="a5186-163">`[Location <String>]`: Regionen där resursen finns.</span><span class="sxs-lookup"><span data-stu-id="a5186-163">`[Location <String>]`: The region where the resource is located.</span></span>
  - <span data-ttu-id="a5186-164">`[Tag <IResourceTags>]`: Lista över par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a5186-164">`[Tag <IResourceTags>]`: List of key-value pairs.</span></span>
    - <span data-ttu-id="a5186-165">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="a5186-165">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a5186-166">`[AddressPrefix <String>]`: Adressprefixet.</span><span class="sxs-lookup"><span data-stu-id="a5186-166">`[AddressPrefix <String>]`: The address prefix.</span></span>
  - <span data-ttu-id="a5186-167">`[EndIPAddress <String>]`: Den avslutande IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="a5186-167">`[EndIPAddress <String>]`: The ending IP address.</span></span>
  - <span data-ttu-id="a5186-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: Antalet för tillfället tilldelade IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="a5186-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: The number of currently allocated IP addresses.</span></span>
  - <span data-ttu-id="a5186-169">`[NumberOfIPAddresses <Int64?>]`: Det totala antalet IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="a5186-169">`[NumberOfIPAddresses <Int64?>]`: The total number of IP addresses.</span></span>
  - <span data-ttu-id="a5186-170">`[NumberOfIPAddressesInTransition <Int64?>]`: Det aktuella antalet IP-adresser i över gången.</span><span class="sxs-lookup"><span data-stu-id="a5186-170">`[NumberOfIPAddressesInTransition <Int64?>]`: The current number of IP addresses in transition.</span></span>
  - <span data-ttu-id="a5186-171">`[StartIPAddress <String>]`: Den första IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="a5186-171">`[StartIPAddress <String>]`: The starting IP address.</span></span>

## <span data-ttu-id="a5186-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5186-172">RELATED LINKS</span></span>

