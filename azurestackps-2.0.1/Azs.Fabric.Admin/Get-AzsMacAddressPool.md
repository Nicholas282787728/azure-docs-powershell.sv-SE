---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsmacaddresspool
schema: 2.0.0
ms.openlocfilehash: f7a2ae035ff0985c84dc78a18131c46239bafd1f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093041"
---
# <span data-ttu-id="64147-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="64147-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="64147-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64147-102">SYNOPSIS</span></span>
<span data-ttu-id="64147-103">Returnerar den begärda MAC-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="64147-103">Returns the requested MAC address pool.</span></span>

## <span data-ttu-id="64147-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64147-104">SYNTAX</span></span>

### <span data-ttu-id="64147-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="64147-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="64147-106">Lära</span><span class="sxs-lookup"><span data-stu-id="64147-106">Get</span></span>
```
Get-AzsMacAddressPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="64147-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64147-107">GetViaIdentity</span></span>
```
Get-AzsMacAddressPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="64147-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64147-108">DESCRIPTION</span></span>
<span data-ttu-id="64147-109">Returnerar den begärda MAC-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="64147-109">Returns the requested MAC address pool.</span></span>

## <span data-ttu-id="64147-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64147-110">EXAMPLES</span></span>

### <span data-ttu-id="64147-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="64147-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsMacAddressPool

A list of all MAC address pools at a location.
```

<span data-ttu-id="64147-112">Returnerar en lista över alla MAC-adresspooler på en plats.</span><span class="sxs-lookup"><span data-stu-id="64147-112">Returns a list of all MAC address pools at a location.</span></span>

### <span data-ttu-id="64147-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="64147-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"

A specific MAC address pool at a location based on name.
```

<span data-ttu-id="64147-114">Skaffa en MAC-adresspool på en plats baserad på namn.</span><span class="sxs-lookup"><span data-stu-id="64147-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="64147-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64147-115">PARAMETERS</span></span>

### <span data-ttu-id="64147-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64147-116">-DefaultProfile</span></span>
<span data-ttu-id="64147-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64147-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64147-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="64147-118">-Filter</span></span>
<span data-ttu-id="64147-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="64147-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="64147-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64147-120">-InputObject</span></span>
<span data-ttu-id="64147-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="64147-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="64147-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="64147-122">-Location</span></span>
<span data-ttu-id="64147-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="64147-123">Location of the resource.</span></span>

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

### <span data-ttu-id="64147-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="64147-124">-Name</span></span>
<span data-ttu-id="64147-125">Namn på MAC-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="64147-125">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="64147-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64147-126">-PassThru</span></span>
<span data-ttu-id="64147-127">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="64147-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="64147-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64147-128">-ResourceGroupName</span></span>
<span data-ttu-id="64147-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="64147-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="64147-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64147-130">-SubscriptionId</span></span>
<span data-ttu-id="64147-131">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="64147-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="64147-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="64147-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="64147-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64147-133">CommonParameters</span></span>
<span data-ttu-id="64147-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64147-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64147-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64147-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64147-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64147-136">INPUTS</span></span>

### <span data-ttu-id="64147-137">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="64147-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="64147-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64147-138">OUTPUTS</span></span>

### <span data-ttu-id="64147-139">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="64147-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IMacAddressPool</span></span>



## <span data-ttu-id="64147-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64147-140">NOTES</span></span>

<span data-ttu-id="64147-141">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="64147-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64147-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64147-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="64147-143">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="64147-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64147-144">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="64147-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="64147-145">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="64147-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="64147-146">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="64147-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="64147-147">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="64147-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="64147-148">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="64147-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="64147-149">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="64147-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="64147-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="64147-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64147-151">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="64147-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="64147-152">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="64147-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="64147-153">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="64147-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="64147-154">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="64147-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="64147-155">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="64147-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="64147-156">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="64147-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="64147-157">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="64147-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="64147-158">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="64147-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="64147-159">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="64147-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="64147-160">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="64147-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="64147-161">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="64147-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="64147-162">`[StoragePool <String>]`: Namn på lagringspool.</span><span class="sxs-lookup"><span data-stu-id="64147-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="64147-163">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="64147-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="64147-164">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="64147-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="64147-165">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="64147-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="64147-166">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="64147-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="64147-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64147-167">RELATED LINKS</span></span>

