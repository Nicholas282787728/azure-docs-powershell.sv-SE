---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092994"
---
# <span data-ttu-id="4a17e-101">Get-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="4a17e-101">Get-AzsIPPool</span></span>

## <span data-ttu-id="4a17e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a17e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a17e-103">Returnera den begärda IP-poolen.</span><span class="sxs-lookup"><span data-stu-id="4a17e-103">Return the requested IP pool.</span></span>

## <span data-ttu-id="4a17e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a17e-104">SYNTAX</span></span>

### <span data-ttu-id="4a17e-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="4a17e-105">List (Default)</span></span>
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4a17e-106">Lära</span><span class="sxs-lookup"><span data-stu-id="4a17e-106">Get</span></span>
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4a17e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a17e-107">GetViaIdentity</span></span>
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4a17e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a17e-108">DESCRIPTION</span></span>
<span data-ttu-id="4a17e-109">Returnera den begärda IP-poolen.</span><span class="sxs-lookup"><span data-stu-id="4a17e-109">Return the requested IP pool.</span></span>

## <span data-ttu-id="4a17e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a17e-110">EXAMPLES</span></span>

### <span data-ttu-id="4a17e-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="4a17e-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

<span data-ttu-id="4a17e-112">Skaffa en IP-pool för alla infrastrukturer.</span><span class="sxs-lookup"><span data-stu-id="4a17e-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="4a17e-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="4a17e-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

<span data-ttu-id="4a17e-114">Skaffa en IP-adresspool för infrastruktur baserat på namn.</span><span class="sxs-lookup"><span data-stu-id="4a17e-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="4a17e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a17e-115">PARAMETERS</span></span>

### <span data-ttu-id="4a17e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a17e-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="4a17e-117">-Filter</span><span class="sxs-lookup"><span data-stu-id="4a17e-117">-Filter</span></span>
<span data-ttu-id="4a17e-118">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="4a17e-118">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a17e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a17e-119">-InputObject</span></span>
<span data-ttu-id="4a17e-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4a17e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4a17e-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="4a17e-121">-Location</span></span>
<span data-ttu-id="4a17e-122">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="4a17e-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a17e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a17e-123">-Name</span></span>
<span data-ttu-id="4a17e-124">IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="4a17e-124">IP pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a17e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a17e-125">-PassThru</span></span>
<span data-ttu-id="4a17e-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="4a17e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4a17e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a17e-127">-ResourceGroupName</span></span>
<span data-ttu-id="4a17e-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4a17e-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a17e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a17e-129">-SubscriptionId</span></span>
<span data-ttu-id="4a17e-130">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4a17e-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4a17e-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4a17e-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a17e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a17e-132">CommonParameters</span></span>
<span data-ttu-id="4a17e-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a17e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a17e-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a17e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a17e-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a17e-135">INPUTS</span></span>

### <span data-ttu-id="4a17e-136">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4a17e-136">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="4a17e-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a17e-137">OUTPUTS</span></span>

### <span data-ttu-id="4a17e-138">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="4a17e-138">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="4a17e-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a17e-139">NOTES</span></span>

<span data-ttu-id="4a17e-140">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="4a17e-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a17e-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a17e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4a17e-142">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="4a17e-142">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a17e-143">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="4a17e-143">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="4a17e-144">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="4a17e-144">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="4a17e-145">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="4a17e-145">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="4a17e-146">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="4a17e-146">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="4a17e-147">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="4a17e-147">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="4a17e-148">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="4a17e-148">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="4a17e-149">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4a17e-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a17e-150">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="4a17e-150">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="4a17e-151">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="4a17e-151">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="4a17e-152">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="4a17e-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4a17e-153">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="4a17e-153">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="4a17e-154">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="4a17e-154">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="4a17e-155">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="4a17e-155">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="4a17e-156">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="4a17e-156">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="4a17e-157">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4a17e-157">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4a17e-158">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="4a17e-158">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="4a17e-159">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="4a17e-159">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="4a17e-160">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="4a17e-160">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="4a17e-161">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="4a17e-161">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="4a17e-162">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="4a17e-162">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="4a17e-163">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4a17e-163">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4a17e-164">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4a17e-164">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4a17e-165">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="4a17e-165">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="4a17e-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a17e-166">RELATED LINKS</span></span>

