---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: c8b1ed8ea0be65e92022cf1ac759024a07fc76c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099928"
---
# <span data-ttu-id="3d67d-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="3d67d-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="3d67d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d67d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d67d-103">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3d67d-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="3d67d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d67d-104">SYNTAX</span></span>

### <span data-ttu-id="3d67d-105">PowerOn (standard)</span><span class="sxs-lookup"><span data-stu-id="3d67d-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3d67d-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d67d-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d67d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d67d-107">DESCRIPTION</span></span>
<span data-ttu-id="3d67d-108">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3d67d-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="3d67d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d67d-109">EXAMPLES</span></span>

### <span data-ttu-id="3d67d-110">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="3d67d-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="3d67d-111">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3d67d-111">Power on a scale unit node.</span></span>

### <span data-ttu-id="3d67d-112">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="3d67d-112">Example 2:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="3d67d-113">Power on a-noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3d67d-113">Power on a scale unit node.</span></span> <span data-ttu-id="3d67d-114">Som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="3d67d-114">As a job.</span></span>

## <span data-ttu-id="3d67d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d67d-115">PARAMETERS</span></span>

### <span data-ttu-id="3d67d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d67d-116">-AsJob</span></span>
<span data-ttu-id="3d67d-117">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="3d67d-117">Run the command as a job</span></span>

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

### <span data-ttu-id="3d67d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d67d-118">-DefaultProfile</span></span>
<span data-ttu-id="3d67d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d67d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d67d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3d67d-120">-Force</span></span>
<span data-ttu-id="3d67d-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3d67d-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3d67d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d67d-122">-InputObject</span></span>
<span data-ttu-id="3d67d-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3d67d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOnViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3d67d-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="3d67d-124">-Location</span></span>
<span data-ttu-id="3d67d-125">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="3d67d-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3d67d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d67d-126">-Name</span></span>
<span data-ttu-id="3d67d-127">Namn på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3d67d-127">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3d67d-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3d67d-128">-NoWait</span></span>
<span data-ttu-id="3d67d-129">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="3d67d-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3d67d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d67d-130">-PassThru</span></span>
<span data-ttu-id="3d67d-131">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="3d67d-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3d67d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d67d-132">-ResourceGroupName</span></span>
<span data-ttu-id="3d67d-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d67d-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3d67d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d67d-134">-SubscriptionId</span></span>
<span data-ttu-id="3d67d-135">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3d67d-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3d67d-136">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3d67d-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3d67d-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d67d-137">-Confirm</span></span>
<span data-ttu-id="3d67d-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d67d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d67d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d67d-139">-WhatIf</span></span>
<span data-ttu-id="3d67d-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d67d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d67d-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d67d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d67d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d67d-142">CommonParameters</span></span>
<span data-ttu-id="3d67d-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d67d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d67d-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d67d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d67d-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d67d-145">INPUTS</span></span>

### <span data-ttu-id="3d67d-146">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3d67d-146">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="3d67d-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d67d-147">OUTPUTS</span></span>

### <span data-ttu-id="3d67d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d67d-148">System.Boolean</span></span>

## <span data-ttu-id="3d67d-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d67d-149">NOTES</span></span>

<span data-ttu-id="3d67d-150">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3d67d-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d67d-151">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d67d-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3d67d-152">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3d67d-152">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d67d-153">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="3d67d-153">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="3d67d-154">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="3d67d-154">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="3d67d-155">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="3d67d-155">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="3d67d-156">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="3d67d-156">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="3d67d-157">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="3d67d-157">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="3d67d-158">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="3d67d-158">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="3d67d-159">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3d67d-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d67d-160">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="3d67d-160">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="3d67d-161">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="3d67d-161">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="3d67d-162">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="3d67d-162">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3d67d-163">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="3d67d-163">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="3d67d-164">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="3d67d-164">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="3d67d-165">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="3d67d-165">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="3d67d-166">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="3d67d-166">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="3d67d-167">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3d67d-167">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3d67d-168">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="3d67d-168">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="3d67d-169">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3d67d-169">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="3d67d-170">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="3d67d-170">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="3d67d-171">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="3d67d-171">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="3d67d-172">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="3d67d-172">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="3d67d-173">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3d67d-173">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3d67d-174">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3d67d-174">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3d67d-175">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="3d67d-175">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="3d67d-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d67d-176">RELATED LINKS</span></span>
