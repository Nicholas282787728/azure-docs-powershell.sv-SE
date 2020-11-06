---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 7c356a3f27959ccb0dd3160b8b984b304eac647d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576898"
---
# <span data-ttu-id="d63cb-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="d63cb-101">Get-AzureRmVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="d63cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d63cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d63cb-103">Visar en lista över vägar som lärts av en Azure Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="d63cb-103">Lists routes learned by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d63cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d63cb-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d63cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d63cb-105">DESCRIPTION</span></span>
<span data-ttu-id="d63cb-106">Räknar upp vägar som upptäckts av en Azure-virtuell nätverksgateway från olika källor.</span><span class="sxs-lookup"><span data-stu-id="d63cb-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="d63cb-107">Detta inkluderar vägar som lärts via BGP samt statiska vägar.</span><span class="sxs-lookup"><span data-stu-id="d63cb-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="d63cb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d63cb-108">EXAMPLES</span></span>

### <span data-ttu-id="d63cb-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d63cb-109">Example 1</span></span>
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

<span data-ttu-id="d63cb-110">För den Azure Virtual Network gateway som heter GatewayName i resurs grupp resourceGroup hämtar vägar som Azure Gateway känner till.</span><span class="sxs-lookup"><span data-stu-id="d63cb-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="d63cb-111">Den virtuella Azure-Nätverksgatewayen i det här fallet har två statiska vägar (10.1.0.0/16 och 10.0.0.254/32) samt en väg som upptäcks via BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="d63cb-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="d63cb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d63cb-112">PARAMETERS</span></span>

### <span data-ttu-id="d63cb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d63cb-113">-AsJob</span></span>
<span data-ttu-id="d63cb-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d63cb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d63cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d63cb-115">-DefaultProfile</span></span>
<span data-ttu-id="d63cb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d63cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d63cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d63cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="d63cb-118">Namn på resurs gruppen virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="d63cb-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="d63cb-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d63cb-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d63cb-120">Namn på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="d63cb-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="d63cb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d63cb-121">CommonParameters</span></span>
<span data-ttu-id="d63cb-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d63cb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d63cb-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d63cb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d63cb-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d63cb-124">INPUTS</span></span>

### <span data-ttu-id="d63cb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d63cb-125">System.String</span></span>

## <span data-ttu-id="d63cb-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d63cb-126">OUTPUTS</span></span>

### <span data-ttu-id="d63cb-127">Microsoft. Azure. commands. Networks. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="d63cb-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="d63cb-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d63cb-128">NOTES</span></span>

## <span data-ttu-id="d63cb-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d63cb-129">RELATED LINKS</span></span>
