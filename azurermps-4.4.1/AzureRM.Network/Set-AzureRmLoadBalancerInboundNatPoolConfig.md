---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 60e4d4dc6ffd095177a4bf53fdea816019a3aff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575979"
---
# <span data-ttu-id="0bb67-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0bb67-101">Set-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="0bb67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0bb67-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bb67-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0bb67-103">SYNTAX</span></span>

### <span data-ttu-id="0bb67-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0bb67-104">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0bb67-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0bb67-105">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bb67-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0bb67-106">DESCRIPTION</span></span>

## <span data-ttu-id="0bb67-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0bb67-107">EXAMPLES</span></span>

### <span data-ttu-id="0bb67-108">9.1</span><span class="sxs-lookup"><span data-stu-id="0bb67-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0bb67-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0bb67-109">PARAMETERS</span></span>

### <span data-ttu-id="0bb67-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0bb67-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb67-111">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0bb67-111">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb67-112">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0bb67-112">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb67-113">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="0bb67-113">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb67-114">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="0bb67-114">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb67-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bb67-115">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bb67-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0bb67-116">-Name</span></span>
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

### <span data-ttu-id="0bb67-117">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0bb67-117">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb67-118">-DefaultProfile</span></span>
<span data-ttu-id="0bb67-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb67-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bb67-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb67-120">CommonParameters</span></span>
<span data-ttu-id="0bb67-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb67-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb67-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb67-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb67-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0bb67-123">INPUTS</span></span>

### <span data-ttu-id="0bb67-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bb67-124">PSLoadBalancer</span></span>
<span data-ttu-id="0bb67-125">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0bb67-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0bb67-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0bb67-126">OUTPUTS</span></span>

### <span data-ttu-id="0bb67-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0bb67-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0bb67-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0bb67-128">NOTES</span></span>

## <span data-ttu-id="0bb67-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0bb67-129">RELATED LINKS</span></span>

[<span data-ttu-id="0bb67-130">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0bb67-130">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="0bb67-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0bb67-131">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="0bb67-132">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0bb67-132">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./New-AzureRmLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="0bb67-133">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0bb67-133">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatPoolConfig.md)


