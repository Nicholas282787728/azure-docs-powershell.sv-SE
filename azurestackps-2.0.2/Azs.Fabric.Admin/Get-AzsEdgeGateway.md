---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099855"
---
# <span data-ttu-id="1c405-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="1c405-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="1c405-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c405-102">SYNOPSIS</span></span>
<span data-ttu-id="1c405-103">Returnerar den begärda gatewayen.</span><span class="sxs-lookup"><span data-stu-id="1c405-103">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="1c405-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c405-104">SYNTAX</span></span>

### <span data-ttu-id="1c405-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="1c405-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="1c405-106">Lära</span><span class="sxs-lookup"><span data-stu-id="1c405-106">Get</span></span>
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="1c405-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1c405-107">GetViaIdentity</span></span>
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="1c405-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c405-108">DESCRIPTION</span></span>
<span data-ttu-id="1c405-109">Returnerar den begärda gatewayen.</span><span class="sxs-lookup"><span data-stu-id="1c405-109">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="1c405-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c405-110">EXAMPLES</span></span>

### <span data-ttu-id="1c405-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="1c405-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

<span data-ttu-id="1c405-112">Returnerar listan över alla Edge-gateways på en viss plats.</span><span class="sxs-lookup"><span data-stu-id="1c405-112">Returns the list of all edge gateways at a certain location.</span></span>


## <span data-ttu-id="1c405-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c405-113">PARAMETERS</span></span>

### <span data-ttu-id="1c405-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c405-114">-DefaultProfile</span></span>
<span data-ttu-id="1c405-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c405-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c405-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="1c405-116">-Filter</span></span>
<span data-ttu-id="1c405-117">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="1c405-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="1c405-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c405-118">-InputObject</span></span>
<span data-ttu-id="1c405-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1c405-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c405-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="1c405-120">-Location</span></span>
<span data-ttu-id="1c405-121">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="1c405-121">Location of the resource.</span></span>

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

### <span data-ttu-id="1c405-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c405-122">-Name</span></span>
<span data-ttu-id="1c405-123">Namn på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="1c405-123">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="1c405-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c405-124">-PassThru</span></span>
<span data-ttu-id="1c405-125">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="1c405-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1c405-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c405-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c405-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1c405-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="1c405-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c405-128">-SubscriptionId</span></span>
<span data-ttu-id="1c405-129">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1c405-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1c405-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="1c405-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1c405-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c405-131">CommonParameters</span></span>
<span data-ttu-id="1c405-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c405-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c405-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c405-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c405-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c405-134">INPUTS</span></span>

### <span data-ttu-id="1c405-135">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1c405-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="1c405-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c405-136">OUTPUTS</span></span>

### <span data-ttu-id="1c405-137">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="1c405-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGateway</span></span>



## <span data-ttu-id="1c405-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c405-138">NOTES</span></span>

<span data-ttu-id="1c405-139">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="1c405-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c405-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c405-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1c405-141">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1c405-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c405-142">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="1c405-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="1c405-143">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="1c405-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="1c405-144">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="1c405-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="1c405-145">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="1c405-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="1c405-146">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="1c405-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="1c405-147">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="1c405-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="1c405-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1c405-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c405-149">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="1c405-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="1c405-150">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="1c405-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="1c405-151">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="1c405-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="1c405-152">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="1c405-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="1c405-153">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="1c405-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="1c405-154">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="1c405-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="1c405-155">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="1c405-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="1c405-156">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1c405-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="1c405-157">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="1c405-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="1c405-158">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="1c405-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="1c405-159">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="1c405-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="1c405-160">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="1c405-160">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="1c405-161">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="1c405-161">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="1c405-162">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1c405-162">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1c405-163">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="1c405-163">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1c405-164">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="1c405-164">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="1c405-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c405-165">RELATED LINKS</span></span>

