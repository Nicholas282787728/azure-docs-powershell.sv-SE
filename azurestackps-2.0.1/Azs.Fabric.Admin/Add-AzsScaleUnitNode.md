---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093105"
---
# <span data-ttu-id="41e95-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="41e95-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="41e95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41e95-102">SYNOPSIS</span></span>
<span data-ttu-id="41e95-103">Skalförändrar en skalen het.</span><span class="sxs-lookup"><span data-stu-id="41e95-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="41e95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41e95-104">SYNTAX</span></span>

### <span data-ttu-id="41e95-105">ScaleExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="41e95-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41e95-106">Storlek</span><span class="sxs-lookup"><span data-stu-id="41e95-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41e95-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41e95-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41e95-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="41e95-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41e95-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41e95-109">DESCRIPTION</span></span>
<span data-ttu-id="41e95-110">Skalförändrar en skalen het.</span><span class="sxs-lookup"><span data-stu-id="41e95-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="41e95-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41e95-111">EXAMPLES</span></span>

### <span data-ttu-id="41e95-112">Exempel 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="41e95-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="41e95-113">Lägga till en ny nod för skalnings enhet i ett kluster för skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="41e95-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="41e95-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41e95-114">PARAMETERS</span></span>

### <span data-ttu-id="41e95-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41e95-115">-AsJob</span></span>
<span data-ttu-id="41e95-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="41e95-116">Run the command as a job</span></span>

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

### <span data-ttu-id="41e95-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="41e95-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="41e95-118">Flagga anger om åtgärden ska vänta på att lagrings platsen ska konvergera innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="41e95-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e95-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e95-119">-DefaultProfile</span></span>
<span data-ttu-id="41e95-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41e95-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41e95-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41e95-121">-InputObject</span></span>
<span data-ttu-id="41e95-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="41e95-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="41e95-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="41e95-123">-Location</span></span>
<span data-ttu-id="41e95-124">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="41e95-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e95-125">-NodeList</span><span class="sxs-lookup"><span data-stu-id="41e95-125">-NodeList</span></span>
<span data-ttu-id="41e95-126">Lista över noder i den skalförändrade enheten.</span><span class="sxs-lookup"><span data-stu-id="41e95-126">List of nodes in the scale unit.</span></span>
<span data-ttu-id="41e95-127">För att konstruera kan du läsa avsnittet anteckningar för NODELIST-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="41e95-127">To construct, see NOTES section for NODELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e95-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="41e95-128">-NoWait</span></span>
<span data-ttu-id="41e95-129">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="41e95-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="41e95-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41e95-130">-PassThru</span></span>
<span data-ttu-id="41e95-131">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="41e95-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="41e95-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41e95-132">-ResourceGroupName</span></span>
<span data-ttu-id="41e95-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="41e95-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e95-134">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="41e95-134">-ScaleUnit</span></span>
<span data-ttu-id="41e95-135">Namnet på enheten.</span><span class="sxs-lookup"><span data-stu-id="41e95-135">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e95-136">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="41e95-136">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="41e95-137">En lista över indata som gör att du kan lägga till en uppsättning noder för skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="41e95-137">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="41e95-138">För att konstruera kan du läsa avsnittet anteckningar för SCALEUNITNODEPARAMETER-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="41e95-138">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="41e95-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41e95-139">-SubscriptionId</span></span>
<span data-ttu-id="41e95-140">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="41e95-140">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="41e95-141">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="41e95-141">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="41e95-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41e95-142">-Confirm</span></span>
<span data-ttu-id="41e95-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41e95-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41e95-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41e95-144">-WhatIf</span></span>
<span data-ttu-id="41e95-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41e95-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41e95-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41e95-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41e95-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e95-147">CommonParameters</span></span>
<span data-ttu-id="41e95-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41e95-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e95-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41e95-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e95-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41e95-150">INPUTS</span></span>

### <span data-ttu-id="41e95-151">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="41e95-151">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="41e95-152">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="41e95-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="41e95-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41e95-153">OUTPUTS</span></span>

### <span data-ttu-id="41e95-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41e95-154">System.Boolean</span></span>



## <span data-ttu-id="41e95-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41e95-155">NOTES</span></span>

<span data-ttu-id="41e95-156">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="41e95-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41e95-157">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41e95-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="41e95-158">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="41e95-158">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41e95-159">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="41e95-159">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="41e95-160">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="41e95-160">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="41e95-161">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="41e95-161">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="41e95-162">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="41e95-162">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="41e95-163">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="41e95-163">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="41e95-164">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="41e95-164">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="41e95-165">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="41e95-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41e95-166">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="41e95-166">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="41e95-167">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="41e95-167">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="41e95-168">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="41e95-168">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="41e95-169">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="41e95-169">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="41e95-170">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="41e95-170">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="41e95-171">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="41e95-171">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="41e95-172">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="41e95-172">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="41e95-173">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="41e95-173">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="41e95-174">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="41e95-174">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="41e95-175">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="41e95-175">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="41e95-176">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="41e95-176">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="41e95-177">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="41e95-177">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="41e95-178">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="41e95-178">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="41e95-179">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="41e95-179">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="41e95-180">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="41e95-180">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="41e95-181">NODELIST <IScaleOutScaleUnitParameters [] >: lista med noder i den skalförändrade enheten.</span><span class="sxs-lookup"><span data-stu-id="41e95-181">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="41e95-182">`[BmciPv4Address <String>]`: Den fysiska datorns BMC-adress.</span><span class="sxs-lookup"><span data-stu-id="41e95-182">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="41e95-183">`[ComputerName <String>]`: Dator namnet på den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="41e95-183">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="41e95-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : en lista över indata som gör att du kan lägga till en uppsättning noder för skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="41e95-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="41e95-185">`[AwaitStorageConvergence <Boolean?>]`: Flaggan anger om åtgärden ska vänta på att lagrings platsen ska konvergera innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="41e95-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="41e95-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Lista med noder i den skalförändrade enheten.</span><span class="sxs-lookup"><span data-stu-id="41e95-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="41e95-187">`[BmciPv4Address <String>]`: Den fysiska datorns BMC-adress.</span><span class="sxs-lookup"><span data-stu-id="41e95-187">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="41e95-188">`[ComputerName <String>]`: Dator namnet på den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="41e95-188">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="41e95-189">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41e95-189">RELATED LINKS</span></span>

