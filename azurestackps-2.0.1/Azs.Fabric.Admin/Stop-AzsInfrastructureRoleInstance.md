---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 07751ba4228faa578e4181ec481eef6e5b033126
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092922"
---
# <span data-ttu-id="a9a2f-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a9a2f-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="a9a2f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a2f-103">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="a9a2f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9a2f-104">SYNTAX</span></span>

### <span data-ttu-id="a9a2f-105">PowerOff (standard)</span><span class="sxs-lookup"><span data-stu-id="a9a2f-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a9a2f-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9a2f-106">PowerOffViaIdentity</span></span>
```
Stop-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a9a2f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9a2f-107">DESCRIPTION</span></span>
<span data-ttu-id="a9a2f-108">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="a9a2f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9a2f-109">EXAMPLES</span></span>

### <span data-ttu-id="a9a2f-110">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="a9a2f-110">Example 1:</span></span> 
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="a9a2f-111">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="a9a2f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9a2f-112">PARAMETERS</span></span>

### <span data-ttu-id="a9a2f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9a2f-113">-AsJob</span></span>
<span data-ttu-id="a9a2f-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="a9a2f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a9a2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a2f-115">-DefaultProfile</span></span>
<span data-ttu-id="a9a2f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9a2f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a9a2f-117">-Force</span></span>
<span data-ttu-id="a9a2f-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a9a2f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9a2f-119">-InputObject</span></span>
<span data-ttu-id="a9a2f-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a9a2f-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="a9a2f-121">-Location</span></span>
<span data-ttu-id="a9a2f-122">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a9a2f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9a2f-123">-Name</span></span>
<span data-ttu-id="a9a2f-124">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-124">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a9a2f-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a9a2f-125">-NoWait</span></span>
<span data-ttu-id="a9a2f-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="a9a2f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a9a2f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9a2f-127">-PassThru</span></span>
<span data-ttu-id="a9a2f-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="a9a2f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a9a2f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a2f-129">-ResourceGroupName</span></span>
<span data-ttu-id="a9a2f-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a9a2f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9a2f-131">-SubscriptionId</span></span>
<span data-ttu-id="a9a2f-132">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a9a2f-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-133">The subscription ID forms part of the URI for every service call.</span></span>


```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a9a2f-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9a2f-134">-Confirm</span></span>
<span data-ttu-id="a9a2f-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9a2f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a2f-136">-WhatIf</span></span>
<span data-ttu-id="a9a2f-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9a2f-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9a2f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a2f-139">CommonParameters</span></span>
<span data-ttu-id="a9a2f-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a2f-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9a2f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a2f-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9a2f-142">INPUTS</span></span>

### <span data-ttu-id="a9a2f-143">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a9a2f-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="a9a2f-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9a2f-144">OUTPUTS</span></span>

### <span data-ttu-id="a9a2f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9a2f-145">System.Boolean</span></span>



## <span data-ttu-id="a9a2f-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9a2f-146">NOTES</span></span>

<span data-ttu-id="a9a2f-147">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9a2f-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a9a2f-149">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="a9a2f-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9a2f-150">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="a9a2f-151">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="a9a2f-152">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="a9a2f-153">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="a9a2f-154">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="a9a2f-155">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="a9a2f-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="a9a2f-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9a2f-157">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="a9a2f-158">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="a9a2f-159">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a9a2f-160">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="a9a2f-161">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="a9a2f-162">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="a9a2f-163">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="a9a2f-164">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a9a2f-165">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="a9a2f-166">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="a9a2f-167">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="a9a2f-168">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="a9a2f-169">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="a9a2f-170">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a9a2f-171">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a9a2f-172">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="a9a2f-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="a9a2f-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9a2f-173">RELATED LINKS</span></span>

