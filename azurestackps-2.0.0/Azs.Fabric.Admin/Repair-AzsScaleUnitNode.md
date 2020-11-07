---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923169"
---
# <span data-ttu-id="7f818-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="7f818-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="7f818-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f818-102">SYNOPSIS</span></span>
<span data-ttu-id="7f818-103">Reparerar en nod i klustret.</span><span class="sxs-lookup"><span data-stu-id="7f818-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="7f818-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f818-104">SYNTAX</span></span>

### <span data-ttu-id="7f818-105">RepairExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="7f818-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7f818-106">Reparera</span><span class="sxs-lookup"><span data-stu-id="7f818-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f818-107">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7f818-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7f818-108">RepairViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7f818-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7f818-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f818-109">DESCRIPTION</span></span>
<span data-ttu-id="7f818-110">Reparerar en nod i klustret.</span><span class="sxs-lookup"><span data-stu-id="7f818-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="7f818-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f818-111">EXAMPLES</span></span>

### <span data-ttu-id="7f818-112">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="7f818-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="7f818-113">Reparera en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="7f818-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="7f818-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f818-114">PARAMETERS</span></span>

### <span data-ttu-id="7f818-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f818-115">-AsJob</span></span>
<span data-ttu-id="7f818-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="7f818-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7f818-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="7f818-117">-BareMetalNode</span></span>
<span data-ttu-id="7f818-118">Beskrivning av en Bare Metal-nod som används för att skalförändra en åtgärd i ett kluster.</span><span class="sxs-lookup"><span data-stu-id="7f818-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="7f818-119">För att konstruera kan du läsa avsnittet anteckningar för BAREMETALNODE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7f818-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription
Parameter Sets: Repair, RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-120">-BiosVersion</span><span class="sxs-lookup"><span data-stu-id="7f818-120">-BiosVersion</span></span>
<span data-ttu-id="7f818-121">BIOS-version av den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="7f818-121">Bios version of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="7f818-122">-BmciPv4Address</span></span>
<span data-ttu-id="7f818-123">BMC-adress för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="7f818-123">BMC address of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-124">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="7f818-124">-ClusterName</span></span>
<span data-ttu-id="7f818-125">Klustrets namn.</span><span class="sxs-lookup"><span data-stu-id="7f818-125">Name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="7f818-126">-ComputerName</span></span>
<span data-ttu-id="7f818-127">Namn på datorn.</span><span class="sxs-lookup"><span data-stu-id="7f818-127">Name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f818-128">-DefaultProfile</span></span>
<span data-ttu-id="7f818-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f818-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f818-130">-Force</span><span class="sxs-lookup"><span data-stu-id="7f818-130">-Force</span></span>
<span data-ttu-id="7f818-131">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7f818-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7f818-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f818-132">-InputObject</span></span>
<span data-ttu-id="7f818-133">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7f818-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RepairViaIdentity, RepairViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="7f818-134">-Location</span></span>
<span data-ttu-id="7f818-135">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="7f818-135">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-136">-MacAddress</span><span class="sxs-lookup"><span data-stu-id="7f818-136">-MacAddress</span></span>
<span data-ttu-id="7f818-137">Namn på MAC-adressen till mappen Bare Metal.</span><span class="sxs-lookup"><span data-stu-id="7f818-137">Name of the MAC address of the bare metal node.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-138">-Modell</span><span class="sxs-lookup"><span data-stu-id="7f818-138">-Model</span></span>
<span data-ttu-id="7f818-139">Modell för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="7f818-139">Model of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f818-140">-Name</span></span>
<span data-ttu-id="7f818-141">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="7f818-141">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-142">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7f818-142">-NoWait</span></span>
<span data-ttu-id="7f818-143">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="7f818-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7f818-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f818-144">-PassThru</span></span>
<span data-ttu-id="7f818-145">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="7f818-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7f818-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f818-146">-ResourceGroupName</span></span>
<span data-ttu-id="7f818-147">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7f818-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-148">-SerialNumber</span><span class="sxs-lookup"><span data-stu-id="7f818-148">-SerialNumber</span></span>
<span data-ttu-id="7f818-149">Serie nummer för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="7f818-149">Serial number of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f818-150">-SubscriptionId</span></span>
<span data-ttu-id="7f818-151">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7f818-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7f818-152">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7f818-152">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-153">-Vendor</span><span class="sxs-lookup"><span data-stu-id="7f818-153">-Vendor</span></span>
<span data-ttu-id="7f818-154">Den fysiska datorns tillverkare.</span><span class="sxs-lookup"><span data-stu-id="7f818-154">Vendor of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7f818-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7f818-155">-Confirm</span></span>
<span data-ttu-id="7f818-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7f818-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f818-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f818-157">-WhatIf</span></span>
<span data-ttu-id="7f818-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7f818-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f818-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7f818-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f818-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f818-160">CommonParameters</span></span>
<span data-ttu-id="7f818-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f818-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f818-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f818-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f818-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f818-163">INPUTS</span></span>

### <span data-ttu-id="7f818-164">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IBareMetalNodeDescription</span><span class="sxs-lookup"><span data-stu-id="7f818-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="7f818-165">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7f818-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="7f818-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f818-166">OUTPUTS</span></span>

### <span data-ttu-id="7f818-167">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f818-167">System.Boolean</span></span>



## <span data-ttu-id="7f818-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f818-168">NOTES</span></span>

<span data-ttu-id="7f818-169">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7f818-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f818-170">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f818-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7f818-171">BAREMETALNODE <IBareMetalNodeDescription> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7f818-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="7f818-172">`[BiosVersion <String>]`: BIOS-version av den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="7f818-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="7f818-173">`[BmciPv4Address <String>]`: Den fysiska datorns BMC-adress.</span><span class="sxs-lookup"><span data-stu-id="7f818-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="7f818-174">`[ClusterName <String>]`: Klustrets namn.</span><span class="sxs-lookup"><span data-stu-id="7f818-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="7f818-175">`[ComputerName <String>]`: Namnet på datorn.</span><span class="sxs-lookup"><span data-stu-id="7f818-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="7f818-176">`[MacAddress <String>]`: Namnet på MAC-adressen till mappen Bare Metal.</span><span class="sxs-lookup"><span data-stu-id="7f818-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="7f818-177">`[Model <String>]`: Modellen för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="7f818-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="7f818-178">`[SerialNumber <String>]`: Serie numret för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="7f818-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="7f818-179">`[Vendor <String>]`: Den fysiska datorns tillverkare.</span><span class="sxs-lookup"><span data-stu-id="7f818-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="7f818-180">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7f818-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7f818-181">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="7f818-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="7f818-182">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="7f818-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="7f818-183">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="7f818-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="7f818-184">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="7f818-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="7f818-185">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="7f818-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="7f818-186">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="7f818-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="7f818-187">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="7f818-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7f818-188">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="7f818-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="7f818-189">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="7f818-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="7f818-190">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="7f818-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="7f818-191">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="7f818-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="7f818-192">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="7f818-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="7f818-193">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="7f818-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="7f818-194">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="7f818-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="7f818-195">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="7f818-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="7f818-196">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="7f818-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="7f818-197">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="7f818-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="7f818-198">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="7f818-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="7f818-199">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="7f818-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="7f818-200">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="7f818-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="7f818-201">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7f818-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7f818-202">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7f818-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7f818-203">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="7f818-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="7f818-204">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f818-204">RELATED LINKS</span></span>

