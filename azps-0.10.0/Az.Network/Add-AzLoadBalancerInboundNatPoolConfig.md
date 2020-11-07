---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a5cd44d1b4b7ac1a1494047affa721dd21d85919
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922409"
---
# <span data-ttu-id="9c21c-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9c21c-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="9c21c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c21c-102">SYNOPSIS</span></span>

## <span data-ttu-id="9c21c-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c21c-103">SYNTAX</span></span>

### <span data-ttu-id="9c21c-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c21c-104">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c21c-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9c21c-105">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c21c-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c21c-106">DESCRIPTION</span></span>

## <span data-ttu-id="9c21c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c21c-107">EXAMPLES</span></span>

### <span data-ttu-id="9c21c-108">9.1</span><span class="sxs-lookup"><span data-stu-id="9c21c-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="9c21c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c21c-109">PARAMETERS</span></span>

### <span data-ttu-id="9c21c-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9c21c-110">-BackendPort</span></span>
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

### <span data-ttu-id="9c21c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c21c-111">-DefaultProfile</span></span>
<span data-ttu-id="9c21c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c21c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c21c-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c21c-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="9c21c-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9c21c-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="9c21c-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="9c21c-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="9c21c-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="9c21c-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="9c21c-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c21c-117">-LoadBalancer</span></span>
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

### <span data-ttu-id="9c21c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c21c-118">-Name</span></span>
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

### <span data-ttu-id="9c21c-119">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9c21c-119">-Protocol</span></span>
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

### <span data-ttu-id="9c21c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c21c-120">CommonParameters</span></span>
<span data-ttu-id="9c21c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c21c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c21c-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c21c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c21c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c21c-123">INPUTS</span></span>

### <span data-ttu-id="9c21c-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c21c-124">PSLoadBalancer</span></span>
<span data-ttu-id="9c21c-125">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9c21c-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9c21c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c21c-126">OUTPUTS</span></span>

### <span data-ttu-id="9c21c-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9c21c-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9c21c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c21c-128">NOTES</span></span>

## <span data-ttu-id="9c21c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c21c-129">RELATED LINKS</span></span>

