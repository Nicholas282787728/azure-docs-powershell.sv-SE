---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258208"
---
# <span data-ttu-id="a1b82-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a1b82-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="a1b82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1b82-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b82-103">Tar bort en konfiguration för en server dels adresspool från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="a1b82-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="a1b82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1b82-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1b82-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b82-106">Cmdleten **Remove-AzLoadBalancerBackendAddressPoolConfig** tar bort en server dels adress från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="a1b82-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="a1b82-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1b82-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b82-108">Exempel 1: ta bort en konfiguration av en server dels adresspool från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="a1b82-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="a1b82-109">Det här kommandot får belastningsutjämnaren med namnet MyLoadBalancer och skickar det till **Remove-AzLoadBalancerBackendAddressPoolConfig** , som tar bort BackendAddressPool02-konfigurationen från MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="a1b82-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="a1b82-110">Slutligen uppdaterar Set-AzLoadBalancer cmdleten MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="a1b82-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="a1b82-111">Observera att en konfiguration för en server dels adresspool måste finnas innan du kan ta bort den.</span><span class="sxs-lookup"><span data-stu-id="a1b82-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="a1b82-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1b82-112">PARAMETERS</span></span>

### <span data-ttu-id="a1b82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b82-113">-DefaultProfile</span></span>
<span data-ttu-id="a1b82-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b82-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b82-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1b82-115">-LoadBalancer</span></span>
<span data-ttu-id="a1b82-116">Anger den belastningsutjämnare som innehåller den server dels adress som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a1b82-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="a1b82-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1b82-117">-Name</span></span>
<span data-ttu-id="a1b82-118">Anger namnet på Server dels adresspoolen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a1b82-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a1b82-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a1b82-119">-Confirm</span></span>
<span data-ttu-id="a1b82-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1b82-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b82-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b82-121">-WhatIf</span></span>
<span data-ttu-id="a1b82-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a1b82-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1b82-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a1b82-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b82-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b82-124">CommonParameters</span></span>
<span data-ttu-id="a1b82-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b82-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b82-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b82-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b82-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1b82-127">INPUTS</span></span>

### <span data-ttu-id="a1b82-128">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1b82-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a1b82-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1b82-129">OUTPUTS</span></span>

### <span data-ttu-id="a1b82-130">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1b82-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a1b82-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1b82-131">NOTES</span></span>

## <span data-ttu-id="a1b82-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1b82-132">RELATED LINKS</span></span>

[<span data-ttu-id="a1b82-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a1b82-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a1b82-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1b82-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a1b82-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a1b82-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a1b82-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a1b82-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


