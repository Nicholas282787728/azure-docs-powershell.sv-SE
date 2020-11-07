---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructurerole
schema: 2.0.0
ms.openlocfilehash: 6e8b5f2dbfde62613a521fd7a49fba27c54ab498
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923166"
---
# <span data-ttu-id="6dff6-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="6dff6-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="6dff6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6dff6-102">SYNOPSIS</span></span>
<span data-ttu-id="6dff6-103">Startar om den begärda infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="6dff6-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="6dff6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6dff6-104">SYNTAX</span></span>

### <span data-ttu-id="6dff6-105">Starta om (standard)</span><span class="sxs-lookup"><span data-stu-id="6dff6-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6dff6-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6dff6-106">RestartViaIdentity</span></span>
```
Restart-AzsInfrastructureRole -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6dff6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6dff6-107">DESCRIPTION</span></span>
<span data-ttu-id="6dff6-108">Startar om den begärda infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="6dff6-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="6dff6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6dff6-109">EXAMPLES</span></span>

### <span data-ttu-id="6dff6-110">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="6dff6-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRole -Name "Compute Controller"

```

<span data-ttu-id="6dff6-111">Starta om en infrastruktur roll som har kraschat.</span><span class="sxs-lookup"><span data-stu-id="6dff6-111">Restart an infrastructure role which has crashed.</span></span>



## <span data-ttu-id="6dff6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6dff6-112">PARAMETERS</span></span>

### <span data-ttu-id="6dff6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6dff6-113">-AsJob</span></span>
<span data-ttu-id="6dff6-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="6dff6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6dff6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dff6-115">-DefaultProfile</span></span>
<span data-ttu-id="6dff6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6dff6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dff6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6dff6-117">-Force</span></span>
<span data-ttu-id="6dff6-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6dff6-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6dff6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dff6-119">-InputObject</span></span>
<span data-ttu-id="6dff6-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6dff6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6dff6-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="6dff6-121">-Location</span></span>
<span data-ttu-id="6dff6-122">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="6dff6-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6dff6-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="6dff6-123">-Name</span></span>
<span data-ttu-id="6dff6-124">Namn på infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="6dff6-124">Infrastructure role name.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6dff6-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6dff6-125">-NoWait</span></span>
<span data-ttu-id="6dff6-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="6dff6-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6dff6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dff6-127">-PassThru</span></span>
<span data-ttu-id="6dff6-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="6dff6-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6dff6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dff6-129">-ResourceGroupName</span></span>
<span data-ttu-id="6dff6-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6dff6-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6dff6-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6dff6-131">-SubscriptionId</span></span>
<span data-ttu-id="6dff6-132">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6dff6-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6dff6-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6dff6-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6dff6-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6dff6-134">-Confirm</span></span>
<span data-ttu-id="6dff6-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6dff6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dff6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dff6-136">-WhatIf</span></span>
<span data-ttu-id="6dff6-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6dff6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dff6-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6dff6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dff6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dff6-139">CommonParameters</span></span>
<span data-ttu-id="6dff6-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dff6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dff6-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dff6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dff6-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6dff6-142">INPUTS</span></span>

### <span data-ttu-id="6dff6-143">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6dff6-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="6dff6-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6dff6-144">OUTPUTS</span></span>

### <span data-ttu-id="6dff6-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6dff6-145">System.Boolean</span></span>



## <span data-ttu-id="6dff6-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6dff6-146">NOTES</span></span>

<span data-ttu-id="6dff6-147">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6dff6-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6dff6-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6dff6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6dff6-149">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="6dff6-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6dff6-150">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="6dff6-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="6dff6-151">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="6dff6-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="6dff6-152">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="6dff6-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="6dff6-153">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="6dff6-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="6dff6-154">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="6dff6-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="6dff6-155">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="6dff6-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="6dff6-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="6dff6-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6dff6-157">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="6dff6-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="6dff6-158">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="6dff6-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="6dff6-159">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="6dff6-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6dff6-160">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="6dff6-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="6dff6-161">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="6dff6-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="6dff6-162">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="6dff6-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="6dff6-163">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="6dff6-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="6dff6-164">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6dff6-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="6dff6-165">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="6dff6-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="6dff6-166">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="6dff6-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="6dff6-167">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="6dff6-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="6dff6-168">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="6dff6-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="6dff6-169">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="6dff6-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="6dff6-170">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6dff6-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6dff6-171">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6dff6-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6dff6-172">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="6dff6-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="6dff6-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6dff6-173">RELATED LINKS</span></span>

