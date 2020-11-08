---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: dc28df7630cbb2c9e239fe31f99ad3361e5c1f54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918262"
---
# <span data-ttu-id="0e337-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e337-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="0e337-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e337-102">SYNOPSIS</span></span>
<span data-ttu-id="0e337-103">Skapar en front-IP-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="0e337-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="0e337-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e337-104">SYNTAX</span></span>

### <span data-ttu-id="0e337-105">SetByResourceSubnet (standard)</span><span class="sxs-lookup"><span data-stu-id="0e337-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e337-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="0e337-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e337-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e337-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e337-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e337-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e337-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e337-109">DESCRIPTION</span></span>
<span data-ttu-id="0e337-110">Cmdleten **New-AzLoadBalancerFrontendIpConfig** skapar en front-IP-konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="0e337-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0e337-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e337-111">EXAMPLES</span></span>

### <span data-ttu-id="0e337-112">Exempel 1: skapa en front-IP-konfiguration för belastningsutjämnaren</span><span class="sxs-lookup"><span data-stu-id="0e337-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="0e337-113">Det första kommandot skapar en dynamisk offentlig IP-adress med namnet MyPublicIP i resurs gruppen som heter MyResourceGroup och lagrar den sedan i $publicip variabel.</span><span class="sxs-lookup"><span data-stu-id="0e337-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="0e337-114">Det andra kommandot skapar en front-IP-konfiguration som heter FrontendIpConfig01 med den offentliga IP-adressen i $publicip.</span><span class="sxs-lookup"><span data-stu-id="0e337-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="0e337-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e337-115">PARAMETERS</span></span>

### <span data-ttu-id="0e337-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e337-116">-DefaultProfile</span></span>
<span data-ttu-id="0e337-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e337-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e337-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e337-118">-Name</span></span>
<span data-ttu-id="0e337-119">Anger den frontend-IP-konfiguration som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="0e337-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0e337-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e337-120">-PrivateIpAddress</span></span>
<span data-ttu-id="0e337-121">Anger belastnings utjämningens privata IP-adress.</span><span class="sxs-lookup"><span data-stu-id="0e337-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="0e337-122">Ange endast den här parametern om du också anger *under nätets* parameter.</span><span class="sxs-lookup"><span data-stu-id="0e337-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="0e337-123">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="0e337-123">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="0e337-124">Den privata IP-adressen för IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="0e337-124">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="0e337-125">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e337-125">-PublicIpAddress</span></span>
<span data-ttu-id="0e337-126">Anger det **PublicIpAddress** -objekt som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e337-126">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0e337-127">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="0e337-127">-PublicIpAddressId</span></span>
<span data-ttu-id="0e337-128">Anger ID för det **PublicIpAddress** -objekt som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e337-128">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0e337-129">-Undernät</span><span class="sxs-lookup"><span data-stu-id="0e337-129">-Subnet</span></span>
<span data-ttu-id="0e337-130">Anger det **under näts** objekt där du vill skapa en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e337-130">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0e337-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0e337-131">-SubnetId</span></span>
<span data-ttu-id="0e337-132">Anger ID för det undernät som du vill skapa en front-IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="0e337-132">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="0e337-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="0e337-133">-Zone</span></span>
<span data-ttu-id="0e337-134">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="0e337-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="0e337-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e337-135">-Confirm</span></span>
<span data-ttu-id="0e337-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e337-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e337-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e337-137">-WhatIf</span></span>
<span data-ttu-id="0e337-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e337-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e337-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e337-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e337-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e337-140">CommonParameters</span></span>
<span data-ttu-id="0e337-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e337-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e337-142">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e337-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e337-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e337-143">INPUTS</span></span>

### <span data-ttu-id="0e337-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0e337-144">System.String</span></span>

### <span data-ttu-id="0e337-145">System. string []</span><span class="sxs-lookup"><span data-stu-id="0e337-145">System.String[]</span></span>

### <span data-ttu-id="0e337-146">Microsoft. Azure. commands. Networks. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="0e337-146">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="0e337-147">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e337-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="0e337-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e337-148">OUTPUTS</span></span>

### <span data-ttu-id="0e337-149">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e337-149">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="0e337-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e337-150">NOTES</span></span>

## <span data-ttu-id="0e337-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e337-151">RELATED LINKS</span></span>

[<span data-ttu-id="0e337-152">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e337-152">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0e337-153">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e337-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0e337-154">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e337-154">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="0e337-155">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e337-155">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="0e337-156">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e337-156">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

