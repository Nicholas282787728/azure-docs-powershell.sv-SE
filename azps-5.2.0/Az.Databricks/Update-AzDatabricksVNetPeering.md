---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412056"
---
# <span data-ttu-id="cd080-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="cd080-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="cd080-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd080-102">SYNOPSIS</span></span>
<span data-ttu-id="cd080-103">Uppdatera vNet-peering för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="cd080-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="cd080-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd080-104">SYNTAX</span></span>

### <span data-ttu-id="cd080-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="cd080-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd080-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cd080-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd080-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd080-107">DESCRIPTION</span></span>
<span data-ttu-id="cd080-108">Uppdatera vNet-peering för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="cd080-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="cd080-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd080-109">EXAMPLES</span></span>

### <span data-ttu-id="cd080-110">Exempel 1: uppdatera AllowForwardedTraffic av VNet peering</span><span class="sxs-lookup"><span data-stu-id="cd080-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="cd080-111">Det här kommandot uppdaterar AllowForwardedTraffic av VNet-peering.</span><span class="sxs-lookup"><span data-stu-id="cd080-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="cd080-112">Exempel 2: uppdatera AllowForwardedTraffic för VNet peering efter objekt</span><span class="sxs-lookup"><span data-stu-id="cd080-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="cd080-113">Det här kommandot uppdaterar AllowForwardedTraffic för VNet-peering efter objekt.</span><span class="sxs-lookup"><span data-stu-id="cd080-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="cd080-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd080-114">PARAMETERS</span></span>

### <span data-ttu-id="cd080-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="cd080-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="cd080-116">[System. Management. Automation. SwitchParameter] om den vidarebefordrade trafiken från datorerna i det lokala virtuella nätverket tillåts/är inte tillåten i virtuellt fjärr nätverk.</span><span class="sxs-lookup"><span data-stu-id="cd080-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd080-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="cd080-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="cd080-118">[System. Management. Automation. SwitchParameter] om Gateway-länkar kan användas i virtuella fjärrnätverk för att länka till det här virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="cd080-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd080-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="cd080-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="cd080-120">[System. Management. Automation. SwitchParameter] om datorerna i det lokala virtuella nätverks utrymmet skulle kunna komma åt de virtuella datorerna i det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="cd080-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd080-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd080-121">-AsJob</span></span>
<span data-ttu-id="cd080-122">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="cd080-122">Run the command as a job</span></span>

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

### <span data-ttu-id="cd080-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd080-123">-DefaultProfile</span></span>
<span data-ttu-id="cd080-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd080-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd080-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd080-125">-InputObject</span></span>
<span data-ttu-id="cd080-126">Identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="cd080-126">Identity parameter.</span></span>
<span data-ttu-id="cd080-127">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="cd080-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd080-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd080-128">-Name</span></span>
<span data-ttu-id="cd080-129">Namnet på VNetPeering.</span><span class="sxs-lookup"><span data-stu-id="cd080-129">The name of the VNetPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PeeringName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd080-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cd080-130">-NoWait</span></span>
<span data-ttu-id="cd080-131">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="cd080-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd080-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd080-132">-ResourceGroupName</span></span>
<span data-ttu-id="cd080-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd080-133">The name of the resource group.</span></span>
<span data-ttu-id="cd080-134">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="cd080-134">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd080-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd080-135">-SubscriptionId</span></span>
<span data-ttu-id="cd080-136">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cd080-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd080-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="cd080-137">-UseRemoteGateway</span></span>
<span data-ttu-id="cd080-138">[System. Management. Automation. SwitchParameter] om du kan använda Fjärrgateways på det här virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="cd080-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="cd080-139">Om flaggan är inställd på True och allowGatewayTransit på fjärr-peering också är sant, använder virtuella nätverk gateways för fjärrnätverk för överföring.</span><span class="sxs-lookup"><span data-stu-id="cd080-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="cd080-140">Endast en peering kan ha den här flaggan inställd på True.</span><span class="sxs-lookup"><span data-stu-id="cd080-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="cd080-141">Det går inte att ange den här flaggan om det redan finns en gateway för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="cd080-141">This flag cannot be set if virtual network already has a gateway.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd080-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cd080-142">-WorkspaceName</span></span>
<span data-ttu-id="cd080-143">Namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="cd080-143">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd080-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd080-144">-Confirm</span></span>
<span data-ttu-id="cd080-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd080-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd080-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd080-146">-WhatIf</span></span>
<span data-ttu-id="cd080-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd080-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd080-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd080-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd080-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd080-149">CommonParameters</span></span>
<span data-ttu-id="cd080-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd080-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd080-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd080-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd080-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd080-152">INPUTS</span></span>

### <span data-ttu-id="cd080-153">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="cd080-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="cd080-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd080-154">OUTPUTS</span></span>

### <span data-ttu-id="cd080-155">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cd080-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="cd080-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd080-156">NOTES</span></span>

<span data-ttu-id="cd080-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cd080-157">ALIASES</span></span>

<span data-ttu-id="cd080-158">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="cd080-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd080-159">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="cd080-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd080-160">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd080-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd080-161">INPUTOBJECT <IDatabricksIdentity> : identitets parameter.</span><span class="sxs-lookup"><span data-stu-id="cd080-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="cd080-162">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="cd080-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd080-163">`[PeeringName <String>]`: Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="cd080-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="cd080-164">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd080-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cd080-165">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="cd080-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="cd080-166">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="cd080-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cd080-167">`[WorkspaceName <String>]`: Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="cd080-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="cd080-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd080-168">RELATED LINKS</span></span>

