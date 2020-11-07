---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 247470ee878a37968cd690d27f8e5e16047febbd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929706"
---
# <span data-ttu-id="d8c15-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d8c15-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d8c15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8c15-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8c15-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8c15-103">SYNTAX</span></span>

### <span data-ttu-id="d8c15-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8c15-104">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8c15-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d8c15-105">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8c15-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8c15-106">DESCRIPTION</span></span>

## <span data-ttu-id="d8c15-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8c15-107">EXAMPLES</span></span>

### <span data-ttu-id="d8c15-108">9.1</span><span class="sxs-lookup"><span data-stu-id="d8c15-108">1:</span></span>
```

```

## <span data-ttu-id="d8c15-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8c15-109">PARAMETERS</span></span>

### <span data-ttu-id="d8c15-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d8c15-110">-BackendPort</span></span>
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

### <span data-ttu-id="d8c15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c15-111">-DefaultProfile</span></span>
<span data-ttu-id="d8c15-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8c15-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8c15-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8c15-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="d8c15-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d8c15-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="d8c15-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="d8c15-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="d8c15-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="d8c15-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="d8c15-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8c15-117">-Name</span></span>
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

### <span data-ttu-id="d8c15-118">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d8c15-118">-Protocol</span></span>
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

### <span data-ttu-id="d8c15-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c15-119">CommonParameters</span></span>
<span data-ttu-id="d8c15-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8c15-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c15-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8c15-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c15-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8c15-122">INPUTS</span></span>

## <span data-ttu-id="d8c15-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8c15-123">OUTPUTS</span></span>

### <span data-ttu-id="d8c15-124">Microsoft. Azure. commands. Networks. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="d8c15-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="d8c15-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8c15-125">NOTES</span></span>

## <span data-ttu-id="d8c15-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8c15-126">RELATED LINKS</span></span>

