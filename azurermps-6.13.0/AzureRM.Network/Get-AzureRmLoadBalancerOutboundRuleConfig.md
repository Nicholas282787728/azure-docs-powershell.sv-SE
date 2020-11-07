---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1bcaab526ac2fbb82d696db7197bbc8d69c0078f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758330"
---
# <span data-ttu-id="21833-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21833-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="21833-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21833-102">SYNOPSIS</span></span>
<span data-ttu-id="21833-103">Hämtar en regel för utgående trafik i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="21833-103">Gets an outbound rule configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21833-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21833-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21833-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21833-105">DESCRIPTION</span></span>
<span data-ttu-id="21833-106">Cmdleten **Get-AzureRmLoadBalancerOutboundRuleConfig** hämtar en konfiguration för utgående regel eller en lista med konfigurationer för utgående trafik i en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="21833-106">The **Get-AzureRmLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="21833-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21833-107">EXAMPLES</span></span>

### <span data-ttu-id="21833-108">Exempel 1: Hämta en konfiguration för utgående regel i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="21833-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="21833-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i variabeln $slb.</span><span class="sxs-lookup"><span data-stu-id="21833-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="21833-110">Det andra kommandot hämtar regeln för utgående regel som heter min regel kopplad till den belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="21833-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="21833-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21833-111">PARAMETERS</span></span>

### <span data-ttu-id="21833-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21833-112">-DefaultProfile</span></span>
<span data-ttu-id="21833-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21833-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21833-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21833-114">-LoadBalancer</span></span>
<span data-ttu-id="21833-115">Referensen för belastnings Utjämnings resursen.</span><span class="sxs-lookup"><span data-stu-id="21833-115">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21833-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="21833-116">-Name</span></span>
<span data-ttu-id="21833-117">Namn på regeln för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="21833-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="21833-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21833-118">CommonParameters</span></span>
<span data-ttu-id="21833-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21833-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21833-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21833-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21833-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21833-121">INPUTS</span></span>

### <span data-ttu-id="21833-122">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21833-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="21833-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21833-123">OUTPUTS</span></span>

### <span data-ttu-id="21833-124">Microsoft. Azure. commands. Networks. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="21833-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="21833-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21833-125">NOTES</span></span>

## <span data-ttu-id="21833-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21833-126">RELATED LINKS</span></span>
