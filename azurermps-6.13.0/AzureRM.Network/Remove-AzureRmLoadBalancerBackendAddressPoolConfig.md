---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 065aa3718f1a66949265e7dca39880c1eff21fa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755700"
---
# <span data-ttu-id="b67d0-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b67d0-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b67d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b67d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b67d0-103">Tar bort en konfiguration för en server dels adresspool från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="b67d0-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b67d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b67d0-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b67d0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b67d0-105">DESCRIPTION</span></span>
<span data-ttu-id="b67d0-106">Cmdleten **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** tar bort en server dels adress från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="b67d0-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="b67d0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b67d0-107">EXAMPLES</span></span>

### <span data-ttu-id="b67d0-108">Exempel 1: ta bort en konfiguration av en server dels adresspool från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="b67d0-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="b67d0-109">Det här kommandot får belastningsutjämnaren med namnet MyLoadBalancer och skickar det till **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , som tar bort BackendAddressPool02-konfigurationen från MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="b67d0-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="b67d0-110">Slutligen uppdaterar Set-AzureRmLoadBalancer cmdleten MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="b67d0-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="b67d0-111">Observera att en konfiguration för en server dels adresspool måste finnas innan du kan ta bort den.</span><span class="sxs-lookup"><span data-stu-id="b67d0-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="b67d0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b67d0-112">PARAMETERS</span></span>

### <span data-ttu-id="b67d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b67d0-113">-DefaultProfile</span></span>
<span data-ttu-id="b67d0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b67d0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b67d0-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b67d0-115">-LoadBalancer</span></span>
<span data-ttu-id="b67d0-116">Anger den belastningsutjämnare som innehåller den server dels adress som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b67d0-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="b67d0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b67d0-117">-Name</span></span>
<span data-ttu-id="b67d0-118">Anger namnet på Server dels adresspoolen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="b67d0-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b67d0-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b67d0-119">-Confirm</span></span>
<span data-ttu-id="b67d0-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b67d0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b67d0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b67d0-121">-WhatIf</span></span>
<span data-ttu-id="b67d0-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b67d0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b67d0-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b67d0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b67d0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b67d0-124">CommonParameters</span></span>
<span data-ttu-id="b67d0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b67d0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b67d0-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b67d0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b67d0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b67d0-127">INPUTS</span></span>

### <span data-ttu-id="b67d0-128">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b67d0-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="b67d0-129">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b67d0-129">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="b67d0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b67d0-130">OUTPUTS</span></span>

### <span data-ttu-id="b67d0-131">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b67d0-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b67d0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b67d0-132">NOTES</span></span>

## <span data-ttu-id="b67d0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b67d0-133">RELATED LINKS</span></span>

[<span data-ttu-id="b67d0-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b67d0-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b67d0-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b67d0-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b67d0-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b67d0-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b67d0-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b67d0-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


