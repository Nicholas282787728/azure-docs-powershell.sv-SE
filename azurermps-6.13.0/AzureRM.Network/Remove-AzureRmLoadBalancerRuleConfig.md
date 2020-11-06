---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b51c7300296644ffeda75d1fb9e4cf695ff61def
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574785"
---
# <span data-ttu-id="ccb50-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ccb50-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="ccb50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ccb50-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb50-103">Tar bort en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="ccb50-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccb50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ccb50-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccb50-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ccb50-105">DESCRIPTION</span></span>
<span data-ttu-id="ccb50-106">Cmdleten **Remove-AzureRmLoadBalancerRuleConfig** tar bort en regel konfiguration för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="ccb50-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ccb50-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ccb50-107">EXAMPLES</span></span>

### <span data-ttu-id="ccb50-108">Exempel 1: ta bort en regel konfiguration från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="ccb50-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="ccb50-109">Det första kommandot får belastningsutjämnaren med namnet MyLoadBalancer och lagrar det sedan i $loadbalancer variabel.</span><span class="sxs-lookup"><span data-stu-id="ccb50-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="ccb50-110">Det andra kommandot tar bort regel konfigurationen med namnet MyLBruleName från belastningsutjämnaren i $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="ccb50-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="ccb50-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ccb50-111">PARAMETERS</span></span>

### <span data-ttu-id="ccb50-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb50-112">-DefaultProfile</span></span>
<span data-ttu-id="ccb50-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ccb50-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccb50-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ccb50-114">-LoadBalancer</span></span>
<span data-ttu-id="ccb50-115">Anger det **Loadbalancer** -objekt som innehåller regel konfigurationen som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ccb50-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ccb50-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="ccb50-116">-Name</span></span>
<span data-ttu-id="ccb50-117">Anger namnet på den regel för belastnings utjämning som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="ccb50-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ccb50-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ccb50-118">-Confirm</span></span>
<span data-ttu-id="ccb50-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ccb50-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccb50-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccb50-120">-WhatIf</span></span>
<span data-ttu-id="ccb50-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ccb50-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccb50-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ccb50-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccb50-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb50-123">CommonParameters</span></span>
<span data-ttu-id="ccb50-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccb50-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb50-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccb50-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb50-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ccb50-126">INPUTS</span></span>

### <span data-ttu-id="ccb50-127">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ccb50-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="ccb50-128">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ccb50-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="ccb50-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ccb50-129">OUTPUTS</span></span>

### <span data-ttu-id="ccb50-130">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ccb50-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ccb50-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ccb50-131">NOTES</span></span>

## <span data-ttu-id="ccb50-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ccb50-132">RELATED LINKS</span></span>

[<span data-ttu-id="ccb50-133">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ccb50-133">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="ccb50-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ccb50-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ccb50-135">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ccb50-135">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="ccb50-136">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ccb50-136">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="ccb50-137">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ccb50-137">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


