---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099903"
---
# <span data-ttu-id="6a07f-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="6a07f-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="6a07f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a07f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a07f-103">Returnerar den begärda Fabric-fildelningen.</span><span class="sxs-lookup"><span data-stu-id="6a07f-103">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="6a07f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a07f-104">SYNTAX</span></span>

### <span data-ttu-id="6a07f-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="6a07f-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="6a07f-106">Lära</span><span class="sxs-lookup"><span data-stu-id="6a07f-106">Get</span></span>
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="6a07f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6a07f-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="6a07f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a07f-108">DESCRIPTION</span></span>
<span data-ttu-id="6a07f-109">Returnerar den begärda Fabric-fildelningen.</span><span class="sxs-lookup"><span data-stu-id="6a07f-109">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="6a07f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a07f-110">EXAMPLES</span></span>

### <span data-ttu-id="6a07f-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="6a07f-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare
```

<span data-ttu-id="6a07f-112">Returnerar en lista över alla fil resurser.</span><span class="sxs-lookup"><span data-stu-id="6a07f-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="6a07f-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="6a07f-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

<span data-ttu-id="6a07f-114">Returnerar en fil resurs baserad på namn.</span><span class="sxs-lookup"><span data-stu-id="6a07f-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="6a07f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a07f-115">PARAMETERS</span></span>

### <span data-ttu-id="6a07f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a07f-116">-DefaultProfile</span></span>
<span data-ttu-id="6a07f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a07f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a07f-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="6a07f-118">-Filter</span></span>
<span data-ttu-id="6a07f-119">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="6a07f-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="6a07f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a07f-120">-InputObject</span></span>
<span data-ttu-id="6a07f-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6a07f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a07f-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="6a07f-122">-Location</span></span>
<span data-ttu-id="6a07f-123">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="6a07f-123">Location of the resource.</span></span>

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

### <span data-ttu-id="6a07f-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a07f-124">-Name</span></span>
<span data-ttu-id="6a07f-125">Namn på Fabric File Share.</span><span class="sxs-lookup"><span data-stu-id="6a07f-125">Fabric file share name.</span></span>

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

### <span data-ttu-id="6a07f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a07f-126">-PassThru</span></span>
<span data-ttu-id="6a07f-127">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="6a07f-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6a07f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a07f-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a07f-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6a07f-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="6a07f-130">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="6a07f-130">-Skip</span></span>
<span data-ttu-id="6a07f-131">OData Skip-parameter.</span><span class="sxs-lookup"><span data-stu-id="6a07f-131">OData skip parameter.</span></span>

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

### <span data-ttu-id="6a07f-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a07f-132">-SubscriptionId</span></span>
<span data-ttu-id="6a07f-133">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6a07f-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a07f-134">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6a07f-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6a07f-135">-Överst</span><span class="sxs-lookup"><span data-stu-id="6a07f-135">-Top</span></span>
<span data-ttu-id="6a07f-136">OData Top-parameter.</span><span class="sxs-lookup"><span data-stu-id="6a07f-136">OData top parameter.</span></span>

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

### <span data-ttu-id="6a07f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a07f-137">CommonParameters</span></span>
<span data-ttu-id="6a07f-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a07f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a07f-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a07f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a07f-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a07f-140">INPUTS</span></span>

### <span data-ttu-id="6a07f-141">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6a07f-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="6a07f-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a07f-142">OUTPUTS</span></span>

### <span data-ttu-id="6a07f-143">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. Api20160501. IFileShare</span><span class="sxs-lookup"><span data-stu-id="6a07f-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFileShare</span></span>



## <span data-ttu-id="6a07f-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a07f-144">NOTES</span></span>

<span data-ttu-id="6a07f-145">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6a07f-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a07f-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a07f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6a07f-147">INPUTOBJECT <IFabricAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="6a07f-147">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a07f-148">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="6a07f-148">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="6a07f-149">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="6a07f-149">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="6a07f-150">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="6a07f-150">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="6a07f-151">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="6a07f-151">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="6a07f-152">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="6a07f-152">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="6a07f-153">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="6a07f-153">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="6a07f-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="6a07f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a07f-155">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="6a07f-155">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="6a07f-156">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="6a07f-156">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="6a07f-157">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="6a07f-157">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6a07f-158">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="6a07f-158">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="6a07f-159">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="6a07f-159">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="6a07f-160">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="6a07f-160">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="6a07f-161">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="6a07f-161">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="6a07f-162">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6a07f-162">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="6a07f-163">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="6a07f-163">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="6a07f-164">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="6a07f-164">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="6a07f-165">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="6a07f-165">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="6a07f-166">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="6a07f-166">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="6a07f-167">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6a07f-167">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6a07f-168">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="6a07f-168">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6a07f-169">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="6a07f-169">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="6a07f-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a07f-170">RELATED LINKS</span></span>

