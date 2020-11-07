---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf99aba02bc4dee18ec6cfd2bdaf9fd83036e6d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924214"
---
# <span data-ttu-id="c98a3-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c98a3-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c98a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c98a3-102">SYNOPSIS</span></span>

## <span data-ttu-id="c98a3-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c98a3-103">SYNTAX</span></span>

### <span data-ttu-id="c98a3-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c98a3-104">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c98a3-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c98a3-105">SetByResource</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c98a3-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c98a3-106">DESCRIPTION</span></span>

## <span data-ttu-id="c98a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c98a3-107">EXAMPLES</span></span>

### <span data-ttu-id="c98a3-108">9.1</span><span class="sxs-lookup"><span data-stu-id="c98a3-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c98a3-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c98a3-109">PARAMETERS</span></span>

### <span data-ttu-id="c98a3-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c98a3-110">-BackendPort</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98a3-111">-DefaultProfile</span></span>
<span data-ttu-id="c98a3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c98a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c98a3-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c98a3-113">-FrontendIpConfiguration</span></span>
```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a3-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c98a3-114">-FrontendIpConfigurationId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a3-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="c98a3-115">-FrontendPortRangeEnd</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a3-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="c98a3-116">-FrontendPortRangeStart</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a3-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c98a3-117">-LoadBalancer</span></span>
```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c98a3-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c98a3-118">-Name</span></span>
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

### <span data-ttu-id="c98a3-119">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c98a3-119">-Protocol</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98a3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98a3-120">CommonParameters</span></span>
<span data-ttu-id="c98a3-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98a3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98a3-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c98a3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98a3-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c98a3-123">INPUTS</span></span>

### <span data-ttu-id="c98a3-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c98a3-124">PSLoadBalancer</span></span>
<span data-ttu-id="c98a3-125">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c98a3-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c98a3-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c98a3-126">OUTPUTS</span></span>

### <span data-ttu-id="c98a3-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c98a3-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c98a3-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c98a3-128">NOTES</span></span>

## <span data-ttu-id="c98a3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c98a3-129">RELATED LINKS</span></span>

[<span data-ttu-id="c98a3-130">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c98a3-130">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c98a3-131">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c98a3-131">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c98a3-132">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c98a3-132">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c98a3-133">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c98a3-133">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)


