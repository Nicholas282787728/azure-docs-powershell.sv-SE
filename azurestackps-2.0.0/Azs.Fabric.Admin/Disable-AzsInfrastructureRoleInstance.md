---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: d6bb118a6b7699672209618e1409fe6a9bed466d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923217"
---
# <span data-ttu-id="70c7f-101">Disable-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="70c7f-101">Disable-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="70c7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70c7f-102">SYNOPSIS</span></span>


## <span data-ttu-id="70c7f-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70c7f-103">SYNTAX</span></span>

### <span data-ttu-id="70c7f-104">Shutdown (standard)</span><span class="sxs-lookup"><span data-stu-id="70c7f-104">Shutdown (Default)</span></span>
```
Disable-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="70c7f-105">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="70c7f-105">ShutdownViaIdentity</span></span>
```
Disable-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="70c7f-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70c7f-106">DESCRIPTION</span></span>
<span data-ttu-id="70c7f-107">Stäng av en infrastruktur roll instans för underhåll.</span><span class="sxs-lookup"><span data-stu-id="70c7f-107">Shutdown an infrastructure role instance for maintenance.</span></span>

## <span data-ttu-id="70c7f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70c7f-108">EXAMPLES</span></span>

### <span data-ttu-id="70c7f-109">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="70c7f-109">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsInfrastructureRoleInstance -Name "n22r0903-Xrp03"

Shutdown an infrastructure role instance for maintenance.
```

<span data-ttu-id="70c7f-110">Stäng av en infrastruktur roll instans för underhåll.</span><span class="sxs-lookup"><span data-stu-id="70c7f-110">Shutdown an infrastructure role instance for maintenance.</span></span>


## <span data-ttu-id="70c7f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70c7f-111">PARAMETERS</span></span>

### <span data-ttu-id="70c7f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70c7f-112">-AsJob</span></span>
<span data-ttu-id="70c7f-113">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="70c7f-113">Run the command as a job</span></span>

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

### <span data-ttu-id="70c7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c7f-114">-DefaultProfile</span></span>
<span data-ttu-id="70c7f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70c7f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70c7f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="70c7f-116">-Force</span></span>
<span data-ttu-id="70c7f-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="70c7f-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="70c7f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70c7f-118">-InputObject</span></span>
<span data-ttu-id="70c7f-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="70c7f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="70c7f-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="70c7f-120">-Location</span></span>
<span data-ttu-id="70c7f-121">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="70c7f-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="70c7f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="70c7f-122">-Name</span></span>
<span data-ttu-id="70c7f-123">Namn på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="70c7f-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="70c7f-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="70c7f-124">-NoWait</span></span>
<span data-ttu-id="70c7f-125">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="70c7f-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="70c7f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70c7f-126">-PassThru</span></span>
<span data-ttu-id="70c7f-127">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="70c7f-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="70c7f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c7f-128">-ResourceGroupName</span></span>
<span data-ttu-id="70c7f-129">Resurs grupp där resurs leverantören har registrerats.</span><span class="sxs-lookup"><span data-stu-id="70c7f-129">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="70c7f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70c7f-130">-SubscriptionId</span></span>
<span data-ttu-id="70c7f-131">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="70c7f-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="70c7f-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="70c7f-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="70c7f-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70c7f-133">-Confirm</span></span>
<span data-ttu-id="70c7f-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70c7f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c7f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c7f-135">-WhatIf</span></span>
<span data-ttu-id="70c7f-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70c7f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c7f-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70c7f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c7f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c7f-138">CommonParameters</span></span>
<span data-ttu-id="70c7f-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70c7f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c7f-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70c7f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c7f-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70c7f-141">INPUTS</span></span>

### <span data-ttu-id="70c7f-142">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="70c7f-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="70c7f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70c7f-143">OUTPUTS</span></span>

### <span data-ttu-id="70c7f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70c7f-144">System.Boolean</span></span>



## <span data-ttu-id="70c7f-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70c7f-145">NOTES</span></span>

<span data-ttu-id="70c7f-146">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="70c7f-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70c7f-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="70c7f-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="70c7f-148">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="70c7f-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="70c7f-149">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="70c7f-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="70c7f-150">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="70c7f-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="70c7f-151">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="70c7f-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="70c7f-152">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="70c7f-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="70c7f-153">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="70c7f-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="70c7f-154">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="70c7f-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="70c7f-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="70c7f-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="70c7f-156">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="70c7f-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="70c7f-157">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="70c7f-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="70c7f-158">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="70c7f-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="70c7f-159">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="70c7f-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="70c7f-160">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="70c7f-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="70c7f-161">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="70c7f-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="70c7f-162">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="70c7f-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="70c7f-163">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="70c7f-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="70c7f-164">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="70c7f-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="70c7f-165">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="70c7f-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="70c7f-166">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="70c7f-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="70c7f-167">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="70c7f-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="70c7f-168">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="70c7f-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="70c7f-169">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="70c7f-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="70c7f-170">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="70c7f-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="70c7f-171">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="70c7f-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="70c7f-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70c7f-172">RELATED LINKS</span></span>

