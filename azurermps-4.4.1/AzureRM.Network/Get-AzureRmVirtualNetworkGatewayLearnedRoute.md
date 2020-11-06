---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: b6a4899fb54ffc4305f6b512046e00bda994b02e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578351"
---
# <span data-ttu-id="d12ba-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="d12ba-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="d12ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d12ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d12ba-103">Visar en lista över vägar som lärts av en Azure Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="d12ba-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d12ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d12ba-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d12ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d12ba-105">DESCRIPTION</span></span>
<span data-ttu-id="d12ba-106">Räknar upp vägar som upptäckts av en Azure-virtuell nätverksgateway från olika källor.</span><span class="sxs-lookup"><span data-stu-id="d12ba-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="d12ba-107">Detta inkluderar vägar som lärts via BGP samt statiska vägar.</span><span class="sxs-lookup"><span data-stu-id="d12ba-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="d12ba-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d12ba-108">EXAMPLES</span></span>

### <span data-ttu-id="d12ba-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d12ba-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.1.0.0/16
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       :
LocalAddress : 10.1.0.254
Network      : 10.0.0.254/32
NextHop      :
Origin       : Network
SourcePeer   : 10.1.0.254
Weight       : 32768

AsPath       : 65515
LocalAddress : 10.1.0.254
Network      : 10.0.0.0/16
NextHop      : 10.0.0.254
Origin       : EBgp
SourcePeer   : 10.0.0.254
Weight       : 32768
```

<span data-ttu-id="d12ba-110">För den Azure Virtual Network gateway som heter GatewayName i resurs grupp resourceGroup hämtar vägar som Azure Gateway känner till.</span><span class="sxs-lookup"><span data-stu-id="d12ba-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> 

<span data-ttu-id="d12ba-111">Den virtuella Azure-Nätverksgatewayen i det här fallet har två statiska vägar (10.1.0.0/16 och 10.0.0.254/32) samt en väg som upptäcks via BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="d12ba-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="d12ba-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d12ba-112">PARAMETERS</span></span>

### <span data-ttu-id="d12ba-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d12ba-113">-ResourceGroupName</span></span>
<span data-ttu-id="d12ba-114">Namn på resurs gruppen virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="d12ba-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="d12ba-115">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d12ba-115">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d12ba-116">Namn på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="d12ba-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12ba-117">-DefaultProfile</span></span>
<span data-ttu-id="d12ba-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d12ba-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d12ba-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12ba-119">CommonParameters</span></span>
<span data-ttu-id="d12ba-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d12ba-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12ba-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d12ba-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12ba-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d12ba-122">INPUTS</span></span>

### <span data-ttu-id="d12ba-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d12ba-123">System.String</span></span>

## <span data-ttu-id="d12ba-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d12ba-124">OUTPUTS</span></span>

### <span data-ttu-id="d12ba-125">Microsoft. Azure. commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="d12ba-125">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="d12ba-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d12ba-126">NOTES</span></span>

## <span data-ttu-id="d12ba-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d12ba-127">RELATED LINKS</span></span>

