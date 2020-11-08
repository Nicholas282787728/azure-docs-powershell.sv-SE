---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalnetwork
schema: 2.0.0
ms.openlocfilehash: 8229e487cd7c616969e049bbbea0ba7a6a18a448
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099893"
---
# <span data-ttu-id="9bf32-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="9bf32-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="9bf32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bf32-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf32-103">Returnerar det begärda logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="9bf32-103">Returns the requested logical network.</span></span>

## <span data-ttu-id="9bf32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bf32-104">SYNTAX</span></span>

### <span data-ttu-id="9bf32-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="9bf32-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9bf32-106">Lära</span><span class="sxs-lookup"><span data-stu-id="9bf32-106">Get</span></span>
```
Get-AzsLogicalNetwork -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9bf32-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9bf32-107">GetViaIdentity</span></span>
```
Get-AzsLogicalNetwork -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="9bf32-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bf32-108">DESCRIPTION</span></span>
<span data-ttu-id="9bf32-109">Returnerar det begärda logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="9bf32-109">Returns the requested logical network.</span></span>

## <span data-ttu-id="9bf32-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bf32-110">EXAMPLES</span></span>

### <span data-ttu-id="9bf32-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="9bf32-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="9bf32-112">Skaffa alla logiska nätverk på en plats.</span><span class="sxs-lookup"><span data-stu-id="9bf32-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="9bf32-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="9bf32-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A specific logical networks at a location based on a name.
```

<span data-ttu-id="9bf32-114">Skaffa ett specifikt logiskt nätverk på en plats baserat på ett namn.</span><span class="sxs-lookup"><span data-stu-id="9bf32-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="9bf32-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bf32-115">PARAMETERS</span></span>

### <span data-ttu-id="9bf32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf32-116">-DefaultProfile</span></span>
<span data-ttu-id="9bf32-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf32-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf32-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="9bf32-118">-Filter</span></span>
<span data-ttu-id="9bf32-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="9bf32-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="9bf32-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bf32-120">-InputObject</span></span>
<span data-ttu-id="9bf32-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9bf32-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9bf32-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="9bf32-122">-Location</span></span>
<span data-ttu-id="9bf32-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="9bf32-123">Location of the resource.</span></span>

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

### <span data-ttu-id="9bf32-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="9bf32-124">-Name</span></span>
<span data-ttu-id="9bf32-125">Namn på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="9bf32-125">Name of the logical network.</span></span>

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

### <span data-ttu-id="9bf32-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bf32-126">-PassThru</span></span>
<span data-ttu-id="9bf32-127">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="9bf32-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9bf32-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf32-128">-ResourceGroupName</span></span>
<span data-ttu-id="9bf32-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9bf32-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="9bf32-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9bf32-130">-SubscriptionId</span></span>
<span data-ttu-id="9bf32-131">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9bf32-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9bf32-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9bf32-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9bf32-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf32-133">CommonParameters</span></span>
<span data-ttu-id="9bf32-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf32-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf32-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bf32-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf32-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bf32-136">INPUTS</span></span>

### <span data-ttu-id="9bf32-137">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9bf32-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="9bf32-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bf32-138">OUTPUTS</span></span>

### <span data-ttu-id="9bf32-139">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. ILogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="9bf32-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalNetwork</span></span>



## <span data-ttu-id="9bf32-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bf32-140">NOTES</span></span>

<span data-ttu-id="9bf32-141">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9bf32-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9bf32-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9bf32-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9bf32-143">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9bf32-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9bf32-144">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="9bf32-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="9bf32-145">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="9bf32-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="9bf32-146">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="9bf32-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="9bf32-147">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="9bf32-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="9bf32-148">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="9bf32-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="9bf32-149">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="9bf32-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="9bf32-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9bf32-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9bf32-151">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="9bf32-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="9bf32-152">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="9bf32-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="9bf32-153">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="9bf32-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9bf32-154">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="9bf32-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="9bf32-155">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="9bf32-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="9bf32-156">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="9bf32-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="9bf32-157">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="9bf32-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="9bf32-158">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9bf32-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9bf32-159">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="9bf32-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="9bf32-160">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="9bf32-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="9bf32-161">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="9bf32-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="9bf32-162">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="9bf32-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="9bf32-163">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="9bf32-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="9bf32-164">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9bf32-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9bf32-165">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9bf32-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9bf32-166">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="9bf32-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="9bf32-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bf32-167">RELATED LINKS</span></span>

