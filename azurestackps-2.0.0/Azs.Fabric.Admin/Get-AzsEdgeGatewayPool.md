---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923209"
---
# <span data-ttu-id="8a303-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="8a303-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="8a303-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a303-102">SYNOPSIS</span></span>


## <span data-ttu-id="8a303-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a303-103">SYNTAX</span></span>

### <span data-ttu-id="8a303-104">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8a303-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8a303-105">Lära</span><span class="sxs-lookup"><span data-stu-id="8a303-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="8a303-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a303-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="8a303-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a303-107">DESCRIPTION</span></span>


## <span data-ttu-id="8a303-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a303-108">EXAMPLES</span></span>

### <span data-ttu-id="8a303-109">Exempel 1: Hämta en lista över alla yttre Gateway-pooler.</span><span class="sxs-lookup"><span data-stu-id="8a303-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="8a303-110">Få en lista över alla yttre Gateway-pooler.</span><span class="sxs-lookup"><span data-stu-id="8a303-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="8a303-111">Exempel 2: Hämta en specifik pool med Gateway.</span><span class="sxs-lookup"><span data-stu-id="8a303-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="8a303-112">Skaffa en specifik pool för gateway.</span><span class="sxs-lookup"><span data-stu-id="8a303-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="8a303-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a303-113">PARAMETERS</span></span>

### <span data-ttu-id="8a303-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a303-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="8a303-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="8a303-115">-Filter</span></span>


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

### <span data-ttu-id="8a303-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a303-116">-InputObject</span></span>
<span data-ttu-id="8a303-117">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8a303-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8a303-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="8a303-118">-Location</span></span>


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

### <span data-ttu-id="8a303-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a303-119">-Name</span></span>


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

### <span data-ttu-id="8a303-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a303-120">-PassThru</span></span>


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

### <span data-ttu-id="8a303-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a303-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="8a303-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a303-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="8a303-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a303-123">CommonParameters</span></span>
<span data-ttu-id="8a303-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a303-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a303-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a303-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a303-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a303-126">INPUTS</span></span>

### <span data-ttu-id="8a303-127">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8a303-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="8a303-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a303-128">OUTPUTS</span></span>

### <span data-ttu-id="8a303-129">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="8a303-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="8a303-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a303-130">NOTES</span></span>

<span data-ttu-id="8a303-131">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8a303-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a303-132">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a303-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8a303-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="8a303-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="8a303-134">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="8a303-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="8a303-135">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="8a303-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="8a303-136">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="8a303-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="8a303-137">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="8a303-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="8a303-138">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="8a303-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="8a303-139">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="8a303-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="8a303-140">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8a303-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a303-141">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="8a303-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="8a303-142">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="8a303-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="8a303-143">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="8a303-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8a303-144">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="8a303-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="8a303-145">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="8a303-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="8a303-146">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="8a303-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="8a303-147">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="8a303-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="8a303-148">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8a303-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8a303-149">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="8a303-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="8a303-150">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="8a303-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="8a303-151">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="8a303-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="8a303-152">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="8a303-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="8a303-153">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8a303-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8a303-154">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="8a303-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8a303-155">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="8a303-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="8a303-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a303-156">RELATED LINKS</span></span>

