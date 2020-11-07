---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9a6879d2b5ad18c33ca53befd94d5e8dc03225df
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922125"
---
# <span data-ttu-id="8a807-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8a807-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="8a807-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a807-102">SYNOPSIS</span></span>

## <span data-ttu-id="8a807-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a807-103">SYNTAX</span></span>

### <span data-ttu-id="8a807-104">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a807-104">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> [-FrontendIpConfigurationId <String>]
 -Protocol <String> -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a807-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8a807-105">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a807-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a807-106">DESCRIPTION</span></span>

## <span data-ttu-id="8a807-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a807-107">EXAMPLES</span></span>

### <span data-ttu-id="8a807-108">9.1</span><span class="sxs-lookup"><span data-stu-id="8a807-108">1:</span></span>
```

```

## <span data-ttu-id="8a807-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a807-109">PARAMETERS</span></span>

### <span data-ttu-id="8a807-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8a807-110">-BackendPort</span></span>
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

### <span data-ttu-id="8a807-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a807-111">-DefaultProfile</span></span>
<span data-ttu-id="8a807-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a807-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a807-113">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a807-113">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="8a807-114">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8a807-114">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="8a807-115">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="8a807-115">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="8a807-116">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="8a807-116">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="8a807-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a807-117">-Name</span></span>
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

### <span data-ttu-id="8a807-118">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="8a807-118">-Protocol</span></span>
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

### <span data-ttu-id="8a807-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a807-119">CommonParameters</span></span>
<span data-ttu-id="8a807-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a807-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a807-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a807-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a807-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a807-122">INPUTS</span></span>

## <span data-ttu-id="8a807-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a807-123">OUTPUTS</span></span>

### <span data-ttu-id="8a807-124">Microsoft. Azure. commands. Networks. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="8a807-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="8a807-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a807-125">NOTES</span></span>

## <span data-ttu-id="8a807-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a807-126">RELATED LINKS</span></span>

