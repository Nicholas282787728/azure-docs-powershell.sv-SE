---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099898"
---
# <span data-ttu-id="5a95a-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="5a95a-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="5a95a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a95a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a95a-103">Returnera det begärda lagrings under systemet.</span><span class="sxs-lookup"><span data-stu-id="5a95a-103">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="5a95a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a95a-104">SYNTAX</span></span>

### <span data-ttu-id="5a95a-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="5a95a-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="5a95a-106">Lära</span><span class="sxs-lookup"><span data-stu-id="5a95a-106">Get</span></span>
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="5a95a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5a95a-107">GetViaIdentity</span></span>
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="5a95a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a95a-108">DESCRIPTION</span></span>
<span data-ttu-id="5a95a-109">Returnera det begärda lagrings under systemet.</span><span class="sxs-lookup"><span data-stu-id="5a95a-109">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="5a95a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a95a-110">EXAMPLES</span></span>

### <span data-ttu-id="5a95a-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="5a95a-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

<span data-ttu-id="5a95a-112">Hämta alla lagrings under system från en enhet.</span><span class="sxs-lookup"><span data-stu-id="5a95a-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="5a95a-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="5a95a-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

<span data-ttu-id="5a95a-114">Skaffa ett underlag rings system med en enhet och ett namn.</span><span class="sxs-lookup"><span data-stu-id="5a95a-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="5a95a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a95a-115">PARAMETERS</span></span>

### <span data-ttu-id="5a95a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a95a-116">-DefaultProfile</span></span>
<span data-ttu-id="5a95a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a95a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a95a-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="5a95a-118">-Filter</span></span>
<span data-ttu-id="5a95a-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="5a95a-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="5a95a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a95a-120">-InputObject</span></span>
<span data-ttu-id="5a95a-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5a95a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5a95a-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="5a95a-122">-Location</span></span>
<span data-ttu-id="5a95a-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="5a95a-123">Location of the resource.</span></span>

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

### <span data-ttu-id="5a95a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a95a-124">-Name</span></span>
<span data-ttu-id="5a95a-125">Namn på lagrings systemet.</span><span class="sxs-lookup"><span data-stu-id="5a95a-125">Name of the storage system.</span></span>

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

### <span data-ttu-id="5a95a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a95a-126">-PassThru</span></span>
<span data-ttu-id="5a95a-127">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="5a95a-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5a95a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a95a-128">-ResourceGroupName</span></span>
<span data-ttu-id="5a95a-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a95a-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="5a95a-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="5a95a-130">-ScaleUnit</span></span>
<span data-ttu-id="5a95a-131">Namnet på enheten.</span><span class="sxs-lookup"><span data-stu-id="5a95a-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="5a95a-132">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="5a95a-132">-Skip</span></span>
<span data-ttu-id="5a95a-133">OData Skip-parameter.</span><span class="sxs-lookup"><span data-stu-id="5a95a-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="5a95a-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a95a-134">-SubscriptionId</span></span>
<span data-ttu-id="5a95a-135">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5a95a-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5a95a-136">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5a95a-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5a95a-137">-Överst</span><span class="sxs-lookup"><span data-stu-id="5a95a-137">-Top</span></span>
<span data-ttu-id="5a95a-138">OData Top-parameter.</span><span class="sxs-lookup"><span data-stu-id="5a95a-138">OData top parameter.</span></span>

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

### <span data-ttu-id="5a95a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a95a-139">CommonParameters</span></span>
<span data-ttu-id="5a95a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a95a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a95a-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a95a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a95a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a95a-142">INPUTS</span></span>

### <span data-ttu-id="5a95a-143">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5a95a-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="5a95a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a95a-144">OUTPUTS</span></span>

### <span data-ttu-id="5a95a-145">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20181001. IStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="5a95a-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20181001.IStorageSubSystem</span></span>



## <span data-ttu-id="5a95a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a95a-146">NOTES</span></span>

<span data-ttu-id="5a95a-147">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="5a95a-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a95a-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5a95a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5a95a-149">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5a95a-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5a95a-150">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="5a95a-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="5a95a-151">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="5a95a-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="5a95a-152">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="5a95a-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="5a95a-153">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="5a95a-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="5a95a-154">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="5a95a-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="5a95a-155">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="5a95a-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="5a95a-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5a95a-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5a95a-157">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="5a95a-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="5a95a-158">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="5a95a-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="5a95a-159">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="5a95a-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5a95a-160">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="5a95a-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="5a95a-161">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="5a95a-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="5a95a-162">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="5a95a-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="5a95a-163">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="5a95a-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="5a95a-164">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5a95a-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5a95a-165">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="5a95a-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="5a95a-166">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="5a95a-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="5a95a-167">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="5a95a-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="5a95a-168">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="5a95a-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="5a95a-169">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5a95a-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5a95a-170">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="5a95a-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5a95a-171">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="5a95a-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="5a95a-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a95a-172">RELATED LINKS</span></span>

