---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092935"
---
# <span data-ttu-id="f31eb-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="f31eb-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="f31eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f31eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f31eb-103">Stänga av en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="f31eb-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="f31eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f31eb-104">SYNTAX</span></span>

### <span data-ttu-id="f31eb-105">PowerOff (standard)</span><span class="sxs-lookup"><span data-stu-id="f31eb-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f31eb-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f31eb-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f31eb-107">Stopp</span><span class="sxs-lookup"><span data-stu-id="f31eb-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f31eb-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f31eb-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f31eb-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f31eb-109">DESCRIPTION</span></span>
<span data-ttu-id="f31eb-110">Stänga av en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="f31eb-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="f31eb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f31eb-111">EXAMPLES</span></span>

### <span data-ttu-id="f31eb-112">Exempel 1: {{lägga till rubrik här}}</span><span class="sxs-lookup"><span data-stu-id="f31eb-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="f31eb-113">Stänga av en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="f31eb-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="f31eb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f31eb-114">PARAMETERS</span></span>

### <span data-ttu-id="f31eb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f31eb-115">-AsJob</span></span>
<span data-ttu-id="f31eb-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="f31eb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f31eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31eb-117">-DefaultProfile</span></span>
<span data-ttu-id="f31eb-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f31eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f31eb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f31eb-119">-Force</span></span>
<span data-ttu-id="f31eb-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f31eb-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f31eb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f31eb-121">-InputObject</span></span>
<span data-ttu-id="f31eb-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f31eb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity, ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f31eb-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="f31eb-123">-Location</span></span>
<span data-ttu-id="f31eb-124">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="f31eb-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f31eb-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="f31eb-125">-Name</span></span>
<span data-ttu-id="f31eb-126">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="f31eb-126">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f31eb-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f31eb-127">-NoWait</span></span>
<span data-ttu-id="f31eb-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="f31eb-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f31eb-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f31eb-129">-PassThru</span></span>
<span data-ttu-id="f31eb-130">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="f31eb-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f31eb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f31eb-131">-ResourceGroupName</span></span>
<span data-ttu-id="f31eb-132">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="f31eb-132">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f31eb-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f31eb-133">-SubscriptionId</span></span>
<span data-ttu-id="f31eb-134">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f31eb-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f31eb-135">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f31eb-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f31eb-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f31eb-136">-Confirm</span></span>
<span data-ttu-id="f31eb-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f31eb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f31eb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f31eb-138">-WhatIf</span></span>
<span data-ttu-id="f31eb-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f31eb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f31eb-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f31eb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f31eb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31eb-141">CommonParameters</span></span>
<span data-ttu-id="f31eb-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f31eb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31eb-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f31eb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31eb-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f31eb-144">INPUTS</span></span>

### <span data-ttu-id="f31eb-145">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f31eb-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="f31eb-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f31eb-146">OUTPUTS</span></span>

### <span data-ttu-id="f31eb-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f31eb-147">System.Boolean</span></span>



## <span data-ttu-id="f31eb-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f31eb-148">NOTES</span></span>

<span data-ttu-id="f31eb-149">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="f31eb-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f31eb-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f31eb-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f31eb-151">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f31eb-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f31eb-152">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="f31eb-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="f31eb-153">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="f31eb-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="f31eb-154">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="f31eb-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="f31eb-155">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="f31eb-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="f31eb-156">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="f31eb-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="f31eb-157">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="f31eb-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="f31eb-158">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f31eb-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f31eb-159">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="f31eb-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="f31eb-160">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="f31eb-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="f31eb-161">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="f31eb-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="f31eb-162">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="f31eb-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="f31eb-163">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="f31eb-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="f31eb-164">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="f31eb-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="f31eb-165">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="f31eb-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="f31eb-166">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f31eb-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f31eb-167">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="f31eb-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="f31eb-168">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="f31eb-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="f31eb-169">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="f31eb-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="f31eb-170">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="f31eb-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="f31eb-171">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="f31eb-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="f31eb-172">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f31eb-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f31eb-173">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f31eb-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f31eb-174">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="f31eb-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="f31eb-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f31eb-175">RELATED LINKS</span></span>

