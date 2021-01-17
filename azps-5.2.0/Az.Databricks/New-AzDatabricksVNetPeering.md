---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415803"
---
# <span data-ttu-id="2e661-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="2e661-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="2e661-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e661-102">SYNOPSIS</span></span>
<span data-ttu-id="2e661-103">Skapar virtuellt nätverk för arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2e661-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="2e661-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e661-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2e661-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e661-105">DESCRIPTION</span></span>
<span data-ttu-id="2e661-106">Skapar virtuellt nätverk för arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2e661-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="2e661-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e661-107">EXAMPLES</span></span>

### <span data-ttu-id="2e661-108">Exempel 1: skapa en VNet-peering för databricks</span><span class="sxs-lookup"><span data-stu-id="2e661-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="2e661-109">Det här kommandot skapar en VNet-peering för databricks.</span><span class="sxs-lookup"><span data-stu-id="2e661-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="2e661-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e661-110">PARAMETERS</span></span>

### <span data-ttu-id="2e661-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="2e661-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="2e661-112">Om den vidarebefordrade trafiken från datorerna i det lokala virtuella nätverket tillåts/inte är tillåten i det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="2e661-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="2e661-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="2e661-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="2e661-114">Om Gateway-länkar kan användas i virtuella fjärrnätverk för att länka till det här virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="2e661-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="2e661-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="2e661-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="2e661-116">Om de virtuella datorerna i det lokala virtuella nätverks utrymmet skulle kunna komma åt virtuella datorer i det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="2e661-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="2e661-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e661-117">-AsJob</span></span>
<span data-ttu-id="2e661-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="2e661-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2e661-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="2e661-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="2e661-120">En lista över adress block som reserveras för det här virtuella nätverket i CIDR-notation.</span><span class="sxs-lookup"><span data-stu-id="2e661-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e661-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2e661-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="2e661-122">ID för det databricks virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="2e661-122">The Id of the databricks virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e661-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e661-123">-DefaultProfile</span></span>
<span data-ttu-id="2e661-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e661-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e661-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e661-125">-Name</span></span>
<span data-ttu-id="2e661-126">Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="2e661-126">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e661-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2e661-127">-NoWait</span></span>
<span data-ttu-id="2e661-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="2e661-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2e661-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="2e661-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="2e661-130">En lista över adress block som reserveras för det här virtuella nätverket i CIDR-notation.</span><span class="sxs-lookup"><span data-stu-id="2e661-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e661-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2e661-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="2e661-132">ID för det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="2e661-132">The Id of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e661-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e661-133">-ResourceGroupName</span></span>
<span data-ttu-id="2e661-134">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2e661-134">The name of the resource group.</span></span>
<span data-ttu-id="2e661-135">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="2e661-135">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e661-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e661-136">-SubscriptionId</span></span>
<span data-ttu-id="2e661-137">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2e661-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e661-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="2e661-138">-UseRemoteGateway</span></span>
<span data-ttu-id="2e661-139">Om du kan använda Fjärrgateways i det här virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="2e661-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="2e661-140">Om flaggan är inställd på True och allowGatewayTransit på fjärr-peering också är sant, använder virtuella nätverk gateways för fjärrnätverk för överföring.</span><span class="sxs-lookup"><span data-stu-id="2e661-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="2e661-141">Endast en peering kan ha den här flaggan inställd på True.</span><span class="sxs-lookup"><span data-stu-id="2e661-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="2e661-142">Det går inte att ange den här flaggan om det redan finns en gateway för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="2e661-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="2e661-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2e661-143">-WorkspaceName</span></span>
<span data-ttu-id="2e661-144">Namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="2e661-144">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e661-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2e661-145">-Confirm</span></span>
<span data-ttu-id="2e661-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e661-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e661-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e661-147">-WhatIf</span></span>
<span data-ttu-id="2e661-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2e661-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e661-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2e661-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e661-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e661-150">CommonParameters</span></span>
<span data-ttu-id="2e661-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e661-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e661-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e661-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e661-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e661-153">INPUTS</span></span>

## <span data-ttu-id="2e661-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e661-154">OUTPUTS</span></span>

### <span data-ttu-id="2e661-155">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2e661-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="2e661-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e661-156">NOTES</span></span>

<span data-ttu-id="2e661-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2e661-157">ALIASES</span></span>

## <span data-ttu-id="2e661-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e661-158">RELATED LINKS</span></span>

