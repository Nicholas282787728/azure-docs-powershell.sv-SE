---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalsubnet
schema: 2.0.0
ms.openlocfilehash: eae4d8e861b6b229cfa3e5fe9b4e424a69c487c2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099904"
---
# <span data-ttu-id="9f0ad-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="9f0ad-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="9f0ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f0ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9f0ad-103">Returnerar det begärda logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-103">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="9f0ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f0ad-104">SYNTAX</span></span>

### <span data-ttu-id="9f0ad-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="9f0ad-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9f0ad-106">Lära</span><span class="sxs-lookup"><span data-stu-id="9f0ad-106">Get</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="9f0ad-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9f0ad-107">GetViaIdentity</span></span>
```
Get-AzsLogicalSubnet -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="9f0ad-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f0ad-108">DESCRIPTION</span></span>
<span data-ttu-id="9f0ad-109">Returnerar det begärda logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-109">Returns the requested logical subnet.</span></span>

## <span data-ttu-id="9f0ad-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f0ad-110">EXAMPLES</span></span>

### <span data-ttu-id="9f0ad-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="9f0ad-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="9f0ad-112">Skaffa alla logiska nätverk på en plats.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="9f0ad-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="9f0ad-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A a specific logical networks at a location based on a name.
```

<span data-ttu-id="9f0ad-114">Skaffa ett specifikt logiskt nätverk på en plats baserat på ett namn.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="9f0ad-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f0ad-115">PARAMETERS</span></span>

### <span data-ttu-id="9f0ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f0ad-116">-DefaultProfile</span></span>
<span data-ttu-id="9f0ad-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f0ad-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="9f0ad-118">-Filter</span></span>
<span data-ttu-id="9f0ad-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="9f0ad-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f0ad-120">-InputObject</span></span>
<span data-ttu-id="9f0ad-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9f0ad-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="9f0ad-122">-Location</span></span>
<span data-ttu-id="9f0ad-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-123">Location of the resource.</span></span>

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

### <span data-ttu-id="9f0ad-124">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="9f0ad-124">-LogicalNetwork</span></span>
<span data-ttu-id="9f0ad-125">Namn på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-125">Name of the logical network.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9f0ad-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f0ad-126">-Name</span></span>
<span data-ttu-id="9f0ad-127">Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-127">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="9f0ad-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f0ad-128">-PassThru</span></span>
<span data-ttu-id="9f0ad-129">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="9f0ad-129">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9f0ad-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f0ad-130">-ResourceGroupName</span></span>
<span data-ttu-id="9f0ad-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="9f0ad-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f0ad-132">-SubscriptionId</span></span>
<span data-ttu-id="9f0ad-133">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9f0ad-134">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9f0ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f0ad-135">CommonParameters</span></span>
<span data-ttu-id="9f0ad-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f0ad-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f0ad-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f0ad-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f0ad-138">INPUTS</span></span>

### <span data-ttu-id="9f0ad-139">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9f0ad-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="9f0ad-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f0ad-140">OUTPUTS</span></span>

### <span data-ttu-id="9f0ad-141">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. ILogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="9f0ad-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalSubnet</span></span>



## <span data-ttu-id="9f0ad-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f0ad-142">NOTES</span></span>

<span data-ttu-id="9f0ad-143">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f0ad-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9f0ad-145">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9f0ad-145">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9f0ad-146">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-146">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="9f0ad-147">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-147">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="9f0ad-148">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-148">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="9f0ad-149">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-149">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="9f0ad-150">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-150">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="9f0ad-151">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-151">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="9f0ad-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9f0ad-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9f0ad-153">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-153">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="9f0ad-154">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-154">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="9f0ad-155">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-155">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9f0ad-156">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-156">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="9f0ad-157">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-157">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="9f0ad-158">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-158">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="9f0ad-159">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-159">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="9f0ad-160">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-160">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9f0ad-161">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-161">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="9f0ad-162">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-162">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="9f0ad-163">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-163">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="9f0ad-164">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-164">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="9f0ad-165">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-165">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="9f0ad-166">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-166">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9f0ad-167">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-167">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9f0ad-168">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="9f0ad-168">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="9f0ad-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f0ad-169">RELATED LINKS</span></span>
