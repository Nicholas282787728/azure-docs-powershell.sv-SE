---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 0ac64d9b1aee363a1681b8d62da2ecf73574f7cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260710"
---
# <span data-ttu-id="5c356-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5c356-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="5c356-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c356-102">SYNOPSIS</span></span>
<span data-ttu-id="5c356-103">Skapar en VirtualNetworkTap-resurs.</span><span class="sxs-lookup"><span data-stu-id="5c356-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="5c356-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c356-104">SYNTAX</span></span>

### <span data-ttu-id="5c356-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="5c356-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c356-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c356-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c356-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c356-107">DESCRIPTION</span></span>
<span data-ttu-id="5c356-108">Cmdleten **New-AzVirtualNetworkTap** skapar ett Azure Virtual Network-tryck resurs.</span><span class="sxs-lookup"><span data-stu-id="5c356-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="5c356-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c356-109">EXAMPLES</span></span>

### <span data-ttu-id="5c356-110">Exempel 1: skapa ett virtuellt Azure-nätverk tryck på</span><span class="sxs-lookup"><span data-stu-id="5c356-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="5c356-111">Det här kommandot skapar ett virtuellt nätverk genom att trycka på "VirtualNetworkTap1" som har mål dator konfigurations information (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="5c356-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="5c356-112">All källa som är konfigurerad för den virtuella datorns trafik dirigeras till den här mål-IP +-porten.</span><span class="sxs-lookup"><span data-stu-id="5c356-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="5c356-113">Exempel 2: skapa ett virtuellt Azure-nätverk tryck på Använd LoadBalancer-IP</span><span class="sxs-lookup"><span data-stu-id="5c356-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="5c356-114">Det här kommandot skapar ett virtuellt nätverk genom att trycka på "VirtualNetworkTap1", som har mål dator konfigurations detaljer (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="5c356-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="5c356-115">All källa för att trycka på konfigurerad virtuell dator trafik dirigeras till denna LoadBalancer IpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c356-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="5c356-116">Standard mål porten är 4789.</span><span class="sxs-lookup"><span data-stu-id="5c356-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="5c356-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c356-117">PARAMETERS</span></span>

### <span data-ttu-id="5c356-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c356-118">-AsJob</span></span>
<span data-ttu-id="5c356-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5c356-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c356-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c356-120">-DefaultProfile</span></span>
<span data-ttu-id="5c356-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c356-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c356-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c356-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="5c356-123">Referensen för mål belastnings utjämningens klient konfigurations resurs.</span><span class="sxs-lookup"><span data-stu-id="5c356-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c356-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5c356-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="5c356-125">Referensen för mål belastnings utjämningens klient konfigurations resurs.</span><span class="sxs-lookup"><span data-stu-id="5c356-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c356-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c356-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="5c356-127">Referens för mål nätverks gränssnittets IP-konfigurationsfil.</span><span class="sxs-lookup"><span data-stu-id="5c356-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c356-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5c356-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="5c356-129">Referens för mål nätverks gränssnittets IP-konfigurationsfil.</span><span class="sxs-lookup"><span data-stu-id="5c356-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c356-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="5c356-130">-DestinationPort</span></span>
<span data-ttu-id="5c356-131">Paket uppsamlarens målport</span><span class="sxs-lookup"><span data-stu-id="5c356-131">The Destination Port of the packet collector</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c356-132">-Force</span><span class="sxs-lookup"><span data-stu-id="5c356-132">-Force</span></span>
<span data-ttu-id="5c356-133">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="5c356-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5c356-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="5c356-134">-Location</span></span>
<span data-ttu-id="5c356-135">Platsen.</span><span class="sxs-lookup"><span data-stu-id="5c356-135">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c356-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c356-136">-Name</span></span>
<span data-ttu-id="5c356-137">Namnet på tryckningen.</span><span class="sxs-lookup"><span data-stu-id="5c356-137">The name of the tap.</span></span>

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

### <span data-ttu-id="5c356-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c356-138">-ResourceGroupName</span></span>
<span data-ttu-id="5c356-139">Resurs grupps namnet för det virtuella nätverkets tryck.</span><span class="sxs-lookup"><span data-stu-id="5c356-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="5c356-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5c356-140">-Tag</span></span>
<span data-ttu-id="5c356-141">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="5c356-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5c356-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c356-142">-Confirm</span></span>
<span data-ttu-id="5c356-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c356-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c356-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c356-144">-WhatIf</span></span>
<span data-ttu-id="5c356-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c356-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c356-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c356-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c356-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c356-147">CommonParameters</span></span>
<span data-ttu-id="5c356-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c356-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c356-149">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c356-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c356-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c356-150">INPUTS</span></span>

### <span data-ttu-id="5c356-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5c356-151">System.String</span></span>

### <span data-ttu-id="5c356-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5c356-152">System.Int32</span></span>

### <span data-ttu-id="5c356-153">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5c356-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5c356-154">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c356-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="5c356-155">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c356-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="5c356-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c356-156">OUTPUTS</span></span>

### <span data-ttu-id="5c356-157">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5c356-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="5c356-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c356-158">NOTES</span></span>

## <span data-ttu-id="5c356-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c356-159">RELATED LINKS</span></span>

[<span data-ttu-id="5c356-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5c356-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="5c356-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5c356-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="5c356-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5c356-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
