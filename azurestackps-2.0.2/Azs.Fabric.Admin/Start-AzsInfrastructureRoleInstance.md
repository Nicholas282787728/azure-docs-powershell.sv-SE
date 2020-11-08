---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/start-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 922aea432548557857b627696e156c75a8e46157
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100329"
---
# <span data-ttu-id="bc483-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="bc483-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="bc483-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc483-102">SYNOPSIS</span></span>
<span data-ttu-id="bc483-103">Koppla en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="bc483-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="bc483-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc483-104">SYNTAX</span></span>

### <span data-ttu-id="bc483-105">PowerOn (standard)</span><span class="sxs-lookup"><span data-stu-id="bc483-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bc483-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc483-106">PowerOnViaIdentity</span></span>
```
Start-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bc483-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc483-107">DESCRIPTION</span></span>
<span data-ttu-id="bc483-108">Koppla en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="bc483-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="bc483-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc483-109">EXAMPLES</span></span>

### <span data-ttu-id="bc483-110">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="bc483-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="bc483-111">Koppla en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="bc483-111">Power on an infrastructure role instance.</span></span>


## <span data-ttu-id="bc483-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc483-112">PARAMETERS</span></span>

### <span data-ttu-id="bc483-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc483-113">-AsJob</span></span>
<span data-ttu-id="bc483-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="bc483-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="bc483-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc483-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="bc483-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bc483-116">-Force</span></span>
<span data-ttu-id="bc483-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bc483-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="bc483-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc483-118">-InputObject</span></span>
<span data-ttu-id="bc483-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="bc483-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc483-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="bc483-120">-Location</span></span>
<span data-ttu-id="bc483-121">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="bc483-121">Location of the resource.</span></span>

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

### <span data-ttu-id="bc483-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="bc483-122">-Name</span></span>
<span data-ttu-id="bc483-123">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="bc483-123">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="bc483-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bc483-124">-NoWait</span></span>
<span data-ttu-id="bc483-125">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="bc483-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bc483-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc483-126">-PassThru</span></span>
<span data-ttu-id="bc483-127">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="bc483-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bc483-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc483-128">-ResourceGroupName</span></span>
<span data-ttu-id="bc483-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bc483-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="bc483-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc483-130">-SubscriptionId</span></span>
<span data-ttu-id="bc483-131">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="bc483-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bc483-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="bc483-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bc483-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bc483-133">-Confirm</span></span>
<span data-ttu-id="bc483-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bc483-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc483-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc483-135">-WhatIf</span></span>
<span data-ttu-id="bc483-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bc483-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc483-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bc483-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc483-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc483-138">CommonParameters</span></span>
<span data-ttu-id="bc483-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc483-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc483-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc483-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc483-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc483-141">INPUTS</span></span>

### <span data-ttu-id="bc483-142">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="bc483-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="bc483-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc483-143">OUTPUTS</span></span>

### <span data-ttu-id="bc483-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc483-144">System.Boolean</span></span>



## <span data-ttu-id="bc483-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc483-145">NOTES</span></span>

<span data-ttu-id="bc483-146">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="bc483-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc483-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc483-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="bc483-148">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="bc483-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc483-149">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="bc483-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="bc483-150">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="bc483-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="bc483-151">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="bc483-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="bc483-152">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="bc483-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="bc483-153">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="bc483-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="bc483-154">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="bc483-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="bc483-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="bc483-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc483-156">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="bc483-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="bc483-157">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="bc483-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="bc483-158">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="bc483-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="bc483-159">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="bc483-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="bc483-160">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="bc483-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="bc483-161">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="bc483-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="bc483-162">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="bc483-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="bc483-163">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="bc483-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="bc483-164">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="bc483-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="bc483-165">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="bc483-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="bc483-166">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="bc483-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="bc483-167">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="bc483-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="bc483-168">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="bc483-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="bc483-169">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="bc483-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bc483-170">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="bc483-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="bc483-171">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="bc483-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="bc483-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc483-172">RELATED LINKS</span></span>

