---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsdrive
schema: 2.0.0
ms.openlocfilehash: ec2216a9234086702e8a9331888c04034d13a99f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092954"
---
# <span data-ttu-id="b587f-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="b587f-101">Get-AzsDrive</span></span>

## <span data-ttu-id="b587f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b587f-102">SYNOPSIS</span></span>
<span data-ttu-id="b587f-103">Returnera den begärda lagrings enheten.</span><span class="sxs-lookup"><span data-stu-id="b587f-103">Return the requested a storage drive.</span></span>

## <span data-ttu-id="b587f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b587f-104">SYNTAX</span></span>

### <span data-ttu-id="b587f-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="b587f-105">List (Default)</span></span>
```
Get-AzsDrive -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b587f-106">Lära</span><span class="sxs-lookup"><span data-stu-id="b587f-106">Get</span></span>
```
Get-AzsDrive -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="b587f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b587f-107">GetViaIdentity</span></span>
```
Get-AzsDrive -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="b587f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b587f-108">DESCRIPTION</span></span>
<span data-ttu-id="b587f-109">Returnera den begärda lagrings enheten.</span><span class="sxs-lookup"><span data-stu-id="b587f-109">Return the requested a storage drive.</span></span>

## <span data-ttu-id="b587f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b587f-110">EXAMPLES</span></span>

### <span data-ttu-id="b587f-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="b587f-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="b587f-112">Få en lista över alla lagrings enheter för ett visst kluster.</span><span class="sxs-lookup"><span data-stu-id="b587f-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="b587f-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="b587f-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name '{a185d466-4d21-4c1f-9489-7c9c66b6b172}:PD:{fd389cf7-2115-2144-5afe-27910562d6b3}'
```

<span data-ttu-id="b587f-114">Skaffa en lagrings enhet per namn för ett visst kluster.</span><span class="sxs-lookup"><span data-stu-id="b587f-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="b587f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b587f-115">PARAMETERS</span></span>

### <span data-ttu-id="b587f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b587f-116">-DefaultProfile</span></span>
<span data-ttu-id="b587f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b587f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b587f-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="b587f-118">-Filter</span></span>
<span data-ttu-id="b587f-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="b587f-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="b587f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b587f-120">-InputObject</span></span>
<span data-ttu-id="b587f-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b587f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b587f-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="b587f-122">-Location</span></span>
<span data-ttu-id="b587f-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="b587f-123">Location of the resource.</span></span>

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

### <span data-ttu-id="b587f-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="b587f-124">-Name</span></span>
<span data-ttu-id="b587f-125">Namn på lagrings enheten.</span><span class="sxs-lookup"><span data-stu-id="b587f-125">Name of the storage drive.</span></span>

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

### <span data-ttu-id="b587f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b587f-126">-PassThru</span></span>
<span data-ttu-id="b587f-127">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="b587f-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b587f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b587f-128">-ResourceGroupName</span></span>
<span data-ttu-id="b587f-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b587f-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="b587f-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="b587f-130">-ScaleUnit</span></span>
<span data-ttu-id="b587f-131">Namnet på enheten.</span><span class="sxs-lookup"><span data-stu-id="b587f-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="b587f-132">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="b587f-132">-Skip</span></span>
<span data-ttu-id="b587f-133">OData Skip-parameter.</span><span class="sxs-lookup"><span data-stu-id="b587f-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="b587f-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="b587f-134">-StorageSubSystem</span></span>
<span data-ttu-id="b587f-135">Namn på lagrings systemet.</span><span class="sxs-lookup"><span data-stu-id="b587f-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="b587f-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b587f-136">-SubscriptionId</span></span>
<span data-ttu-id="b587f-137">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b587f-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b587f-138">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b587f-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b587f-139">-Överst</span><span class="sxs-lookup"><span data-stu-id="b587f-139">-Top</span></span>
<span data-ttu-id="b587f-140">OData Top-parameter.</span><span class="sxs-lookup"><span data-stu-id="b587f-140">OData top parameter.</span></span>

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

### <span data-ttu-id="b587f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b587f-141">CommonParameters</span></span>
<span data-ttu-id="b587f-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b587f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b587f-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b587f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b587f-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b587f-144">INPUTS</span></span>

### <span data-ttu-id="b587f-145">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b587f-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="b587f-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b587f-146">OUTPUTS</span></span>

### <span data-ttu-id="b587f-147">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20190501. IDrive</span><span class="sxs-lookup"><span data-stu-id="b587f-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IDrive</span></span>



## <span data-ttu-id="b587f-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b587f-148">NOTES</span></span>

<span data-ttu-id="b587f-149">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="b587f-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b587f-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b587f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b587f-151">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="b587f-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b587f-152">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="b587f-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="b587f-153">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="b587f-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="b587f-154">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="b587f-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="b587f-155">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="b587f-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="b587f-156">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="b587f-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="b587f-157">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="b587f-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="b587f-158">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="b587f-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b587f-159">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="b587f-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="b587f-160">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="b587f-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="b587f-161">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="b587f-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b587f-162">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="b587f-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="b587f-163">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="b587f-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="b587f-164">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="b587f-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="b587f-165">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="b587f-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="b587f-166">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b587f-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="b587f-167">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="b587f-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="b587f-168">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="b587f-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="b587f-169">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="b587f-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="b587f-170">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="b587f-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="b587f-171">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b587f-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b587f-172">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="b587f-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b587f-173">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="b587f-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="b587f-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b587f-174">RELATED LINKS</span></span>

