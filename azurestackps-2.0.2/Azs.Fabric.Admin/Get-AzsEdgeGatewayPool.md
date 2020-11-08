---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099856"
---
# <span data-ttu-id="dc0d3-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="dc0d3-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="dc0d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc0d3-102">SYNOPSIS</span></span>


## <span data-ttu-id="dc0d3-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc0d3-103">SYNTAX</span></span>

### <span data-ttu-id="dc0d3-104">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="dc0d3-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="dc0d3-105">Lära</span><span class="sxs-lookup"><span data-stu-id="dc0d3-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="dc0d3-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc0d3-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="dc0d3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc0d3-107">DESCRIPTION</span></span>


## <span data-ttu-id="dc0d3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc0d3-108">EXAMPLES</span></span>

### <span data-ttu-id="dc0d3-109">Exempel 1: Hämta en lista över alla yttre Gateway-pooler.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="dc0d3-110">Få en lista över alla yttre Gateway-pooler.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="dc0d3-111">Exempel 2: Hämta en specifik pool med Gateway.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="dc0d3-112">Skaffa en specifik pool för gateway.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="dc0d3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc0d3-113">PARAMETERS</span></span>

### <span data-ttu-id="dc0d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0d3-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="dc0d3-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="dc0d3-115">-Filter</span></span>


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

### <span data-ttu-id="dc0d3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc0d3-116">-InputObject</span></span>
<span data-ttu-id="dc0d3-117">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc0d3-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="dc0d3-118">-Location</span></span>


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

### <span data-ttu-id="dc0d3-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc0d3-119">-Name</span></span>


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

### <span data-ttu-id="dc0d3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc0d3-120">-PassThru</span></span>


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

### <span data-ttu-id="dc0d3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0d3-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="dc0d3-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc0d3-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="dc0d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0d3-123">CommonParameters</span></span>
<span data-ttu-id="dc0d3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0d3-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc0d3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0d3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc0d3-126">INPUTS</span></span>

### <span data-ttu-id="dc0d3-127">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="dc0d3-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="dc0d3-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc0d3-128">OUTPUTS</span></span>

### <span data-ttu-id="dc0d3-129">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="dc0d3-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="dc0d3-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc0d3-130">NOTES</span></span>

<span data-ttu-id="dc0d3-131">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc0d3-132">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dc0d3-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="dc0d3-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="dc0d3-134">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="dc0d3-135">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="dc0d3-136">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="dc0d3-137">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="dc0d3-138">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="dc0d3-139">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="dc0d3-140">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="dc0d3-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc0d3-141">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="dc0d3-142">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="dc0d3-143">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="dc0d3-144">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="dc0d3-145">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="dc0d3-146">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="dc0d3-147">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="dc0d3-148">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="dc0d3-149">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="dc0d3-150">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="dc0d3-151">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="dc0d3-152">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="dc0d3-153">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dc0d3-154">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dc0d3-155">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="dc0d3-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="dc0d3-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc0d3-156">RELATED LINKS</span></span>

