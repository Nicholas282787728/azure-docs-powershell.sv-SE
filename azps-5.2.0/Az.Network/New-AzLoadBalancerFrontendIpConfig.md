---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 5b5ca651442a0150461da64bb5e33a37167fec3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392536"
---
# <span data-ttu-id="9abe5-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9abe5-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="9abe5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9abe5-102">SYNOPSIS</span></span>
<span data-ttu-id="9abe5-103">Skapar en front-IP-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="9abe5-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="9abe5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9abe5-104">SYNTAX</span></span>

### <span data-ttu-id="9abe5-105">SetByResourceSubnet (standard)</span><span class="sxs-lookup"><span data-stu-id="9abe5-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abe5-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="9abe5-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abe5-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9abe5-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abe5-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9abe5-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abe5-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9abe5-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abe5-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9abe5-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9abe5-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9abe5-111">DESCRIPTION</span></span>
<span data-ttu-id="9abe5-112">Cmdleten **New-AzLoadBalancerFrontendIpConfig** skapar en front-IP-konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="9abe5-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9abe5-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9abe5-113">EXAMPLES</span></span>

### <span data-ttu-id="9abe5-114">Exempel 1: skapa en front-IP-konfiguration för belastningsutjämnaren</span><span class="sxs-lookup"><span data-stu-id="9abe5-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="9abe5-115">Det första kommandot skapar en dynamisk offentlig IP-adress med namnet MyPublicIP i resurs gruppen som heter MyResourceGroup och lagrar den sedan i $publicip variabel.</span><span class="sxs-lookup"><span data-stu-id="9abe5-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="9abe5-116">Det andra kommandot skapar en front-IP-konfiguration som heter FrontendIpConfig01 med den offentliga IP-adressen i $publicip.</span><span class="sxs-lookup"><span data-stu-id="9abe5-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="9abe5-117">Exempel 2: skapa en front-IP-konfiguration för belastningsutjämnaren med prefix</span><span class="sxs-lookup"><span data-stu-id="9abe5-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="9abe5-118">Det första kommandot skapar ett offentlig IP-prefix med namnet MyPublicIP med längden 28 i resurs gruppen med namnet MyResourceGroup och lagrar sedan den i $publicipprefix variabel.</span><span class="sxs-lookup"><span data-stu-id="9abe5-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="9abe5-119">Det andra kommandot skapar en front-IP-konfiguration med namnet FrontendIpConfig01 med hjälp av det offentliga IP-prefixet i $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="9abe5-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="9abe5-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9abe5-120">PARAMETERS</span></span>

### <span data-ttu-id="9abe5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abe5-121">-DefaultProfile</span></span>
<span data-ttu-id="9abe5-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9abe5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9abe5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9abe5-123">-Name</span></span>
<span data-ttu-id="9abe5-124">Anger den frontend-IP-konfiguration som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="9abe5-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9abe5-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9abe5-125">-PrivateIpAddress</span></span>
<span data-ttu-id="9abe5-126">Anger belastnings utjämningens privata IP-adress.</span><span class="sxs-lookup"><span data-stu-id="9abe5-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="9abe5-127">Ange endast den här parametern om du också anger *under nätets* parameter.</span><span class="sxs-lookup"><span data-stu-id="9abe5-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abe5-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9abe5-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="9abe5-129">Den privata IP-adressen för IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9abe5-129">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abe5-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9abe5-130">-PublicIpAddress</span></span>
<span data-ttu-id="9abe5-131">Anger det **PublicIpAddress** -objekt som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9abe5-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abe5-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9abe5-132">-PublicIpAddressId</span></span>
<span data-ttu-id="9abe5-133">Anger ID för det **PublicIpAddress** -objekt som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9abe5-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abe5-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9abe5-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="9abe5-135">Anger det **PublicIpAddressPrefix** -objekt som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9abe5-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abe5-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="9abe5-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="9abe5-137">Anger ID för det **PublicIpAddressPrefix** -objekt som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9abe5-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abe5-138">-Undernät</span><span class="sxs-lookup"><span data-stu-id="9abe5-138">-Subnet</span></span>
<span data-ttu-id="9abe5-139">Anger det **under näts** objekt där du vill skapa en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9abe5-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abe5-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9abe5-140">-SubnetId</span></span>
<span data-ttu-id="9abe5-141">Anger ID för det undernät som du vill skapa en front-IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="9abe5-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abe5-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="9abe5-142">-Zone</span></span>
<span data-ttu-id="9abe5-143">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="9abe5-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="9abe5-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9abe5-144">-Confirm</span></span>
<span data-ttu-id="9abe5-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9abe5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9abe5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9abe5-146">-WhatIf</span></span>
<span data-ttu-id="9abe5-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9abe5-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9abe5-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9abe5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9abe5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abe5-149">CommonParameters</span></span>
<span data-ttu-id="9abe5-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9abe5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abe5-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9abe5-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abe5-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9abe5-152">INPUTS</span></span>

### <span data-ttu-id="9abe5-153">System. String</span><span class="sxs-lookup"><span data-stu-id="9abe5-153">System.String</span></span>

### <span data-ttu-id="9abe5-154">System. string []</span><span class="sxs-lookup"><span data-stu-id="9abe5-154">System.String[]</span></span>

### <span data-ttu-id="9abe5-155">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="9abe5-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="9abe5-156">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9abe5-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="9abe5-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9abe5-157">OUTPUTS</span></span>

### <span data-ttu-id="9abe5-158">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9abe5-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="9abe5-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9abe5-159">NOTES</span></span>

## <span data-ttu-id="9abe5-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9abe5-160">RELATED LINKS</span></span>

[<span data-ttu-id="9abe5-161">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9abe5-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9abe5-162">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9abe5-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9abe5-163">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9abe5-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="9abe5-164">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9abe5-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9abe5-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9abe5-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


