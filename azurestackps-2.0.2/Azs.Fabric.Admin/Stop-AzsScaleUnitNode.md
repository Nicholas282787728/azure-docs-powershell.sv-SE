---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 3f5adef6382038fdaf8c17620508b4a450ff74bc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100039"
---
# <span data-ttu-id="98fcc-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="98fcc-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="98fcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="98fcc-103">Stänga av en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="98fcc-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="98fcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98fcc-104">SYNTAX</span></span>

### <span data-ttu-id="98fcc-105">PowerOff (standard)</span><span class="sxs-lookup"><span data-stu-id="98fcc-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="98fcc-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="98fcc-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="98fcc-107">Stopp</span><span class="sxs-lookup"><span data-stu-id="98fcc-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="98fcc-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="98fcc-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="98fcc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98fcc-109">DESCRIPTION</span></span>
<span data-ttu-id="98fcc-110">Stänga av en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="98fcc-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="98fcc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98fcc-111">EXAMPLES</span></span>

### <span data-ttu-id="98fcc-112">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="98fcc-112">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="98fcc-113">Stänga av en nod för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="98fcc-113">Power down a scale unit node.</span></span>

### <span data-ttu-id="98fcc-114">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="98fcc-114">Example 2:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="98fcc-115">Stänga av en nod för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="98fcc-115">Power down a scale unit node.</span></span> <span data-ttu-id="98fcc-116">Som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="98fcc-116">As a job.</span></span>

## <span data-ttu-id="98fcc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98fcc-117">PARAMETERS</span></span>

### <span data-ttu-id="98fcc-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98fcc-118">-AsJob</span></span>
<span data-ttu-id="98fcc-119">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="98fcc-119">Run the command as a job</span></span>

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

### <span data-ttu-id="98fcc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98fcc-120">-DefaultProfile</span></span>
<span data-ttu-id="98fcc-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98fcc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98fcc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="98fcc-122">-Force</span></span>
<span data-ttu-id="98fcc-123">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="98fcc-123">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="98fcc-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98fcc-124">-InputObject</span></span>
<span data-ttu-id="98fcc-125">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="98fcc-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="98fcc-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="98fcc-126">-Location</span></span>
<span data-ttu-id="98fcc-127">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="98fcc-127">Location of the resource.</span></span>

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

### <span data-ttu-id="98fcc-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="98fcc-128">-Name</span></span>
<span data-ttu-id="98fcc-129">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="98fcc-129">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="98fcc-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="98fcc-130">-NoWait</span></span>
<span data-ttu-id="98fcc-131">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="98fcc-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="98fcc-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98fcc-132">-PassThru</span></span>
<span data-ttu-id="98fcc-133">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="98fcc-133">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="98fcc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98fcc-134">-ResourceGroupName</span></span>
<span data-ttu-id="98fcc-135">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="98fcc-135">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="98fcc-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98fcc-136">-SubscriptionId</span></span>
<span data-ttu-id="98fcc-137">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="98fcc-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="98fcc-138">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="98fcc-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="98fcc-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98fcc-139">-Confirm</span></span>
<span data-ttu-id="98fcc-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98fcc-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98fcc-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98fcc-141">-WhatIf</span></span>
<span data-ttu-id="98fcc-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98fcc-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98fcc-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="98fcc-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98fcc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fcc-144">CommonParameters</span></span>
<span data-ttu-id="98fcc-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98fcc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fcc-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98fcc-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fcc-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98fcc-147">INPUTS</span></span>

### <span data-ttu-id="98fcc-148">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="98fcc-148">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="98fcc-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98fcc-149">OUTPUTS</span></span>

### <span data-ttu-id="98fcc-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98fcc-150">System.Boolean</span></span>

## <span data-ttu-id="98fcc-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98fcc-151">NOTES</span></span>

<span data-ttu-id="98fcc-152">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="98fcc-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="98fcc-153">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="98fcc-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="98fcc-154">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="98fcc-154">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="98fcc-155">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="98fcc-155">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="98fcc-156">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="98fcc-156">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="98fcc-157">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="98fcc-157">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="98fcc-158">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="98fcc-158">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="98fcc-159">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="98fcc-159">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="98fcc-160">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="98fcc-160">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="98fcc-161">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="98fcc-161">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="98fcc-162">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="98fcc-162">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="98fcc-163">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="98fcc-163">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="98fcc-164">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="98fcc-164">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="98fcc-165">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="98fcc-165">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="98fcc-166">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="98fcc-166">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="98fcc-167">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="98fcc-167">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="98fcc-168">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="98fcc-168">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="98fcc-169">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="98fcc-169">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="98fcc-170">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="98fcc-170">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="98fcc-171">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="98fcc-171">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="98fcc-172">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="98fcc-172">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="98fcc-173">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="98fcc-173">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="98fcc-174">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="98fcc-174">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="98fcc-175">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="98fcc-175">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="98fcc-176">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="98fcc-176">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="98fcc-177">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="98fcc-177">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="98fcc-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98fcc-178">RELATED LINKS</span></span>
