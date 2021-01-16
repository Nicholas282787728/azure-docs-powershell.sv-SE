---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391595"
---
# <span data-ttu-id="18b80-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18b80-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="18b80-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18b80-102">SYNOPSIS</span></span>
<span data-ttu-id="18b80-103">Skapar en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="18b80-103">Creates a private link service</span></span>

## <span data-ttu-id="18b80-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18b80-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18b80-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18b80-105">DESCRIPTION</span></span>
<span data-ttu-id="18b80-106">Cmdleten **New-AzPrivateLinkService** skapar en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="18b80-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="18b80-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18b80-107">EXAMPLES</span></span>

### <span data-ttu-id="18b80-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="18b80-108">Example 1</span></span>

<span data-ttu-id="18b80-109">I följande exempel skapas en privat länk tjänst.</span><span class="sxs-lookup"><span data-stu-id="18b80-109">The following example creates a private link service.</span></span>

```powershell
$vnet = Get-AzVirtualNetwork -ResourceName 'myvnet' -ResourceGroupName 'myresourcegroup'
# View the results of $vnet and change 'mysubnet' in the following line to the appropriate subnet name.
$subnet = $vnet | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mysubnet'
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -Subnet $subnet -PrivateIpAddress '10.0.0.5'
$publicip = Get-AzPublicIpAddress -ResourceGroupName 'myresourcegroup'
$frontend = New-AzLoadBalancerFrontendIpConfig -Name 'FrontendIpConfig01' -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name 'MyLoadBalancer' -ResourceGroupName 'myresourcegroup' -Location 'West US' -FrontendIpConfiguration $frontend
New-AzPrivateLinkService -Name 'mypls' -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

## <span data-ttu-id="18b80-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18b80-110">PARAMETERS</span></span>

### <span data-ttu-id="18b80-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18b80-111">-AsJob</span></span>
<span data-ttu-id="18b80-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="18b80-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18b80-113">-Autogodkännande</span><span class="sxs-lookup"><span data-stu-id="18b80-113">-AutoApproval</span></span>
<span data-ttu-id="18b80-114">Automatiska godkännande abonnemang för privata länkar</span><span class="sxs-lookup"><span data-stu-id="18b80-114">The auto approval subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b80-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b80-115">-DefaultProfile</span></span>
<span data-ttu-id="18b80-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18b80-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b80-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="18b80-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="18b80-118">Aktivera Proxy Protocol för den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="18b80-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="18b80-119">-Force</span><span class="sxs-lookup"><span data-stu-id="18b80-119">-Force</span></span>
<span data-ttu-id="18b80-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="18b80-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="18b80-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="18b80-121">-IpConfiguration</span></span>
<span data-ttu-id="18b80-122">IP-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="18b80-122">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b80-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="18b80-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="18b80-124">Klient konfigurationerna front</span><span class="sxs-lookup"><span data-stu-id="18b80-124">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b80-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="18b80-125">-Location</span></span>
<span data-ttu-id="18b80-126">plats.</span><span class="sxs-lookup"><span data-stu-id="18b80-126">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b80-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="18b80-127">-Name</span></span>
<span data-ttu-id="18b80-128">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="18b80-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b80-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b80-129">-ResourceGroupName</span></span>
<span data-ttu-id="18b80-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="18b80-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b80-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="18b80-131">-Tag</span></span>
<span data-ttu-id="18b80-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="18b80-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="18b80-133">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="18b80-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b80-134">-Synlighet</span><span class="sxs-lookup"><span data-stu-id="18b80-134">-Visibility</span></span>
<span data-ttu-id="18b80-135">Synlighets abonnemang för privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="18b80-135">The visibility subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b80-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18b80-136">-Confirm</span></span>
<span data-ttu-id="18b80-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18b80-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18b80-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b80-138">-WhatIf</span></span>
<span data-ttu-id="18b80-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18b80-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18b80-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18b80-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18b80-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b80-141">CommonParameters</span></span>
<span data-ttu-id="18b80-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b80-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b80-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18b80-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b80-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18b80-144">INPUTS</span></span>

### <span data-ttu-id="18b80-145">System. String</span><span class="sxs-lookup"><span data-stu-id="18b80-145">System.String</span></span>

### <span data-ttu-id="18b80-146">Microsoft. Azure. commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="18b80-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="18b80-147">Microsoft. Azure. commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="18b80-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="18b80-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18b80-148">OUTPUTS</span></span>

### <span data-ttu-id="18b80-149">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18b80-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="18b80-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18b80-150">NOTES</span></span>

## <span data-ttu-id="18b80-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18b80-151">RELATED LINKS</span></span>

[<span data-ttu-id="18b80-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18b80-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="18b80-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="18b80-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="18b80-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="18b80-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
