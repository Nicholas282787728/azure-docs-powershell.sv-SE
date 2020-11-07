---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/enable-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4a7140d5162f046377e37b92d4e6931abdbb4cf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923214"
---
# <span data-ttu-id="e12a4-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="e12a4-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="e12a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e12a4-102">SYNOPSIS</span></span>


## <span data-ttu-id="e12a4-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e12a4-103">SYNTAX</span></span>

### <span data-ttu-id="e12a4-104">Start (standard)</span><span class="sxs-lookup"><span data-stu-id="e12a4-104">Start (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e12a4-105">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e12a4-105">StartViaIdentity</span></span>
```
Enable-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e12a4-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e12a4-106">DESCRIPTION</span></span>


## <span data-ttu-id="e12a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e12a4-107">EXAMPLES</span></span>

### <span data-ttu-id="e12a4-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="e12a4-108">Example 1:</span></span>
```powershell
PS C:\> Enable-AzsScaleUnitNode -Name "HC1n25r2236"

Stop maintenance mode on a scale unit node.
```

<span data-ttu-id="e12a4-109">Stoppa underhålls läget för en noden Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="e12a4-109">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="e12a4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e12a4-110">PARAMETERS</span></span>

### <span data-ttu-id="e12a4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e12a4-111">-AsJob</span></span>


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

### <span data-ttu-id="e12a4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12a4-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="e12a4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e12a4-113">-Force</span></span>


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

### <span data-ttu-id="e12a4-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e12a4-114">-InputObject</span></span>
<span data-ttu-id="e12a4-115">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e12a4-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e12a4-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="e12a4-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e12a4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e12a4-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e12a4-118">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e12a4-118">-NoWait</span></span>


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

### <span data-ttu-id="e12a4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e12a4-119">-PassThru</span></span>


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

### <span data-ttu-id="e12a4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e12a4-120">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e12a4-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e12a4-121">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e12a4-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e12a4-122">-Confirm</span></span>
<span data-ttu-id="e12a4-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e12a4-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e12a4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e12a4-124">-WhatIf</span></span>
<span data-ttu-id="e12a4-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e12a4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e12a4-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e12a4-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e12a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12a4-127">CommonParameters</span></span>
<span data-ttu-id="e12a4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12a4-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e12a4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12a4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e12a4-130">INPUTS</span></span>

### <span data-ttu-id="e12a4-131">Microsoft. Azure. PowerShell. cmdletar. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e12a4-131">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="e12a4-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e12a4-132">OUTPUTS</span></span>

### <span data-ttu-id="e12a4-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e12a4-133">System.Boolean</span></span>



## <span data-ttu-id="e12a4-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e12a4-134">NOTES</span></span>

<span data-ttu-id="e12a4-135">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e12a4-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e12a4-136">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e12a4-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e12a4-137">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="e12a4-137">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="e12a4-138">`[Drive <String>]`: Lagrings enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="e12a4-138">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="e12a4-139">`[EdgeGateway <String>]`: Namnet på Edge Gateway.</span><span class="sxs-lookup"><span data-stu-id="e12a4-139">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="e12a4-140">`[EdgeGatewayPool <String>]`: Namnet på Edge Gateway-poolen.</span><span class="sxs-lookup"><span data-stu-id="e12a4-140">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="e12a4-141">`[FabricLocation <String>]`: Fabric-plats.</span><span class="sxs-lookup"><span data-stu-id="e12a4-141">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="e12a4-142">`[FileShare <String>]`: Fil resurs namn för Fabric.</span><span class="sxs-lookup"><span data-stu-id="e12a4-142">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="e12a4-143">`[IPPool <String>]`: IP-poolnamn.</span><span class="sxs-lookup"><span data-stu-id="e12a4-143">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="e12a4-144">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e12a4-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e12a4-145">`[InfraRole <String>]`: Infrastruktur roll namn.</span><span class="sxs-lookup"><span data-stu-id="e12a4-145">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="e12a4-146">`[InfraRoleInstance <String>]`: Namnet på en infrastruktur roll instans.</span><span class="sxs-lookup"><span data-stu-id="e12a4-146">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="e12a4-147">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="e12a4-147">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e12a4-148">`[LogicalNetwork <String>]`: Namnet på det logiska nätverket.</span><span class="sxs-lookup"><span data-stu-id="e12a4-148">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="e12a4-149">`[LogicalSubnet <String>]`: Namnet på det logiska under nätet.</span><span class="sxs-lookup"><span data-stu-id="e12a4-149">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="e12a4-150">`[MacAddressPool <String>]`: MAC-adresspoolen namn.</span><span class="sxs-lookup"><span data-stu-id="e12a4-150">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="e12a4-151">`[Operation <String>]`: Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="e12a4-151">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="e12a4-152">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e12a4-152">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e12a4-153">`[ScaleUnit <String>]`: Enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="e12a4-153">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="e12a4-154">`[ScaleUnitNode <String>]`: Namnet på noden för Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="e12a4-154">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="e12a4-155">`[SlbMuxInstance <String>]`: Namnet på en SLB MUX-instans.</span><span class="sxs-lookup"><span data-stu-id="e12a4-155">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="e12a4-156">`[StorageSubSystem <String>]`: Lagrings systemets namn.</span><span class="sxs-lookup"><span data-stu-id="e12a4-156">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="e12a4-157">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e12a4-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e12a4-158">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e12a4-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e12a4-159">`[Volume <String>]`: Lagrings volymens namn.</span><span class="sxs-lookup"><span data-stu-id="e12a4-159">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="e12a4-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e12a4-160">RELATED LINKS</span></span>

