---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: fe7726c25ee9dd83ca940b4ac6e47b3cc26a6457
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099943"
---
# <span data-ttu-id="3394a-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="3394a-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="3394a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3394a-102">SYNOPSIS</span></span>
<span data-ttu-id="3394a-103">Skalförändrar en skalen het.</span><span class="sxs-lookup"><span data-stu-id="3394a-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="3394a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3394a-104">SYNTAX</span></span>

### <span data-ttu-id="3394a-105">ScaleExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="3394a-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-BmciPv4Address <String>] [-ComputerName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3394a-106">Storlek</span><span class="sxs-lookup"><span data-stu-id="3394a-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3394a-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3394a-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3394a-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3394a-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-BmciPv4Address <String>] [-ComputerName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3394a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3394a-109">DESCRIPTION</span></span>
<span data-ttu-id="3394a-110">Skalförändrar en skalen het.</span><span class="sxs-lookup"><span data-stu-id="3394a-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="3394a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3394a-111">EXAMPLES</span></span>

### <span data-ttu-id="3394a-112">Exempel 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="3394a-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -BmciPv4Address $BmciPv4Address -ComputerName $ComputerName -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="3394a-113">Lägga till en ny nod för skalnings enhet i ett kluster för skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="3394a-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="3394a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3394a-114">PARAMETERS</span></span>

### <span data-ttu-id="3394a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3394a-115">-AsJob</span></span>
<span data-ttu-id="3394a-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="3394a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3394a-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="3394a-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="3394a-118">Flagga anger om åtgärden ska vänta på att lagrings platsen ska konvergera innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="3394a-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="3394a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3394a-119">-DefaultProfile</span></span>
<span data-ttu-id="3394a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3394a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3394a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3394a-121">-InputObject</span></span>
<span data-ttu-id="3394a-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3394a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3394a-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="3394a-123">-Location</span></span>
<span data-ttu-id="3394a-124">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="3394a-124">Location of the resource.</span></span>

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

### <span data-ttu-id="3394a-125">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="3394a-125">-BmciPv4Address</span></span> 
<span data-ttu-id="3394a-126">BMC-adress för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="3394a-126">BMC address of the physical machine.</span></span>

### <span data-ttu-id="3394a-127">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="3394a-127">-ComputerName</span></span> 
<span data-ttu-id="3394a-128">Dator namnet på den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="3394a-128">Computer name of the physical machine.</span></span>

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

### <span data-ttu-id="3394a-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3394a-129">-NoWait</span></span>
<span data-ttu-id="3394a-130">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="3394a-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3394a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3394a-131">-PassThru</span></span>
<span data-ttu-id="3394a-132">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="3394a-132">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3394a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3394a-133">-ResourceGroupName</span></span>
<span data-ttu-id="3394a-134">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3394a-134">Name of the resource group.</span></span>

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

### <span data-ttu-id="3394a-135">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="3394a-135">-ScaleUnit</span></span>
<span data-ttu-id="3394a-136">Namnet på enheten.</span><span class="sxs-lookup"><span data-stu-id="3394a-136">Name of the scale units.</span></span>

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

### <span data-ttu-id="3394a-137">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="3394a-137">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="3394a-138">En lista över indata som gör att du kan lägga till en uppsättning noder för skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="3394a-138">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="3394a-139">För att konstruera kan du läsa avsnittet anteckningar för SCALEUNITNODEPARAMETER-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3394a-139">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="3394a-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3394a-140">-SubscriptionId</span></span>
<span data-ttu-id="3394a-141">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3394a-141">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3394a-142">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3394a-142">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3394a-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3394a-143">-Confirm</span></span>
<span data-ttu-id="3394a-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3394a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3394a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3394a-145">-WhatIf</span></span>
<span data-ttu-id="3394a-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3394a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3394a-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3394a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3394a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3394a-148">CommonParameters</span></span>
<span data-ttu-id="3394a-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3394a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3394a-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3394a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3394a-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3394a-151">INPUTS</span></span>

### <span data-ttu-id="3394a-152">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="3394a-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="3394a-153">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3394a-153">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="3394a-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3394a-154">OUTPUTS</span></span>

### <span data-ttu-id="3394a-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3394a-155">System.Boolean</span></span>

## <span data-ttu-id="3394a-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3394a-156">NOTES</span></span>

<span data-ttu-id="3394a-157">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3394a-157">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3394a-158">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3394a-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3394a-159">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3394a-159">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3394a-160">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="3394a-160">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="3394a-161">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="3394a-161">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="3394a-162">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="3394a-162">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="3394a-163">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="3394a-163">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="3394a-164">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="3394a-164">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="3394a-165">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="3394a-165">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="3394a-166">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3394a-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3394a-167">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="3394a-167">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="3394a-168">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="3394a-168">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="3394a-169">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="3394a-169">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3394a-170">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="3394a-170">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="3394a-171">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="3394a-171">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="3394a-172">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="3394a-172">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="3394a-173">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="3394a-173">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="3394a-174">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3394a-174">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3394a-175">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="3394a-175">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="3394a-176">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3394a-176">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="3394a-177">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="3394a-177">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="3394a-178">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="3394a-178">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="3394a-179">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3394a-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3394a-180">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3394a-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3394a-181">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="3394a-181">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="3394a-182">NODELIST <IScaleOutScaleUnitParameters [] >: lista med noder i den skalförändrade enheten.</span><span class="sxs-lookup"><span data-stu-id="3394a-182">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="3394a-183">`[BmciPv4Address <String>]`: Den fysiska datorns BMC-adress.</span><span class="sxs-lookup"><span data-stu-id="3394a-183">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="3394a-184">`[ComputerName <String>]`: Dator namnet på den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="3394a-184">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="3394a-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : en lista över indata som gör att du kan lägga till en uppsättning noder för skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="3394a-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="3394a-186">`[AwaitStorageConvergence <Boolean?>]`: Flaggan anger om åtgärden ska vänta på att lagrings platsen ska konvergera innan den returneras.</span><span class="sxs-lookup"><span data-stu-id="3394a-186">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="3394a-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Lista med noder i den skalförändrade enheten.</span><span class="sxs-lookup"><span data-stu-id="3394a-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="3394a-188">`[BmciPv4Address <String>]`: Den fysiska datorns BMC-adress.</span><span class="sxs-lookup"><span data-stu-id="3394a-188">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="3394a-189">`[ComputerName <String>]`: Dator namnet på den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="3394a-189">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="3394a-190">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3394a-190">RELATED LINKS</span></span>
