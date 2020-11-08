---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 0b4cc79358723e6249a0c9d4e22929e224165402
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090989"
---
# <span data-ttu-id="f4e52-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f4e52-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="f4e52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4e52-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e52-103">Skapar en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="f4e52-103">Creates a private link service</span></span>

## <span data-ttu-id="f4e52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4e52-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4e52-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4e52-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e52-106">Cmdleten **New-AzPrivateLinkService** skapar en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="f4e52-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="f4e52-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4e52-107">EXAMPLES</span></span>

### <span data-ttu-id="f4e52-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f4e52-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="f4e52-109">I det här exemplet skapas en privat länk tjänst.</span><span class="sxs-lookup"><span data-stu-id="f4e52-109">This example creates a private link service.</span></span>

## <span data-ttu-id="f4e52-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4e52-110">PARAMETERS</span></span>

### <span data-ttu-id="f4e52-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4e52-111">-AsJob</span></span>
<span data-ttu-id="f4e52-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f4e52-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4e52-113">-Autogodkännande</span><span class="sxs-lookup"><span data-stu-id="f4e52-113">-AutoApproval</span></span>
<span data-ttu-id="f4e52-114">Automatiska godkännande abonnemang för privata länkar</span><span class="sxs-lookup"><span data-stu-id="f4e52-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="f4e52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e52-115">-DefaultProfile</span></span>
<span data-ttu-id="f4e52-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e52-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="f4e52-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="f4e52-118">Aktivera Proxy Protocol för den privata länk tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f4e52-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="f4e52-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f4e52-119">-Force</span></span>
<span data-ttu-id="f4e52-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="f4e52-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f4e52-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4e52-121">-IpConfiguration</span></span>
<span data-ttu-id="f4e52-122">IP-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="f4e52-122">The ip configurations</span></span>

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

### <span data-ttu-id="f4e52-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4e52-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="f4e52-124">Klient konfigurationerna front</span><span class="sxs-lookup"><span data-stu-id="f4e52-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="f4e52-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="f4e52-125">-Location</span></span>
<span data-ttu-id="f4e52-126">plats.</span><span class="sxs-lookup"><span data-stu-id="f4e52-126">location.</span></span>

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

### <span data-ttu-id="f4e52-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4e52-127">-Name</span></span>
<span data-ttu-id="f4e52-128">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f4e52-128">The name of the service.</span></span>

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

### <span data-ttu-id="f4e52-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e52-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4e52-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f4e52-130">The resource group name.</span></span>

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

### <span data-ttu-id="f4e52-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f4e52-131">-Tag</span></span>
<span data-ttu-id="f4e52-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f4e52-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f4e52-133">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="f4e52-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f4e52-134">-Synlighet</span><span class="sxs-lookup"><span data-stu-id="f4e52-134">-Visibility</span></span>
<span data-ttu-id="f4e52-135">Synlighets abonnemang för privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="f4e52-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="f4e52-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4e52-136">-Confirm</span></span>
<span data-ttu-id="f4e52-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4e52-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e52-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e52-138">-WhatIf</span></span>
<span data-ttu-id="f4e52-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4e52-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4e52-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4e52-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e52-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e52-141">CommonParameters</span></span>
<span data-ttu-id="f4e52-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e52-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e52-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4e52-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e52-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4e52-144">INPUTS</span></span>

### <span data-ttu-id="f4e52-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f4e52-145">System.String</span></span>

### <span data-ttu-id="f4e52-146">Microsoft. Azure. commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f4e52-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="f4e52-147">Microsoft. Azure. commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f4e52-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="f4e52-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4e52-148">OUTPUTS</span></span>

### <span data-ttu-id="f4e52-149">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f4e52-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="f4e52-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4e52-150">NOTES</span></span>

## <span data-ttu-id="f4e52-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4e52-151">RELATED LINKS</span></span>

[<span data-ttu-id="f4e52-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f4e52-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="f4e52-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f4e52-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="f4e52-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4e52-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
