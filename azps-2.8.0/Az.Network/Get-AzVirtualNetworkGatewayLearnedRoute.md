---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaylearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayLearnedRoute.md
ms.openlocfilehash: 80bb8e05b110f1b3e9689895ae9bea2aad1207b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918697"
---
# <span data-ttu-id="e38da-101">Get-AzVirtualNetworkGatewayLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="e38da-101">Get-AzVirtualNetworkGatewayLearnedRoute</span></span>

## <span data-ttu-id="e38da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e38da-102">SYNOPSIS</span></span>
<span data-ttu-id="e38da-103">Visar en lista över vägar som lärts av en Azure Virtual Network Gateway</span><span class="sxs-lookup"><span data-stu-id="e38da-103">Lists routes learned by an Azure virtual network gateway</span></span>

## <span data-ttu-id="e38da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e38da-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayLearnedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e38da-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e38da-105">DESCRIPTION</span></span>
<span data-ttu-id="e38da-106">Räknar upp vägar som upptäckts av en Azure-virtuell nätverksgateway från olika källor.</span><span class="sxs-lookup"><span data-stu-id="e38da-106">Enumerates routes learned by an Azure virtual network gateway from various sources.</span></span> <span data-ttu-id="e38da-107">Detta inkluderar vägar som lärts via BGP samt statiska vägar.</span><span class="sxs-lookup"><span data-stu-id="e38da-107">This includes routes learned over BGP, as well as static routes.</span></span> 

## <span data-ttu-id="e38da-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e38da-108">EXAMPLES</span></span>

### <span data-ttu-id="e38da-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e38da-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayLearnedRoute -ResourceGroupName resourceGroup -VirtualNetworkGatewayname gatewayName

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

<span data-ttu-id="e38da-110">För den Azure Virtual Network gateway som heter GatewayName i resurs grupp resourceGroup hämtar vägar som Azure Gateway känner till.</span><span class="sxs-lookup"><span data-stu-id="e38da-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves routes the Azure gateway knows.</span></span> <span data-ttu-id="e38da-111">Den virtuella Azure-Nätverksgatewayen i det här fallet har två statiska vägar (10.1.0.0/16 och 10.0.0.254/32) samt en väg som upptäcks via BGP (10.0.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="e38da-111">The Azure virtual network gateway in this case has two static routes (10.1.0.0/16 and 10.0.0.254/32), as well as one route learned over BGP (10.0.0.0/16).</span></span>

## <span data-ttu-id="e38da-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e38da-112">PARAMETERS</span></span>

### <span data-ttu-id="e38da-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e38da-113">-AsJob</span></span>
<span data-ttu-id="e38da-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e38da-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e38da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e38da-115">-DefaultProfile</span></span>
<span data-ttu-id="e38da-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e38da-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e38da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e38da-117">-ResourceGroupName</span></span>
<span data-ttu-id="e38da-118">Namn på resurs gruppen virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="e38da-118">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="e38da-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e38da-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e38da-120">Namn på virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="e38da-120">Virtual network gateway name</span></span>

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

### <span data-ttu-id="e38da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e38da-121">CommonParameters</span></span>
<span data-ttu-id="e38da-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e38da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e38da-123">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e38da-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e38da-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e38da-124">INPUTS</span></span>

### <span data-ttu-id="e38da-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e38da-125">System.String</span></span>

## <span data-ttu-id="e38da-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e38da-126">OUTPUTS</span></span>

### <span data-ttu-id="e38da-127">Microsoft. Azure. commands. Networks. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="e38da-127">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="e38da-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e38da-128">NOTES</span></span>

## <span data-ttu-id="e38da-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e38da-129">RELATED LINKS</span></span>
