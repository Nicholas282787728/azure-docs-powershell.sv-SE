---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 77dbd80f03cb26adbb68e320d761200cd9ee7bc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576891"
---
# <span data-ttu-id="dd836-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd836-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="dd836-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd836-102">SYNOPSIS</span></span>
<span data-ttu-id="dd836-103">Skapar en front-IP-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="dd836-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd836-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd836-104">SYNTAX</span></span>

### <span data-ttu-id="dd836-105">SetByResourceSubnet (standard)</span><span class="sxs-lookup"><span data-stu-id="dd836-105">SetByResourceSubnet (Default)</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd836-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="dd836-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd836-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dd836-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd836-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dd836-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd836-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd836-109">DESCRIPTION</span></span>
<span data-ttu-id="dd836-110">Cmdleten **New-AzureRmLoadBalancerFrontendIpConfig** skapar en front-IP-konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="dd836-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="dd836-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd836-111">EXAMPLES</span></span>

### <span data-ttu-id="dd836-112">Exempel 1: skapa en front-IP-konfiguration för belastningsutjämnaren</span><span class="sxs-lookup"><span data-stu-id="dd836-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="dd836-113">Det första kommandot skapar en dynamisk offentlig IP-adress med namnet MyPublicIP i resurs gruppen som heter MyResourceGroup och lagrar den sedan i $publicip variabel.</span><span class="sxs-lookup"><span data-stu-id="dd836-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="dd836-114">Det andra kommandot skapar en front-IP-konfiguration som heter FrontendIpConfig01 med den offentliga IP-adressen i $publicip.</span><span class="sxs-lookup"><span data-stu-id="dd836-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="dd836-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd836-115">PARAMETERS</span></span>

### <span data-ttu-id="dd836-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd836-116">-DefaultProfile</span></span>
<span data-ttu-id="dd836-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd836-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd836-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="dd836-118">-Name</span></span>
<span data-ttu-id="dd836-119">Anger den frontend-IP-konfiguration som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="dd836-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="dd836-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="dd836-120">-PrivateIpAddress</span></span>
<span data-ttu-id="dd836-121">Anger belastnings utjämningens privata IP-adress.</span><span class="sxs-lookup"><span data-stu-id="dd836-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="dd836-122">Ange endast den här parametern om du också anger *under nätets* parameter.</span><span class="sxs-lookup"><span data-stu-id="dd836-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="dd836-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dd836-123">-PublicIpAddress</span></span>
<span data-ttu-id="dd836-124">Anger det **PublicIpAddress** -objekt som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd836-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="dd836-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="dd836-125">-PublicIpAddressId</span></span>
<span data-ttu-id="dd836-126">Anger ID för det **PublicIpAddress** -objekt som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd836-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="dd836-127">-Undernät</span><span class="sxs-lookup"><span data-stu-id="dd836-127">-Subnet</span></span>
<span data-ttu-id="dd836-128">Anger det **under näts** objekt där du vill skapa en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd836-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="dd836-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dd836-129">-SubnetId</span></span>
<span data-ttu-id="dd836-130">Anger ID för det undernät som du vill skapa en front-IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="dd836-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="dd836-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="dd836-131">-Zone</span></span>
<span data-ttu-id="dd836-132">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="dd836-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd836-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dd836-133">-Confirm</span></span>
<span data-ttu-id="dd836-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd836-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd836-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd836-135">-WhatIf</span></span>
<span data-ttu-id="dd836-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dd836-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd836-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dd836-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd836-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd836-138">CommonParameters</span></span>
<span data-ttu-id="dd836-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd836-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd836-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd836-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd836-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd836-141">INPUTS</span></span>

### <span data-ttu-id="dd836-142">System. Collections. Generic. list \` 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="dd836-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="dd836-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd836-143">OUTPUTS</span></span>

### <span data-ttu-id="dd836-144">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd836-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="dd836-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd836-145">NOTES</span></span>

## <span data-ttu-id="dd836-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd836-146">RELATED LINKS</span></span>

[<span data-ttu-id="dd836-147">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd836-147">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dd836-148">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd836-148">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dd836-149">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dd836-149">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="dd836-150">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd836-150">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dd836-151">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dd836-151">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


