---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: cc9a79b424d6ad81804aaed0d941ca017463abba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578876"
---
# <span data-ttu-id="c216c-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c216c-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c216c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c216c-102">SYNOPSIS</span></span>
<span data-ttu-id="c216c-103">Tar bort en konfiguration för utgående regel från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c216c-103">Removes an outbound rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c216c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c216c-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c216c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c216c-105">DESCRIPTION</span></span>
<span data-ttu-id="c216c-106">Cmdleten **Remove-AzureRmLoadBalancerOutboundRuleConfig** tar bort en konfiguration för utgående regel från en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c216c-106">The **Remove-AzureRmLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="c216c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c216c-107">EXAMPLES</span></span>

### <span data-ttu-id="c216c-108">Exempel 1: ta bort en regel för utgående trafik från en Azure-belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="c216c-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzureRmLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzureRmLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="c216c-109">Det första kommandot får belastningsutjämnaren som är kopplad till den utgående regel konfiguration som du vill ta bort och sedan spara den i $slb variabel.</span><span class="sxs-lookup"><span data-stu-id="c216c-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c216c-110">Det andra kommandot tar bort den associerade konfigurationen för utgående trafik från belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="c216c-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="c216c-111">Det tredje kommandot uppdaterar belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="c216c-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="c216c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c216c-112">PARAMETERS</span></span>

### <span data-ttu-id="c216c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c216c-113">-DefaultProfile</span></span>
<span data-ttu-id="c216c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c216c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c216c-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c216c-115">-LoadBalancer</span></span>
<span data-ttu-id="c216c-116">Referensen för belastnings Utjämnings resursen.</span><span class="sxs-lookup"><span data-stu-id="c216c-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="c216c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c216c-117">-Name</span></span>
<span data-ttu-id="c216c-118">Namnet på regeln för utgående trafik</span><span class="sxs-lookup"><span data-stu-id="c216c-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="c216c-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c216c-119">-Confirm</span></span>
<span data-ttu-id="c216c-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c216c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c216c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c216c-121">-WhatIf</span></span>
<span data-ttu-id="c216c-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c216c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c216c-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c216c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c216c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c216c-124">CommonParameters</span></span>
<span data-ttu-id="c216c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c216c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c216c-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c216c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c216c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c216c-127">INPUTS</span></span>

### <span data-ttu-id="c216c-128">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c216c-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c216c-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c216c-129">OUTPUTS</span></span>

### <span data-ttu-id="c216c-130">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c216c-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c216c-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c216c-131">NOTES</span></span>

## <span data-ttu-id="c216c-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c216c-132">RELATED LINKS</span></span>
