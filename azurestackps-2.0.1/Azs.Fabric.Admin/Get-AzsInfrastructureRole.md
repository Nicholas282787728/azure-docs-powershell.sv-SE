---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurerole
schema: 2.0.0
ms.openlocfilehash: dcd4f9da702425808e3e2565a7b668930ff7aa32
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093010"
---
# <span data-ttu-id="3699f-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="3699f-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="3699f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3699f-102">SYNOPSIS</span></span>
<span data-ttu-id="3699f-103">Returnerar den begärda infrastruktur roll beskrivningen.</span><span class="sxs-lookup"><span data-stu-id="3699f-103">Returns the requested infrastructure role description.</span></span>

## <span data-ttu-id="3699f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3699f-104">SYNTAX</span></span>

### <span data-ttu-id="3699f-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="3699f-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3699f-106">Lära</span><span class="sxs-lookup"><span data-stu-id="3699f-106">Get</span></span>
```
Get-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="3699f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3699f-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureRole -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="3699f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3699f-108">DESCRIPTION</span></span>
<span data-ttu-id="3699f-109">Returnerar den begärda infrastruktur roll beskrivningen.</span><span class="sxs-lookup"><span data-stu-id="3699f-109">Returns the requested infrastructure role description.</span></span>

## <span data-ttu-id="3699f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3699f-110">EXAMPLES</span></span>

### <span data-ttu-id="3699f-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="3699f-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRole

A list of all infrastructure roles.
```

<span data-ttu-id="3699f-112">Få en lista över alla infrastruktur roller.</span><span class="sxs-lookup"><span data-stu-id="3699f-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="3699f-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="3699f-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRole -Name "Active Directory Federation Services"

An infrastructure role based on the name.
```

<span data-ttu-id="3699f-114">Skaffa en infrastruktur roll baserat på namnet.</span><span class="sxs-lookup"><span data-stu-id="3699f-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="3699f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3699f-115">PARAMETERS</span></span>

### <span data-ttu-id="3699f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3699f-116">-DefaultProfile</span></span>
<span data-ttu-id="3699f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3699f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3699f-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="3699f-118">-Filter</span></span>
<span data-ttu-id="3699f-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="3699f-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="3699f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3699f-120">-InputObject</span></span>
<span data-ttu-id="3699f-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3699f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3699f-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="3699f-122">-Location</span></span>
<span data-ttu-id="3699f-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="3699f-123">Location of the resource.</span></span>

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

### <span data-ttu-id="3699f-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3699f-124">-Name</span></span>
<span data-ttu-id="3699f-125">Namn på infrastruktur rollen.</span><span class="sxs-lookup"><span data-stu-id="3699f-125">Infrastructure role name.</span></span>

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

### <span data-ttu-id="3699f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3699f-126">-PassThru</span></span>
<span data-ttu-id="3699f-127">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="3699f-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3699f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3699f-128">-ResourceGroupName</span></span>
<span data-ttu-id="3699f-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3699f-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="3699f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3699f-130">-SubscriptionId</span></span>
<span data-ttu-id="3699f-131">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3699f-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3699f-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3699f-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3699f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3699f-133">CommonParameters</span></span>
<span data-ttu-id="3699f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3699f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3699f-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3699f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3699f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3699f-136">INPUTS</span></span>

### <span data-ttu-id="3699f-137">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3699f-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="3699f-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3699f-138">OUTPUTS</span></span>

### <span data-ttu-id="3699f-139">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IInfraRole</span><span class="sxs-lookup"><span data-stu-id="3699f-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IInfraRole</span></span>



## <span data-ttu-id="3699f-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3699f-140">NOTES</span></span>

<span data-ttu-id="3699f-141">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3699f-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3699f-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3699f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3699f-143">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3699f-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3699f-144">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="3699f-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="3699f-145">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="3699f-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="3699f-146">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="3699f-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="3699f-147">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="3699f-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="3699f-148">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="3699f-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="3699f-149">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="3699f-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="3699f-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3699f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3699f-151">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="3699f-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="3699f-152">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="3699f-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="3699f-153">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="3699f-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3699f-154">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="3699f-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="3699f-155">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="3699f-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="3699f-156">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="3699f-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="3699f-157">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="3699f-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="3699f-158">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3699f-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3699f-159">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="3699f-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="3699f-160">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3699f-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="3699f-161">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="3699f-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="3699f-162">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="3699f-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="3699f-163">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="3699f-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="3699f-164">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3699f-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3699f-165">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3699f-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3699f-166">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="3699f-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="3699f-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3699f-167">RELATED LINKS</span></span>

