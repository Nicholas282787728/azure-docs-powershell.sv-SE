---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryNetworkRule.md
ms.openlocfilehash: f60f85a14df42043352af1b71f0455983e03061a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319587"
---
# <span data-ttu-id="d4de0-101">New-AzContainerRegistryNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d4de0-101">New-AzContainerRegistryNetworkRule</span></span>

## <span data-ttu-id="d4de0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4de0-102">SYNOPSIS</span></span>
<span data-ttu-id="d4de0-103">Skapa en nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="d4de0-103">Create a network rule.</span></span>

## <span data-ttu-id="d4de0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4de0-104">SYNTAX</span></span>

### <span data-ttu-id="d4de0-105">ByVirtualNetworkRule (standard)</span><span class="sxs-lookup"><span data-stu-id="d4de0-105">ByVirtualNetworkRule (Default)</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-VirtualNetworkRule] -VirtualNetworkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4de0-106">ByIPRule</span><span class="sxs-lookup"><span data-stu-id="d4de0-106">ByIPRule</span></span>
```
New-AzContainerRegistryNetworkRule [-Action <String>] [-IPRule] -IPAddressOrRange <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4de0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4de0-107">DESCRIPTION</span></span>
<span data-ttu-id="d4de0-108">Skapa ett nätverks regel objekt i den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="d4de0-108">Create a network rule object in current powershell session.</span></span>

## <span data-ttu-id="d4de0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4de0-109">EXAMPLES</span></span>

### <span data-ttu-id="d4de0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d4de0-110">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
```

<span data-ttu-id="d4de0-111">Skapa en VirtualNetwork-regel uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d4de0-111">Create virtualnetwork rule set.</span></span>

## <span data-ttu-id="d4de0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4de0-112">PARAMETERS</span></span>

### <span data-ttu-id="d4de0-113">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="d4de0-113">-Action</span></span>
<span data-ttu-id="d4de0-114">Nätverks regelns funktion.</span><span class="sxs-lookup"><span data-stu-id="d4de0-114">The action of network rule.</span></span>

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

### <span data-ttu-id="d4de0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4de0-115">-DefaultProfile</span></span>
<span data-ttu-id="d4de0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4de0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4de0-117">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d4de0-117">-IPAddressOrRange</span></span>
<span data-ttu-id="d4de0-118">Anger IP-eller IP-adressintervallet i CIDR-format.</span><span class="sxs-lookup"><span data-stu-id="d4de0-118">Specifies the IP or IP range in CIDR format.</span></span>
<span data-ttu-id="d4de0-119">Endast IPV4-adresser tillåts.</span><span class="sxs-lookup"><span data-stu-id="d4de0-119">Only IPV4 address is allowed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4de0-120">-IPRule</span><span class="sxs-lookup"><span data-stu-id="d4de0-120">-IPRule</span></span>
<span data-ttu-id="d4de0-121">Ange för att skapa IPRule.</span><span class="sxs-lookup"><span data-stu-id="d4de0-121">Indicate to create IPRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByIPRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4de0-122">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d4de0-122">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="d4de0-123">Resurs-ID för ett undernät, till exempel:/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span><span class="sxs-lookup"><span data-stu-id="d4de0-123">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}/subnets/{subnetName}.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4de0-124">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d4de0-124">-VirtualNetworkRule</span></span>
<span data-ttu-id="d4de0-125">Ange för att skapa VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="d4de0-125">Indicate to create VirtualNetworkRule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVirtualNetworkRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4de0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4de0-126">CommonParameters</span></span>
<span data-ttu-id="d4de0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4de0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4de0-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4de0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4de0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4de0-129">INPUTS</span></span>

### <span data-ttu-id="d4de0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d4de0-130">System.String</span></span>

## <span data-ttu-id="d4de0-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4de0-131">OUTPUTS</span></span>

### <span data-ttu-id="d4de0-132">Microsoft. Azure. commands. ContainerRegistry. Models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d4de0-132">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="d4de0-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4de0-133">NOTES</span></span>

## <span data-ttu-id="d4de0-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4de0-134">RELATED LINKS</span></span>