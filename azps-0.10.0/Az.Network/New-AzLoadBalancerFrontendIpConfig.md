---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: ba29cef7afe862f8aeb33f66488e0970b5ac6e9c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922126"
---
# <span data-ttu-id="5ed94-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ed94-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="5ed94-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ed94-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed94-103">Skapar en front-IP-konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="5ed94-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="5ed94-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ed94-104">SYNTAX</span></span>

### <span data-ttu-id="5ed94-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="5ed94-105">SetByResourceSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ed94-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="5ed94-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ed94-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ed94-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ed94-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ed94-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ed94-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ed94-109">DESCRIPTION</span></span>
<span data-ttu-id="5ed94-110">Cmdleten **New-AzLoadBalancerFrontendIpConfig** skapar en front-IP-konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="5ed94-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="5ed94-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ed94-111">EXAMPLES</span></span>

### <span data-ttu-id="5ed94-112">Exempel 1: skapa en front-IP-konfiguration för belastningsutjämnaren</span><span class="sxs-lookup"><span data-stu-id="5ed94-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="5ed94-113">Det första kommandot skapar en dynamisk offentlig IP-adress med namnet MyPublicIP i resurs gruppen som heter MyResourceGroup och lagrar den sedan i $publicip variabel.</span><span class="sxs-lookup"><span data-stu-id="5ed94-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="5ed94-114">Det andra kommandot skapar en front-IP-konfiguration som heter FrontendIpConfig01 med den offentliga IP-adressen i $publicip.</span><span class="sxs-lookup"><span data-stu-id="5ed94-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="5ed94-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ed94-115">PARAMETERS</span></span>

### <span data-ttu-id="5ed94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed94-116">-DefaultProfile</span></span>
<span data-ttu-id="5ed94-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ed94-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed94-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ed94-118">-Name</span></span>
<span data-ttu-id="5ed94-119">Anger den frontend-IP-konfiguration som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="5ed94-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed94-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ed94-120">-PrivateIpAddress</span></span>
<span data-ttu-id="5ed94-121">Anger belastnings utjämningens privata IP-adress.</span><span class="sxs-lookup"><span data-stu-id="5ed94-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="5ed94-122">Ange endast den här parametern om du också anger *under nätets* parameter.</span><span class="sxs-lookup"><span data-stu-id="5ed94-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed94-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ed94-123">-PublicIpAddress</span></span>
<span data-ttu-id="5ed94-124">Anger det **PublicIpAddress** -objekt som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5ed94-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed94-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="5ed94-125">-PublicIpAddressId</span></span>
<span data-ttu-id="5ed94-126">Anger ID för det **PublicIpAddress** -objekt som ska kopplas till en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5ed94-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed94-127">-Undernät</span><span class="sxs-lookup"><span data-stu-id="5ed94-127">-Subnet</span></span>
<span data-ttu-id="5ed94-128">Anger det **under näts** objekt där du vill skapa en front-IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5ed94-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed94-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5ed94-129">-SubnetId</span></span>
<span data-ttu-id="5ed94-130">Anger ID för det undernät som du vill skapa en front-IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="5ed94-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ed94-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="5ed94-131">-Zone</span></span>
<span data-ttu-id="5ed94-132">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="5ed94-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="5ed94-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed94-133">CommonParameters</span></span>
<span data-ttu-id="5ed94-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ed94-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed94-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed94-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed94-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ed94-136">INPUTS</span></span>

## <span data-ttu-id="5ed94-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ed94-137">OUTPUTS</span></span>

### <span data-ttu-id="5ed94-138">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ed94-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="5ed94-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ed94-139">NOTES</span></span>

## <span data-ttu-id="5ed94-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ed94-140">RELATED LINKS</span></span>

[<span data-ttu-id="5ed94-141">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ed94-141">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5ed94-142">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ed94-142">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5ed94-143">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ed94-143">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="5ed94-144">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ed94-144">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5ed94-145">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ed94-145">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


