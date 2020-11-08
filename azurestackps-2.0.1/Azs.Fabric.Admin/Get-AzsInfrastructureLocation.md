---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093011"
---
# <span data-ttu-id="06a7e-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="06a7e-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="06a7e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="06a7e-103">Returnerar den begärda infrastruktur platsen.</span><span class="sxs-lookup"><span data-stu-id="06a7e-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="06a7e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06a7e-104">SYNTAX</span></span>

### <span data-ttu-id="06a7e-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="06a7e-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="06a7e-106">Lära</span><span class="sxs-lookup"><span data-stu-id="06a7e-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="06a7e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="06a7e-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="06a7e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06a7e-108">DESCRIPTION</span></span>
<span data-ttu-id="06a7e-109">Returnerar den begärda infrastruktur platsen.</span><span class="sxs-lookup"><span data-stu-id="06a7e-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="06a7e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06a7e-110">EXAMPLES</span></span>

### <span data-ttu-id="06a7e-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="06a7e-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="06a7e-112">Få en lista över alla infrastruktur platser.</span><span class="sxs-lookup"><span data-stu-id="06a7e-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="06a7e-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="06a7e-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="06a7e-114">Få en plats utifrån namnet.</span><span class="sxs-lookup"><span data-stu-id="06a7e-114">Get a location based on the name.</span></span>

## <span data-ttu-id="06a7e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06a7e-115">PARAMETERS</span></span>

### <span data-ttu-id="06a7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a7e-116">-DefaultProfile</span></span>
<span data-ttu-id="06a7e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06a7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06a7e-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="06a7e-118">-FabricLocation</span></span>
<span data-ttu-id="06a7e-119">Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="06a7e-119">Fabric location.</span></span>

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

### <span data-ttu-id="06a7e-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="06a7e-120">-Filter</span></span>
<span data-ttu-id="06a7e-121">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="06a7e-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="06a7e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06a7e-122">-InputObject</span></span>
<span data-ttu-id="06a7e-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="06a7e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="06a7e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06a7e-124">-PassThru</span></span>
<span data-ttu-id="06a7e-125">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="06a7e-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06a7e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a7e-126">-ResourceGroupName</span></span>
<span data-ttu-id="06a7e-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="06a7e-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="06a7e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06a7e-128">-SubscriptionId</span></span>
<span data-ttu-id="06a7e-129">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="06a7e-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="06a7e-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="06a7e-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="06a7e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a7e-131">CommonParameters</span></span>
<span data-ttu-id="06a7e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a7e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a7e-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06a7e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a7e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06a7e-134">INPUTS</span></span>

### <span data-ttu-id="06a7e-135">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="06a7e-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="06a7e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06a7e-136">OUTPUTS</span></span>

### <span data-ttu-id="06a7e-137">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IFabricLocation</span><span class="sxs-lookup"><span data-stu-id="06a7e-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="06a7e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06a7e-138">NOTES</span></span>

<span data-ttu-id="06a7e-139">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="06a7e-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06a7e-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06a7e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="06a7e-141">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="06a7e-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06a7e-142">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="06a7e-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="06a7e-143">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="06a7e-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="06a7e-144">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="06a7e-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="06a7e-145">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="06a7e-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="06a7e-146">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="06a7e-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="06a7e-147">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="06a7e-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="06a7e-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="06a7e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06a7e-149">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="06a7e-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="06a7e-150">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="06a7e-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="06a7e-151">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="06a7e-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="06a7e-152">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="06a7e-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="06a7e-153">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="06a7e-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="06a7e-154">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="06a7e-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="06a7e-155">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="06a7e-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="06a7e-156">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="06a7e-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="06a7e-157">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="06a7e-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="06a7e-158">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="06a7e-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="06a7e-159">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="06a7e-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="06a7e-160">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="06a7e-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="06a7e-161">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="06a7e-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="06a7e-162">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="06a7e-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="06a7e-163">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="06a7e-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="06a7e-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06a7e-164">RELATED LINKS</span></span>

