---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 7d373092f850dd25abe5b6d913ddcf2572d4be94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324623"
---
# <span data-ttu-id="0ef0e-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="0ef0e-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="0ef0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ef0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef0e-103">Returnerar en server för belastnings Utjämnings adresser.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="0ef0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ef0e-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ef0e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ef0e-105">DESCRIPTION</span></span>
<span data-ttu-id="0ef0e-106">Returnerar en server för belastnings Utjämnings adresser.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-106">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="0ef0e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ef0e-107">EXAMPLES</span></span>

### <span data-ttu-id="0ef0e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0ef0e-108">Example 1</span></span>
### <span data-ttu-id="0ef0e-109">Exempel 2: ny Loadbalancer-adress konfiguration med virtuell nätverks referens</span><span class="sxs-lookup"><span data-stu-id="0ef0e-109">Example 2: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

## <span data-ttu-id="0ef0e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ef0e-110">PARAMETERS</span></span>

### <span data-ttu-id="0ef0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef0e-111">-DefaultProfile</span></span>
<span data-ttu-id="0ef0e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ef0e-113">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="0ef0e-113">-IpAddress</span></span>
<span data-ttu-id="0ef0e-114">Den IP-adress som ska läggas till i backend-poolen</span><span class="sxs-lookup"><span data-stu-id="0ef0e-114">The IPAddress to add to the backend pool</span></span>

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

### <span data-ttu-id="0ef0e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ef0e-115">-Name</span></span>
<span data-ttu-id="0ef0e-116">Namnet på Server delens konfiguration</span><span class="sxs-lookup"><span data-stu-id="0ef0e-116">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="0ef0e-117">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0ef0e-117">-VirtualNetworkId</span></span>
<span data-ttu-id="0ef0e-118">Det virtuella nätverk som är kopplat till Server dels adress konfiguration</span><span class="sxs-lookup"><span data-stu-id="0ef0e-118">The virtual network associated with Backend Address config</span></span>

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

### <span data-ttu-id="0ef0e-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0ef0e-119">-Confirm</span></span>
<span data-ttu-id="0ef0e-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ef0e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef0e-121">-WhatIf</span></span>
<span data-ttu-id="0ef0e-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ef0e-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ef0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef0e-124">CommonParameters</span></span>
<span data-ttu-id="0ef0e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef0e-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ef0e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef0e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ef0e-127">INPUTS</span></span>

### <span data-ttu-id="0ef0e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0ef0e-128">System.String</span></span>

### <span data-ttu-id="0ef0e-129">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0ef0e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="0ef0e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ef0e-130">OUTPUTS</span></span>

### <span data-ttu-id="0ef0e-131">Microsoft. Azure. commands. Networks. Models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="0ef0e-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="0ef0e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ef0e-132">NOTES</span></span>

## <span data-ttu-id="0ef0e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ef0e-133">RELATED LINKS</span></span>