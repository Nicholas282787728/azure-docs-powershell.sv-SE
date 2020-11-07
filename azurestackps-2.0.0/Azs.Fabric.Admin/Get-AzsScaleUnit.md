---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunit
schema: 2.0.0
ms.openlocfilehash: cef23066fe1bfcd0b428302aab6c8077a8f676b6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925370"
---
# <span data-ttu-id="8e7b7-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="8e7b7-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="8e7b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e7b7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7b7-103">Returnerar den begärda skalnings enheten.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-103">Returns the requested scale unit.</span></span>

## <span data-ttu-id="8e7b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e7b7-104">SYNTAX</span></span>

### <span data-ttu-id="8e7b7-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8e7b7-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8e7b7-106">Lära</span><span class="sxs-lookup"><span data-stu-id="8e7b7-106">Get</span></span>
```
Get-AzsScaleUnit -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8e7b7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e7b7-107">GetViaIdentity</span></span>
```
Get-AzsScaleUnit -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="8e7b7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e7b7-108">DESCRIPTION</span></span>
<span data-ttu-id="8e7b7-109">Returnerar den begärda skalnings enheten.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-109">Returns the requested scale unit.</span></span>

## <span data-ttu-id="8e7b7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e7b7-110">EXAMPLES</span></span>

### <span data-ttu-id="8e7b7-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="8e7b7-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnit

A list of information about scale units.
```

<span data-ttu-id="8e7b7-112">Returnera en lista med information om skalnings enheter.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="8e7b7-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="8e7b7-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnit -Name "S-Cluster"

The information about a specific scale unit.
```

<span data-ttu-id="8e7b7-114">Returnera information om en viss enhet.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="8e7b7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e7b7-115">PARAMETERS</span></span>

### <span data-ttu-id="8e7b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7b7-116">-DefaultProfile</span></span>
<span data-ttu-id="8e7b7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e7b7-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="8e7b7-118">-Filter</span></span>
<span data-ttu-id="8e7b7-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="8e7b7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e7b7-120">-InputObject</span></span>
<span data-ttu-id="8e7b7-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8e7b7-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="8e7b7-122">-Location</span></span>
<span data-ttu-id="8e7b7-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-123">Location of the resource.</span></span>

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

### <span data-ttu-id="8e7b7-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e7b7-124">-Name</span></span>
<span data-ttu-id="8e7b7-125">Namnet på enheten.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-125">Name of the scale units.</span></span>

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

### <span data-ttu-id="8e7b7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e7b7-126">-PassThru</span></span>
<span data-ttu-id="8e7b7-127">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="8e7b7-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8e7b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e7b7-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="8e7b7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e7b7-130">-SubscriptionId</span></span>
<span data-ttu-id="8e7b7-131">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8e7b7-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-132">The subscription ID forms part of the URI for every service call.</span></span>


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

### <span data-ttu-id="8e7b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7b7-133">CommonParameters</span></span>
<span data-ttu-id="8e7b7-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7b7-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e7b7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7b7-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e7b7-136">INPUTS</span></span>

### <span data-ttu-id="8e7b7-137">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8e7b7-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="8e7b7-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e7b7-138">OUTPUTS</span></span>

### <span data-ttu-id="8e7b7-139">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IScaleUnit</span><span class="sxs-lookup"><span data-stu-id="8e7b7-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnit</span></span>



## <span data-ttu-id="8e7b7-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e7b7-140">NOTES</span></span>

<span data-ttu-id="8e7b7-141">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e7b7-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8e7b7-143">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8e7b7-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e7b7-144">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="8e7b7-145">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="8e7b7-146">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="8e7b7-147">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="8e7b7-148">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="8e7b7-149">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="8e7b7-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8e7b7-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e7b7-151">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="8e7b7-152">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="8e7b7-153">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8e7b7-154">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="8e7b7-155">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="8e7b7-156">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="8e7b7-157">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="8e7b7-158">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8e7b7-159">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="8e7b7-160">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="8e7b7-161">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="8e7b7-162">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="8e7b7-163">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="8e7b7-164">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8e7b7-165">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8e7b7-166">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="8e7b7-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="8e7b7-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e7b7-167">RELATED LINKS</span></span>

