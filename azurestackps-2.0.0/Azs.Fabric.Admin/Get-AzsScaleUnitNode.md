---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d1534c7cfacbcc70c2fe822676d67142401f9ff9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923181"
---
# <span data-ttu-id="fbf56-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="fbf56-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="fbf56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fbf56-102">SYNOPSIS</span></span>


## <span data-ttu-id="fbf56-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fbf56-103">SYNTAX</span></span>

### <span data-ttu-id="fbf56-104">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="fbf56-104">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="fbf56-105">Lära</span><span class="sxs-lookup"><span data-stu-id="fbf56-105">Get</span></span>
```
Get-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="fbf56-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fbf56-106">GetViaIdentity</span></span>
```
Get-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="fbf56-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fbf56-107">DESCRIPTION</span></span>


## <span data-ttu-id="fbf56-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fbf56-108">EXAMPLES</span></span>

### <span data-ttu-id="fbf56-109">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="fbf56-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode

A list of all scale unit nodes at a location.
```

<span data-ttu-id="fbf56-110">Hämta alla enheter för mått enhet på en plats.</span><span class="sxs-lookup"><span data-stu-id="fbf56-110">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="fbf56-111">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="fbf56-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode -Name "HC1n25r2231"

A specific scale unit node at a location given a name.
```

<span data-ttu-id="fbf56-112">Skaffa en särskild nod för Scale Unit på en plats med ett namn.</span><span class="sxs-lookup"><span data-stu-id="fbf56-112">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="fbf56-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fbf56-113">PARAMETERS</span></span>

### <span data-ttu-id="fbf56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf56-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="fbf56-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="fbf56-115">-Filter</span></span>


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

### <span data-ttu-id="fbf56-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbf56-116">-InputObject</span></span>
<span data-ttu-id="fbf56-117">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="fbf56-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fbf56-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="fbf56-118">-Location</span></span>


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

### <span data-ttu-id="fbf56-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="fbf56-119">-Name</span></span>


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

### <span data-ttu-id="fbf56-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbf56-120">-PassThru</span></span>


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

### <span data-ttu-id="fbf56-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf56-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="fbf56-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fbf56-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="fbf56-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf56-123">CommonParameters</span></span>
<span data-ttu-id="fbf56-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbf56-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf56-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbf56-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf56-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fbf56-126">INPUTS</span></span>

### <span data-ttu-id="fbf56-127">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="fbf56-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="fbf56-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fbf56-128">OUTPUTS</span></span>

### <span data-ttu-id="fbf56-129">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="fbf56-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnitNode</span></span>



## <span data-ttu-id="fbf56-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fbf56-130">NOTES</span></span>

<span data-ttu-id="fbf56-131">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="fbf56-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fbf56-132">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fbf56-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fbf56-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="fbf56-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="fbf56-134">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="fbf56-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="fbf56-135">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="fbf56-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="fbf56-136">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="fbf56-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="fbf56-137">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="fbf56-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="fbf56-138">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="fbf56-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="fbf56-139">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="fbf56-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="fbf56-140">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="fbf56-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fbf56-141">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="fbf56-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="fbf56-142">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="fbf56-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="fbf56-143">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="fbf56-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="fbf56-144">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="fbf56-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="fbf56-145">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="fbf56-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="fbf56-146">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="fbf56-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="fbf56-147">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="fbf56-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="fbf56-148">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fbf56-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="fbf56-149">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="fbf56-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="fbf56-150">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="fbf56-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="fbf56-151">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="fbf56-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="fbf56-152">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="fbf56-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="fbf56-153">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="fbf56-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fbf56-154">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="fbf56-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="fbf56-155">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="fbf56-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="fbf56-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fbf56-156">RELATED LINKS</span></span>

