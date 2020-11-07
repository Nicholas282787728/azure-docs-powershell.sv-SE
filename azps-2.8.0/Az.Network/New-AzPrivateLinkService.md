---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 75c8f7b52fec0e429820d43f86a8a41798b1d5f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918218"
---
# <span data-ttu-id="7efe8-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7efe8-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="7efe8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7efe8-102">SYNOPSIS</span></span>
<span data-ttu-id="7efe8-103">Skapar en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="7efe8-103">Creates a private link service</span></span>

## <span data-ttu-id="7efe8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7efe8-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7efe8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7efe8-105">DESCRIPTION</span></span>
<span data-ttu-id="7efe8-106">Cmdleten **New-AzPrivateLinkService** skapar en privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="7efe8-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="7efe8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7efe8-107">EXAMPLES</span></span>

### <span data-ttu-id="7efe8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7efe8-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="7efe8-109">I det här exemplet skapas en privat länk tjänst.</span><span class="sxs-lookup"><span data-stu-id="7efe8-109">This example creates a private link service.</span></span>

## <span data-ttu-id="7efe8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7efe8-110">PARAMETERS</span></span>

### <span data-ttu-id="7efe8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7efe8-111">-AsJob</span></span>
<span data-ttu-id="7efe8-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7efe8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7efe8-113">-Autogodkännande</span><span class="sxs-lookup"><span data-stu-id="7efe8-113">-AutoApproval</span></span>
<span data-ttu-id="7efe8-114">Automatiska godkännande abonnemang för privata länkar</span><span class="sxs-lookup"><span data-stu-id="7efe8-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="7efe8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efe8-115">-DefaultProfile</span></span>
<span data-ttu-id="7efe8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7efe8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7efe8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7efe8-117">-Force</span></span>
<span data-ttu-id="7efe8-118">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="7efe8-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7efe8-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7efe8-119">-IpConfiguration</span></span>
<span data-ttu-id="7efe8-120">IP-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="7efe8-120">The ip configurations</span></span>

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

### <span data-ttu-id="7efe8-121">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7efe8-121">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="7efe8-122">Klient konfigurationerna front</span><span class="sxs-lookup"><span data-stu-id="7efe8-122">The front end ip configurations</span></span>

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

### <span data-ttu-id="7efe8-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="7efe8-123">-Location</span></span>
<span data-ttu-id="7efe8-124">plats.</span><span class="sxs-lookup"><span data-stu-id="7efe8-124">location.</span></span>

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

### <span data-ttu-id="7efe8-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="7efe8-125">-Name</span></span>
<span data-ttu-id="7efe8-126">Namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7efe8-126">The name of the service.</span></span>

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

### <span data-ttu-id="7efe8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7efe8-127">-ResourceGroupName</span></span>
<span data-ttu-id="7efe8-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="7efe8-128">The resource group name.</span></span>

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

### <span data-ttu-id="7efe8-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7efe8-129">-Tag</span></span>
<span data-ttu-id="7efe8-130">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7efe8-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7efe8-131">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="7efe8-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7efe8-132">-Synlighet</span><span class="sxs-lookup"><span data-stu-id="7efe8-132">-Visibility</span></span>
<span data-ttu-id="7efe8-133">Synlighets abonnemang för privat länk tjänst</span><span class="sxs-lookup"><span data-stu-id="7efe8-133">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="7efe8-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7efe8-134">-Confirm</span></span>
<span data-ttu-id="7efe8-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7efe8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7efe8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7efe8-136">-WhatIf</span></span>
<span data-ttu-id="7efe8-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7efe8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7efe8-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7efe8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7efe8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efe8-139">CommonParameters</span></span>
<span data-ttu-id="7efe8-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7efe8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efe8-141">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7efe8-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efe8-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7efe8-142">INPUTS</span></span>

### <span data-ttu-id="7efe8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7efe8-143">System.String</span></span>

### <span data-ttu-id="7efe8-144">Microsoft. Azure. commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="7efe8-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="7efe8-145">Microsoft. Azure. commands. Network. Models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="7efe8-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="7efe8-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7efe8-146">OUTPUTS</span></span>

### <span data-ttu-id="7efe8-147">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7efe8-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="7efe8-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7efe8-148">NOTES</span></span>

## <span data-ttu-id="7efe8-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7efe8-149">RELATED LINKS</span></span>

[<span data-ttu-id="7efe8-150">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7efe8-150">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="7efe8-151">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7efe8-151">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="7efe8-152">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7efe8-152">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
