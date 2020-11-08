---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101042"
---
# <span data-ttu-id="89e6c-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="89e6c-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="89e6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="89e6c-103">Skapar virtuellt nätverk för arbets yta.</span><span class="sxs-lookup"><span data-stu-id="89e6c-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="89e6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89e6c-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="89e6c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="89e6c-106">Skapar virtuellt nätverk för arbets yta.</span><span class="sxs-lookup"><span data-stu-id="89e6c-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="89e6c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="89e6c-108">Exempel 1: skapa en VNet-peering för databricks</span><span class="sxs-lookup"><span data-stu-id="89e6c-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="89e6c-109">Det här kommandot skapar en VNet-peering för databricks.</span><span class="sxs-lookup"><span data-stu-id="89e6c-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="89e6c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89e6c-110">PARAMETERS</span></span>

### <span data-ttu-id="89e6c-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="89e6c-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="89e6c-112">Om den vidarebefordrade trafiken från datorerna i det lokala virtuella nätverket tillåts/inte är tillåten i det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="89e6c-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="89e6c-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="89e6c-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="89e6c-114">Om Gateway-länkar kan användas i virtuella fjärrnätverk för att länka till det här virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="89e6c-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="89e6c-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="89e6c-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="89e6c-116">Om de virtuella datorerna i det lokala virtuella nätverks utrymmet skulle kunna komma åt virtuella datorer i det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="89e6c-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="89e6c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89e6c-117">-AsJob</span></span>
<span data-ttu-id="89e6c-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="89e6c-118">Run the command as a job</span></span>

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

### <span data-ttu-id="89e6c-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="89e6c-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="89e6c-120">En lista över adress block som reserveras för det här virtuella nätverket i CIDR-notation.</span><span class="sxs-lookup"><span data-stu-id="89e6c-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="89e6c-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="89e6c-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="89e6c-122">ID för det databricks virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="89e6c-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="89e6c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e6c-123">-DefaultProfile</span></span>
<span data-ttu-id="89e6c-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89e6c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89e6c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="89e6c-125">-Name</span></span>
<span data-ttu-id="89e6c-126">Namnet på arbets ytans vNet-peering.</span><span class="sxs-lookup"><span data-stu-id="89e6c-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="89e6c-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="89e6c-127">-NoWait</span></span>
<span data-ttu-id="89e6c-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="89e6c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="89e6c-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="89e6c-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="89e6c-130">En lista över adress block som reserveras för det här virtuella nätverket i CIDR-notation.</span><span class="sxs-lookup"><span data-stu-id="89e6c-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="89e6c-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="89e6c-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="89e6c-132">ID för det virtuella fjärrnätverket.</span><span class="sxs-lookup"><span data-stu-id="89e6c-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="89e6c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89e6c-133">-ResourceGroupName</span></span>
<span data-ttu-id="89e6c-134">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="89e6c-134">The name of the resource group.</span></span>
<span data-ttu-id="89e6c-135">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="89e6c-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="89e6c-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89e6c-136">-SubscriptionId</span></span>
<span data-ttu-id="89e6c-137">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="89e6c-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="89e6c-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="89e6c-138">-UseRemoteGateway</span></span>
<span data-ttu-id="89e6c-139">Om du kan använda Fjärrgateways i det här virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="89e6c-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="89e6c-140">Om flaggan är inställd på True och allowGatewayTransit på fjärr-peering också är sant, använder virtuella nätverk gateways för fjärrnätverk för överföring.</span><span class="sxs-lookup"><span data-stu-id="89e6c-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="89e6c-141">Endast en peering kan ha den här flaggan inställd på True.</span><span class="sxs-lookup"><span data-stu-id="89e6c-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="89e6c-142">Det går inte att ange den här flaggan om det redan finns en gateway för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="89e6c-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="89e6c-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89e6c-143">-WorkspaceName</span></span>
<span data-ttu-id="89e6c-144">Namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="89e6c-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="89e6c-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89e6c-145">-Confirm</span></span>
<span data-ttu-id="89e6c-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89e6c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e6c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e6c-147">-WhatIf</span></span>
<span data-ttu-id="89e6c-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89e6c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89e6c-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89e6c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89e6c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e6c-150">CommonParameters</span></span>
<span data-ttu-id="89e6c-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e6c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e6c-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89e6c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e6c-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89e6c-153">INPUTS</span></span>

## <span data-ttu-id="89e6c-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89e6c-154">OUTPUTS</span></span>

### <span data-ttu-id="89e6c-155">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="89e6c-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="89e6c-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89e6c-156">NOTES</span></span>

<span data-ttu-id="89e6c-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="89e6c-157">ALIASES</span></span>

## <span data-ttu-id="89e6c-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89e6c-158">RELATED LINKS</span></span>

